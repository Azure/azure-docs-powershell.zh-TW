---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794987"
---
# <span data-ttu-id="8caed-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8caed-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="8caed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8caed-102">SYNOPSIS</span></span>
<span data-ttu-id="8caed-103">取得適用于 web 應用程式的快照。</span><span class="sxs-lookup"><span data-stu-id="8caed-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="8caed-104">句法</span><span class="sxs-lookup"><span data-stu-id="8caed-104">SYNTAX</span></span>

### <span data-ttu-id="8caed-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8caed-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="8caed-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8caed-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="8caed-107">說明</span><span class="sxs-lookup"><span data-stu-id="8caed-107">DESCRIPTION</span></span>
<span data-ttu-id="8caed-108">**AzWebAppSnapshot** Cmdlet 會傳回 web 應用程式的所有快照。</span><span class="sxs-lookup"><span data-stu-id="8caed-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="8caed-109">快照是 web 應用程式檔案和設定的自動備份。</span><span class="sxs-lookup"><span data-stu-id="8caed-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="8caed-110">您可以使用 **Restore AzWebAppSnapshot** Cmdlet 來還原快照。</span><span class="sxs-lookup"><span data-stu-id="8caed-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="8caed-111">示例</span><span class="sxs-lookup"><span data-stu-id="8caed-111">EXAMPLES</span></span>

### <span data-ttu-id="8caed-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8caed-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="8caed-113">取得名為「ConstosoApp」的 web app 快照，並在「預設-Web-WestUS」資源群組中使用名為「暫存」的槽</span><span class="sxs-lookup"><span data-stu-id="8caed-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="8caed-114">參數</span><span class="sxs-lookup"><span data-stu-id="8caed-114">PARAMETERS</span></span>

### <span data-ttu-id="8caed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8caed-115">-DefaultProfile</span></span>
<span data-ttu-id="8caed-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8caed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8caed-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8caed-117">-Name</span></span>
<span data-ttu-id="8caed-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8caed-118">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8caed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8caed-119">-ResourceGroupName</span></span>
<span data-ttu-id="8caed-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8caed-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8caed-121">-槽</span><span class="sxs-lookup"><span data-stu-id="8caed-121">-Slot</span></span>
<span data-ttu-id="8caed-122">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="8caed-122">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8caed-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8caed-123">-WebApp</span></span>
<span data-ttu-id="8caed-124">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="8caed-124">The web app object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## <span data-ttu-id="8caed-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8caed-125">INPUTS</span></span>

### <span data-ttu-id="8caed-126">System.object</span><span class="sxs-lookup"><span data-stu-id="8caed-126">System.String</span></span>
<span data-ttu-id="8caed-127">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="8caed-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="8caed-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8caed-128">OUTPUTS</span></span>

### <span data-ttu-id="8caed-129">WebApps BackupRestore. AzureWebAppSnapshot （）</span><span class="sxs-lookup"><span data-stu-id="8caed-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="8caed-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8caed-130">NOTES</span></span>

## <span data-ttu-id="8caed-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8caed-131">RELATED LINKS</span></span>


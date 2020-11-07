---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800025"
---
# <span data-ttu-id="60872-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="60872-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="60872-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60872-102">SYNOPSIS</span></span>
<span data-ttu-id="60872-103">取得適用于 web 應用程式的快照。</span><span class="sxs-lookup"><span data-stu-id="60872-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60872-104">句法</span><span class="sxs-lookup"><span data-stu-id="60872-104">SYNTAX</span></span>

### <span data-ttu-id="60872-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="60872-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="60872-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="60872-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="60872-107">說明</span><span class="sxs-lookup"><span data-stu-id="60872-107">DESCRIPTION</span></span>
<span data-ttu-id="60872-108">**AzureRmWebAppSnapshot** Cmdlet 會傳回 web 應用程式的所有快照。</span><span class="sxs-lookup"><span data-stu-id="60872-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="60872-109">快照是 web 應用程式檔案和設定的自動備份。</span><span class="sxs-lookup"><span data-stu-id="60872-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="60872-110">您可以使用 **Restore AzureRmWebAppSnapshot** Cmdlet 來還原快照。</span><span class="sxs-lookup"><span data-stu-id="60872-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="60872-111">示例</span><span class="sxs-lookup"><span data-stu-id="60872-111">EXAMPLES</span></span>

### <span data-ttu-id="60872-112">範例1</span><span class="sxs-lookup"><span data-stu-id="60872-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="60872-113">取得名為「ConstosoApp」的 web app 快照，並在「預設-Web-WestUS」資源群組中使用名為「暫存」的槽</span><span class="sxs-lookup"><span data-stu-id="60872-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="60872-114">參數</span><span class="sxs-lookup"><span data-stu-id="60872-114">PARAMETERS</span></span>

### <span data-ttu-id="60872-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60872-115">-DefaultProfile</span></span>
<span data-ttu-id="60872-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60872-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60872-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="60872-117">-Name</span></span>
<span data-ttu-id="60872-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="60872-118">The name of the web app.</span></span>

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

### <span data-ttu-id="60872-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60872-119">-ResourceGroupName</span></span>
<span data-ttu-id="60872-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60872-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="60872-121">-槽</span><span class="sxs-lookup"><span data-stu-id="60872-121">-Slot</span></span>
<span data-ttu-id="60872-122">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="60872-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="60872-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="60872-123">-WebApp</span></span>
<span data-ttu-id="60872-124">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="60872-124">The web app object</span></span>

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

## <span data-ttu-id="60872-125">輸入</span><span class="sxs-lookup"><span data-stu-id="60872-125">INPUTS</span></span>

### <span data-ttu-id="60872-126">System.object</span><span class="sxs-lookup"><span data-stu-id="60872-126">System.String</span></span>
<span data-ttu-id="60872-127">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="60872-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="60872-128">輸出</span><span class="sxs-lookup"><span data-stu-id="60872-128">OUTPUTS</span></span>

### <span data-ttu-id="60872-129">WebApps BackupRestore. AzureWebAppSnapshot （）</span><span class="sxs-lookup"><span data-stu-id="60872-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="60872-130">筆記</span><span class="sxs-lookup"><span data-stu-id="60872-130">NOTES</span></span>

## <span data-ttu-id="60872-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="60872-131">RELATED LINKS</span></span>


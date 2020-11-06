---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443627"
---
# <span data-ttu-id="c2327-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c2327-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="c2327-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2327-102">SYNOPSIS</span></span>
<span data-ttu-id="c2327-103">取得適用于 web 應用程式的快照。</span><span class="sxs-lookup"><span data-stu-id="c2327-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2327-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2327-104">SYNTAX</span></span>

### <span data-ttu-id="c2327-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c2327-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2327-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c2327-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2327-107">說明</span><span class="sxs-lookup"><span data-stu-id="c2327-107">DESCRIPTION</span></span>
<span data-ttu-id="c2327-108">**AzureRmWebAppSnapshot** Cmdlet 會傳回 web 應用程式的所有快照。</span><span class="sxs-lookup"><span data-stu-id="c2327-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="c2327-109">快照是 web 應用程式檔案和設定的自動備份。</span><span class="sxs-lookup"><span data-stu-id="c2327-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="c2327-110">您可以使用 **Restore AzureRmWebAppSnapshot** Cmdlet 來還原快照。</span><span class="sxs-lookup"><span data-stu-id="c2327-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="c2327-111">示例</span><span class="sxs-lookup"><span data-stu-id="c2327-111">EXAMPLES</span></span>

### <span data-ttu-id="c2327-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c2327-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="c2327-113">取得名為「ConstosoApp」的 web app 快照，並在「預設-Web-WestUS」資源群組中使用名為「暫存」的槽</span><span class="sxs-lookup"><span data-stu-id="c2327-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="c2327-114">參數</span><span class="sxs-lookup"><span data-stu-id="c2327-114">PARAMETERS</span></span>

### <span data-ttu-id="c2327-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2327-115">-DefaultProfile</span></span>
<span data-ttu-id="c2327-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2327-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2327-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2327-117">-Name</span></span>
<span data-ttu-id="c2327-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2327-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2327-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2327-119">-ResourceGroupName</span></span>
<span data-ttu-id="c2327-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2327-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2327-121">-槽</span><span class="sxs-lookup"><span data-stu-id="c2327-121">-Slot</span></span>
<span data-ttu-id="c2327-122">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2327-122">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2327-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c2327-123">-WebApp</span></span>
<span data-ttu-id="c2327-124">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="c2327-124">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2327-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2327-125">CommonParameters</span></span>
<span data-ttu-id="c2327-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2327-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2327-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2327-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2327-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c2327-128">INPUTS</span></span>

### <span data-ttu-id="c2327-129">System.object</span><span class="sxs-lookup"><span data-stu-id="c2327-129">System.String</span></span>

### <span data-ttu-id="c2327-130">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="c2327-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c2327-131">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c2327-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c2327-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c2327-132">OUTPUTS</span></span>

### <span data-ttu-id="c2327-133">WebApps BackupRestore. AzureWebAppSnapshot （）</span><span class="sxs-lookup"><span data-stu-id="c2327-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="c2327-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c2327-134">NOTES</span></span>

## <span data-ttu-id="c2327-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2327-135">RELATED LINKS</span></span>

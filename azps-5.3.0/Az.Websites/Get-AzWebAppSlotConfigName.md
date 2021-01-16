---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436013"
---
# <span data-ttu-id="c3e0c-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="c3e0c-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="c3e0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e0c-103">取得 Web 應用程式槽配置名稱的清單</span><span class="sxs-lookup"><span data-stu-id="c3e0c-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="c3e0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3e0c-104">SYNTAX</span></span>

### <span data-ttu-id="c3e0c-105">S1</span><span class="sxs-lookup"><span data-stu-id="c3e0c-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e0c-106">S2</span><span class="sxs-lookup"><span data-stu-id="c3e0c-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e0c-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3e0c-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e0c-108">**AzWebAppSlotConfigName** Cmdlet 會檢索應用程式設定清單，以及目前標示為槽設定的連接字串名稱</span><span class="sxs-lookup"><span data-stu-id="c3e0c-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="c3e0c-109">示例</span><span class="sxs-lookup"><span data-stu-id="c3e0c-109">EXAMPLES</span></span>

### <span data-ttu-id="c3e0c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c3e0c-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c3e0c-111">這個命令會取得與資源群組預設的 Web 應用程式相關的 App 設定和連線字串（與資源群組預設的 Web WestUS 有關）。</span><span class="sxs-lookup"><span data-stu-id="c3e0c-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c3e0c-112">參數</span><span class="sxs-lookup"><span data-stu-id="c3e0c-112">PARAMETERS</span></span>

### <span data-ttu-id="c3e0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e0c-113">-DefaultProfile</span></span>
<span data-ttu-id="c3e0c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3e0c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e0c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3e0c-115">-Name</span></span>
<span data-ttu-id="c3e0c-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c3e0c-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e0c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e0c-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3e0c-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c3e0c-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e0c-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c3e0c-119">-WebApp</span></span>
<span data-ttu-id="c3e0c-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c3e0c-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e0c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e0c-121">CommonParameters</span></span>
<span data-ttu-id="c3e0c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3e0c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e0c-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3e0c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e0c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c3e0c-124">INPUTS</span></span>

### <span data-ttu-id="c3e0c-125">System.object</span><span class="sxs-lookup"><span data-stu-id="c3e0c-125">System.String</span></span>

### <span data-ttu-id="c3e0c-126">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="c3e0c-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c3e0c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c3e0c-127">OUTPUTS</span></span>

### <span data-ttu-id="c3e0c-128">SlotConfigNamesResource 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="c3e0c-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="c3e0c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c3e0c-129">NOTES</span></span>

## <span data-ttu-id="c3e0c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3e0c-130">RELATED LINKS</span></span>

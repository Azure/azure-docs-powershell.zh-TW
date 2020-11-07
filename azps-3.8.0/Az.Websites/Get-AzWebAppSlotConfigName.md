---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 6ff0defc39e2bb2418bf1d42e917c0dadeef1c9b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957952"
---
# <span data-ttu-id="287eb-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="287eb-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="287eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="287eb-102">SYNOPSIS</span></span>
<span data-ttu-id="287eb-103">取得 Web 應用程式槽配置名稱的清單</span><span class="sxs-lookup"><span data-stu-id="287eb-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="287eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="287eb-104">SYNTAX</span></span>

### <span data-ttu-id="287eb-105">S1</span><span class="sxs-lookup"><span data-stu-id="287eb-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="287eb-106">S2</span><span class="sxs-lookup"><span data-stu-id="287eb-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="287eb-107">說明</span><span class="sxs-lookup"><span data-stu-id="287eb-107">DESCRIPTION</span></span>
<span data-ttu-id="287eb-108">**AzWebAppSlotConfigName** Cmdlet 會檢索應用程式設定清單，以及目前標示為槽設定的連接字串名稱</span><span class="sxs-lookup"><span data-stu-id="287eb-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="287eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="287eb-109">EXAMPLES</span></span>

### <span data-ttu-id="287eb-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="287eb-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="287eb-111">這個命令會取得與資源群組預設的 Web 應用程式相關的 App 設定和連線字串（與資源群組預設的 Web WestUS 有關）。</span><span class="sxs-lookup"><span data-stu-id="287eb-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="287eb-112">參數</span><span class="sxs-lookup"><span data-stu-id="287eb-112">PARAMETERS</span></span>

### <span data-ttu-id="287eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287eb-113">-DefaultProfile</span></span>
<span data-ttu-id="287eb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="287eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="287eb-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="287eb-115">-Name</span></span>
<span data-ttu-id="287eb-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="287eb-116">WebApp Name</span></span>

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

### <span data-ttu-id="287eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="287eb-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="287eb-118">Resource Group Name</span></span>

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

### <span data-ttu-id="287eb-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="287eb-119">-WebApp</span></span>
<span data-ttu-id="287eb-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="287eb-120">WebApp Object</span></span>

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

### <span data-ttu-id="287eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287eb-121">CommonParameters</span></span>
<span data-ttu-id="287eb-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="287eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287eb-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="287eb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287eb-124">輸入</span><span class="sxs-lookup"><span data-stu-id="287eb-124">INPUTS</span></span>

### <span data-ttu-id="287eb-125">System.object</span><span class="sxs-lookup"><span data-stu-id="287eb-125">System.String</span></span>

### <span data-ttu-id="287eb-126">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="287eb-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="287eb-127">輸出</span><span class="sxs-lookup"><span data-stu-id="287eb-127">OUTPUTS</span></span>

### <span data-ttu-id="287eb-128">SlotConfigNamesResource 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="287eb-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="287eb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="287eb-129">NOTES</span></span>

## <span data-ttu-id="287eb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="287eb-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: b1b9760d129a4177f979996f1ef46bd2a225f452
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623396"
---
# <span data-ttu-id="49acf-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="49acf-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="49acf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49acf-102">SYNOPSIS</span></span>
<span data-ttu-id="49acf-103">取得 Web 應用程式槽配置名稱的清單</span><span class="sxs-lookup"><span data-stu-id="49acf-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49acf-104">句法</span><span class="sxs-lookup"><span data-stu-id="49acf-104">SYNTAX</span></span>

### <span data-ttu-id="49acf-105">S1</span><span class="sxs-lookup"><span data-stu-id="49acf-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49acf-106">S2</span><span class="sxs-lookup"><span data-stu-id="49acf-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49acf-107">說明</span><span class="sxs-lookup"><span data-stu-id="49acf-107">DESCRIPTION</span></span>
<span data-ttu-id="49acf-108">**AzureRmWebAppSlotConfigName** Cmdlet 會檢索應用程式設定清單，以及目前標示為槽設定的連接字串名稱</span><span class="sxs-lookup"><span data-stu-id="49acf-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="49acf-109">示例</span><span class="sxs-lookup"><span data-stu-id="49acf-109">EXAMPLES</span></span>

### <span data-ttu-id="49acf-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="49acf-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="49acf-111">這個命令會取得與資源群組預設的 Web 應用程式相關的 App 設定和連線字串（與資源群組預設的 Web WestUS 有關）。</span><span class="sxs-lookup"><span data-stu-id="49acf-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="49acf-112">參數</span><span class="sxs-lookup"><span data-stu-id="49acf-112">PARAMETERS</span></span>

### <span data-ttu-id="49acf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49acf-113">-DefaultProfile</span></span>
<span data-ttu-id="49acf-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49acf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49acf-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="49acf-115">-Name</span></span>
<span data-ttu-id="49acf-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="49acf-116">WebApp Name</span></span>

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

### <span data-ttu-id="49acf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49acf-117">-ResourceGroupName</span></span>
<span data-ttu-id="49acf-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="49acf-118">Resource Group Name</span></span>

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

### <span data-ttu-id="49acf-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="49acf-119">-WebApp</span></span>
<span data-ttu-id="49acf-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="49acf-120">WebApp Object</span></span>

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

### <span data-ttu-id="49acf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49acf-121">CommonParameters</span></span>
<span data-ttu-id="49acf-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49acf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49acf-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49acf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49acf-124">輸入</span><span class="sxs-lookup"><span data-stu-id="49acf-124">INPUTS</span></span>

### <span data-ttu-id="49acf-125">System.object</span><span class="sxs-lookup"><span data-stu-id="49acf-125">System.String</span></span>

### <span data-ttu-id="49acf-126">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="49acf-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="49acf-127">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="49acf-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="49acf-128">輸出</span><span class="sxs-lookup"><span data-stu-id="49acf-128">OUTPUTS</span></span>

### <span data-ttu-id="49acf-129">SlotConfigNamesResource 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="49acf-129">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="49acf-130">筆記</span><span class="sxs-lookup"><span data-stu-id="49acf-130">NOTES</span></span>

## <span data-ttu-id="49acf-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="49acf-131">RELATED LINKS</span></span>

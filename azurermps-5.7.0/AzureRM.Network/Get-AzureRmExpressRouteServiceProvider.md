---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: d8d5abedd0deaf5af341995552ad72bef4703058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623596"
---
# <span data-ttu-id="8b245-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="8b245-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="8b245-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b245-102">SYNOPSIS</span></span>
<span data-ttu-id="8b245-103">取得清單 ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="8b245-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b245-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b245-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b245-105">說明</span><span class="sxs-lookup"><span data-stu-id="8b245-105">DESCRIPTION</span></span>
<span data-ttu-id="8b245-106">**AzureRmExpressRouteServiceProvider** Cmdlet 會檢索 list ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="8b245-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="8b245-107">[屬性] 包含位置和頻寬選項。</span><span class="sxs-lookup"><span data-stu-id="8b245-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="8b245-108">示例</span><span class="sxs-lookup"><span data-stu-id="8b245-108">EXAMPLES</span></span>

### <span data-ttu-id="8b245-109">範例1：取得服務提供者清單，其中包含「矽谷」的位置</span><span class="sxs-lookup"><span data-stu-id="8b245-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="8b245-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b245-110">PARAMETERS</span></span>

### <span data-ttu-id="8b245-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b245-111">-DefaultProfile</span></span>
<span data-ttu-id="8b245-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b245-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b245-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b245-113">CommonParameters</span></span>
<span data-ttu-id="8b245-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b245-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b245-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b245-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b245-116">輸入</span><span class="sxs-lookup"><span data-stu-id="8b245-116">INPUTS</span></span>

### <span data-ttu-id="8b245-117">所有</span><span class="sxs-lookup"><span data-stu-id="8b245-117">None</span></span>
<span data-ttu-id="8b245-118">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8b245-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b245-119">輸出</span><span class="sxs-lookup"><span data-stu-id="8b245-119">OUTPUTS</span></span>

### <span data-ttu-id="8b245-120">PSExpressRouteServiceProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b245-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="8b245-121">筆記</span><span class="sxs-lookup"><span data-stu-id="8b245-121">NOTES</span></span>

## <span data-ttu-id="8b245-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b245-122">RELATED LINKS</span></span>

[<span data-ttu-id="8b245-123">AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8b245-123">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="8b245-124">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8b245-124">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="8b245-125">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8b245-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="8b245-126">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="8b245-126">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)

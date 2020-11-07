---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800866"
---
# <span data-ttu-id="1c72b-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="1c72b-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="1c72b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c72b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c72b-103">取得清單 ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="1c72b-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c72b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c72b-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c72b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c72b-105">DESCRIPTION</span></span>
<span data-ttu-id="1c72b-106">**AzureRmExpressRouteServiceProvider** Cmdlet 會檢索 list ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="1c72b-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="1c72b-107">[屬性] 包含位置和頻寬選項。</span><span class="sxs-lookup"><span data-stu-id="1c72b-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="1c72b-108">示例</span><span class="sxs-lookup"><span data-stu-id="1c72b-108">EXAMPLES</span></span>

### <span data-ttu-id="1c72b-109">範例1：取得服務提供者清單，其中包含「矽谷」的位置</span><span class="sxs-lookup"><span data-stu-id="1c72b-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="1c72b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c72b-110">PARAMETERS</span></span>

### <span data-ttu-id="1c72b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c72b-111">-DefaultProfile</span></span>
<span data-ttu-id="1c72b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c72b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c72b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c72b-113">CommonParameters</span></span>
<span data-ttu-id="1c72b-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c72b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c72b-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c72b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c72b-116">輸入</span><span class="sxs-lookup"><span data-stu-id="1c72b-116">INPUTS</span></span>

## <span data-ttu-id="1c72b-117">輸出</span><span class="sxs-lookup"><span data-stu-id="1c72b-117">OUTPUTS</span></span>

### <span data-ttu-id="1c72b-118">PSExpressRouteServiceProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1c72b-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="1c72b-119">筆記</span><span class="sxs-lookup"><span data-stu-id="1c72b-119">NOTES</span></span>

## <span data-ttu-id="1c72b-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c72b-120">RELATED LINKS</span></span>

[<span data-ttu-id="1c72b-121">AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1c72b-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="1c72b-122">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c72b-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="1c72b-123">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1c72b-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="1c72b-124">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="1c72b-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)

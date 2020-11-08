---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127047"
---
# <span data-ttu-id="1dc41-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1dc41-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="1dc41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dc41-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc41-103">取得 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="1dc41-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="1dc41-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dc41-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc41-105">說明</span><span class="sxs-lookup"><span data-stu-id="1dc41-105">DESCRIPTION</span></span>
<span data-ttu-id="1dc41-106">**AzExpressRouteCircuitPeeringConfig** Cmdlet 會針對 ExpressRoute 回路檢索對等關係的設定。</span><span class="sxs-lookup"><span data-stu-id="1dc41-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1dc41-107">示例</span><span class="sxs-lookup"><span data-stu-id="1dc41-107">EXAMPLES</span></span>

### <span data-ttu-id="1dc41-108">範例1：顯示 ExpressRoute 回路的對等設定</span><span class="sxs-lookup"><span data-stu-id="1dc41-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="1dc41-109">參數</span><span class="sxs-lookup"><span data-stu-id="1dc41-109">PARAMETERS</span></span>

### <span data-ttu-id="1dc41-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc41-110">-DefaultProfile</span></span>
<span data-ttu-id="1dc41-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dc41-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc41-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1dc41-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1dc41-113">包含對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="1dc41-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc41-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dc41-114">-Name</span></span>
<span data-ttu-id="1dc41-115">要檢索之對等配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc41-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc41-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc41-116">CommonParameters</span></span>
<span data-ttu-id="1dc41-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dc41-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc41-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1dc41-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc41-119">輸入</span><span class="sxs-lookup"><span data-stu-id="1dc41-119">INPUTS</span></span>

### <span data-ttu-id="1dc41-120">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1dc41-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1dc41-121">輸出</span><span class="sxs-lookup"><span data-stu-id="1dc41-121">OUTPUTS</span></span>

### <span data-ttu-id="1dc41-122">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1dc41-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="1dc41-123">筆記</span><span class="sxs-lookup"><span data-stu-id="1dc41-123">NOTES</span></span>

## <span data-ttu-id="1dc41-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dc41-124">RELATED LINKS</span></span>

[<span data-ttu-id="1dc41-125">附加 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1dc41-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1dc41-126">新-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1dc41-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1dc41-127">移除-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1dc41-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1dc41-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1dc41-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
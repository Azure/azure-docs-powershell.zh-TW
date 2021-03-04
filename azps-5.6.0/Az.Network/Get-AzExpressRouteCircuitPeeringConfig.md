---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7da632a1496b22e2f0be183640995a2aaa96735e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916399"
---
# <span data-ttu-id="a71af-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a71af-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a71af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a71af-102">SYNOPSIS</span></span>
<span data-ttu-id="a71af-103">獲得 ExpressRoute 回路對等配置。</span><span class="sxs-lookup"><span data-stu-id="a71af-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a71af-104">語法</span><span class="sxs-lookup"><span data-stu-id="a71af-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a71af-105">描述</span><span class="sxs-lookup"><span data-stu-id="a71af-105">DESCRIPTION</span></span>
<span data-ttu-id="a71af-106">**Get-AzExpressRouteRouteCircuitPeeringConfig** Cmdlet 會針對 ExpressRoute 回路取得對等互連關係的組式。</span><span class="sxs-lookup"><span data-stu-id="a71af-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a71af-107">例子</span><span class="sxs-lookup"><span data-stu-id="a71af-107">EXAMPLES</span></span>

### <span data-ttu-id="a71af-108">範例 1：顯示 ExpressRoute 回路的對等組</span><span class="sxs-lookup"><span data-stu-id="a71af-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="a71af-109">參數</span><span class="sxs-lookup"><span data-stu-id="a71af-109">PARAMETERS</span></span>

### <span data-ttu-id="a71af-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71af-110">-DefaultProfile</span></span>
<span data-ttu-id="a71af-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a71af-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a71af-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a71af-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a71af-113">包含對等配置的 ExpressRoute 回路物件。</span><span class="sxs-lookup"><span data-stu-id="a71af-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="a71af-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a71af-114">-Name</span></span>
<span data-ttu-id="a71af-115">要取取的對等組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a71af-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="a71af-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71af-116">CommonParameters</span></span>
<span data-ttu-id="a71af-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a71af-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71af-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a71af-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71af-119">輸入</span><span class="sxs-lookup"><span data-stu-id="a71af-119">INPUTS</span></span>

### <span data-ttu-id="a71af-120">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a71af-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a71af-121">輸出</span><span class="sxs-lookup"><span data-stu-id="a71af-121">OUTPUTS</span></span>

### <span data-ttu-id="a71af-122">Microsoft.Azure.Commands.Network.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a71af-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="a71af-123">筆記</span><span class="sxs-lookup"><span data-stu-id="a71af-123">NOTES</span></span>

## <span data-ttu-id="a71af-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="a71af-124">RELATED LINKS</span></span>

[<span data-ttu-id="a71af-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a71af-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a71af-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a71af-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a71af-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a71af-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a71af-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a71af-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

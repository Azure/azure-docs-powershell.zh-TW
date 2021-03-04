---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 187921598b21747764436dd4ae6f988961d4a951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913453"
---
# <span data-ttu-id="85ae2-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="85ae2-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="85ae2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="85ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="85ae2-103">移除 ExpressRoute 回路對等配置。</span><span class="sxs-lookup"><span data-stu-id="85ae2-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="85ae2-104">語法</span><span class="sxs-lookup"><span data-stu-id="85ae2-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85ae2-105">描述</span><span class="sxs-lookup"><span data-stu-id="85ae2-105">DESCRIPTION</span></span>
<span data-ttu-id="85ae2-106">**Remove-AzExpressRouteCircuitPeeringConfig** Cmdlet 會移除 ExpressRoute 回路對等配置。</span><span class="sxs-lookup"><span data-stu-id="85ae2-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="85ae2-107">例子</span><span class="sxs-lookup"><span data-stu-id="85ae2-107">EXAMPLES</span></span>

### <span data-ttu-id="85ae2-108">範例 1：從 ExpressRoute 回路移除對等組</span><span class="sxs-lookup"><span data-stu-id="85ae2-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="85ae2-109">參數</span><span class="sxs-lookup"><span data-stu-id="85ae2-109">PARAMETERS</span></span>

### <span data-ttu-id="85ae2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ae2-110">-DefaultProfile</span></span>
<span data-ttu-id="85ae2-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="85ae2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85ae2-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="85ae2-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="85ae2-113">包含要移除之對等配置的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="85ae2-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="85ae2-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="85ae2-114">-Name</span></span>
<span data-ttu-id="85ae2-115">要移除的對等組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ae2-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="85ae2-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="85ae2-116">-PeerAddressType</span></span>
<span data-ttu-id="85ae2-117">對等的網址系列</span><span class="sxs-lookup"><span data-stu-id="85ae2-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ae2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ae2-118">CommonParameters</span></span>
<span data-ttu-id="85ae2-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="85ae2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ae2-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="85ae2-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ae2-121">輸入</span><span class="sxs-lookup"><span data-stu-id="85ae2-121">INPUTS</span></span>

### <span data-ttu-id="85ae2-122">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="85ae2-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="85ae2-123">輸出</span><span class="sxs-lookup"><span data-stu-id="85ae2-123">OUTPUTS</span></span>

### <span data-ttu-id="85ae2-124">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="85ae2-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="85ae2-125">筆記</span><span class="sxs-lookup"><span data-stu-id="85ae2-125">NOTES</span></span>

## <span data-ttu-id="85ae2-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="85ae2-126">RELATED LINKS</span></span>

[<span data-ttu-id="85ae2-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="85ae2-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="85ae2-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="85ae2-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="85ae2-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="85ae2-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="85ae2-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="85ae2-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

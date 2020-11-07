---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c7d60c3d2f69e7ea18bcd256d8ad4a943817769a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790674"
---
# <span data-ttu-id="eadba-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="eadba-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="eadba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eadba-102">SYNOPSIS</span></span>
<span data-ttu-id="eadba-103">移除 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="eadba-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="eadba-104">句法</span><span class="sxs-lookup"><span data-stu-id="eadba-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eadba-105">說明</span><span class="sxs-lookup"><span data-stu-id="eadba-105">DESCRIPTION</span></span>
<span data-ttu-id="eadba-106">**AzExpressRouteCircuitPeeringConfig** Cmdlet 會移除 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="eadba-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="eadba-107">示例</span><span class="sxs-lookup"><span data-stu-id="eadba-107">EXAMPLES</span></span>

### <span data-ttu-id="eadba-108">範例1：從 ExpressRoute 回路移除對等設定</span><span class="sxs-lookup"><span data-stu-id="eadba-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="eadba-109">參數</span><span class="sxs-lookup"><span data-stu-id="eadba-109">PARAMETERS</span></span>

### <span data-ttu-id="eadba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eadba-110">-DefaultProfile</span></span>
<span data-ttu-id="eadba-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eadba-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eadba-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eadba-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="eadba-113">包含要移除之對等設定的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="eadba-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="eadba-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="eadba-114">-Name</span></span>
<span data-ttu-id="eadba-115">要移除之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="eadba-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="eadba-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="eadba-116">-PeerAddressType</span></span>
<span data-ttu-id="eadba-117">對等的位址族</span><span class="sxs-lookup"><span data-stu-id="eadba-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="eadba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadba-118">CommonParameters</span></span>
<span data-ttu-id="eadba-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eadba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadba-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eadba-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadba-121">輸入</span><span class="sxs-lookup"><span data-stu-id="eadba-121">INPUTS</span></span>

### <span data-ttu-id="eadba-122">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eadba-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="eadba-123">輸出</span><span class="sxs-lookup"><span data-stu-id="eadba-123">OUTPUTS</span></span>

### <span data-ttu-id="eadba-124">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eadba-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="eadba-125">筆記</span><span class="sxs-lookup"><span data-stu-id="eadba-125">NOTES</span></span>

## <span data-ttu-id="eadba-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="eadba-126">RELATED LINKS</span></span>

[<span data-ttu-id="eadba-127">附加 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="eadba-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="eadba-128">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eadba-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="eadba-129">新-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="eadba-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="eadba-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eadba-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

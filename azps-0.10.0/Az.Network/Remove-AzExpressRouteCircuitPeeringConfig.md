---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794181"
---
# <span data-ttu-id="192eb-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="192eb-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="192eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="192eb-102">SYNOPSIS</span></span>
<span data-ttu-id="192eb-103">移除 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="192eb-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="192eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="192eb-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="192eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="192eb-105">DESCRIPTION</span></span>
<span data-ttu-id="192eb-106">**AzExpressRouteCircuitPeeringConfig** Cmdlet 會移除 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="192eb-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="192eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="192eb-107">EXAMPLES</span></span>

### <span data-ttu-id="192eb-108">範例1：從 ExpressRoute 回路移除對等設定</span><span class="sxs-lookup"><span data-stu-id="192eb-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="192eb-109">參數</span><span class="sxs-lookup"><span data-stu-id="192eb-109">PARAMETERS</span></span>

### <span data-ttu-id="192eb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192eb-110">-DefaultProfile</span></span>
<span data-ttu-id="192eb-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="192eb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="192eb-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="192eb-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="192eb-113">包含要移除之對等設定的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="192eb-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="192eb-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="192eb-114">-Name</span></span>
<span data-ttu-id="192eb-115">要移除之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="192eb-115">The name of the peering configuration to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="192eb-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="192eb-116">-PeerAddressType</span></span>
<span data-ttu-id="192eb-117">對等的位址族</span><span class="sxs-lookup"><span data-stu-id="192eb-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="192eb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192eb-118">CommonParameters</span></span>
<span data-ttu-id="192eb-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="192eb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192eb-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="192eb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192eb-121">輸入</span><span class="sxs-lookup"><span data-stu-id="192eb-121">INPUTS</span></span>

### <span data-ttu-id="192eb-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="192eb-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="192eb-123">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="192eb-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="192eb-124">輸出</span><span class="sxs-lookup"><span data-stu-id="192eb-124">OUTPUTS</span></span>

### <span data-ttu-id="192eb-125">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="192eb-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="192eb-126">筆記</span><span class="sxs-lookup"><span data-stu-id="192eb-126">NOTES</span></span>

## <span data-ttu-id="192eb-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="192eb-127">RELATED LINKS</span></span>

[<span data-ttu-id="192eb-128">附加 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="192eb-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="192eb-129">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="192eb-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="192eb-130">新-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="192eb-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="192eb-131">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="192eb-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

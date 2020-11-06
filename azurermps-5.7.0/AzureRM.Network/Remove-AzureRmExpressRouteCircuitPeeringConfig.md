---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 36cf08aa4cb201beac284ae2296dfa508bf4edba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447035"
---
# <span data-ttu-id="8a824-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8a824-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="8a824-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a824-102">SYNOPSIS</span></span>
<span data-ttu-id="8a824-103">移除 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="8a824-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a824-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a824-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a824-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a824-105">DESCRIPTION</span></span>
<span data-ttu-id="8a824-106">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet 會移除 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="8a824-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="8a824-107">示例</span><span class="sxs-lookup"><span data-stu-id="8a824-107">EXAMPLES</span></span>

### <span data-ttu-id="8a824-108">範例1：從 ExpressRoute 回路移除對等設定</span><span class="sxs-lookup"><span data-stu-id="8a824-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="8a824-109">參數</span><span class="sxs-lookup"><span data-stu-id="8a824-109">PARAMETERS</span></span>

### <span data-ttu-id="8a824-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a824-110">-DefaultProfile</span></span>
<span data-ttu-id="8a824-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a824-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a824-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a824-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8a824-113">包含要移除之對等設定的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="8a824-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="8a824-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a824-114">-Name</span></span>
<span data-ttu-id="8a824-115">要移除之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a824-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="8a824-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8a824-116">-PeerAddressType</span></span>
<span data-ttu-id="8a824-117">對等的位址族</span><span class="sxs-lookup"><span data-stu-id="8a824-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="8a824-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a824-118">CommonParameters</span></span>
<span data-ttu-id="8a824-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a824-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a824-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a824-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a824-121">輸入</span><span class="sxs-lookup"><span data-stu-id="8a824-121">INPUTS</span></span>

### <span data-ttu-id="8a824-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a824-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="8a824-123">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8a824-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="8a824-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8a824-124">OUTPUTS</span></span>

### <span data-ttu-id="8a824-125">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8a824-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8a824-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8a824-126">NOTES</span></span>

## <span data-ttu-id="8a824-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a824-127">RELATED LINKS</span></span>

[<span data-ttu-id="8a824-128">附加 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8a824-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8a824-129">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a824-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8a824-130">新-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8a824-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8a824-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8a824-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

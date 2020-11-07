---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957288"
---
# <span data-ttu-id="21532-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="21532-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="21532-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21532-102">SYNOPSIS</span></span>
<span data-ttu-id="21532-103">針對快速路由線路更新在私人 Peerings 中建立的線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="21532-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="21532-104">句法</span><span class="sxs-lookup"><span data-stu-id="21532-104">SYNTAX</span></span>

### <span data-ttu-id="21532-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="21532-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21532-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="21532-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21532-107">說明</span><span class="sxs-lookup"><span data-stu-id="21532-107">DESCRIPTION</span></span>
<span data-ttu-id="21532-108">**AzExpressRouteCircuitConnectionConfig** Cmdlet 會更新針對 ExpressRoute 回路在私有對等中建立的線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="21532-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="21532-109">這可讓跨地區或訂閱的兩個 Express 路線電路對等。</span><span class="sxs-lookup"><span data-stu-id="21532-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="21532-110">請注意，在執行 **AzExpressRouteCircuitConnectionConfig 設定** 前，您必須使用 **AzExpressRouteCircuitConnectionConfig** 加入線路連線。</span><span class="sxs-lookup"><span data-stu-id="21532-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="21532-111">此外，在執行 **設定 AzExpressRouteCircuitPeeringConfig** 之後，您必須呼叫 Set-AzExpressRouteCircuit Cmdlet 才能啟動設定。</span><span class="sxs-lookup"><span data-stu-id="21532-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="21532-112">示例</span><span class="sxs-lookup"><span data-stu-id="21532-112">EXAMPLES</span></span>

### <span data-ttu-id="21532-113">範例1：將線路連線資源更新至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="21532-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="21532-114">範例2：使用管道將線路連線設定設定成現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="21532-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="21532-115">參數</span><span class="sxs-lookup"><span data-stu-id="21532-115">PARAMETERS</span></span>

### <span data-ttu-id="21532-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="21532-116">-AddressPrefix</span></span>
<span data-ttu-id="21532-117">最小/29 個客戶位址空間，可在 IPv4 隧道的快速路由回路之間建立 VxLan 隧道。</span><span class="sxs-lookup"><span data-stu-id="21532-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="21532-118">或最小的/125 客戶位址空間，以在 IPv6 隧道的快速路由回路之間建立 VxLan 隧道。</span><span class="sxs-lookup"><span data-stu-id="21532-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="21532-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="21532-119">-AddressPrefixType</span></span>
<span data-ttu-id="21532-120">指定位址首碼所屬的位址族。</span><span class="sxs-lookup"><span data-stu-id="21532-120">Specifies the address family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21532-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="21532-121">-AuthorizationKey</span></span>
<span data-ttu-id="21532-122">另一個訂閱中對等快速路由回路的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="21532-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="21532-123">您可以使用現有的命令來建立對等電路的授權。</span><span class="sxs-lookup"><span data-stu-id="21532-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="21532-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21532-124">-DefaultProfile</span></span>
<span data-ttu-id="21532-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21532-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21532-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="21532-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="21532-127">要修改的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="21532-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="21532-128">這是 **AzExpressRouteCircuit** Cmdlet 傳回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="21532-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21532-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="21532-129">-Name</span></span>
<span data-ttu-id="21532-130">要新增之電路連線資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="21532-130">The name of the circuit connection resource to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21532-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="21532-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="21532-132">要與目前電路 peered 的私人對等遠端電路對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="21532-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21532-133">-確認</span><span class="sxs-lookup"><span data-stu-id="21532-133">-Confirm</span></span>
<span data-ttu-id="21532-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21532-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21532-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21532-135">-WhatIf</span></span>
<span data-ttu-id="21532-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21532-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21532-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21532-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21532-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21532-138">CommonParameters</span></span>
<span data-ttu-id="21532-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21532-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21532-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21532-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21532-141">輸入</span><span class="sxs-lookup"><span data-stu-id="21532-141">INPUTS</span></span>

### <span data-ttu-id="21532-142">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="21532-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="21532-143">System.object</span><span class="sxs-lookup"><span data-stu-id="21532-143">System.String</span></span>

## <span data-ttu-id="21532-144">輸出</span><span class="sxs-lookup"><span data-stu-id="21532-144">OUTPUTS</span></span>

### <span data-ttu-id="21532-145">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="21532-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="21532-146">筆記</span><span class="sxs-lookup"><span data-stu-id="21532-146">NOTES</span></span>

## <span data-ttu-id="21532-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="21532-147">RELATED LINKS</span></span>

[<span data-ttu-id="21532-148">AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="21532-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="21532-149">移除-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="21532-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="21532-150">附加 AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="21532-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="21532-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="21532-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="21532-152">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="21532-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

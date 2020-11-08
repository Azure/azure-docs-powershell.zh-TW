---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139042"
---
# <span data-ttu-id="f3ac4-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f3ac4-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="f3ac4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ac4-103">將線路連線設定新增到快速路由線路的專用對等。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="f3ac4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3ac4-104">SYNTAX</span></span>

### <span data-ttu-id="f3ac4-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f3ac4-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3ac4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3ac4-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3ac4-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3ac4-107">DESCRIPTION</span></span>
<span data-ttu-id="f3ac4-108">**AzExpressRouteCircuitConnectionConfig** Cmdlet 會將線路連線設定新增至 ExpressRoute 回路的專用對等。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="f3ac4-109">這可讓跨地區或訂閱的兩個 Express 路線電路對等。請注意，執行 **附加 AzExpressRouteCircuitConnectionConfig** 之後，您必須呼叫 Set-AzExpressRouteCircuit Cmdlet 才能啟動設定。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="f3ac4-110">示例</span><span class="sxs-lookup"><span data-stu-id="f3ac4-110">EXAMPLES</span></span>

### <span data-ttu-id="f3ac4-111">範例1：將電路連線資源新增至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="f3ac4-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="f3ac4-112">範例2：使用管道將電路連線設定新增至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="f3ac4-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="f3ac4-113">參數</span><span class="sxs-lookup"><span data-stu-id="f3ac4-113">PARAMETERS</span></span>

### <span data-ttu-id="f3ac4-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f3ac4-114">-AddressPrefix</span></span>
<span data-ttu-id="f3ac4-115">最小/29 個客戶位址空間，可在 IPv4 隧道的快速路由回路之間建立 VxLan 隧道。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="f3ac4-116">或最小的/125 客戶位址空間，以在 IPv6 隧道的快速路由回路之間建立 VxLan 隧道。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="f3ac4-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="f3ac4-117">-AddressPrefixType</span></span>
<span data-ttu-id="f3ac4-118">這會指定位址首碼所屬的位址族。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="f3ac4-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="f3ac4-119">-AuthorizationKey</span></span>
<span data-ttu-id="f3ac4-120">另一個訂閱中對等快速路由回路的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="f3ac4-121">您可以使用現有的命令來建立對等電路的授權。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="f3ac4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ac4-122">-DefaultProfile</span></span>
<span data-ttu-id="f3ac4-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3ac4-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f3ac4-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f3ac4-125">要修改的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="f3ac4-126">這是 **AzExpressRouteCircuit** Cmdlet 傳回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="f3ac4-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3ac4-127">-Name</span></span>
<span data-ttu-id="f3ac4-128">要新增之電路連線資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="f3ac4-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="f3ac4-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="f3ac4-130">要與目前電路 peered 的私人對等遠端電路對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="f3ac4-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f3ac4-131">-Confirm</span></span>
<span data-ttu-id="f3ac4-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ac4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ac4-133">-WhatIf</span></span>
<span data-ttu-id="f3ac4-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3ac4-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ac4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ac4-136">CommonParameters</span></span>
<span data-ttu-id="f3ac4-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ac4-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3ac4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ac4-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f3ac4-139">INPUTS</span></span>

### <span data-ttu-id="f3ac4-140">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3ac4-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="f3ac4-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f3ac4-141">System.String</span></span>

## <span data-ttu-id="f3ac4-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f3ac4-142">OUTPUTS</span></span>

### <span data-ttu-id="f3ac4-143">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3ac4-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f3ac4-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f3ac4-144">NOTES</span></span>

## <span data-ttu-id="f3ac4-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3ac4-145">RELATED LINKS</span></span>

[<span data-ttu-id="f3ac4-146">AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f3ac4-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f3ac4-147">移除-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f3ac4-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f3ac4-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f3ac4-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f3ac4-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f3ac4-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="f3ac4-150">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f3ac4-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
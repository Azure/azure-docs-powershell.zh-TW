---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901934"
---
# <span data-ttu-id="cdb33-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cdb33-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="cdb33-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cdb33-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb33-103">更新在 Express Route 回路的專用對等互連中建立回路連接組。</span><span class="sxs-lookup"><span data-stu-id="cdb33-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="cdb33-104">語法</span><span class="sxs-lookup"><span data-stu-id="cdb33-104">SYNTAX</span></span>

### <span data-ttu-id="cdb33-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="cdb33-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb33-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb33-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb33-107">描述</span><span class="sxs-lookup"><span data-stu-id="cdb33-107">DESCRIPTION</span></span>
<span data-ttu-id="cdb33-108">**Set-AzExpressRouteRouteCircuitConnectionConfig** Cmdlet 會更新在 ExpressRoute 回路的專用對等中建立回路連接設定。</span><span class="sxs-lookup"><span data-stu-id="cdb33-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="cdb33-109">這可讓跨區域或訂閱對等兩個 Express Route 回路。</span><span class="sxs-lookup"><span data-stu-id="cdb33-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="cdb33-110">請注意，在啟動 **Set-AzExpressRouteRouteCircuitConnectionConfig** 之前，您必須使用 **Add-AzExpressRouteRouteCircuitConnectionConfig** 來新增回路連接。</span><span class="sxs-lookup"><span data-stu-id="cdb33-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="cdb33-111">此外，在啟動 **Set-AzExpressRouteRouteCircuitPeeringConfig** 之後，您必須撥打 Set-AzExpressRouteCircuit Cmdlet 以啟用設定。</span><span class="sxs-lookup"><span data-stu-id="cdb33-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="cdb33-112">例子</span><span class="sxs-lookup"><span data-stu-id="cdb33-112">EXAMPLES</span></span>

### <span data-ttu-id="cdb33-113">範例 1：將回路連接資源更新至現有的 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="cdb33-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="cdb33-114">範例 2：使用管道設定回路連接設定至現有的 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="cdb33-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="cdb33-115">參數</span><span class="sxs-lookup"><span data-stu-id="cdb33-115">PARAMETERS</span></span>

### <span data-ttu-id="cdb33-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cdb33-116">-AddressPrefix</span></span>
<span data-ttu-id="cdb33-117">最低 /29 個客戶位址空間，以在 Express Route 回路之間為 IPv4 軸線建立 VxLan 軸線。</span><span class="sxs-lookup"><span data-stu-id="cdb33-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="cdb33-118">或最低 /125 個客戶位址空間，以在 Express Route 回路之間為 IPv6 軸線建立 VxLan 軸線。</span><span class="sxs-lookup"><span data-stu-id="cdb33-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="cdb33-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="cdb33-119">-AddressPrefixType</span></span>
<span data-ttu-id="cdb33-120">指定位址首碼所屬的位址系列。</span><span class="sxs-lookup"><span data-stu-id="cdb33-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="cdb33-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="cdb33-121">-AuthorizationKey</span></span>
<span data-ttu-id="cdb33-122">在另一個訂閱中對等 Express Route 回路的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="cdb33-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="cdb33-123">您可以使用現有的命令建立對等回路上的授權。</span><span class="sxs-lookup"><span data-stu-id="cdb33-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="cdb33-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb33-124">-DefaultProfile</span></span>
<span data-ttu-id="cdb33-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdb33-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb33-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cdb33-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cdb33-127">要修改的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="cdb33-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="cdb33-128">這是 **Get-AzExpressRouteCircuit Cmdlet** 所返回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="cdb33-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="cdb33-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="cdb33-129">-Name</span></span>
<span data-ttu-id="cdb33-130">要新增的回路連接資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb33-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="cdb33-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="cdb33-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="cdb33-132">與目前回路對等的遠端回路之私人對等的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cdb33-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="cdb33-133">-確認</span><span class="sxs-lookup"><span data-stu-id="cdb33-133">-Confirm</span></span>
<span data-ttu-id="cdb33-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cdb33-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb33-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb33-135">-WhatIf</span></span>
<span data-ttu-id="cdb33-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cdb33-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdb33-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdb33-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb33-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb33-138">CommonParameters</span></span>
<span data-ttu-id="cdb33-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cdb33-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb33-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cdb33-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb33-141">輸入</span><span class="sxs-lookup"><span data-stu-id="cdb33-141">INPUTS</span></span>

### <span data-ttu-id="cdb33-142">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cdb33-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="cdb33-143">System.String</span><span class="sxs-lookup"><span data-stu-id="cdb33-143">System.String</span></span>

## <span data-ttu-id="cdb33-144">輸出</span><span class="sxs-lookup"><span data-stu-id="cdb33-144">OUTPUTS</span></span>

### <span data-ttu-id="cdb33-145">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cdb33-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cdb33-146">筆記</span><span class="sxs-lookup"><span data-stu-id="cdb33-146">NOTES</span></span>

## <span data-ttu-id="cdb33-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdb33-147">RELATED LINKS</span></span>

[<span data-ttu-id="cdb33-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cdb33-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="cdb33-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cdb33-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="cdb33-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cdb33-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="cdb33-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cdb33-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="cdb33-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cdb33-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

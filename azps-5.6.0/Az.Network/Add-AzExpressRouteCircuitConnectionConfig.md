---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 19ceeb045c3a7cc86dd9152ee08d12078d858240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903186"
---
# <span data-ttu-id="61159-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="61159-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="61159-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61159-102">SYNOPSIS</span></span>
<span data-ttu-id="61159-103">新增回路連接組對 Express Route 回路的專用對等。</span><span class="sxs-lookup"><span data-stu-id="61159-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="61159-104">語法</span><span class="sxs-lookup"><span data-stu-id="61159-104">SYNTAX</span></span>

### <span data-ttu-id="61159-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="61159-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61159-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="61159-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61159-107">描述</span><span class="sxs-lookup"><span data-stu-id="61159-107">DESCRIPTION</span></span>
<span data-ttu-id="61159-108">**Add-AzExpressRouteRouteCircuitConnectionConfig** Cmdlet 會將回路連接組配置新增到 ExpressRoute 回路的私人對等。</span><span class="sxs-lookup"><span data-stu-id="61159-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="61159-109">這可讓跨區域或訂閱對等兩個 Express Route 回路。請注意，在啟動 **Add-AzExpressRouteRouteCircuitConnectionConfig** 之後，您必須呼叫 Set-AzExpressRouteCircuit Cmdlet 以啟用該組配置。</span><span class="sxs-lookup"><span data-stu-id="61159-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="61159-110">例子</span><span class="sxs-lookup"><span data-stu-id="61159-110">EXAMPLES</span></span>

### <span data-ttu-id="61159-111">範例 1：新增回路連接資源至現有的 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="61159-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="61159-112">範例 2：使用管道將回路連接組組新增到現有的 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="61159-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="61159-113">參數</span><span class="sxs-lookup"><span data-stu-id="61159-113">PARAMETERS</span></span>

### <span data-ttu-id="61159-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="61159-114">-AddressPrefix</span></span>
<span data-ttu-id="61159-115">最低 /29 個客戶位址空間，以在 Express Route 回路之間為 IPv4 軸線建立 VxLan 軸線。</span><span class="sxs-lookup"><span data-stu-id="61159-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="61159-116">或最低 /125 個客戶位址空間，以在 Express Route 回路之間為 IPv6 軸線建立 VxLan 軸線。</span><span class="sxs-lookup"><span data-stu-id="61159-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="61159-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="61159-117">-AddressPrefixType</span></span>
<span data-ttu-id="61159-118">這會指定位址首碼所屬的位址系列。</span><span class="sxs-lookup"><span data-stu-id="61159-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="61159-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="61159-119">-AuthorizationKey</span></span>
<span data-ttu-id="61159-120">在另一個訂閱中對等 Express Route 回路的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="61159-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="61159-121">您可以使用現有的命令建立對等回路上的授權。</span><span class="sxs-lookup"><span data-stu-id="61159-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="61159-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61159-122">-DefaultProfile</span></span>
<span data-ttu-id="61159-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="61159-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61159-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61159-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="61159-125">要修改的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="61159-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="61159-126">這是 **Get-AzExpressRouteCircuit Cmdlet** 所返回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="61159-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="61159-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="61159-127">-Name</span></span>
<span data-ttu-id="61159-128">要新增的回路連接資源名稱。</span><span class="sxs-lookup"><span data-stu-id="61159-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="61159-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="61159-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="61159-130">與目前回路對等的遠端回路之私人對等的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="61159-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="61159-131">-確認</span><span class="sxs-lookup"><span data-stu-id="61159-131">-Confirm</span></span>
<span data-ttu-id="61159-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61159-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61159-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61159-133">-WhatIf</span></span>
<span data-ttu-id="61159-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61159-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61159-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61159-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61159-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61159-136">CommonParameters</span></span>
<span data-ttu-id="61159-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61159-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61159-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="61159-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61159-139">輸入</span><span class="sxs-lookup"><span data-stu-id="61159-139">INPUTS</span></span>

### <span data-ttu-id="61159-140">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61159-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="61159-141">System.String</span><span class="sxs-lookup"><span data-stu-id="61159-141">System.String</span></span>

## <span data-ttu-id="61159-142">輸出</span><span class="sxs-lookup"><span data-stu-id="61159-142">OUTPUTS</span></span>

### <span data-ttu-id="61159-143">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61159-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="61159-144">筆記</span><span class="sxs-lookup"><span data-stu-id="61159-144">NOTES</span></span>

## <span data-ttu-id="61159-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="61159-145">RELATED LINKS</span></span>

[<span data-ttu-id="61159-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="61159-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="61159-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="61159-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="61159-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="61159-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="61159-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61159-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="61159-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="61159-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
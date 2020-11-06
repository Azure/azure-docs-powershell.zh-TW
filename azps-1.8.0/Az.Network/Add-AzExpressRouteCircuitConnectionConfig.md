---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: a3b5b20eac34076dd6a5490a5d9cf1a5e2c49684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622166"
---
# <span data-ttu-id="799cf-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="799cf-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="799cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="799cf-102">SYNOPSIS</span></span>
<span data-ttu-id="799cf-103">將線路連線設定新增到快速路由線路的專用對等。</span><span class="sxs-lookup"><span data-stu-id="799cf-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="799cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="799cf-104">SYNTAX</span></span>

### <span data-ttu-id="799cf-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="799cf-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="799cf-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="799cf-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="799cf-107">說明</span><span class="sxs-lookup"><span data-stu-id="799cf-107">DESCRIPTION</span></span>
<span data-ttu-id="799cf-108">**AzExpressRouteCircuitConnectionConfig** Cmdlet 會將線路連線設定新增至 ExpressRoute 回路的專用對等。</span><span class="sxs-lookup"><span data-stu-id="799cf-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="799cf-109">這可讓跨地區或訂閱的兩個 Express 路線電路對等。請注意，執行 **附加 AzExpressRouteCircuitPeeringConfig** 之後，您必須呼叫 Set-AzExpressRouteCircuit Cmdlet 才能啟動設定。</span><span class="sxs-lookup"><span data-stu-id="799cf-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="799cf-110">示例</span><span class="sxs-lookup"><span data-stu-id="799cf-110">EXAMPLES</span></span>

### <span data-ttu-id="799cf-111">範例1：將電路連線資源新增至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="799cf-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="799cf-112">範例2：使用管道將電路連線設定新增至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="799cf-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="799cf-113">參數</span><span class="sxs-lookup"><span data-stu-id="799cf-113">PARAMETERS</span></span>

### <span data-ttu-id="799cf-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="799cf-114">-AddressPrefix</span></span>
<span data-ttu-id="799cf-115">在快速路線回路之間建立 VxLan 隧道的最小/29 個客戶位址空間</span><span class="sxs-lookup"><span data-stu-id="799cf-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="799cf-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="799cf-116">-AuthorizationKey</span></span>
<span data-ttu-id="799cf-117">另一個訂閱中對等快速路由回路的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="799cf-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="799cf-118">您可以使用現有的命令來建立對等電路的授權。</span><span class="sxs-lookup"><span data-stu-id="799cf-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="799cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799cf-119">-DefaultProfile</span></span>
<span data-ttu-id="799cf-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="799cf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="799cf-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="799cf-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="799cf-122">要修改的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="799cf-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="799cf-123">這是 **AzExpressRouteCircuit** Cmdlet 傳回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="799cf-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="799cf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="799cf-124">-Name</span></span>
<span data-ttu-id="799cf-125">要新增之電路連線資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="799cf-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="799cf-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="799cf-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="799cf-127">要與目前電路 peered 的私人對等遠端電路對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="799cf-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="799cf-128">-確認</span><span class="sxs-lookup"><span data-stu-id="799cf-128">-Confirm</span></span>
<span data-ttu-id="799cf-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="799cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="799cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="799cf-130">-WhatIf</span></span>
<span data-ttu-id="799cf-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="799cf-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="799cf-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="799cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="799cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799cf-133">CommonParameters</span></span>
<span data-ttu-id="799cf-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="799cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799cf-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="799cf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799cf-136">輸入</span><span class="sxs-lookup"><span data-stu-id="799cf-136">INPUTS</span></span>

### <span data-ttu-id="799cf-137">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="799cf-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="799cf-138">System.object</span><span class="sxs-lookup"><span data-stu-id="799cf-138">System.String</span></span>

## <span data-ttu-id="799cf-139">輸出</span><span class="sxs-lookup"><span data-stu-id="799cf-139">OUTPUTS</span></span>

### <span data-ttu-id="799cf-140">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="799cf-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="799cf-141">筆記</span><span class="sxs-lookup"><span data-stu-id="799cf-141">NOTES</span></span>

## <span data-ttu-id="799cf-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="799cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="799cf-143">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="799cf-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="799cf-144">AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="799cf-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="799cf-145">移除-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="799cf-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="799cf-146">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="799cf-146">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="799cf-147">新-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="799cf-147">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="799cf-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="799cf-148">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="799cf-149">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="799cf-149">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
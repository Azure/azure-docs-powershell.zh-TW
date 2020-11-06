---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455224"
---
# <span data-ttu-id="c2647-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c2647-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="c2647-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2647-102">SYNOPSIS</span></span>
<span data-ttu-id="c2647-103">將線路連線設定新增到快速路由線路的專用對等。</span><span class="sxs-lookup"><span data-stu-id="c2647-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2647-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2647-104">SYNTAX</span></span>

### <span data-ttu-id="c2647-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c2647-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2647-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2647-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2647-107">說明</span><span class="sxs-lookup"><span data-stu-id="c2647-107">DESCRIPTION</span></span>
<span data-ttu-id="c2647-108">**AzureRmExpressRouteCircuitConnectionConfig** Cmdlet 會將線路連線設定新增至 ExpressRoute 回路的專用對等。</span><span class="sxs-lookup"><span data-stu-id="c2647-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="c2647-109">這可讓跨地區或訂閱的兩個 Express 路線電路對等。請注意，執行 **附加 AzureRmExpressRouteCircuitPeeringConfig** 之後，您必須呼叫 Set-AzureRmExpressRouteCircuit Cmdlet 才能啟動設定。</span><span class="sxs-lookup"><span data-stu-id="c2647-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="c2647-110">示例</span><span class="sxs-lookup"><span data-stu-id="c2647-110">EXAMPLES</span></span>

### <span data-ttu-id="c2647-111">範例1：將電路連線資源新增至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="c2647-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="c2647-112">範例2：使用管道將電路連線設定新增至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="c2647-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="c2647-113">參數</span><span class="sxs-lookup"><span data-stu-id="c2647-113">PARAMETERS</span></span>

### <span data-ttu-id="c2647-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c2647-114">-AddressPrefix</span></span>
<span data-ttu-id="c2647-115">在快速路線回路之間建立 VxLan 隧道的最小/29 個客戶位址空間</span><span class="sxs-lookup"><span data-stu-id="c2647-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="c2647-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="c2647-116">-AuthorizationKey</span></span>
<span data-ttu-id="c2647-117">另一個訂閱中對等快速路由回路的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2647-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="c2647-118">您可以使用現有的命令來建立對等電路的授權。</span><span class="sxs-lookup"><span data-stu-id="c2647-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="c2647-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2647-119">-DefaultProfile</span></span>
<span data-ttu-id="c2647-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2647-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2647-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c2647-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c2647-122">要修改的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="c2647-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="c2647-123">這是 **AzureRmExpressRouteCircuit** Cmdlet 傳回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="c2647-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="c2647-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2647-124">-Name</span></span>
<span data-ttu-id="c2647-125">要新增之電路連線資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2647-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="c2647-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="c2647-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="c2647-127">要與目前電路 peered 的私人對等遠端電路對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2647-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="c2647-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c2647-128">-Confirm</span></span>
<span data-ttu-id="c2647-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2647-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2647-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2647-130">-WhatIf</span></span>
<span data-ttu-id="c2647-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2647-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2647-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2647-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2647-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2647-133">CommonParameters</span></span>
<span data-ttu-id="c2647-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2647-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2647-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2647-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2647-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c2647-136">INPUTS</span></span>

### <span data-ttu-id="c2647-137">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2647-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="c2647-138">參數： ExpressRouteCircuit (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c2647-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="c2647-139">System.object</span><span class="sxs-lookup"><span data-stu-id="c2647-139">System.String</span></span>

## <span data-ttu-id="c2647-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c2647-140">OUTPUTS</span></span>

### <span data-ttu-id="c2647-141">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2647-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c2647-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c2647-142">NOTES</span></span>

## <span data-ttu-id="c2647-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2647-143">RELATED LINKS</span></span>

[<span data-ttu-id="c2647-144">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c2647-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c2647-145">AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c2647-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c2647-146">移除-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c2647-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c2647-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c2647-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c2647-148">新-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c2647-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c2647-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c2647-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c2647-150">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c2647-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

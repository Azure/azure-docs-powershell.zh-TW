---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 78adeb351c0b18fe8ca7e3c3a2d286abe2f97400
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908382"
---
# <span data-ttu-id="63623-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="63623-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="63623-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63623-102">SYNOPSIS</span></span>
<span data-ttu-id="63623-103">在虛擬網路閘道與 on-prem VPN 裝置之間建立網站對網站 VPN 連接。</span><span class="sxs-lookup"><span data-stu-id="63623-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="63623-104">語法</span><span class="sxs-lookup"><span data-stu-id="63623-104">SYNTAX</span></span>

### <span data-ttu-id="63623-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="63623-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63623-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63623-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63623-107">描述</span><span class="sxs-lookup"><span data-stu-id="63623-107">DESCRIPTION</span></span>
<span data-ttu-id="63623-108">在虛擬網路閘道與 on-prem VPN 裝置之間建立網站對網站 VPN 連接。</span><span class="sxs-lookup"><span data-stu-id="63623-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="63623-109">例子</span><span class="sxs-lookup"><span data-stu-id="63623-109">EXAMPLES</span></span>

### <span data-ttu-id="63623-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="63623-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="63623-111">參數</span><span class="sxs-lookup"><span data-stu-id="63623-111">PARAMETERS</span></span>

### <span data-ttu-id="63623-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63623-112">-AsJob</span></span>
<span data-ttu-id="63623-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="63623-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63623-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="63623-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="63623-115">-ConnectionProtocol</span></span>
<span data-ttu-id="63623-116">閘道連接通訊協定：IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="63623-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63623-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="63623-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63623-118">-DefaultProfile</span></span>
<span data-ttu-id="63623-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63623-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63623-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="63623-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="63623-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-122">-強制</span><span class="sxs-lookup"><span data-stu-id="63623-122">-Force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63623-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="63623-123">-IpsecPolicies</span></span>
<span data-ttu-id="63623-124">IPSec 政策清單。</span><span class="sxs-lookup"><span data-stu-id="63623-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="63623-125">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-126">-位置</span><span class="sxs-lookup"><span data-stu-id="63623-126">-Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="63623-127">-Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-128">-對等</span><span class="sxs-lookup"><span data-stu-id="63623-128">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="63623-129">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63623-130">-ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="63623-131">-RoutingWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-132">-DpdTimeoutIn用秒</span><span class="sxs-lookup"><span data-stu-id="63623-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="63623-133">在數秒後，連接會暫停對等偵測</span><span class="sxs-lookup"><span data-stu-id="63623-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-134">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="63623-134">-ConnectionMode</span></span>
<span data-ttu-id="63623-135">虛擬網路閘道連接模式</span><span class="sxs-lookup"><span data-stu-id="63623-135">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="63623-136">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="63623-136">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-137">-標記</span><span class="sxs-lookup"><span data-stu-id="63623-137">-Tag</span></span>
<span data-ttu-id="63623-138">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="63623-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="63623-139">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="63623-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-140">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="63623-140">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="63623-141">流量選取器規則清單。</span><span class="sxs-lookup"><span data-stu-id="63623-141">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-142">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="63623-142">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="63623-143">是否要使用 PrivateIP 進行此 S2S VPN 服務</span><span class="sxs-lookup"><span data-stu-id="63623-143">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-144">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="63623-144">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="63623-145">針對 S2S 連接使用以策略為基礎的流量選取器</span><span class="sxs-lookup"><span data-stu-id="63623-145">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63623-146">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="63623-146">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-147">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="63623-147">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63623-148">-確認</span><span class="sxs-lookup"><span data-stu-id="63623-148">-Confirm</span></span>
<span data-ttu-id="63623-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="63623-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63623-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63623-150">-WhatIf</span></span>
<span data-ttu-id="63623-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63623-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63623-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63623-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63623-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63623-153">CommonParameters</span></span>
<span data-ttu-id="63623-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63623-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63623-155">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="63623-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63623-156">輸入</span><span class="sxs-lookup"><span data-stu-id="63623-156">INPUTS</span></span>

### <span data-ttu-id="63623-157">System.String</span><span class="sxs-lookup"><span data-stu-id="63623-157">System.String</span></span>

### <span data-ttu-id="63623-158">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63623-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="63623-159">Microsoft.Azure.Commands.Network.models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63623-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="63623-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="63623-160">System.Int32</span></span>

### <span data-ttu-id="63623-161">Microsoft.Azure.Commands.Network.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="63623-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="63623-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63623-162">System.Boolean</span></span>

### <span data-ttu-id="63623-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="63623-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="63623-164">Microsoft.Azure.Commands.Network.models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="63623-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="63623-165">Microsoft.Azure.Commands.Network.models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="63623-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="63623-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63623-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63623-167">輸出</span><span class="sxs-lookup"><span data-stu-id="63623-167">OUTPUTS</span></span>

### <span data-ttu-id="63623-168">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="63623-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="63623-169">筆記</span><span class="sxs-lookup"><span data-stu-id="63623-169">NOTES</span></span>

## <span data-ttu-id="63623-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="63623-170">RELATED LINKS</span></span>

[<span data-ttu-id="63623-171">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="63623-171">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="63623-172">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="63623-172">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="63623-173">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="63623-173">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 120e20eb62b5475a587a3d272e84c7af1e40cd45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140334"
---
# <span data-ttu-id="6c7a5-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6c7a5-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6c7a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7a5-103">在虛擬網路閘道與內部部署 VPN 裝置之間建立點對點 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="6c7a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c7a5-104">SYNTAX</span></span>

### <span data-ttu-id="6c7a5-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="6c7a5-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="6c7a5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c7a5-106">SetByResourceId</span></span>
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

## <span data-ttu-id="6c7a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c7a5-107">DESCRIPTION</span></span>
<span data-ttu-id="6c7a5-108">在虛擬網路閘道與內部部署 VPN 裝置之間建立點對點 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="6c7a5-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c7a5-109">EXAMPLES</span></span>

### <span data-ttu-id="6c7a5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6c7a5-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="6c7a5-111">參數</span><span class="sxs-lookup"><span data-stu-id="6c7a5-111">PARAMETERS</span></span>

### <span data-ttu-id="6c7a5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c7a5-112">-AsJob</span></span>
<span data-ttu-id="6c7a5-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6c7a5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c7a5-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="6c7a5-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="6c7a5-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="6c7a5-115">-ConnectionProtocol</span></span>
<span data-ttu-id="6c7a5-116">閘道連線通訊協定： IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="6c7a5-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="6c7a5-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="6c7a5-117">-ConnectionType</span></span>

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

### <span data-ttu-id="6c7a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7a5-118">-DefaultProfile</span></span>
<span data-ttu-id="6c7a5-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c7a5-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6c7a5-120">-EnableBgp</span></span>

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

### <span data-ttu-id="6c7a5-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="6c7a5-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="6c7a5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6c7a5-122">-Force</span></span>

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

### <span data-ttu-id="6c7a5-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="6c7a5-123">-IpsecPolicies</span></span>
<span data-ttu-id="6c7a5-124">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="6c7a5-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="6c7a5-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="6c7a5-126">-位置</span><span class="sxs-lookup"><span data-stu-id="6c7a5-126">-Location</span></span>

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

### <span data-ttu-id="6c7a5-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c7a5-127">-Name</span></span>

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

### <span data-ttu-id="6c7a5-128">對等</span><span class="sxs-lookup"><span data-stu-id="6c7a5-128">-Peer</span></span>

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

### <span data-ttu-id="6c7a5-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="6c7a5-129">-PeerId</span></span>

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

### <span data-ttu-id="6c7a5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c7a5-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="6c7a5-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="6c7a5-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="6c7a5-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="6c7a5-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="6c7a5-133">連線的死對等檢測超時值（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="6c7a5-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="6c7a5-134">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="6c7a5-134">-ConnectionMode</span></span>
<span data-ttu-id="6c7a5-135">虛擬網路閘道連線模式</span><span class="sxs-lookup"><span data-stu-id="6c7a5-135">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="6c7a5-136">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6c7a5-136">-SharedKey</span></span>

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

### <span data-ttu-id="6c7a5-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c7a5-137">-Tag</span></span>
<span data-ttu-id="6c7a5-138">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6c7a5-139">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6c7a5-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6c7a5-140">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6c7a5-140">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="6c7a5-141">流量選取器原則的清單。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-141">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="6c7a5-142">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="6c7a5-142">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="6c7a5-143">是否針對此 S2S VPN 隧道使用 PrivateIP</span><span class="sxs-lookup"><span data-stu-id="6c7a5-143">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

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

### <span data-ttu-id="6c7a5-144">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6c7a5-144">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6c7a5-145">針對 S2S 連線使用原則式流量選擇器</span><span class="sxs-lookup"><span data-stu-id="6c7a5-145">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="6c7a5-146">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="6c7a5-146">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="6c7a5-147">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="6c7a5-147">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="6c7a5-148">-確認</span><span class="sxs-lookup"><span data-stu-id="6c7a5-148">-Confirm</span></span>
<span data-ttu-id="6c7a5-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c7a5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c7a5-150">-WhatIf</span></span>
<span data-ttu-id="6c7a5-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c7a5-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c7a5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7a5-153">CommonParameters</span></span>
<span data-ttu-id="6c7a5-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7a5-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c7a5-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7a5-156">輸入</span><span class="sxs-lookup"><span data-stu-id="6c7a5-156">INPUTS</span></span>

### <span data-ttu-id="6c7a5-157">System.object</span><span class="sxs-lookup"><span data-stu-id="6c7a5-157">System.String</span></span>

### <span data-ttu-id="6c7a5-158">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c7a5-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="6c7a5-159">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c7a5-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="6c7a5-160">System.object</span><span class="sxs-lookup"><span data-stu-id="6c7a5-160">System.Int32</span></span>

### <span data-ttu-id="6c7a5-161">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c7a5-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="6c7a5-162">System.object</span><span class="sxs-lookup"><span data-stu-id="6c7a5-162">System.Boolean</span></span>

### <span data-ttu-id="6c7a5-163">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c7a5-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6c7a5-164">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6c7a5-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="6c7a5-165">PSTrafficSelectorPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6c7a5-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="6c7a5-166">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="6c7a5-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6c7a5-167">輸出</span><span class="sxs-lookup"><span data-stu-id="6c7a5-167">OUTPUTS</span></span>

### <span data-ttu-id="6c7a5-168">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c7a5-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6c7a5-169">筆記</span><span class="sxs-lookup"><span data-stu-id="6c7a5-169">NOTES</span></span>

## <span data-ttu-id="6c7a5-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c7a5-170">RELATED LINKS</span></span>

[<span data-ttu-id="6c7a5-171">AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6c7a5-171">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6c7a5-172">移除-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6c7a5-172">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6c7a5-173">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6c7a5-173">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)

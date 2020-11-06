---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: a9ad0933ce42dc0d031d9ca44d9b5ff7b84d6b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451832"
---
# <span data-ttu-id="53cbc-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="53cbc-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="53cbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="53cbc-103">在虛擬網路閘道與內部部署 VPN 裝置之間建立點對點 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="53cbc-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53cbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="53cbc-104">SYNTAX</span></span>

### <span data-ttu-id="53cbc-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="53cbc-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53cbc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53cbc-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53cbc-107">說明</span><span class="sxs-lookup"><span data-stu-id="53cbc-107">DESCRIPTION</span></span>
<span data-ttu-id="53cbc-108">在虛擬網路閘道與內部部署 VPN 裝置之間建立點對點 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="53cbc-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="53cbc-109">示例</span><span class="sxs-lookup"><span data-stu-id="53cbc-109">EXAMPLES</span></span>

### <span data-ttu-id="53cbc-110">範例1</span><span class="sxs-lookup"><span data-stu-id="53cbc-110">Example 1</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="53cbc-111">參數</span><span class="sxs-lookup"><span data-stu-id="53cbc-111">PARAMETERS</span></span>

### <span data-ttu-id="53cbc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53cbc-112">-AsJob</span></span>
<span data-ttu-id="53cbc-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="53cbc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53cbc-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="53cbc-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="53cbc-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="53cbc-115">-ConnectionType</span></span>

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

### <span data-ttu-id="53cbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53cbc-116">-DefaultProfile</span></span>
<span data-ttu-id="53cbc-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53cbc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53cbc-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="53cbc-118">-EnableBgp</span></span>

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

### <span data-ttu-id="53cbc-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="53cbc-119">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input:  True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53cbc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="53cbc-120">-Force</span></span>

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

### <span data-ttu-id="53cbc-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="53cbc-121">-IpsecPolicies</span></span>
<span data-ttu-id="53cbc-122">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="53cbc-122">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53cbc-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="53cbc-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="53cbc-124">-位置</span><span class="sxs-lookup"><span data-stu-id="53cbc-124">-Location</span></span>

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

### <span data-ttu-id="53cbc-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="53cbc-125">-Name</span></span>

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

### <span data-ttu-id="53cbc-126">對等</span><span class="sxs-lookup"><span data-stu-id="53cbc-126">-Peer</span></span>

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

### <span data-ttu-id="53cbc-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="53cbc-127">-PeerId</span></span>

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

### <span data-ttu-id="53cbc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53cbc-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="53cbc-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="53cbc-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="53cbc-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="53cbc-130">-SharedKey</span></span>

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

### <span data-ttu-id="53cbc-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="53cbc-131">-Tag</span></span>
<span data-ttu-id="53cbc-132">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="53cbc-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="53cbc-133">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="53cbc-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="53cbc-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="53cbc-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="53cbc-135">針對 S2S 連線使用原則式流量選擇器</span><span class="sxs-lookup"><span data-stu-id="53cbc-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="53cbc-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="53cbc-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="53cbc-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="53cbc-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="53cbc-138">-確認</span><span class="sxs-lookup"><span data-stu-id="53cbc-138">-Confirm</span></span>
<span data-ttu-id="53cbc-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53cbc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53cbc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53cbc-140">-WhatIf</span></span>
<span data-ttu-id="53cbc-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53cbc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53cbc-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53cbc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53cbc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53cbc-143">CommonParameters</span></span>
<span data-ttu-id="53cbc-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53cbc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53cbc-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53cbc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53cbc-146">輸入</span><span class="sxs-lookup"><span data-stu-id="53cbc-146">INPUTS</span></span>

### <span data-ttu-id="53cbc-147">System.object</span><span class="sxs-lookup"><span data-stu-id="53cbc-147">System.String</span></span>

### <span data-ttu-id="53cbc-148">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="53cbc-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="53cbc-149">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="53cbc-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="53cbc-150">System.object</span><span class="sxs-lookup"><span data-stu-id="53cbc-150">System.Int32</span></span>

### <span data-ttu-id="53cbc-151">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="53cbc-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="53cbc-152">System.object</span><span class="sxs-lookup"><span data-stu-id="53cbc-152">System.Boolean</span></span>

### <span data-ttu-id="53cbc-153">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="53cbc-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="53cbc-154">[System.object]. 清單 ' 1 [PSIpsecPolicy，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="53cbc-154">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="53cbc-155">輸出</span><span class="sxs-lookup"><span data-stu-id="53cbc-155">OUTPUTS</span></span>

### <span data-ttu-id="53cbc-156">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="53cbc-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="53cbc-157">筆記</span><span class="sxs-lookup"><span data-stu-id="53cbc-157">NOTES</span></span>

## <span data-ttu-id="53cbc-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="53cbc-158">RELATED LINKS</span></span>

[<span data-ttu-id="53cbc-159">AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="53cbc-159">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="53cbc-160">移除-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="53cbc-160">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="53cbc-161">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="53cbc-161">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)

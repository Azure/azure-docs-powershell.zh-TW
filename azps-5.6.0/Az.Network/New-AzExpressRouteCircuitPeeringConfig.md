---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 23dc75532c7b23c584d586b486e0d67d32af795f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912362"
---
# <span data-ttu-id="1ae44-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1ae44-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="1ae44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ae44-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae44-103">建立要新加入 ExpressRoute 回路的新對等互連組。</span><span class="sxs-lookup"><span data-stu-id="1ae44-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1ae44-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ae44-104">SYNTAX</span></span>

### <span data-ttu-id="1ae44-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1ae44-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ae44-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="1ae44-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ae44-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="1ae44-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae44-108">描述</span><span class="sxs-lookup"><span data-stu-id="1ae44-108">DESCRIPTION</span></span>
<span data-ttu-id="1ae44-109">**New-AzExpressRouteRouteCircuitPeeringConfig** Cmdlet 會新增對等組配置至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="1ae44-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="1ae44-110">ExpressRoute 回路會使用連接提供者而非公用網際網路，將您的內部部署網路連接至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="1ae44-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="1ae44-111">例子</span><span class="sxs-lookup"><span data-stu-id="1ae44-111">EXAMPLES</span></span>

### <span data-ttu-id="1ae44-112">範例 1：使用對等配置建立新 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="1ae44-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```powershell
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="1ae44-113">參數</span><span class="sxs-lookup"><span data-stu-id="1ae44-113">PARAMETERS</span></span>

### <span data-ttu-id="1ae44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae44-114">-DefaultProfile</span></span>
<span data-ttu-id="1ae44-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ae44-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae44-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="1ae44-116">-LegacyMode</span></span>
<span data-ttu-id="1ae44-117">舊版對等模式</span><span class="sxs-lookup"><span data-stu-id="1ae44-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="1ae44-118">-MicrosoftConfigAdvertvertlicPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="1ae44-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="1ae44-119">針對 MicrosoftPeering 的對等類型，您必須提供計畫要以 BGP 會話宣告的所有首碼清單。</span><span class="sxs-lookup"><span data-stu-id="1ae44-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="1ae44-120">僅接受公用 IP 位址首碼。</span><span class="sxs-lookup"><span data-stu-id="1ae44-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="1ae44-121">如果您打算傳送一組首碼，可以傳送逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="1ae44-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="1ae44-122">這些首碼必須在路由登錄名稱的 RIR /IRR (中註冊) 。</span><span class="sxs-lookup"><span data-stu-id="1ae44-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="1ae44-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="1ae44-124">如果您是未註冊至對等 AS 號碼的廣告首碼，您可以指定其註冊的 AS 號碼。</span><span class="sxs-lookup"><span data-stu-id="1ae44-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="1ae44-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="1ae44-126">路由登錄名稱 (RIR / IRR) AS 號碼和首碼的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="1ae44-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="1ae44-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ae44-127">-Name</span></span>
<span data-ttu-id="1ae44-128">要建立之對等組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae44-128">The name of the peering configuration to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1ae44-129">-PeerAddressType</span></span>
<span data-ttu-id="1ae44-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1ae44-130">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="1ae44-131">-PeerASN</span></span>
<span data-ttu-id="1ae44-132">ExpressRoute 回路的 AS 號碼。</span><span class="sxs-lookup"><span data-stu-id="1ae44-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="1ae44-133">當對等類型為 AzurePublicPeering 時，這必須是公用 ASN。</span><span class="sxs-lookup"><span data-stu-id="1ae44-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1ae44-134">-PeeringType</span></span>
<span data-ttu-id="1ae44-135">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1ae44-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1ae44-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="1ae44-137">這是此對等互連關係之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="1ae44-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="1ae44-138">這必須是 /30 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="1ae44-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="1ae44-139">此子網的第一個奇數編號位址應指派給路由器介面。</span><span class="sxs-lookup"><span data-stu-id="1ae44-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="1ae44-140">Azure 會設定 Azure 路由器介面的下一個均勻編號位址。</span><span class="sxs-lookup"><span data-stu-id="1ae44-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ae44-141">-RouteFilter</span></span>
<span data-ttu-id="1ae44-142">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="1ae44-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="1ae44-143">-RouteFilterId</span></span>
<span data-ttu-id="1ae44-144">這是現有 RouteFilter 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ae44-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1ae44-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="1ae44-146">這是此對等互連關係的次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="1ae44-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="1ae44-147">這必須是 /30 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="1ae44-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="1ae44-148">此子網的第一個奇數編號位址應指派給路由器介面。</span><span class="sxs-lookup"><span data-stu-id="1ae44-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="1ae44-149">Azure 會設定 Azure 路由器介面的下一個均勻編號位址。</span><span class="sxs-lookup"><span data-stu-id="1ae44-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="1ae44-150">-SharedKey</span></span>
<span data-ttu-id="1ae44-151">這是選擇性的 MD5 雜湊，用來做為對等配置的預先共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="1ae44-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="1ae44-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="1ae44-152">-VlanId</span></span>
<span data-ttu-id="1ae44-153">這是為此對等指派的 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ae44-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae44-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae44-154">CommonParameters</span></span>
<span data-ttu-id="1ae44-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ae44-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae44-156">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1ae44-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae44-157">輸入</span><span class="sxs-lookup"><span data-stu-id="1ae44-157">INPUTS</span></span>

### <span data-ttu-id="1ae44-158">System.String</span><span class="sxs-lookup"><span data-stu-id="1ae44-158">System.String</span></span>

### <span data-ttu-id="1ae44-159">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ae44-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="1ae44-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ae44-160">System.Boolean</span></span>

## <span data-ttu-id="1ae44-161">輸出</span><span class="sxs-lookup"><span data-stu-id="1ae44-161">OUTPUTS</span></span>

### <span data-ttu-id="1ae44-162">Microsoft.Azure.Commands.Network.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="1ae44-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="1ae44-163">筆記</span><span class="sxs-lookup"><span data-stu-id="1ae44-163">NOTES</span></span>

## <span data-ttu-id="1ae44-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ae44-164">RELATED LINKS</span></span>

[<span data-ttu-id="1ae44-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1ae44-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1ae44-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1ae44-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="1ae44-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1ae44-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1ae44-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1ae44-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

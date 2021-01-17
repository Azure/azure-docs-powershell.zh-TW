---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286920"
---
# <span data-ttu-id="086f0-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="086f0-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="086f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="086f0-102">SYNOPSIS</span></span>
<span data-ttu-id="086f0-103">建立要新增至 ExpressRoute 回路的新對等設定。</span><span class="sxs-lookup"><span data-stu-id="086f0-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="086f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="086f0-104">SYNTAX</span></span>

### <span data-ttu-id="086f0-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="086f0-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="086f0-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="086f0-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="086f0-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="086f0-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="086f0-108">說明</span><span class="sxs-lookup"><span data-stu-id="086f0-108">DESCRIPTION</span></span>
<span data-ttu-id="086f0-109">**新的-AzExpressRouteCircuitPeeringConfig** Cmdlet 會將對等設定新增至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="086f0-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="086f0-110">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="086f0-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="086f0-111">示例</span><span class="sxs-lookup"><span data-stu-id="086f0-111">EXAMPLES</span></span>

### <span data-ttu-id="086f0-112">範例1：使用對等設定建立新的 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="086f0-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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

## <span data-ttu-id="086f0-113">參數</span><span class="sxs-lookup"><span data-stu-id="086f0-113">PARAMETERS</span></span>

### <span data-ttu-id="086f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086f0-114">-DefaultProfile</span></span>
<span data-ttu-id="086f0-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="086f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="086f0-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="086f0-116">-LegacyMode</span></span>
<span data-ttu-id="086f0-117">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="086f0-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="086f0-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="086f0-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="086f0-119">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="086f0-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="086f0-120">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="086f0-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="086f0-121">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="086f0-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="086f0-122">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="086f0-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="086f0-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="086f0-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="086f0-124">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="086f0-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="086f0-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="086f0-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="086f0-126">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="086f0-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="086f0-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="086f0-127">-Name</span></span>
<span data-ttu-id="086f0-128">要建立之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="086f0-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="086f0-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="086f0-129">-PeerAddressType</span></span>
<span data-ttu-id="086f0-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="086f0-130">PeerAddressType</span></span>

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

### <span data-ttu-id="086f0-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="086f0-131">-PeerASN</span></span>
<span data-ttu-id="086f0-132">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="086f0-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="086f0-133">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="086f0-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="086f0-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="086f0-134">-PeeringType</span></span>
<span data-ttu-id="086f0-135">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="086f0-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="086f0-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="086f0-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="086f0-137">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="086f0-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="086f0-138">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="086f0-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="086f0-139">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="086f0-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="086f0-140">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="086f0-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="086f0-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="086f0-141">-RouteFilter</span></span>
<span data-ttu-id="086f0-142">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="086f0-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="086f0-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="086f0-143">-RouteFilterId</span></span>
<span data-ttu-id="086f0-144">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="086f0-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="086f0-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="086f0-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="086f0-146">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="086f0-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="086f0-147">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="086f0-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="086f0-148">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="086f0-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="086f0-149">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="086f0-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="086f0-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="086f0-150">-SharedKey</span></span>
<span data-ttu-id="086f0-151">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="086f0-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="086f0-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="086f0-152">-VlanId</span></span>
<span data-ttu-id="086f0-153">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="086f0-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="086f0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086f0-154">CommonParameters</span></span>
<span data-ttu-id="086f0-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="086f0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086f0-156">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="086f0-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086f0-157">輸入</span><span class="sxs-lookup"><span data-stu-id="086f0-157">INPUTS</span></span>

### <span data-ttu-id="086f0-158">System.object</span><span class="sxs-lookup"><span data-stu-id="086f0-158">System.String</span></span>

### <span data-ttu-id="086f0-159">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="086f0-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="086f0-160">System.object</span><span class="sxs-lookup"><span data-stu-id="086f0-160">System.Boolean</span></span>

## <span data-ttu-id="086f0-161">輸出</span><span class="sxs-lookup"><span data-stu-id="086f0-161">OUTPUTS</span></span>

### <span data-ttu-id="086f0-162">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="086f0-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="086f0-163">筆記</span><span class="sxs-lookup"><span data-stu-id="086f0-163">NOTES</span></span>

## <span data-ttu-id="086f0-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="086f0-164">RELATED LINKS</span></span>

[<span data-ttu-id="086f0-165">附加 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="086f0-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="086f0-166">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="086f0-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="086f0-167">移除-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="086f0-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="086f0-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="086f0-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

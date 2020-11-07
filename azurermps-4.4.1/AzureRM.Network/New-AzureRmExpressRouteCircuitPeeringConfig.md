---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7008ec07c4ed8800d5817e6dbf306a1540d89a04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624012"
---
# <span data-ttu-id="c5860-101">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c5860-101">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="c5860-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5860-102">SYNOPSIS</span></span>
<span data-ttu-id="c5860-103">建立要新增至 ExpressRoute 回路的新對等設定。</span><span class="sxs-lookup"><span data-stu-id="c5860-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5860-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5860-104">SYNTAX</span></span>

### <span data-ttu-id="c5860-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c5860-105">SetByResource (Default)</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5860-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="c5860-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5860-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="c5860-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5860-108">說明</span><span class="sxs-lookup"><span data-stu-id="c5860-108">DESCRIPTION</span></span>
<span data-ttu-id="c5860-109">**新的-AzureRmExpressRouteCircuitPeeringConfig** Cmdlet 會將對等設定新增至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="c5860-109">The **New-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="c5860-110">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="c5860-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="c5860-111">示例</span><span class="sxs-lookup"><span data-stu-id="c5860-111">EXAMPLES</span></span>

### <span data-ttu-id="c5860-112">範例1：使用對等設定建立新的 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="c5860-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzureRmExpressRouteCircuitPeeringConfig @parameters

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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="c5860-113">參數</span><span class="sxs-lookup"><span data-stu-id="c5860-113">PARAMETERS</span></span>

### <span data-ttu-id="c5860-114">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="c5860-114">-LegacyMode</span></span>
<span data-ttu-id="c5860-115">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="c5860-115">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="c5860-116">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="c5860-116">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="c5860-117">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="c5860-117">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="c5860-118">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="c5860-118">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="c5860-119">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="c5860-119">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="c5860-120">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="c5860-120">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-121">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="c5860-121">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="c5860-122">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="c5860-122">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="c5860-123">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="c5860-123">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="c5860-124">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="c5860-124">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="c5860-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5860-125">-Name</span></span>
<span data-ttu-id="c5860-126">要建立之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5860-126">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="c5860-127">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c5860-127">-PeerAddressType</span></span>
<span data-ttu-id="c5860-128">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c5860-128">PeerAddressType</span></span>

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

### <span data-ttu-id="c5860-129">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="c5860-129">-PeerASN</span></span>
<span data-ttu-id="c5860-130">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="c5860-130">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="c5860-131">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="c5860-131">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="c5860-132">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c5860-132">-PeeringType</span></span>
<span data-ttu-id="c5860-133">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c5860-133">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c5860-134">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c5860-134">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="c5860-135">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="c5860-135">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="c5860-136">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="c5860-136">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c5860-137">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="c5860-137">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c5860-138">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="c5860-138">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c5860-139">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c5860-139">-RouteFilter</span></span>
<span data-ttu-id="c5860-140">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="c5860-140">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c5860-141">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="c5860-141">-RouteFilterId</span></span>
<span data-ttu-id="c5860-142">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="c5860-142">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c5860-143">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c5860-143">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="c5860-144">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="c5860-144">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="c5860-145">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="c5860-145">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c5860-146">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="c5860-146">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c5860-147">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="c5860-147">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c5860-148">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c5860-148">-SharedKey</span></span>
<span data-ttu-id="c5860-149">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5860-149">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="c5860-150">-VlanId</span><span class="sxs-lookup"><span data-stu-id="c5860-150">-VlanId</span></span>
<span data-ttu-id="c5860-151">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="c5860-151">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="c5860-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5860-152">-DefaultProfile</span></span>
<span data-ttu-id="c5860-153">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5860-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5860-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5860-154">CommonParameters</span></span>
<span data-ttu-id="c5860-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5860-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5860-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5860-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5860-157">輸入</span><span class="sxs-lookup"><span data-stu-id="c5860-157">INPUTS</span></span>

## <span data-ttu-id="c5860-158">輸出</span><span class="sxs-lookup"><span data-stu-id="c5860-158">OUTPUTS</span></span>

### <span data-ttu-id="c5860-159">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c5860-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="c5860-160">筆記</span><span class="sxs-lookup"><span data-stu-id="c5860-160">NOTES</span></span>

## <span data-ttu-id="c5860-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5860-161">RELATED LINKS</span></span>

[<span data-ttu-id="c5860-162">附加 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c5860-162">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c5860-163">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c5860-163">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c5860-164">移除-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c5860-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c5860-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c5860-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 42a2ec1c3fb19647cc956c6b7321f52e6ad6e63e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901933"
---
# <span data-ttu-id="a7cec-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a7cec-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a7cec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7cec-102">SYNOPSIS</span></span>
<span data-ttu-id="a7cec-103">會保存經過修改的 ExpressRoute 對等互連組。</span><span class="sxs-lookup"><span data-stu-id="a7cec-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="a7cec-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7cec-104">SYNTAX</span></span>

### <span data-ttu-id="a7cec-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a7cec-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7cec-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="a7cec-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7cec-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="a7cec-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7cec-108">描述</span><span class="sxs-lookup"><span data-stu-id="a7cec-108">DESCRIPTION</span></span>
<span data-ttu-id="a7cec-109">**Set-AzExpressRouteCircuitPeeringConfig** Cmdlet 會將經過修改的 ExpressRoute 對等設定存回 Azure。</span><span class="sxs-lookup"><span data-stu-id="a7cec-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="a7cec-110">例子</span><span class="sxs-lookup"><span data-stu-id="a7cec-110">EXAMPLES</span></span>

### <span data-ttu-id="a7cec-111">範例 1：變更現有的對等組</span><span class="sxs-lookup"><span data-stu-id="a7cec-111">Example 1: Change an existing peering configuration</span></span>
```powershell
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

### <span data-ttu-id="a7cec-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="a7cec-112">Example 2</span></span>

<span data-ttu-id="a7cec-113">會保存經過修改的 ExpressRoute 對等互連組。</span><span class="sxs-lookup"><span data-stu-id="a7cec-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="a7cec-114"> (自動) </span><span class="sxs-lookup"><span data-stu-id="a7cec-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="a7cec-115">參數</span><span class="sxs-lookup"><span data-stu-id="a7cec-115">PARAMETERS</span></span>

### <span data-ttu-id="a7cec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7cec-116">-DefaultProfile</span></span>
<span data-ttu-id="a7cec-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7cec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7cec-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7cec-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a7cec-119">包含要修改對等配置的 ExpressRoute 回路物件。</span><span class="sxs-lookup"><span data-stu-id="a7cec-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7cec-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="a7cec-120">-LegacyMode</span></span>
<span data-ttu-id="a7cec-121">舊版對等模式</span><span class="sxs-lookup"><span data-stu-id="a7cec-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="a7cec-122">-MicrosoftConfigAdvertvertlicPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="a7cec-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="a7cec-123">針對 MicrosoftPeering 的對等類型，您必須提供計畫要以 BGP 會話宣告的所有首碼清單。</span><span class="sxs-lookup"><span data-stu-id="a7cec-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="a7cec-124">僅接受公用 IP 位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a7cec-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="a7cec-125">如果您打算傳送一組首碼，可以傳送逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="a7cec-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="a7cec-126">這些首碼必須在路由登錄名稱的 RIR /IRR (中註冊) 。</span><span class="sxs-lookup"><span data-stu-id="a7cec-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="a7cec-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="a7cec-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="a7cec-128">如果您是未註冊至對等 AS 號碼的廣告首碼，您可以指定其註冊的 AS 號碼。</span><span class="sxs-lookup"><span data-stu-id="a7cec-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="a7cec-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="a7cec-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="a7cec-130">路由登錄名稱 (RIR / IRR) AS 號碼和首碼的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="a7cec-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="a7cec-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7cec-131">-Name</span></span>
<span data-ttu-id="a7cec-132">要修改的對等組名。</span><span class="sxs-lookup"><span data-stu-id="a7cec-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="a7cec-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a7cec-133">-PeerAddressType</span></span>
<span data-ttu-id="a7cec-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a7cec-134">PeerAddressType</span></span>

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

### <span data-ttu-id="a7cec-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="a7cec-135">-PeerASN</span></span>
<span data-ttu-id="a7cec-136">ExpressRoute 回路的 AS 號碼。</span><span class="sxs-lookup"><span data-stu-id="a7cec-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="a7cec-137">當對等類型為 AzurePublicPeering 時，這必須是公用 ASN。</span><span class="sxs-lookup"><span data-stu-id="a7cec-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="a7cec-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a7cec-138">-PeeringType</span></span>
<span data-ttu-id="a7cec-139">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a7cec-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a7cec-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a7cec-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="a7cec-141">這是此對等互連關係之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="a7cec-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="a7cec-142">這必須是 /30 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="a7cec-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a7cec-143">此子網的第一個奇數編號位址應指派給路由器介面。</span><span class="sxs-lookup"><span data-stu-id="a7cec-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a7cec-144">Azure 會設定 Azure 路由器介面的下一個均勻編號位址。</span><span class="sxs-lookup"><span data-stu-id="a7cec-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a7cec-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7cec-145">-RouteFilter</span></span>
<span data-ttu-id="a7cec-146">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="a7cec-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a7cec-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="a7cec-147">-RouteFilterId</span></span>
<span data-ttu-id="a7cec-148">這是現有 RouteFilter 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7cec-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a7cec-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a7cec-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="a7cec-150">這是此對等互連關係的次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="a7cec-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="a7cec-151">這必須是 /30 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="a7cec-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a7cec-152">此子網的第一個奇數編號位址應指派給路由器介面。</span><span class="sxs-lookup"><span data-stu-id="a7cec-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a7cec-153">Azure 會設定 Azure 路由器介面的下一個均勻編號位址。</span><span class="sxs-lookup"><span data-stu-id="a7cec-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a7cec-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a7cec-154">-SharedKey</span></span>
<span data-ttu-id="a7cec-155">這是選擇性的 MD5 雜湊，用來做為對等配置的預先共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="a7cec-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="a7cec-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="a7cec-156">-VlanId</span></span>
<span data-ttu-id="a7cec-157">這是為此對等指派的 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7cec-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="a7cec-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7cec-158">CommonParameters</span></span>
<span data-ttu-id="a7cec-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7cec-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7cec-160">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a7cec-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7cec-161">輸入</span><span class="sxs-lookup"><span data-stu-id="a7cec-161">INPUTS</span></span>

### <span data-ttu-id="a7cec-162">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7cec-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="a7cec-163">System.String</span><span class="sxs-lookup"><span data-stu-id="a7cec-163">System.String</span></span>

### <span data-ttu-id="a7cec-164">Microsoft.Azure.Commands.Network.models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7cec-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="a7cec-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7cec-165">System.Boolean</span></span>

## <span data-ttu-id="a7cec-166">輸出</span><span class="sxs-lookup"><span data-stu-id="a7cec-166">OUTPUTS</span></span>

### <span data-ttu-id="a7cec-167">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7cec-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a7cec-168">筆記</span><span class="sxs-lookup"><span data-stu-id="a7cec-168">NOTES</span></span>

## <span data-ttu-id="a7cec-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7cec-169">RELATED LINKS</span></span>

[<span data-ttu-id="a7cec-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a7cec-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a7cec-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a7cec-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a7cec-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a7cec-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a7cec-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a7cec-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

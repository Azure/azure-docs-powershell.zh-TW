---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449004"
---
# <span data-ttu-id="ec907-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ec907-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ec907-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec907-102">SYNOPSIS</span></span>
<span data-ttu-id="ec907-103">在 ExpressRoute 回路中新增對等設定。</span><span class="sxs-lookup"><span data-stu-id="ec907-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ec907-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec907-104">SYNTAX</span></span>

### <span data-ttu-id="ec907-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ec907-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec907-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="ec907-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec907-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="ec907-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec907-108">說明</span><span class="sxs-lookup"><span data-stu-id="ec907-108">DESCRIPTION</span></span>
<span data-ttu-id="ec907-109">**AzExpressRouteCircuitPeeringConfig** Cmdlet 會將對等設定新增至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="ec907-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="ec907-110">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="ec907-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="ec907-111">請注意，執行 **附加 AzExpressRouteCircuitPeeringConfig** 之後，您必須呼叫 Set-AzExpressRouteCircuit Cmdlet 才能啟動設定。</span><span class="sxs-lookup"><span data-stu-id="ec907-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="ec907-112">示例</span><span class="sxs-lookup"><span data-stu-id="ec907-112">EXAMPLES</span></span>

### <span data-ttu-id="ec907-113">範例1：將對等新增至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="ec907-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="ec907-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec907-114">PARAMETERS</span></span>

### <span data-ttu-id="ec907-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec907-115">-DefaultProfile</span></span>
<span data-ttu-id="ec907-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec907-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec907-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec907-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ec907-118">要修改的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="ec907-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="ec907-119">這是 **AzExpressRouteCircuit** Cmdlet 傳回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="ec907-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="ec907-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="ec907-120">-LegacyMode</span></span>
<span data-ttu-id="ec907-121">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="ec907-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="ec907-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="ec907-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="ec907-123">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="ec907-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="ec907-124">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="ec907-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="ec907-125">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="ec907-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="ec907-126">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="ec907-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="ec907-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="ec907-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="ec907-128">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="ec907-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="ec907-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="ec907-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="ec907-130">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="ec907-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="ec907-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec907-131">-Name</span></span>
<span data-ttu-id="ec907-132">要新增之對等關係的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec907-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="ec907-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ec907-133">-PeerAddressType</span></span>
<span data-ttu-id="ec907-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ec907-134">PeerAddressType</span></span>

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

### <span data-ttu-id="ec907-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="ec907-135">-PeerASN</span></span>
<span data-ttu-id="ec907-136">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="ec907-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="ec907-137">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="ec907-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="ec907-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ec907-138">-PeeringType</span></span>
<span data-ttu-id="ec907-139">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ec907-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ec907-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ec907-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="ec907-141">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="ec907-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="ec907-142">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="ec907-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ec907-143">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="ec907-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ec907-144">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="ec907-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ec907-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec907-145">-RouteFilter</span></span>
<span data-ttu-id="ec907-146">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="ec907-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="ec907-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="ec907-147">-RouteFilterId</span></span>
<span data-ttu-id="ec907-148">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="ec907-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="ec907-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ec907-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="ec907-150">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="ec907-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="ec907-151">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="ec907-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ec907-152">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="ec907-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ec907-153">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="ec907-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ec907-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ec907-154">-SharedKey</span></span>
<span data-ttu-id="ec907-155">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ec907-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="ec907-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="ec907-156">-VlanId</span></span>
<span data-ttu-id="ec907-157">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="ec907-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="ec907-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec907-158">CommonParameters</span></span>
<span data-ttu-id="ec907-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec907-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec907-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec907-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec907-161">輸入</span><span class="sxs-lookup"><span data-stu-id="ec907-161">INPUTS</span></span>

### <span data-ttu-id="ec907-162">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec907-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="ec907-163">System.object</span><span class="sxs-lookup"><span data-stu-id="ec907-163">System.String</span></span>

### <span data-ttu-id="ec907-164">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec907-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="ec907-165">System.object</span><span class="sxs-lookup"><span data-stu-id="ec907-165">System.Boolean</span></span>

## <span data-ttu-id="ec907-166">輸出</span><span class="sxs-lookup"><span data-stu-id="ec907-166">OUTPUTS</span></span>

### <span data-ttu-id="ec907-167">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec907-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ec907-168">筆記</span><span class="sxs-lookup"><span data-stu-id="ec907-168">NOTES</span></span>

## <span data-ttu-id="ec907-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec907-169">RELATED LINKS</span></span>

[<span data-ttu-id="ec907-170">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec907-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ec907-171">新-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ec907-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ec907-172">移除-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ec907-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ec907-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec907-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

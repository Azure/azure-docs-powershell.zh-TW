---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131118"
---
# <span data-ttu-id="72e6b-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="72e6b-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="72e6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="72e6b-103">儲存已修改的 ExpressRoute 對等設定。</span><span class="sxs-lookup"><span data-stu-id="72e6b-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="72e6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="72e6b-104">SYNTAX</span></span>

### <span data-ttu-id="72e6b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="72e6b-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e6b-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="72e6b-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e6b-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="72e6b-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e6b-108">說明</span><span class="sxs-lookup"><span data-stu-id="72e6b-108">DESCRIPTION</span></span>
<span data-ttu-id="72e6b-109">**AzExpressRouteCircuitPeeringConfig** Cmdlet 會將已修改的 ExpressRoute 對等設定儲存回 Azure。</span><span class="sxs-lookup"><span data-stu-id="72e6b-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="72e6b-110">示例</span><span class="sxs-lookup"><span data-stu-id="72e6b-110">EXAMPLES</span></span>

### <span data-ttu-id="72e6b-111">範例1：變更現有的對等設定</span><span class="sxs-lookup"><span data-stu-id="72e6b-111">Example 1: Change an existing peering configuration</span></span>
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

### <span data-ttu-id="72e6b-112">範例2</span><span class="sxs-lookup"><span data-stu-id="72e6b-112">Example 2</span></span>

<span data-ttu-id="72e6b-113">儲存已修改的 ExpressRoute 對等設定。</span><span class="sxs-lookup"><span data-stu-id="72e6b-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="72e6b-114"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="72e6b-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="72e6b-115">參數</span><span class="sxs-lookup"><span data-stu-id="72e6b-115">PARAMETERS</span></span>

### <span data-ttu-id="72e6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e6b-116">-DefaultProfile</span></span>
<span data-ttu-id="72e6b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72e6b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e6b-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72e6b-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="72e6b-119">包含要修改之對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="72e6b-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="72e6b-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="72e6b-120">-LegacyMode</span></span>
<span data-ttu-id="72e6b-121">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="72e6b-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="72e6b-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="72e6b-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="72e6b-123">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="72e6b-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="72e6b-124">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="72e6b-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="72e6b-125">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="72e6b-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="72e6b-126">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="72e6b-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="72e6b-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="72e6b-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="72e6b-128">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="72e6b-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="72e6b-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="72e6b-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="72e6b-130">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="72e6b-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="72e6b-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="72e6b-131">-Name</span></span>
<span data-ttu-id="72e6b-132">要修改之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="72e6b-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="72e6b-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="72e6b-133">-PeerAddressType</span></span>
<span data-ttu-id="72e6b-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="72e6b-134">PeerAddressType</span></span>

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

### <span data-ttu-id="72e6b-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="72e6b-135">-PeerASN</span></span>
<span data-ttu-id="72e6b-136">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="72e6b-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="72e6b-137">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="72e6b-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="72e6b-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="72e6b-138">-PeeringType</span></span>
<span data-ttu-id="72e6b-139">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="72e6b-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="72e6b-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="72e6b-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="72e6b-141">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="72e6b-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="72e6b-142">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="72e6b-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="72e6b-143">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="72e6b-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="72e6b-144">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="72e6b-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="72e6b-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="72e6b-145">-RouteFilter</span></span>
<span data-ttu-id="72e6b-146">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="72e6b-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="72e6b-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="72e6b-147">-RouteFilterId</span></span>
<span data-ttu-id="72e6b-148">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="72e6b-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="72e6b-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="72e6b-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="72e6b-150">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="72e6b-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="72e6b-151">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="72e6b-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="72e6b-152">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="72e6b-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="72e6b-153">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="72e6b-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="72e6b-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="72e6b-154">-SharedKey</span></span>
<span data-ttu-id="72e6b-155">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="72e6b-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="72e6b-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="72e6b-156">-VlanId</span></span>
<span data-ttu-id="72e6b-157">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="72e6b-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="72e6b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e6b-158">CommonParameters</span></span>
<span data-ttu-id="72e6b-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72e6b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e6b-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72e6b-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e6b-161">輸入</span><span class="sxs-lookup"><span data-stu-id="72e6b-161">INPUTS</span></span>

### <span data-ttu-id="72e6b-162">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="72e6b-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="72e6b-163">System.object</span><span class="sxs-lookup"><span data-stu-id="72e6b-163">System.String</span></span>

### <span data-ttu-id="72e6b-164">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="72e6b-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="72e6b-165">System.object</span><span class="sxs-lookup"><span data-stu-id="72e6b-165">System.Boolean</span></span>

## <span data-ttu-id="72e6b-166">輸出</span><span class="sxs-lookup"><span data-stu-id="72e6b-166">OUTPUTS</span></span>

### <span data-ttu-id="72e6b-167">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="72e6b-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="72e6b-168">筆記</span><span class="sxs-lookup"><span data-stu-id="72e6b-168">NOTES</span></span>

## <span data-ttu-id="72e6b-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="72e6b-169">RELATED LINKS</span></span>

[<span data-ttu-id="72e6b-170">附加 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="72e6b-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="72e6b-171">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72e6b-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="72e6b-172">新-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="72e6b-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="72e6b-173">移除-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="72e6b-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

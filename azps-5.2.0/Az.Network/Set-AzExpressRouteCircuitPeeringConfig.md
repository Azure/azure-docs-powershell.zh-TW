---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274364"
---
# <span data-ttu-id="4bff6-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4bff6-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4bff6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bff6-102">SYNOPSIS</span></span>
<span data-ttu-id="4bff6-103">儲存已修改的 ExpressRoute 對等設定。</span><span class="sxs-lookup"><span data-stu-id="4bff6-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="4bff6-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bff6-104">SYNTAX</span></span>

### <span data-ttu-id="4bff6-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="4bff6-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bff6-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="4bff6-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bff6-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="4bff6-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bff6-108">說明</span><span class="sxs-lookup"><span data-stu-id="4bff6-108">DESCRIPTION</span></span>
<span data-ttu-id="4bff6-109">**AzExpressRouteCircuitPeeringConfig** Cmdlet 會將已修改的 ExpressRoute 對等設定儲存回 Azure。</span><span class="sxs-lookup"><span data-stu-id="4bff6-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="4bff6-110">示例</span><span class="sxs-lookup"><span data-stu-id="4bff6-110">EXAMPLES</span></span>

### <span data-ttu-id="4bff6-111">範例1：變更現有的對等設定</span><span class="sxs-lookup"><span data-stu-id="4bff6-111">Example 1: Change an existing peering configuration</span></span>
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

### <span data-ttu-id="4bff6-112">範例2</span><span class="sxs-lookup"><span data-stu-id="4bff6-112">Example 2</span></span>

<span data-ttu-id="4bff6-113">儲存已修改的 ExpressRoute 對等設定。</span><span class="sxs-lookup"><span data-stu-id="4bff6-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="4bff6-114"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="4bff6-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="4bff6-115">參數</span><span class="sxs-lookup"><span data-stu-id="4bff6-115">PARAMETERS</span></span>

### <span data-ttu-id="4bff6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bff6-116">-DefaultProfile</span></span>
<span data-ttu-id="4bff6-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bff6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bff6-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bff6-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4bff6-119">包含要修改之對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="4bff6-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="4bff6-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="4bff6-120">-LegacyMode</span></span>
<span data-ttu-id="4bff6-121">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="4bff6-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="4bff6-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="4bff6-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="4bff6-123">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="4bff6-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="4bff6-124">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="4bff6-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="4bff6-125">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="4bff6-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="4bff6-126">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="4bff6-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="4bff6-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="4bff6-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="4bff6-128">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="4bff6-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="4bff6-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="4bff6-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="4bff6-130">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="4bff6-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="4bff6-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bff6-131">-Name</span></span>
<span data-ttu-id="4bff6-132">要修改之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bff6-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="4bff6-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4bff6-133">-PeerAddressType</span></span>
<span data-ttu-id="4bff6-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4bff6-134">PeerAddressType</span></span>

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

### <span data-ttu-id="4bff6-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="4bff6-135">-PeerASN</span></span>
<span data-ttu-id="4bff6-136">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="4bff6-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="4bff6-137">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="4bff6-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="4bff6-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4bff6-138">-PeeringType</span></span>
<span data-ttu-id="4bff6-139">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4bff6-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4bff6-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4bff6-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="4bff6-141">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="4bff6-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="4bff6-142">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="4bff6-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4bff6-143">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="4bff6-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4bff6-144">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="4bff6-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4bff6-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4bff6-145">-RouteFilter</span></span>
<span data-ttu-id="4bff6-146">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="4bff6-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4bff6-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="4bff6-147">-RouteFilterId</span></span>
<span data-ttu-id="4bff6-148">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="4bff6-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4bff6-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4bff6-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="4bff6-150">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="4bff6-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="4bff6-151">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="4bff6-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4bff6-152">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="4bff6-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4bff6-153">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="4bff6-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4bff6-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4bff6-154">-SharedKey</span></span>
<span data-ttu-id="4bff6-155">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="4bff6-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="4bff6-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="4bff6-156">-VlanId</span></span>
<span data-ttu-id="4bff6-157">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="4bff6-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="4bff6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bff6-158">CommonParameters</span></span>
<span data-ttu-id="4bff6-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bff6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bff6-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bff6-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bff6-161">輸入</span><span class="sxs-lookup"><span data-stu-id="4bff6-161">INPUTS</span></span>

### <span data-ttu-id="4bff6-162">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4bff6-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="4bff6-163">System.object</span><span class="sxs-lookup"><span data-stu-id="4bff6-163">System.String</span></span>

### <span data-ttu-id="4bff6-164">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4bff6-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="4bff6-165">System.object</span><span class="sxs-lookup"><span data-stu-id="4bff6-165">System.Boolean</span></span>

## <span data-ttu-id="4bff6-166">輸出</span><span class="sxs-lookup"><span data-stu-id="4bff6-166">OUTPUTS</span></span>

### <span data-ttu-id="4bff6-167">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4bff6-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4bff6-168">筆記</span><span class="sxs-lookup"><span data-stu-id="4bff6-168">NOTES</span></span>

## <span data-ttu-id="4bff6-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bff6-169">RELATED LINKS</span></span>

[<span data-ttu-id="4bff6-170">附加 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4bff6-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4bff6-171">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bff6-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4bff6-172">新-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4bff6-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4bff6-173">移除-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4bff6-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

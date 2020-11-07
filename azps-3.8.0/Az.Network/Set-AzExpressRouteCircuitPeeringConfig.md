---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ffc605a9376864a0576c4f7a6ae69f157ab9bacc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957284"
---
# <span data-ttu-id="76ae7-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="76ae7-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="76ae7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="76ae7-103">儲存已修改的 ExpressRoute 對等設定。</span><span class="sxs-lookup"><span data-stu-id="76ae7-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="76ae7-104">句法</span><span class="sxs-lookup"><span data-stu-id="76ae7-104">SYNTAX</span></span>

### <span data-ttu-id="76ae7-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="76ae7-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76ae7-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="76ae7-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76ae7-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="76ae7-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ae7-108">說明</span><span class="sxs-lookup"><span data-stu-id="76ae7-108">DESCRIPTION</span></span>
<span data-ttu-id="76ae7-109">**AzExpressRouteCircuitPeeringConfig** Cmdlet 會將已修改的 ExpressRoute 對等設定儲存回 Azure。</span><span class="sxs-lookup"><span data-stu-id="76ae7-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="76ae7-110">示例</span><span class="sxs-lookup"><span data-stu-id="76ae7-110">EXAMPLES</span></span>

### <span data-ttu-id="76ae7-111">範例1：變更現有的對等設定</span><span class="sxs-lookup"><span data-stu-id="76ae7-111">Example 1: Change an existing peering configuration</span></span>
```
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

## <span data-ttu-id="76ae7-112">參數</span><span class="sxs-lookup"><span data-stu-id="76ae7-112">PARAMETERS</span></span>

### <span data-ttu-id="76ae7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ae7-113">-DefaultProfile</span></span>
<span data-ttu-id="76ae7-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76ae7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76ae7-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76ae7-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="76ae7-116">包含要修改之對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="76ae7-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="76ae7-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="76ae7-117">-LegacyMode</span></span>
<span data-ttu-id="76ae7-118">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="76ae7-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="76ae7-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="76ae7-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="76ae7-120">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="76ae7-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="76ae7-121">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="76ae7-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="76ae7-122">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="76ae7-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="76ae7-123">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="76ae7-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="76ae7-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="76ae7-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="76ae7-125">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="76ae7-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="76ae7-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="76ae7-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="76ae7-127">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="76ae7-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="76ae7-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="76ae7-128">-Name</span></span>
<span data-ttu-id="76ae7-129">要修改之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="76ae7-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="76ae7-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="76ae7-130">-PeerAddressType</span></span>
<span data-ttu-id="76ae7-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="76ae7-131">PeerAddressType</span></span>

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

### <span data-ttu-id="76ae7-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="76ae7-132">-PeerASN</span></span>
<span data-ttu-id="76ae7-133">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="76ae7-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="76ae7-134">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="76ae7-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="76ae7-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="76ae7-135">-PeeringType</span></span>
<span data-ttu-id="76ae7-136">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="76ae7-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="76ae7-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="76ae7-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="76ae7-138">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="76ae7-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="76ae7-139">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="76ae7-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="76ae7-140">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="76ae7-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="76ae7-141">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="76ae7-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="76ae7-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="76ae7-142">-RouteFilter</span></span>
<span data-ttu-id="76ae7-143">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="76ae7-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="76ae7-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="76ae7-144">-RouteFilterId</span></span>
<span data-ttu-id="76ae7-145">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="76ae7-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="76ae7-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="76ae7-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="76ae7-147">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="76ae7-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="76ae7-148">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="76ae7-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="76ae7-149">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="76ae7-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="76ae7-150">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="76ae7-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="76ae7-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="76ae7-151">-SharedKey</span></span>
<span data-ttu-id="76ae7-152">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="76ae7-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="76ae7-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="76ae7-153">-VlanId</span></span>
<span data-ttu-id="76ae7-154">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="76ae7-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="76ae7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ae7-155">CommonParameters</span></span>
<span data-ttu-id="76ae7-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76ae7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ae7-157">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76ae7-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ae7-158">輸入</span><span class="sxs-lookup"><span data-stu-id="76ae7-158">INPUTS</span></span>

### <span data-ttu-id="76ae7-159">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76ae7-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="76ae7-160">System.object</span><span class="sxs-lookup"><span data-stu-id="76ae7-160">System.String</span></span>

### <span data-ttu-id="76ae7-161">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76ae7-161">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="76ae7-162">System.object</span><span class="sxs-lookup"><span data-stu-id="76ae7-162">System.Boolean</span></span>

## <span data-ttu-id="76ae7-163">輸出</span><span class="sxs-lookup"><span data-stu-id="76ae7-163">OUTPUTS</span></span>

### <span data-ttu-id="76ae7-164">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76ae7-164">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="76ae7-165">筆記</span><span class="sxs-lookup"><span data-stu-id="76ae7-165">NOTES</span></span>

## <span data-ttu-id="76ae7-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="76ae7-166">RELATED LINKS</span></span>

[<span data-ttu-id="76ae7-167">附加 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="76ae7-167">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="76ae7-168">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76ae7-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="76ae7-169">新-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="76ae7-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="76ae7-170">移除-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="76ae7-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

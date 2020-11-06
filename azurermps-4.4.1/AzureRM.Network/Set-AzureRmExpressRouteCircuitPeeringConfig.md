---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 87c956769efb41485e43e65ff31d7a9cd7387d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454883"
---
# <span data-ttu-id="b3399-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b3399-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="b3399-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3399-102">SYNOPSIS</span></span>
<span data-ttu-id="b3399-103">儲存已修改的 ExpressRoute 對等設定。</span><span class="sxs-lookup"><span data-stu-id="b3399-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3399-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3399-104">SYNTAX</span></span>

### <span data-ttu-id="b3399-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b3399-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3399-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="b3399-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3399-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="b3399-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3399-108">說明</span><span class="sxs-lookup"><span data-stu-id="b3399-108">DESCRIPTION</span></span>
<span data-ttu-id="b3399-109">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet 會將已修改的 ExpressRoute 對等設定儲存回 Azure。</span><span class="sxs-lookup"><span data-stu-id="b3399-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="b3399-110">示例</span><span class="sxs-lookup"><span data-stu-id="b3399-110">EXAMPLES</span></span>

### <span data-ttu-id="b3399-111">範例1：變更現有的對等設定</span><span class="sxs-lookup"><span data-stu-id="b3399-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="b3399-112">參數</span><span class="sxs-lookup"><span data-stu-id="b3399-112">PARAMETERS</span></span>

### <span data-ttu-id="b3399-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3399-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b3399-114">包含要修改之對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="b3399-114">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="b3399-115">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="b3399-115">-LegacyMode</span></span>
<span data-ttu-id="b3399-116">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="b3399-116">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="b3399-117">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="b3399-117">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="b3399-118">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="b3399-118">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="b3399-119">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="b3399-119">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="b3399-120">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="b3399-120">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="b3399-121">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="b3399-121">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="b3399-122">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="b3399-122">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="b3399-123">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="b3399-123">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="b3399-124">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="b3399-124">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="b3399-125">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="b3399-125">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="b3399-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3399-126">-Name</span></span>
<span data-ttu-id="b3399-127">要修改之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3399-127">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="b3399-128">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b3399-128">-PeerAddressType</span></span>
<span data-ttu-id="b3399-129">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b3399-129">PeerAddressType</span></span>

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

### <span data-ttu-id="b3399-130">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="b3399-130">-PeerASN</span></span>
<span data-ttu-id="b3399-131">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="b3399-131">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="b3399-132">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="b3399-132">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="b3399-133">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b3399-133">-PeeringType</span></span>
<span data-ttu-id="b3399-134">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b3399-134">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b3399-135">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b3399-135">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="b3399-136">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="b3399-136">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="b3399-137">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="b3399-137">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b3399-138">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="b3399-138">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b3399-139">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="b3399-139">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b3399-140">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b3399-140">-RouteFilter</span></span>
<span data-ttu-id="b3399-141">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="b3399-141">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b3399-142">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="b3399-142">-RouteFilterId</span></span>
<span data-ttu-id="b3399-143">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="b3399-143">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b3399-144">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b3399-144">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="b3399-145">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="b3399-145">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="b3399-146">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="b3399-146">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b3399-147">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="b3399-147">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b3399-148">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="b3399-148">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b3399-149">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b3399-149">-SharedKey</span></span>
<span data-ttu-id="b3399-150">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="b3399-150">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="b3399-151">-VlanId</span><span class="sxs-lookup"><span data-stu-id="b3399-151">-VlanId</span></span>
<span data-ttu-id="b3399-152">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="b3399-152">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="b3399-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3399-153">-DefaultProfile</span></span>
<span data-ttu-id="b3399-154">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3399-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3399-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3399-155">CommonParameters</span></span>
<span data-ttu-id="b3399-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3399-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3399-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3399-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3399-158">輸入</span><span class="sxs-lookup"><span data-stu-id="b3399-158">INPUTS</span></span>

### <span data-ttu-id="b3399-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3399-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="b3399-160">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b3399-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="b3399-161">輸出</span><span class="sxs-lookup"><span data-stu-id="b3399-161">OUTPUTS</span></span>

### <span data-ttu-id="b3399-162">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b3399-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b3399-163">筆記</span><span class="sxs-lookup"><span data-stu-id="b3399-163">NOTES</span></span>

## <span data-ttu-id="b3399-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3399-164">RELATED LINKS</span></span>

[<span data-ttu-id="b3399-165">附加 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b3399-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b3399-166">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3399-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b3399-167">新-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b3399-167">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b3399-168">移除-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b3399-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

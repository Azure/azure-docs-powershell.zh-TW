---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 19b86fdaab8eac6ae5d711e7ed8bd2952312fcae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800742"
---
# <span data-ttu-id="50fcb-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="50fcb-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="50fcb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="50fcb-103">儲存已修改的 ExpressRoute 對等設定。</span><span class="sxs-lookup"><span data-stu-id="50fcb-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50fcb-104">句法</span><span class="sxs-lookup"><span data-stu-id="50fcb-104">SYNTAX</span></span>

### <span data-ttu-id="50fcb-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="50fcb-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50fcb-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="50fcb-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50fcb-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="50fcb-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50fcb-108">說明</span><span class="sxs-lookup"><span data-stu-id="50fcb-108">DESCRIPTION</span></span>
<span data-ttu-id="50fcb-109">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet 會將已修改的 ExpressRoute 對等設定儲存回 Azure。</span><span class="sxs-lookup"><span data-stu-id="50fcb-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="50fcb-110">示例</span><span class="sxs-lookup"><span data-stu-id="50fcb-110">EXAMPLES</span></span>

### <span data-ttu-id="50fcb-111">範例1：變更現有的對等設定</span><span class="sxs-lookup"><span data-stu-id="50fcb-111">Example 1: Change an existing peering configuration</span></span>
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

## <span data-ttu-id="50fcb-112">參數</span><span class="sxs-lookup"><span data-stu-id="50fcb-112">PARAMETERS</span></span>

### <span data-ttu-id="50fcb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fcb-113">-DefaultProfile</span></span>
<span data-ttu-id="50fcb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50fcb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50fcb-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="50fcb-116">包含要修改之對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="50fcb-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="50fcb-117">-LegacyMode</span></span>
<span data-ttu-id="50fcb-118">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="50fcb-118">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="50fcb-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="50fcb-120">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="50fcb-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="50fcb-121">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="50fcb-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="50fcb-122">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="50fcb-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="50fcb-123">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="50fcb-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="50fcb-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="50fcb-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="50fcb-125">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="50fcb-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="50fcb-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="50fcb-127">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="50fcb-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="50fcb-128">-Name</span></span>
<span data-ttu-id="50fcb-129">要修改之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="50fcb-129">The name of the peering configuration to be modified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="50fcb-130">-PeerAddressType</span></span>
<span data-ttu-id="50fcb-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="50fcb-131">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="50fcb-132">-PeerASN</span></span>
<span data-ttu-id="50fcb-133">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="50fcb-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="50fcb-134">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="50fcb-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="50fcb-135">-PeeringType</span></span>
<span data-ttu-id="50fcb-136">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="50fcb-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="50fcb-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="50fcb-138">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="50fcb-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="50fcb-139">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="50fcb-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="50fcb-140">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="50fcb-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="50fcb-141">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="50fcb-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="50fcb-142">-RouteFilter</span></span>
<span data-ttu-id="50fcb-143">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="50fcb-143">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="50fcb-144">-RouteFilterId</span></span>
<span data-ttu-id="50fcb-145">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="50fcb-145">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="50fcb-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="50fcb-147">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="50fcb-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="50fcb-148">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="50fcb-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="50fcb-149">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="50fcb-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="50fcb-150">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="50fcb-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="50fcb-151">-SharedKey</span></span>
<span data-ttu-id="50fcb-152">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="50fcb-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="50fcb-153">-VlanId</span></span>
<span data-ttu-id="50fcb-154">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="50fcb-154">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fcb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fcb-155">CommonParameters</span></span>
<span data-ttu-id="50fcb-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50fcb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fcb-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50fcb-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fcb-158">輸入</span><span class="sxs-lookup"><span data-stu-id="50fcb-158">INPUTS</span></span>

### <span data-ttu-id="50fcb-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50fcb-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="50fcb-160">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="50fcb-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="50fcb-161">輸出</span><span class="sxs-lookup"><span data-stu-id="50fcb-161">OUTPUTS</span></span>

### <span data-ttu-id="50fcb-162">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="50fcb-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="50fcb-163">筆記</span><span class="sxs-lookup"><span data-stu-id="50fcb-163">NOTES</span></span>

## <span data-ttu-id="50fcb-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="50fcb-164">RELATED LINKS</span></span>

[<span data-ttu-id="50fcb-165">附加 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="50fcb-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="50fcb-166">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50fcb-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="50fcb-167">新-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="50fcb-167">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="50fcb-168">移除-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="50fcb-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

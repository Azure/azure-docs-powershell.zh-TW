---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5655fafa866fbc3702a1c6bf017caddd21df6fab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456524"
---
# <span data-ttu-id="cece6-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cece6-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="cece6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cece6-102">SYNOPSIS</span></span>
<span data-ttu-id="cece6-103">在 ExpressRoute 回路中新增對等設定。</span><span class="sxs-lookup"><span data-stu-id="cece6-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cece6-104">句法</span><span class="sxs-lookup"><span data-stu-id="cece6-104">SYNTAX</span></span>

### <span data-ttu-id="cece6-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="cece6-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cece6-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="cece6-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cece6-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="cece6-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cece6-108">說明</span><span class="sxs-lookup"><span data-stu-id="cece6-108">DESCRIPTION</span></span>
<span data-ttu-id="cece6-109">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet 會將對等設定新增至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="cece6-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="cece6-110">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="cece6-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="cece6-111">請注意，執行 **附加 AzureRmExpressRouteCircuitPeeringConfig** 之後，您必須呼叫 Set-AzureRmExpressRouteCircuit Cmdlet 才能啟動設定。</span><span class="sxs-lookup"><span data-stu-id="cece6-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="cece6-112">示例</span><span class="sxs-lookup"><span data-stu-id="cece6-112">EXAMPLES</span></span>

### <span data-ttu-id="cece6-113">範例1：將對等新增至現有的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="cece6-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="cece6-114">參數</span><span class="sxs-lookup"><span data-stu-id="cece6-114">PARAMETERS</span></span>

### <span data-ttu-id="cece6-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cece6-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cece6-116">要修改的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="cece6-116">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="cece6-117">這是 **AzureRmExpressRouteCircuit** Cmdlet 傳回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="cece6-117">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="cece6-118">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="cece6-118">-LegacyMode</span></span>
<span data-ttu-id="cece6-119">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="cece6-119">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="cece6-120">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="cece6-120">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="cece6-121">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="cece6-121">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="cece6-122">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="cece6-122">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="cece6-123">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="cece6-123">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="cece6-124">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="cece6-124">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="cece6-125">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="cece6-125">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="cece6-126">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="cece6-126">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="cece6-127">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="cece6-127">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="cece6-128">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="cece6-128">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="cece6-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="cece6-129">-Name</span></span>
<span data-ttu-id="cece6-130">要新增之對等關係的名稱。</span><span class="sxs-lookup"><span data-stu-id="cece6-130">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="cece6-131">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="cece6-131">-PeerAddressType</span></span>
<span data-ttu-id="cece6-132">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="cece6-132">PeerAddressType</span></span>

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

### <span data-ttu-id="cece6-133">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="cece6-133">-PeerASN</span></span>
<span data-ttu-id="cece6-134">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="cece6-134">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="cece6-135">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="cece6-135">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="cece6-136">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="cece6-136">-PeeringType</span></span>
<span data-ttu-id="cece6-137">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="cece6-137">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="cece6-138">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cece6-138">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="cece6-139">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="cece6-139">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="cece6-140">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="cece6-140">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="cece6-141">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="cece6-141">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="cece6-142">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="cece6-142">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="cece6-143">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="cece6-143">-RouteFilter</span></span>
<span data-ttu-id="cece6-144">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="cece6-144">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="cece6-145">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="cece6-145">-RouteFilterId</span></span>
<span data-ttu-id="cece6-146">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="cece6-146">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="cece6-147">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cece6-147">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="cece6-148">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="cece6-148">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="cece6-149">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="cece6-149">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="cece6-150">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="cece6-150">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="cece6-151">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="cece6-151">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="cece6-152">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="cece6-152">-SharedKey</span></span>
<span data-ttu-id="cece6-153">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="cece6-153">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="cece6-154">-VlanId</span><span class="sxs-lookup"><span data-stu-id="cece6-154">-VlanId</span></span>
<span data-ttu-id="cece6-155">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="cece6-155">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="cece6-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cece6-156">-DefaultProfile</span></span>
<span data-ttu-id="cece6-157">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cece6-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cece6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cece6-158">CommonParameters</span></span>
<span data-ttu-id="cece6-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cece6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cece6-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cece6-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cece6-161">輸入</span><span class="sxs-lookup"><span data-stu-id="cece6-161">INPUTS</span></span>

### <span data-ttu-id="cece6-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cece6-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="cece6-163">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="cece6-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="cece6-164">輸出</span><span class="sxs-lookup"><span data-stu-id="cece6-164">OUTPUTS</span></span>

### <span data-ttu-id="cece6-165">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cece6-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cece6-166">筆記</span><span class="sxs-lookup"><span data-stu-id="cece6-166">NOTES</span></span>

## <span data-ttu-id="cece6-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="cece6-167">RELATED LINKS</span></span>

[<span data-ttu-id="cece6-168">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cece6-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="cece6-169">新-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cece6-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cece6-170">移除-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cece6-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cece6-171">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cece6-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

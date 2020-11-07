---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ad57558eeaa9480e6574b74d052131700feaefae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626366"
---
# <span data-ttu-id="0feca-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0feca-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="0feca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0feca-102">SYNOPSIS</span></span>
<span data-ttu-id="0feca-103">儲存已修改的 ExpressRoute 對等設定。</span><span class="sxs-lookup"><span data-stu-id="0feca-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0feca-104">句法</span><span class="sxs-lookup"><span data-stu-id="0feca-104">SYNTAX</span></span>

### <span data-ttu-id="0feca-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="0feca-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0feca-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="0feca-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0feca-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="0feca-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0feca-108">說明</span><span class="sxs-lookup"><span data-stu-id="0feca-108">DESCRIPTION</span></span>
<span data-ttu-id="0feca-109">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet 會將已修改的 ExpressRoute 對等設定儲存回 Azure。</span><span class="sxs-lookup"><span data-stu-id="0feca-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="0feca-110">示例</span><span class="sxs-lookup"><span data-stu-id="0feca-110">EXAMPLES</span></span>

### <span data-ttu-id="0feca-111">範例1：變更現有的對等設定</span><span class="sxs-lookup"><span data-stu-id="0feca-111">Example 1: Change an existing peering configuration</span></span>
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

## <span data-ttu-id="0feca-112">參數</span><span class="sxs-lookup"><span data-stu-id="0feca-112">PARAMETERS</span></span>

### <span data-ttu-id="0feca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0feca-113">-DefaultProfile</span></span>
<span data-ttu-id="0feca-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0feca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0feca-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0feca-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0feca-116">包含要修改之對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="0feca-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="0feca-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="0feca-117">-LegacyMode</span></span>
<span data-ttu-id="0feca-118">對等的舊版模式</span><span class="sxs-lookup"><span data-stu-id="0feca-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="0feca-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="0feca-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="0feca-120">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="0feca-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="0feca-121">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="0feca-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="0feca-122">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="0feca-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="0feca-123">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="0feca-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="0feca-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="0feca-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="0feca-125">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="0feca-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="0feca-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="0feca-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="0feca-127">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="0feca-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="0feca-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="0feca-128">-Name</span></span>
<span data-ttu-id="0feca-129">要修改之對等設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="0feca-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="0feca-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="0feca-130">-PeerAddressType</span></span>
<span data-ttu-id="0feca-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="0feca-131">PeerAddressType</span></span>

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

### <span data-ttu-id="0feca-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="0feca-132">-PeerASN</span></span>
<span data-ttu-id="0feca-133">您的 ExpressRoute 回路編號。</span><span class="sxs-lookup"><span data-stu-id="0feca-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="0feca-134">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="0feca-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="0feca-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0feca-135">-PeeringType</span></span>
<span data-ttu-id="0feca-136">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0feca-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="0feca-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0feca-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="0feca-138">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="0feca-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="0feca-139">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="0feca-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="0feca-140">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="0feca-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="0feca-141">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="0feca-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="0feca-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0feca-142">-RouteFilter</span></span>
<span data-ttu-id="0feca-143">這是現有的 RouteFilter 物件。</span><span class="sxs-lookup"><span data-stu-id="0feca-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="0feca-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="0feca-144">-RouteFilterId</span></span>
<span data-ttu-id="0feca-145">這是現有 RouteFilter 物件的資源 Id。</span><span class="sxs-lookup"><span data-stu-id="0feca-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="0feca-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0feca-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="0feca-147">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="0feca-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="0feca-148">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="0feca-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="0feca-149">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="0feca-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="0feca-150">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="0feca-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="0feca-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="0feca-151">-SharedKey</span></span>
<span data-ttu-id="0feca-152">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="0feca-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="0feca-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="0feca-153">-VlanId</span></span>
<span data-ttu-id="0feca-154">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="0feca-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="0feca-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0feca-155">CommonParameters</span></span>
<span data-ttu-id="0feca-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0feca-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0feca-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0feca-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0feca-158">輸入</span><span class="sxs-lookup"><span data-stu-id="0feca-158">INPUTS</span></span>

### <span data-ttu-id="0feca-159">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0feca-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="0feca-160">參數： ExpressRouteCircuit (ByValue) </span><span class="sxs-lookup"><span data-stu-id="0feca-160">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="0feca-161">System.object</span><span class="sxs-lookup"><span data-stu-id="0feca-161">System.String</span></span>

### <span data-ttu-id="0feca-162">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0feca-162">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="0feca-163">System.object</span><span class="sxs-lookup"><span data-stu-id="0feca-163">System.Boolean</span></span>

## <span data-ttu-id="0feca-164">輸出</span><span class="sxs-lookup"><span data-stu-id="0feca-164">OUTPUTS</span></span>

### <span data-ttu-id="0feca-165">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0feca-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0feca-166">筆記</span><span class="sxs-lookup"><span data-stu-id="0feca-166">NOTES</span></span>

## <span data-ttu-id="0feca-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="0feca-167">RELATED LINKS</span></span>

[<span data-ttu-id="0feca-168">附加 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0feca-168">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0feca-169">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0feca-169">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0feca-170">新-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0feca-170">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0feca-171">移除-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0feca-171">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

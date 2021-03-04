---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b16206fdcaf775315947ca9fe71f487d1f9d8df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916915"
---
# <span data-ttu-id="06a7a-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="06a7a-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="06a7a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="06a7a-103">新增對等組配置至 ExpressRoute 交叉連接。</span><span class="sxs-lookup"><span data-stu-id="06a7a-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="06a7a-104">語法</span><span class="sxs-lookup"><span data-stu-id="06a7a-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a7a-105">描述</span><span class="sxs-lookup"><span data-stu-id="06a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="06a7a-106">**Add-AzExpressRouteCrossConnectionPeering** Cmdlet 會新增對等組配置至 ExpressRoute 交叉連接。</span><span class="sxs-lookup"><span data-stu-id="06a7a-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="06a7a-107">請注意，在啟動 **Add-AzExpressRouteCrossConnectionPeering** 之後，您必須呼叫 Set-AzExpressRouteCrossConnection Cmdlet 以啟用組配置。</span><span class="sxs-lookup"><span data-stu-id="06a7a-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="06a7a-108">例子</span><span class="sxs-lookup"><span data-stu-id="06a7a-108">EXAMPLES</span></span>

### <span data-ttu-id="06a7a-109">範例 1：新增對等至現有的 ExpressRoute 交叉連接</span><span class="sxs-lookup"><span data-stu-id="06a7a-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="06a7a-110">參數</span><span class="sxs-lookup"><span data-stu-id="06a7a-110">PARAMETERS</span></span>

### <span data-ttu-id="06a7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a7a-111">-DefaultProfile</span></span>
<span data-ttu-id="06a7a-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06a7a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a7a-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="06a7a-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="06a7a-114">要修改的 ExpressRoute 交叉連接。</span><span class="sxs-lookup"><span data-stu-id="06a7a-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="06a7a-115">這是 **Get-AzExpressRouteCrossConnection Cmdlet 所返回的** Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="06a7a-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06a7a-116">-強制</span><span class="sxs-lookup"><span data-stu-id="06a7a-116">-Force</span></span>
<span data-ttu-id="06a7a-117">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="06a7a-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a7a-118">-MicrosoftConfigAdvertvertlicPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="06a7a-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="06a7a-119">針對 MicrosoftPeering 的對等類型，您必須提供計畫要以 BGP 會話宣告的所有首碼清單。</span><span class="sxs-lookup"><span data-stu-id="06a7a-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="06a7a-120">僅接受公用 IP 位址首碼。</span><span class="sxs-lookup"><span data-stu-id="06a7a-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="06a7a-121">如果您打算傳送一組首碼，可以傳送逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="06a7a-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="06a7a-122">這些首碼必須在路由登錄名稱的 RIR /IRR (中註冊) 。</span><span class="sxs-lookup"><span data-stu-id="06a7a-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="06a7a-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="06a7a-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="06a7a-124">如果您是未註冊至對等 AS 號碼的廣告首碼，您可以指定其註冊的 AS 號碼。</span><span class="sxs-lookup"><span data-stu-id="06a7a-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="06a7a-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="06a7a-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="06a7a-126">路由登錄名稱 (RIR / IRR) AS 號碼和首碼的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="06a7a-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="06a7a-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="06a7a-127">-Name</span></span>
<span data-ttu-id="06a7a-128">要新增的對等關係名稱。</span><span class="sxs-lookup"><span data-stu-id="06a7a-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="06a7a-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="06a7a-129">-PeerAddressType</span></span>
<span data-ttu-id="06a7a-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="06a7a-130">PeerAddressType</span></span>

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

### <span data-ttu-id="06a7a-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="06a7a-131">-PeerASN</span></span>
<span data-ttu-id="06a7a-132">ExpressRoute 交叉連接的 AS 號碼。</span><span class="sxs-lookup"><span data-stu-id="06a7a-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="06a7a-133">當對等類型為 AzurePublicPeering 時，這必須是公用 ASN。</span><span class="sxs-lookup"><span data-stu-id="06a7a-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="06a7a-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="06a7a-134">-PeeringType</span></span>
<span data-ttu-id="06a7a-135">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="06a7a-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="06a7a-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="06a7a-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="06a7a-137">這是此對等互連關係之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="06a7a-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="06a7a-138">這必須是 /30 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="06a7a-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="06a7a-139">此子網的第一個奇數編號位址應指派給路由器介面。</span><span class="sxs-lookup"><span data-stu-id="06a7a-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="06a7a-140">Azure 會設定 Azure 路由器介面的下一個均勻編號位址。</span><span class="sxs-lookup"><span data-stu-id="06a7a-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="06a7a-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="06a7a-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="06a7a-142">這是此對等互連關係的次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="06a7a-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="06a7a-143">這必須是 /30 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="06a7a-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="06a7a-144">此子網的第一個奇數編號位址應指派給路由器介面。</span><span class="sxs-lookup"><span data-stu-id="06a7a-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="06a7a-145">Azure 會設定 Azure 路由器介面的下一個均勻編號位址。</span><span class="sxs-lookup"><span data-stu-id="06a7a-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="06a7a-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="06a7a-146">-SharedKey</span></span>
<span data-ttu-id="06a7a-147">這是選擇性的 MD5 雜湊，用來做為對等配置的預先共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="06a7a-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="06a7a-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="06a7a-148">-VlanId</span></span>
<span data-ttu-id="06a7a-149">這是為此對等指派的 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="06a7a-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="06a7a-150">-確認</span><span class="sxs-lookup"><span data-stu-id="06a7a-150">-Confirm</span></span>
<span data-ttu-id="06a7a-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06a7a-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a7a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a7a-152">-WhatIf</span></span>
<span data-ttu-id="06a7a-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06a7a-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06a7a-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06a7a-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a7a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a7a-155">CommonParameters</span></span>
<span data-ttu-id="06a7a-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06a7a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a7a-157">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="06a7a-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a7a-158">輸入</span><span class="sxs-lookup"><span data-stu-id="06a7a-158">INPUTS</span></span>

### <span data-ttu-id="06a7a-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="06a7a-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="06a7a-160">參數 'ExpressRouteCrossConnection' 接受來自管線之類型 'PSExpressRouteCrossConnection'的值</span><span class="sxs-lookup"><span data-stu-id="06a7a-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="06a7a-161">輸出</span><span class="sxs-lookup"><span data-stu-id="06a7a-161">OUTPUTS</span></span>

### <span data-ttu-id="06a7a-162">Microsoft.Azure.Commands.Network.models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="06a7a-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="06a7a-163">筆記</span><span class="sxs-lookup"><span data-stu-id="06a7a-163">NOTES</span></span>

## <span data-ttu-id="06a7a-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="06a7a-164">RELATED LINKS</span></span>

[<span data-ttu-id="06a7a-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="06a7a-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="06a7a-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="06a7a-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="06a7a-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="06a7a-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="06a7a-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="06a7a-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)

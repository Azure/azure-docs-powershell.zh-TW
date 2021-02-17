---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140526"
---
# <span data-ttu-id="ff112-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ff112-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="ff112-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff112-102">SYNOPSIS</span></span>
<span data-ttu-id="ff112-103">將對等設定新增至 ExpressRoute 交叉連線。</span><span class="sxs-lookup"><span data-stu-id="ff112-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="ff112-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff112-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff112-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff112-105">DESCRIPTION</span></span>
<span data-ttu-id="ff112-106">**AzExpressRouteCrossConnectionPeering** Cmdlet 會將對等設定新增至 ExpressRoute 交叉連線。</span><span class="sxs-lookup"><span data-stu-id="ff112-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="ff112-107">請注意，執行 **附加 AzExpressRouteCrossConnectionPeering** 之後，您必須呼叫 Set-AzExpressRouteCrossConnection Cmdlet 才能啟動設定。</span><span class="sxs-lookup"><span data-stu-id="ff112-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="ff112-108">示例</span><span class="sxs-lookup"><span data-stu-id="ff112-108">EXAMPLES</span></span>

### <span data-ttu-id="ff112-109">範例1：將對等新增至現有的 ExpressRoute 交叉連接</span><span class="sxs-lookup"><span data-stu-id="ff112-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="ff112-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff112-110">PARAMETERS</span></span>

### <span data-ttu-id="ff112-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff112-111">-DefaultProfile</span></span>
<span data-ttu-id="ff112-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff112-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff112-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ff112-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ff112-114">要修改的 ExpressRoute 交叉連線。</span><span class="sxs-lookup"><span data-stu-id="ff112-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="ff112-115">這是 **AzExpressRouteCrossConnection** Cmdlet 傳回的 Azure 物件。</span><span class="sxs-lookup"><span data-stu-id="ff112-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="ff112-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ff112-116">-Force</span></span>
<span data-ttu-id="ff112-117">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="ff112-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ff112-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="ff112-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="ff112-119">針對 MicrosoftPeering 的 PeeringType，您必須提供您計畫在 BGP 會話中宣告的所有首碼的清單。</span><span class="sxs-lookup"><span data-stu-id="ff112-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="ff112-120">只接受公用 IP 位址的首碼。</span><span class="sxs-lookup"><span data-stu-id="ff112-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="ff112-121">如果您打算傳送一組首碼，您可以傳送以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="ff112-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="ff112-122">這些首碼必須以路由註冊名稱登錄至您， (RIR/IRR) 。</span><span class="sxs-lookup"><span data-stu-id="ff112-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="ff112-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="ff112-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="ff112-124">如果您要公佈未以數位方式登錄到對等的首碼，您可以指定其註冊的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="ff112-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="ff112-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="ff112-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="ff112-126">路由登錄的名稱 (的 RIR/IRR) ，將其註冊為數字與首碼。</span><span class="sxs-lookup"><span data-stu-id="ff112-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="ff112-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff112-127">-Name</span></span>
<span data-ttu-id="ff112-128">要新增之對等關係的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff112-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="ff112-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ff112-129">-PeerAddressType</span></span>
<span data-ttu-id="ff112-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ff112-130">PeerAddressType</span></span>

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

### <span data-ttu-id="ff112-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="ff112-131">-PeerASN</span></span>
<span data-ttu-id="ff112-132">您的 ExpressRoute 交叉連接的 AS 編號。</span><span class="sxs-lookup"><span data-stu-id="ff112-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="ff112-133">這必須是 PeeringType 為 AzurePublicPeering 時的公開 ASN。</span><span class="sxs-lookup"><span data-stu-id="ff112-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="ff112-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ff112-134">-PeeringType</span></span>
<span data-ttu-id="ff112-135">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ff112-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ff112-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ff112-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="ff112-137">這是此對等關聯之主要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="ff112-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="ff112-138">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="ff112-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ff112-139">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="ff112-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ff112-140">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="ff112-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ff112-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ff112-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="ff112-142">這是此對等關係之次要路由路徑的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="ff112-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="ff112-143">這必須是/30 個 CIDR 子網。</span><span class="sxs-lookup"><span data-stu-id="ff112-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ff112-144">這個子網上的第一個奇數位址應該指派給您的路由器介面。</span><span class="sxs-lookup"><span data-stu-id="ff112-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ff112-145">Azure 會將下一個偶數位址設定為 Azure 路由器介面。</span><span class="sxs-lookup"><span data-stu-id="ff112-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ff112-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ff112-146">-SharedKey</span></span>
<span data-ttu-id="ff112-147">這個選用的 MD5 雜湊是用來做為對等設定的預共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ff112-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="ff112-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="ff112-148">-VlanId</span></span>
<span data-ttu-id="ff112-149">這是指派給這個對等的 VLAN Id 號碼。</span><span class="sxs-lookup"><span data-stu-id="ff112-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="ff112-150">-確認</span><span class="sxs-lookup"><span data-stu-id="ff112-150">-Confirm</span></span>
<span data-ttu-id="ff112-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff112-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff112-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff112-152">-WhatIf</span></span>
<span data-ttu-id="ff112-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff112-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff112-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff112-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff112-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff112-155">CommonParameters</span></span>
<span data-ttu-id="ff112-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff112-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff112-157">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff112-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff112-158">輸入</span><span class="sxs-lookup"><span data-stu-id="ff112-158">INPUTS</span></span>

### <span data-ttu-id="ff112-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ff112-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="ff112-160">形參 "ExpressRouteCrossConnection" 接受管線中 "PSExpressRouteCrossConnection" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ff112-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="ff112-161">輸出</span><span class="sxs-lookup"><span data-stu-id="ff112-161">OUTPUTS</span></span>

### <span data-ttu-id="ff112-162">PSExpressRouteCrossConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ff112-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="ff112-163">筆記</span><span class="sxs-lookup"><span data-stu-id="ff112-163">NOTES</span></span>

## <span data-ttu-id="ff112-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff112-164">RELATED LINKS</span></span>

[<span data-ttu-id="ff112-165">AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ff112-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ff112-166">移除-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ff112-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ff112-167">AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ff112-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="ff112-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ff112-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)

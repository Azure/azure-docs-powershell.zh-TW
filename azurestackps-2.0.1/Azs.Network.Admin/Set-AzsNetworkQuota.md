---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966708"
---
# <span data-ttu-id="e640c-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="e640c-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="e640c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e640c-102">SYNOPSIS</span></span>
<span data-ttu-id="e640c-103">建立或更新配額。</span><span class="sxs-lookup"><span data-stu-id="e640c-103">Create or update a quota.</span></span>

## <span data-ttu-id="e640c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e640c-104">SYNTAX</span></span>

### <span data-ttu-id="e640c-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="e640c-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e640c-106">時更新</span><span class="sxs-lookup"><span data-stu-id="e640c-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e640c-107">說明</span><span class="sxs-lookup"><span data-stu-id="e640c-107">DESCRIPTION</span></span>
<span data-ttu-id="e640c-108">建立或更新配額。</span><span class="sxs-lookup"><span data-stu-id="e640c-108">Create or update a quota.</span></span>

## <span data-ttu-id="e640c-109">示例</span><span class="sxs-lookup"><span data-stu-id="e640c-109">EXAMPLES</span></span>

### <span data-ttu-id="e640c-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e640c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="e640c-111">依名稱更新網路配額。</span><span class="sxs-lookup"><span data-stu-id="e640c-111">Update a network quota by name.</span></span>

### <span data-ttu-id="e640c-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e640c-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="e640c-113">依名稱更新網路配額。</span><span class="sxs-lookup"><span data-stu-id="e640c-113">Update a network quota by name.</span></span>

## <span data-ttu-id="e640c-114">參數</span><span class="sxs-lookup"><span data-stu-id="e640c-114">PARAMETERS</span></span>

### <span data-ttu-id="e640c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e640c-115">-DefaultProfile</span></span>
<span data-ttu-id="e640c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e640c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-117">-位置</span><span class="sxs-lookup"><span data-stu-id="e640c-117">-Location</span></span>
<span data-ttu-id="e640c-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e640c-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e640c-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="e640c-120">租使用者訂閱可提供的負載等化器數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e640c-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="e640c-122">租使用者訂閱可提供的 Nic 數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e640c-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="e640c-124">租使用者訂閱可提供的公用 IP 位址數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e640c-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="e640c-126">租使用者訂閱可提供的安全性群組數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e640c-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="e640c-128">租使用者訂閱可提供的虛擬網路閘道連線數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e640c-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="e640c-130">租使用者訂閱可提供的虛擬網路閘道數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e640c-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="e640c-132">租使用者訂閱可提供的虛擬網路數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="e640c-133">-Name</span></span>
<span data-ttu-id="e640c-134">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e640c-134">Name of the resource.</span></span>

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

### <span data-ttu-id="e640c-135">-配額</span><span class="sxs-lookup"><span data-stu-id="e640c-135">-Quota</span></span>
<span data-ttu-id="e640c-136">網路配額資源。</span><span class="sxs-lookup"><span data-stu-id="e640c-136">Network quota resource.</span></span>
<span data-ttu-id="e640c-137">若要建立，請參閱配額屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e640c-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e640c-138">-SubscriptionId</span></span>
<span data-ttu-id="e640c-139">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e640c-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e640c-140">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e640c-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="e640c-141">-Tag</span></span>
<span data-ttu-id="e640c-142">鍵值對清單。</span><span class="sxs-lookup"><span data-stu-id="e640c-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e640c-143">-確認</span><span class="sxs-lookup"><span data-stu-id="e640c-143">-Confirm</span></span>
<span data-ttu-id="e640c-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e640c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e640c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e640c-145">-WhatIf</span></span>
<span data-ttu-id="e640c-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e640c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e640c-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e640c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e640c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e640c-148">CommonParameters</span></span>
<span data-ttu-id="e640c-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e640c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e640c-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e640c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e640c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="e640c-151">INPUTS</span></span>

### <span data-ttu-id="e640c-152">IQuota （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="e640c-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="e640c-153">輸出</span><span class="sxs-lookup"><span data-stu-id="e640c-153">OUTPUTS</span></span>

### <span data-ttu-id="e640c-154">IQuota （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="e640c-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="e640c-155">筆記</span><span class="sxs-lookup"><span data-stu-id="e640c-155">NOTES</span></span>

<span data-ttu-id="e640c-156">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e640c-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e640c-157">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e640c-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e640c-158">配額 <IQuota> ：網路配額資源。</span><span class="sxs-lookup"><span data-stu-id="e640c-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="e640c-159">`[Tag <IResourceTags>]`： [鍵值] 對的清單。</span><span class="sxs-lookup"><span data-stu-id="e640c-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="e640c-160">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="e640c-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e640c-161">`[MaxLoadBalancersPerSubscription <Int64?>]`：租使用者訂閱可提供的負載等化器數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="e640c-162">`[MaxNicsPerSubscription <Int64?>]`：租使用者訂閱可提供的 Nic 數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="e640c-163">`[MaxPublicIpsPerSubscription <Int64?>]`：租使用者訂閱可提供的公用 IP 位址數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="e640c-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`：租使用者訂閱可提供的安全性群組數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="e640c-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`：租使用者訂閱可提供的虛擬網路閘道連線數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="e640c-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`：租使用者訂閱可提供的虛擬網路閘道數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="e640c-167">`[MaxVnetsPerSubscription <Int64?>]`：租使用者訂閱可提供的虛擬網路數目上限。</span><span class="sxs-lookup"><span data-stu-id="e640c-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="e640c-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="e640c-168">RELATED LINKS</span></span>


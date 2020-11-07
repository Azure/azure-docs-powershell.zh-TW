---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968316"
---
# <span data-ttu-id="a4882-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a4882-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="a4882-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4882-102">SYNOPSIS</span></span>
<span data-ttu-id="a4882-103">建立或更新配額。</span><span class="sxs-lookup"><span data-stu-id="a4882-103">Create or update a quota.</span></span>

## <span data-ttu-id="a4882-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4882-104">SYNTAX</span></span>

### <span data-ttu-id="a4882-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a4882-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4882-106">建立</span><span class="sxs-lookup"><span data-stu-id="a4882-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4882-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4882-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4882-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a4882-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4882-109">說明</span><span class="sxs-lookup"><span data-stu-id="a4882-109">DESCRIPTION</span></span>
<span data-ttu-id="a4882-110">建立或更新配額。</span><span class="sxs-lookup"><span data-stu-id="a4882-110">Create or update a quota.</span></span>

## <span data-ttu-id="a4882-111">示例</span><span class="sxs-lookup"><span data-stu-id="a4882-111">EXAMPLES</span></span>

### <span data-ttu-id="a4882-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4882-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="a4882-113">建立具有所有預設值的新網路配額。</span><span class="sxs-lookup"><span data-stu-id="a4882-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="a4882-114">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4882-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="a4882-115">使用非預設值為 [配額] 建立新的網路配額。</span><span class="sxs-lookup"><span data-stu-id="a4882-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="a4882-116">參數</span><span class="sxs-lookup"><span data-stu-id="a4882-116">PARAMETERS</span></span>

### <span data-ttu-id="a4882-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4882-117">-DefaultProfile</span></span>
<span data-ttu-id="a4882-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4882-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4882-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4882-119">-InputObject</span></span>
<span data-ttu-id="a4882-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a4882-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-121">-位置</span><span class="sxs-lookup"><span data-stu-id="a4882-121">-Location</span></span>
<span data-ttu-id="a4882-122">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a4882-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4882-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="a4882-124">租使用者訂閱可提供的負載等化器數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4882-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="a4882-126">租使用者訂閱可提供的 Nic 數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4882-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="a4882-128">租使用者訂閱可提供的公用 IP 位址數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4882-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="a4882-130">租使用者訂閱可提供的安全性群組數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4882-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="a4882-132">租使用者訂閱可提供的虛擬網路閘道連線數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4882-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="a4882-134">租使用者訂閱可提供的虛擬網路閘道數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4882-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="a4882-136">租使用者訂閱可提供的虛擬網路數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4882-137">-Name</span></span>
<span data-ttu-id="a4882-138">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4882-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-139">-配額</span><span class="sxs-lookup"><span data-stu-id="a4882-139">-Quota</span></span>
<span data-ttu-id="a4882-140">網路配額資源。</span><span class="sxs-lookup"><span data-stu-id="a4882-140">Network quota resource.</span></span>
<span data-ttu-id="a4882-141">若要建立，請參閱配額屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a4882-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4882-142">-SubscriptionId</span></span>
<span data-ttu-id="a4882-143">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a4882-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a4882-144">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a4882-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4882-145">-Tag</span></span>
<span data-ttu-id="a4882-146">鍵值對清單。</span><span class="sxs-lookup"><span data-stu-id="a4882-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a4882-147">-確認</span><span class="sxs-lookup"><span data-stu-id="a4882-147">-Confirm</span></span>
<span data-ttu-id="a4882-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4882-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4882-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4882-149">-WhatIf</span></span>
<span data-ttu-id="a4882-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4882-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4882-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4882-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4882-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4882-152">CommonParameters</span></span>
<span data-ttu-id="a4882-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4882-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4882-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4882-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4882-155">輸入</span><span class="sxs-lookup"><span data-stu-id="a4882-155">INPUTS</span></span>

### <span data-ttu-id="a4882-156">IQuota （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="a4882-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="a4882-157">INetworkAdminIdentity （NetworkAdmin）的</span><span class="sxs-lookup"><span data-stu-id="a4882-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="a4882-158">輸出</span><span class="sxs-lookup"><span data-stu-id="a4882-158">OUTPUTS</span></span>

### <span data-ttu-id="a4882-159">IQuota （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="a4882-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="a4882-160">筆記</span><span class="sxs-lookup"><span data-stu-id="a4882-160">NOTES</span></span>

<span data-ttu-id="a4882-161">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a4882-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4882-162">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a4882-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a4882-163">INPUTOBJECT <INetworkAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a4882-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4882-164">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a4882-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4882-165">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a4882-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a4882-166">`[ResourceName <String>]`：資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4882-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="a4882-167">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a4882-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a4882-168">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a4882-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="a4882-169">配額 <IQuota> ：網路配額資源。</span><span class="sxs-lookup"><span data-stu-id="a4882-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="a4882-170">`[Tag <IResourceTags>]`： [鍵值] 對的清單。</span><span class="sxs-lookup"><span data-stu-id="a4882-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="a4882-171">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="a4882-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a4882-172">`[MaxLoadBalancersPerSubscription <Int64?>]`：租使用者訂閱可提供的負載等化器數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a4882-173">`[MaxNicsPerSubscription <Int64?>]`：租使用者訂閱可提供的 Nic 數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a4882-174">`[MaxPublicIpsPerSubscription <Int64?>]`：租使用者訂閱可提供的公用 IP 位址數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a4882-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`：租使用者訂閱可提供的安全性群組數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a4882-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`：租使用者訂閱可提供的虛擬網路閘道連線數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a4882-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`：租使用者訂閱可提供的虛擬網路閘道數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="a4882-178">`[MaxVnetsPerSubscription <Int64?>]`：租使用者訂閱可提供的虛擬網路數目上限。</span><span class="sxs-lookup"><span data-stu-id="a4882-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="a4882-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4882-179">RELATED LINKS</span></span>


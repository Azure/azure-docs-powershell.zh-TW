---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968333"
---
# <span data-ttu-id="8f8f4-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="8f8f4-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="8f8f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8f8f4-103">建立或更新配額。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-103">Create or update a quota.</span></span>

## <span data-ttu-id="8f8f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f8f4-104">SYNTAX</span></span>

### <span data-ttu-id="8f8f4-105">配額 (預設) </span><span class="sxs-lookup"><span data-stu-id="8f8f4-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f8f4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f8f4-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f8f4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8f8f4-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f8f4-108">說明</span><span class="sxs-lookup"><span data-stu-id="8f8f4-108">DESCRIPTION</span></span>
<span data-ttu-id="8f8f4-109">建立或更新配額。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-109">Create or update a quota.</span></span>

## <span data-ttu-id="8f8f4-110">示例</span><span class="sxs-lookup"><span data-stu-id="8f8f4-110">EXAMPLES</span></span>

### <span data-ttu-id="8f8f4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8f8f4-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="8f8f4-112">依名稱更新網路配額。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-112">Update a network quota by name.</span></span>

### <span data-ttu-id="8f8f4-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8f8f4-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="8f8f4-114">依名稱更新網路配額。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-114">Update a network quota by name.</span></span>

## <span data-ttu-id="8f8f4-115">參數</span><span class="sxs-lookup"><span data-stu-id="8f8f4-115">PARAMETERS</span></span>

### <span data-ttu-id="8f8f4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f8f4-116">-Name</span></span>
<span data-ttu-id="8f8f4-117">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-117">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f8f4-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="8f8f4-119">每個訂閱所允許的最大 Nic 數。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-119">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f8f4-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="8f8f4-121">每個訂閱所允許的最大公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-121">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f8f4-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="8f8f4-123">每個訂閱所允許的虛擬網路閘道連線數目上限。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f8f4-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="8f8f4-125">每個訂閱所允許的虛擬網路 maxium 數目。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-125">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f8f4-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="8f8f4-127">每個訂閱所允許的虛擬網路閘道數目上限。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f8f4-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="8f8f4-129">每個訂閱所允許的安全性群組數目上限。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-129">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f8f4-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="8f8f4-131">每個訂閱所允許的負載等化器數目上限。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-131">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-132">-位置</span><span class="sxs-lookup"><span data-stu-id="8f8f4-132">-Location</span></span>
<span data-ttu-id="8f8f4-133">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-133">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f8f4-134">-ResourceId</span></span>
<span data-ttu-id="8f8f4-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f8f4-136">-InputObject</span></span>
<span data-ttu-id="8f8f4-137">Posbbily Get-AzsNetworkQuota 傳回的修改的網路配額</span><span class="sxs-lookup"><span data-stu-id="8f8f4-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f8f4-138">-WhatIf</span></span>
<span data-ttu-id="8f8f4-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f8f4-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-141">-確認</span><span class="sxs-lookup"><span data-stu-id="8f8f4-141">-Confirm</span></span>
<span data-ttu-id="8f8f4-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8f4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f8f4-143">CommonParameters</span></span>
<span data-ttu-id="8f8f4-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f8f4-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f8f4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f8f4-146">輸入</span><span class="sxs-lookup"><span data-stu-id="8f8f4-146">INPUTS</span></span>

## <span data-ttu-id="8f8f4-147">輸出</span><span class="sxs-lookup"><span data-stu-id="8f8f4-147">OUTPUTS</span></span>

### <span data-ttu-id="8f8f4-148">AzureStack. 系統管理員. Quota</span><span class="sxs-lookup"><span data-stu-id="8f8f4-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="8f8f4-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8f8f4-149">NOTES</span></span>

## <span data-ttu-id="8f8f4-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f8f4-150">RELATED LINKS</span></span>

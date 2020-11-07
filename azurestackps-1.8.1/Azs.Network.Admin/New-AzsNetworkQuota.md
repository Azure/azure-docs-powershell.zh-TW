---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793966"
---
# <span data-ttu-id="9bc1f-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="9bc1f-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="9bc1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9bc1f-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc1f-103">建立或更新配額。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-103">Create or update a quota.</span></span>

## <span data-ttu-id="9bc1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9bc1f-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bc1f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9bc1f-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc1f-106">建立或更新配額。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-106">Create or update a quota.</span></span>

## <span data-ttu-id="9bc1f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9bc1f-107">EXAMPLES</span></span>

### <span data-ttu-id="9bc1f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9bc1f-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="9bc1f-109">建立具有所有預設值的新網路配額。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="9bc1f-110">範例2</span><span class="sxs-lookup"><span data-stu-id="9bc1f-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="9bc1f-111">使用非預設值為 [配額] 建立新的網路配額。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="9bc1f-112">參數</span><span class="sxs-lookup"><span data-stu-id="9bc1f-112">PARAMETERS</span></span>

### <span data-ttu-id="9bc1f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9bc1f-113">-Name</span></span>
<span data-ttu-id="9bc1f-114">網路配額資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-114">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9bc1f-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="9bc1f-116">每個訂閱所允許的最大 Nic 數。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-116">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9bc1f-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="9bc1f-118">每個訂閱所允許的最大公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-118">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9bc1f-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="9bc1f-120">每個訂閱所允許的虛擬網路閘道連線數目上限。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9bc1f-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="9bc1f-122">每個訂閱所允許的虛擬網路 maxium 數目。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-122">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9bc1f-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="9bc1f-124">每個訂閱所允許的虛擬網路閘道數目上限。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9bc1f-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="9bc1f-126">每個訂閱所允許的安全性群組數目上限。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-126">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9bc1f-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="9bc1f-128">每個訂閱所允許的負載等化器數目上限。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-128">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-129">-位置</span><span class="sxs-lookup"><span data-stu-id="9bc1f-129">-Location</span></span>
<span data-ttu-id="9bc1f-130">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-130">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="9bc1f-131">-MigrationPhase</span></span>
<span data-ttu-id="9bc1f-132">遷移的狀態，例如 [無]、[準備]、[提交] 和 [中止]。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc1f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc1f-133">-WhatIf</span></span>
<span data-ttu-id="9bc1f-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bc1f-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bc1f-136">-確認</span><span class="sxs-lookup"><span data-stu-id="9bc1f-136">-Confirm</span></span>
<span data-ttu-id="9bc1f-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bc1f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc1f-138">CommonParameters</span></span>
<span data-ttu-id="9bc1f-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc1f-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9bc1f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc1f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="9bc1f-141">INPUTS</span></span>

## <span data-ttu-id="9bc1f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9bc1f-142">OUTPUTS</span></span>

### <span data-ttu-id="9bc1f-143">AzureStack. 系統管理員. Quota</span><span class="sxs-lookup"><span data-stu-id="9bc1f-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="9bc1f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9bc1f-144">NOTES</span></span>

## <span data-ttu-id="9bc1f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bc1f-145">RELATED LINKS</span></span>

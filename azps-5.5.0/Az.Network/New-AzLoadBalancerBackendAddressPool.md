---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128842"
---
# <span data-ttu-id="64222-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="64222-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="64222-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64222-102">SYNOPSIS</span></span>
<span data-ttu-id="64222-103">在 loadbalancer 上建立後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="64222-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="64222-104">句法</span><span class="sxs-lookup"><span data-stu-id="64222-104">SYNTAX</span></span>

### <span data-ttu-id="64222-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64222-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64222-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64222-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64222-107">說明</span><span class="sxs-lookup"><span data-stu-id="64222-107">DESCRIPTION</span></span>
<span data-ttu-id="64222-108">在 loadbalancer 上建立後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="64222-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="64222-109">允許 specifiying PSLoadBalancerBackendAddress 的陣列。</span><span class="sxs-lookup"><span data-stu-id="64222-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="64222-110">示例</span><span class="sxs-lookup"><span data-stu-id="64222-110">EXAMPLES</span></span>

### <span data-ttu-id="64222-111">範例1</span><span class="sxs-lookup"><span data-stu-id="64222-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="64222-112">範例2</span><span class="sxs-lookup"><span data-stu-id="64222-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="64222-113">範例3</span><span class="sxs-lookup"><span data-stu-id="64222-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="64222-114">範例4</span><span class="sxs-lookup"><span data-stu-id="64222-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="64222-115">參數</span><span class="sxs-lookup"><span data-stu-id="64222-115">PARAMETERS</span></span>

### <span data-ttu-id="64222-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64222-116">-DefaultProfile</span></span>
<span data-ttu-id="64222-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64222-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64222-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="64222-118">-LoadBalancer</span></span>
<span data-ttu-id="64222-119">負載平衡器資源。</span><span class="sxs-lookup"><span data-stu-id="64222-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64222-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="64222-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="64222-121">後端位址。</span><span class="sxs-lookup"><span data-stu-id="64222-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64222-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="64222-122">-LoadBalancerName</span></span>
<span data-ttu-id="64222-123">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="64222-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64222-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="64222-124">-Name</span></span>
<span data-ttu-id="64222-125">後端池的名稱。</span><span class="sxs-lookup"><span data-stu-id="64222-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="64222-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64222-126">-ResourceGroupName</span></span>
<span data-ttu-id="64222-127">負載平衡器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="64222-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64222-128">-確認</span><span class="sxs-lookup"><span data-stu-id="64222-128">-Confirm</span></span>
<span data-ttu-id="64222-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64222-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64222-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64222-130">-WhatIf</span></span>
<span data-ttu-id="64222-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64222-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64222-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64222-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64222-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64222-133">CommonParameters</span></span>
<span data-ttu-id="64222-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64222-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64222-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64222-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64222-136">輸入</span><span class="sxs-lookup"><span data-stu-id="64222-136">INPUTS</span></span>

### <span data-ttu-id="64222-137">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64222-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="64222-138">輸出</span><span class="sxs-lookup"><span data-stu-id="64222-138">OUTPUTS</span></span>

### <span data-ttu-id="64222-139">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64222-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="64222-140">筆記</span><span class="sxs-lookup"><span data-stu-id="64222-140">NOTES</span></span>

## <span data-ttu-id="64222-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="64222-141">RELATED LINKS</span></span>

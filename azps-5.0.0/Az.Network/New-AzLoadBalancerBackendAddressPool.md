---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139705"
---
# <span data-ttu-id="97de7-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97de7-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="97de7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97de7-102">SYNOPSIS</span></span>
<span data-ttu-id="97de7-103">在 loadbalancer 上建立後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="97de7-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="97de7-104">句法</span><span class="sxs-lookup"><span data-stu-id="97de7-104">SYNTAX</span></span>

### <span data-ttu-id="97de7-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97de7-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97de7-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97de7-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97de7-107">說明</span><span class="sxs-lookup"><span data-stu-id="97de7-107">DESCRIPTION</span></span>
<span data-ttu-id="97de7-108">在 loadbalancer 上建立後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="97de7-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="97de7-109">允許 specifiying PSLoadBalancerBackendAddress 的陣列。</span><span class="sxs-lookup"><span data-stu-id="97de7-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="97de7-110">示例</span><span class="sxs-lookup"><span data-stu-id="97de7-110">EXAMPLES</span></span>

### <span data-ttu-id="97de7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="97de7-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="97de7-112">範例2</span><span class="sxs-lookup"><span data-stu-id="97de7-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="97de7-113">範例3</span><span class="sxs-lookup"><span data-stu-id="97de7-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="97de7-114">範例4</span><span class="sxs-lookup"><span data-stu-id="97de7-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="97de7-115">參數</span><span class="sxs-lookup"><span data-stu-id="97de7-115">PARAMETERS</span></span>

### <span data-ttu-id="97de7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97de7-116">-DefaultProfile</span></span>
<span data-ttu-id="97de7-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97de7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97de7-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97de7-118">-LoadBalancer</span></span>
<span data-ttu-id="97de7-119">負載平衡器資源。</span><span class="sxs-lookup"><span data-stu-id="97de7-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="97de7-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="97de7-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="97de7-121">後端位址。</span><span class="sxs-lookup"><span data-stu-id="97de7-121">The backend addresses.</span></span>

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

### <span data-ttu-id="97de7-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="97de7-122">-LoadBalancerName</span></span>
<span data-ttu-id="97de7-123">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="97de7-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="97de7-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="97de7-124">-Name</span></span>
<span data-ttu-id="97de7-125">後端池的名稱。</span><span class="sxs-lookup"><span data-stu-id="97de7-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="97de7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97de7-126">-ResourceGroupName</span></span>
<span data-ttu-id="97de7-127">負載平衡器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="97de7-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="97de7-128">-確認</span><span class="sxs-lookup"><span data-stu-id="97de7-128">-Confirm</span></span>
<span data-ttu-id="97de7-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97de7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97de7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97de7-130">-WhatIf</span></span>
<span data-ttu-id="97de7-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97de7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97de7-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97de7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97de7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97de7-133">CommonParameters</span></span>
<span data-ttu-id="97de7-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97de7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97de7-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="97de7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97de7-136">輸入</span><span class="sxs-lookup"><span data-stu-id="97de7-136">INPUTS</span></span>

### <span data-ttu-id="97de7-137">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97de7-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="97de7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="97de7-138">OUTPUTS</span></span>

### <span data-ttu-id="97de7-139">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97de7-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="97de7-140">筆記</span><span class="sxs-lookup"><span data-stu-id="97de7-140">NOTES</span></span>

## <span data-ttu-id="97de7-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="97de7-141">RELATED LINKS</span></span>

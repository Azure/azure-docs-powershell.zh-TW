---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 783eb017f336cd587f51f286cad296c267e6b68c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913821"
---
# <span data-ttu-id="d93c6-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d93c6-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="d93c6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d93c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d93c6-103">在負載平衡器上建立後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="d93c6-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="d93c6-104">語法</span><span class="sxs-lookup"><span data-stu-id="d93c6-104">SYNTAX</span></span>

### <span data-ttu-id="d93c6-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93c6-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93c6-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93c6-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d93c6-107">描述</span><span class="sxs-lookup"><span data-stu-id="d93c6-107">DESCRIPTION</span></span>
<span data-ttu-id="d93c6-108">在負載平衡器上建立後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="d93c6-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="d93c6-109">允許指定 PSLoadBalancerBackendAddress 陣列。</span><span class="sxs-lookup"><span data-stu-id="d93c6-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="d93c6-110">例子</span><span class="sxs-lookup"><span data-stu-id="d93c6-110">EXAMPLES</span></span>

### <span data-ttu-id="d93c6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d93c6-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="d93c6-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="d93c6-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="d93c6-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="d93c6-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="d93c6-114">範例 4</span><span class="sxs-lookup"><span data-stu-id="d93c6-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="d93c6-115">參數</span><span class="sxs-lookup"><span data-stu-id="d93c6-115">PARAMETERS</span></span>

### <span data-ttu-id="d93c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93c6-116">-DefaultProfile</span></span>
<span data-ttu-id="d93c6-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d93c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d93c6-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d93c6-118">-LoadBalancer</span></span>
<span data-ttu-id="d93c6-119">負載平衡器資源。</span><span class="sxs-lookup"><span data-stu-id="d93c6-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="d93c6-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="d93c6-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="d93c6-121">後端位址。</span><span class="sxs-lookup"><span data-stu-id="d93c6-121">The backend addresses.</span></span>

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

### <span data-ttu-id="d93c6-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="d93c6-122">-LoadBalancerName</span></span>
<span data-ttu-id="d93c6-123">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d93c6-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="d93c6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d93c6-124">-Name</span></span>
<span data-ttu-id="d93c6-125">後端資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d93c6-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="d93c6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d93c6-126">-ResourceGroupName</span></span>
<span data-ttu-id="d93c6-127">負載平衡器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d93c6-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="d93c6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d93c6-128">-Confirm</span></span>
<span data-ttu-id="d93c6-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d93c6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d93c6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d93c6-130">-WhatIf</span></span>
<span data-ttu-id="d93c6-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d93c6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d93c6-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d93c6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d93c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93c6-133">CommonParameters</span></span>
<span data-ttu-id="d93c6-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d93c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93c6-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d93c6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93c6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d93c6-136">INPUTS</span></span>

### <span data-ttu-id="d93c6-137">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d93c6-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d93c6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d93c6-138">OUTPUTS</span></span>

### <span data-ttu-id="d93c6-139">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d93c6-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="d93c6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d93c6-140">NOTES</span></span>

## <span data-ttu-id="d93c6-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d93c6-141">RELATED LINKS</span></span>

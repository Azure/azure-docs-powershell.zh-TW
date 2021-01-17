---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450137"
---
# <span data-ttu-id="baa77-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="baa77-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="baa77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="baa77-102">SYNOPSIS</span></span>
<span data-ttu-id="baa77-103">更新 loadbalancer 上的後端池</span><span class="sxs-lookup"><span data-stu-id="baa77-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="baa77-104">句法</span><span class="sxs-lookup"><span data-stu-id="baa77-104">SYNTAX</span></span>

### <span data-ttu-id="baa77-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="baa77-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa77-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baa77-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa77-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baa77-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa77-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="baa77-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="baa77-109">說明</span><span class="sxs-lookup"><span data-stu-id="baa77-109">DESCRIPTION</span></span>
<span data-ttu-id="baa77-110">更新 loadbalancer 上的後端池</span><span class="sxs-lookup"><span data-stu-id="baa77-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="baa77-111">示例</span><span class="sxs-lookup"><span data-stu-id="baa77-111">EXAMPLES</span></span>

### <span data-ttu-id="baa77-112">範例1</span><span class="sxs-lookup"><span data-stu-id="baa77-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="baa77-113">範例2</span><span class="sxs-lookup"><span data-stu-id="baa77-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="baa77-114">範例3</span><span class="sxs-lookup"><span data-stu-id="baa77-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="baa77-115">參數</span><span class="sxs-lookup"><span data-stu-id="baa77-115">PARAMETERS</span></span>

### <span data-ttu-id="baa77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa77-116">-DefaultProfile</span></span>
<span data-ttu-id="baa77-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="baa77-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa77-118">-Force</span><span class="sxs-lookup"><span data-stu-id="baa77-118">-Force</span></span>
<span data-ttu-id="baa77-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="baa77-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baa77-120">-InputObject</span></span>
<span data-ttu-id="baa77-121">要設定的後端位址集區</span><span class="sxs-lookup"><span data-stu-id="baa77-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="baa77-122">-LoadBalancer</span></span>
<span data-ttu-id="baa77-123">負載平衡器資源。</span><span class="sxs-lookup"><span data-stu-id="baa77-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="baa77-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="baa77-125">後端位址。</span><span class="sxs-lookup"><span data-stu-id="baa77-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="baa77-126">-LoadBalancerName</span></span>
<span data-ttu-id="baa77-127">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="baa77-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="baa77-128">-Name</span></span>
<span data-ttu-id="baa77-129">後端池的名稱。</span><span class="sxs-lookup"><span data-stu-id="baa77-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="baa77-130">-PassThru</span></span>
<span data-ttu-id="baa77-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="baa77-131">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa77-132">-ResourceGroupName</span></span>
<span data-ttu-id="baa77-133">負載平衡器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="baa77-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="baa77-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-135">-確認</span><span class="sxs-lookup"><span data-stu-id="baa77-135">-Confirm</span></span>
<span data-ttu-id="baa77-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="baa77-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baa77-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa77-137">-WhatIf</span></span>
<span data-ttu-id="baa77-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="baa77-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baa77-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="baa77-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baa77-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa77-140">CommonParameters</span></span>
<span data-ttu-id="baa77-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="baa77-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa77-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="baa77-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa77-143">輸入</span><span class="sxs-lookup"><span data-stu-id="baa77-143">INPUTS</span></span>

### <span data-ttu-id="baa77-144">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="baa77-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="baa77-145">System.object</span><span class="sxs-lookup"><span data-stu-id="baa77-145">System.String</span></span>

## <span data-ttu-id="baa77-146">輸出</span><span class="sxs-lookup"><span data-stu-id="baa77-146">OUTPUTS</span></span>

### <span data-ttu-id="baa77-147">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="baa77-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="baa77-148">筆記</span><span class="sxs-lookup"><span data-stu-id="baa77-148">NOTES</span></span>

## <span data-ttu-id="baa77-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="baa77-149">RELATED LINKS</span></span>

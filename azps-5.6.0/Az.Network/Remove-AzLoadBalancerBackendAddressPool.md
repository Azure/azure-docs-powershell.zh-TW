---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 6e12cc4bb296a1c523547aebc44c6992dd2b687e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912681"
---
# <span data-ttu-id="01937-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="01937-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="01937-102">簡介</span><span class="sxs-lookup"><span data-stu-id="01937-102">SYNOPSIS</span></span>
<span data-ttu-id="01937-103">從負載平衡器移除後端資料庫</span><span class="sxs-lookup"><span data-stu-id="01937-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="01937-104">語法</span><span class="sxs-lookup"><span data-stu-id="01937-104">SYNTAX</span></span>

### <span data-ttu-id="01937-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="01937-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01937-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01937-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01937-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01937-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01937-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01937-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01937-109">描述</span><span class="sxs-lookup"><span data-stu-id="01937-109">DESCRIPTION</span></span>
<span data-ttu-id="01937-110">從負載平衡器移除後端資料庫</span><span class="sxs-lookup"><span data-stu-id="01937-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="01937-111">例子</span><span class="sxs-lookup"><span data-stu-id="01937-111">EXAMPLES</span></span>

### <span data-ttu-id="01937-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="01937-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="01937-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="01937-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="01937-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="01937-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="01937-115">參數</span><span class="sxs-lookup"><span data-stu-id="01937-115">PARAMETERS</span></span>

### <span data-ttu-id="01937-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01937-116">-DefaultProfile</span></span>
<span data-ttu-id="01937-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="01937-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01937-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01937-118">-InputObject</span></span>
<span data-ttu-id="01937-119">要移除的後端位址資料庫</span><span class="sxs-lookup"><span data-stu-id="01937-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01937-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="01937-120">-LoadBalancer</span></span>
<span data-ttu-id="01937-121">負載平衡器資源。</span><span class="sxs-lookup"><span data-stu-id="01937-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01937-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="01937-122">-LoadBalancerName</span></span>
<span data-ttu-id="01937-123">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="01937-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01937-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="01937-124">-Name</span></span>
<span data-ttu-id="01937-125">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="01937-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01937-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01937-126">-PassThru</span></span>
<span data-ttu-id="01937-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="01937-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="01937-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01937-128">-ResourceGroupName</span></span>
<span data-ttu-id="01937-129">負載平衡器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="01937-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01937-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01937-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01937-131">-確認</span><span class="sxs-lookup"><span data-stu-id="01937-131">-Confirm</span></span>
<span data-ttu-id="01937-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="01937-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01937-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01937-133">-WhatIf</span></span>
<span data-ttu-id="01937-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01937-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01937-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01937-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01937-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01937-136">CommonParameters</span></span>
<span data-ttu-id="01937-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="01937-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01937-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01937-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01937-139">輸入</span><span class="sxs-lookup"><span data-stu-id="01937-139">INPUTS</span></span>

### <span data-ttu-id="01937-140">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="01937-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="01937-141">System.String</span><span class="sxs-lookup"><span data-stu-id="01937-141">System.String</span></span>

## <span data-ttu-id="01937-142">輸出</span><span class="sxs-lookup"><span data-stu-id="01937-142">OUTPUTS</span></span>

### <span data-ttu-id="01937-143">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="01937-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="01937-144">筆記</span><span class="sxs-lookup"><span data-stu-id="01937-144">NOTES</span></span>

## <span data-ttu-id="01937-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="01937-145">RELATED LINKS</span></span>

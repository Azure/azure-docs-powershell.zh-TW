---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273016"
---
# <span data-ttu-id="f674b-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f674b-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="f674b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f674b-102">SYNOPSIS</span></span>
<span data-ttu-id="f674b-103">從負載平衡器移除後端池</span><span class="sxs-lookup"><span data-stu-id="f674b-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="f674b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f674b-104">SYNTAX</span></span>

### <span data-ttu-id="f674b-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f674b-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f674b-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f674b-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f674b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f674b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f674b-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f674b-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f674b-109">說明</span><span class="sxs-lookup"><span data-stu-id="f674b-109">DESCRIPTION</span></span>
<span data-ttu-id="f674b-110">從負載平衡器移除後端池</span><span class="sxs-lookup"><span data-stu-id="f674b-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="f674b-111">示例</span><span class="sxs-lookup"><span data-stu-id="f674b-111">EXAMPLES</span></span>

### <span data-ttu-id="f674b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f674b-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="f674b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f674b-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="f674b-114">範例3</span><span class="sxs-lookup"><span data-stu-id="f674b-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="f674b-115">參數</span><span class="sxs-lookup"><span data-stu-id="f674b-115">PARAMETERS</span></span>

### <span data-ttu-id="f674b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f674b-116">-DefaultProfile</span></span>
<span data-ttu-id="f674b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f674b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f674b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f674b-118">-InputObject</span></span>
<span data-ttu-id="f674b-119">要移除的後端位址集區</span><span class="sxs-lookup"><span data-stu-id="f674b-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="f674b-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f674b-120">-LoadBalancer</span></span>
<span data-ttu-id="f674b-121">負載平衡器資源。</span><span class="sxs-lookup"><span data-stu-id="f674b-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="f674b-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="f674b-122">-LoadBalancerName</span></span>
<span data-ttu-id="f674b-123">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f674b-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="f674b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f674b-124">-Name</span></span>
<span data-ttu-id="f674b-125">負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f674b-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="f674b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f674b-126">-PassThru</span></span>
<span data-ttu-id="f674b-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="f674b-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f674b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f674b-128">-ResourceGroupName</span></span>
<span data-ttu-id="f674b-129">負載平衡器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f674b-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="f674b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f674b-130">-ResourceId</span></span>

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

### <span data-ttu-id="f674b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f674b-131">-Confirm</span></span>
<span data-ttu-id="f674b-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f674b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f674b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f674b-133">-WhatIf</span></span>
<span data-ttu-id="f674b-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f674b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f674b-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f674b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f674b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f674b-136">CommonParameters</span></span>
<span data-ttu-id="f674b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f674b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f674b-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f674b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f674b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f674b-139">INPUTS</span></span>

### <span data-ttu-id="f674b-140">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f674b-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f674b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f674b-141">System.String</span></span>

## <span data-ttu-id="f674b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f674b-142">OUTPUTS</span></span>

### <span data-ttu-id="f674b-143">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f674b-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f674b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f674b-144">NOTES</span></span>

## <span data-ttu-id="f674b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f674b-145">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138158"
---
# <span data-ttu-id="522ee-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="522ee-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="522ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="522ee-102">SYNOPSIS</span></span>
<span data-ttu-id="522ee-103">針對節點類型的特定 ndes 設定 [節點類型] 資源屬性或執行重新鏡像動作（含重新鏡像參數）。</span><span class="sxs-lookup"><span data-stu-id="522ee-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="522ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="522ee-104">SYNTAX</span></span>

### <span data-ttu-id="522ee-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="522ee-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522ee-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="522ee-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="522ee-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="522ee-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522ee-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="522ee-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522ee-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="522ee-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522ee-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="522ee-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="522ee-111">說明</span><span class="sxs-lookup"><span data-stu-id="522ee-111">DESCRIPTION</span></span>
<span data-ttu-id="522ee-112">針對節點類型的特定 ndes 設定 [節點類型] 資源屬性或執行重新鏡像動作（含重新鏡像參數）。</span><span class="sxs-lookup"><span data-stu-id="522ee-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="522ee-113">在 reimgae 操作中，服務結構節點會在重新建立 vm 之前停用，然後在它們返回之後再次啟用。</span><span class="sxs-lookup"><span data-stu-id="522ee-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="522ee-114">如果這是在主要節點類型上完成，可能需要一段時間，因為它可能不會同時重新鏡像所有節點。</span><span class="sxs-lookup"><span data-stu-id="522ee-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="522ee-115">Use-ForceReimage 會強制執行作業，即使服務結構無法停用節點，但使用時請小心，因為如果狀態工作負荷在節點上執行，可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="522ee-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="522ee-116">示例</span><span class="sxs-lookup"><span data-stu-id="522ee-116">EXAMPLES</span></span>

### <span data-ttu-id="522ee-117">範例1</span><span class="sxs-lookup"><span data-stu-id="522ee-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="522ee-118">更新節點類型的實例計數。</span><span class="sxs-lookup"><span data-stu-id="522ee-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="522ee-119">範例2</span><span class="sxs-lookup"><span data-stu-id="522ee-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="522ee-120">更新節點類型的放置 properites。</span><span class="sxs-lookup"><span data-stu-id="522ee-120">Update placement properites of the node type.</span></span> <span data-ttu-id="522ee-121">這會覆寫較舊的位置 properites （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="522ee-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="522ee-122">範例3</span><span class="sxs-lookup"><span data-stu-id="522ee-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="522ee-123">重新鏡像節點類型上的節點0和3。</span><span class="sxs-lookup"><span data-stu-id="522ee-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="522ee-124">範例4</span><span class="sxs-lookup"><span data-stu-id="522ee-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="522ee-125">使用管道來更新節點類型的實例計數。</span><span class="sxs-lookup"><span data-stu-id="522ee-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="522ee-126">參數</span><span class="sxs-lookup"><span data-stu-id="522ee-126">PARAMETERS</span></span>

### <span data-ttu-id="522ee-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="522ee-127">-ApplicationEndPort</span></span>
<span data-ttu-id="522ee-128">埠範圍的應用程式結束埠。</span><span class="sxs-lookup"><span data-stu-id="522ee-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="522ee-129">-ApplicationStartPort</span></span>
<span data-ttu-id="522ee-130">埠範圍的應用程式啟動埠。</span><span class="sxs-lookup"><span data-stu-id="522ee-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="522ee-131">-AsJob</span></span>
<span data-ttu-id="522ee-132">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="522ee-132">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-133">-容量</span><span class="sxs-lookup"><span data-stu-id="522ee-133">-Capacity</span></span>
<span data-ttu-id="522ee-134">針對節點類型中的節點套用的容量標籤是鍵/值對，而 [群集資源管理器] 會使用這些標籤來瞭解節點擁有的資源數量。</span><span class="sxs-lookup"><span data-stu-id="522ee-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="522ee-135">更新這將會覆寫目前的值。</span><span class="sxs-lookup"><span data-stu-id="522ee-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="522ee-136">-ClusterName</span></span>
<span data-ttu-id="522ee-137">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="522ee-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522ee-138">-DefaultProfile</span></span>
<span data-ttu-id="522ee-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="522ee-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="522ee-140">-EphemeralEndPort</span></span>
<span data-ttu-id="522ee-141">埠範圍的暫時結束埠。</span><span class="sxs-lookup"><span data-stu-id="522ee-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="522ee-142">-EphemeralStartPort</span></span>
<span data-ttu-id="522ee-143">埠範圍的暫時啟動埠。</span><span class="sxs-lookup"><span data-stu-id="522ee-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="522ee-144">-ForceReimage</span></span>
<span data-ttu-id="522ee-145">即使服務結構無法停用節點，使用這個標誌也會強制移除。</span><span class="sxs-lookup"><span data-stu-id="522ee-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="522ee-146">請謹慎使用，因為如果狀態工作負載是在節點上執行，這可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="522ee-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="522ee-147">-InputObject</span></span>
<span data-ttu-id="522ee-148">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="522ee-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="522ee-149">-InstanceCount</span></span>
<span data-ttu-id="522ee-150">節點類型中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="522ee-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="522ee-151">-Name</span></span>
<span data-ttu-id="522ee-152">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="522ee-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="522ee-153">-NodeName</span></span>
<span data-ttu-id="522ee-154">操作的節點名稱清單。</span><span class="sxs-lookup"><span data-stu-id="522ee-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="522ee-155">-PassThru</span></span>
<span data-ttu-id="522ee-156">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="522ee-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="522ee-157">-PlacementProperty</span></span>
<span data-ttu-id="522ee-158">將位置標記套用至節點類型中的節點做為索引鍵/值組，可以用來指出特定服務 (工作負荷) 應該如何執行。</span><span class="sxs-lookup"><span data-stu-id="522ee-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="522ee-159">更新這將會覆寫目前的值。</span><span class="sxs-lookup"><span data-stu-id="522ee-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-160">-重新映射</span><span class="sxs-lookup"><span data-stu-id="522ee-160">-Reimage</span></span>
<span data-ttu-id="522ee-161">指定要重新鏡像節點類型上的節點。</span><span class="sxs-lookup"><span data-stu-id="522ee-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="522ee-162">-ResourceGroupName</span></span>
<span data-ttu-id="522ee-163">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="522ee-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="522ee-164">-ResourceId</span></span>
<span data-ttu-id="522ee-165">節點類型資源識別碼</span><span class="sxs-lookup"><span data-stu-id="522ee-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="522ee-166">-確認</span><span class="sxs-lookup"><span data-stu-id="522ee-166">-Confirm</span></span>
<span data-ttu-id="522ee-167">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="522ee-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="522ee-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="522ee-168">-WhatIf</span></span>
<span data-ttu-id="522ee-169">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="522ee-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="522ee-170">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="522ee-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="522ee-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522ee-171">CommonParameters</span></span>
<span data-ttu-id="522ee-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="522ee-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522ee-173">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="522ee-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522ee-174">輸入</span><span class="sxs-lookup"><span data-stu-id="522ee-174">INPUTS</span></span>

### <span data-ttu-id="522ee-175">System.object</span><span class="sxs-lookup"><span data-stu-id="522ee-175">System.String</span></span>

## <span data-ttu-id="522ee-176">輸出</span><span class="sxs-lookup"><span data-stu-id="522ee-176">OUTPUTS</span></span>

### <span data-ttu-id="522ee-177">System.object</span><span class="sxs-lookup"><span data-stu-id="522ee-177">System.Boolean</span></span>

## <span data-ttu-id="522ee-178">筆記</span><span class="sxs-lookup"><span data-stu-id="522ee-178">NOTES</span></span>

## <span data-ttu-id="522ee-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="522ee-179">RELATED LINKS</span></span>

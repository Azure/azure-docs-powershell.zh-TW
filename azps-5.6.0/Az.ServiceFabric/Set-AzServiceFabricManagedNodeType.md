---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3f3f19f88ffdd37cbad009950c064e672e186b34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908006"
---
# <span data-ttu-id="2628d-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2628d-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="2628d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2628d-102">SYNOPSIS</span></span>
<span data-ttu-id="2628d-103">使用 -Reimage 參數設定節點類型資源屬性，或在節點類型的特定數個數上執行重新映射動作。</span><span class="sxs-lookup"><span data-stu-id="2628d-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="2628d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2628d-104">SYNTAX</span></span>

### <span data-ttu-id="2628d-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="2628d-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2628d-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="2628d-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2628d-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="2628d-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2628d-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="2628d-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2628d-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="2628d-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2628d-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="2628d-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2628d-111">描述</span><span class="sxs-lookup"><span data-stu-id="2628d-111">DESCRIPTION</span></span>
<span data-ttu-id="2628d-112">使用 -Reimage 參數設定節點類型資源屬性，或在節點類型的特定數個數上執行重新映射動作。</span><span class="sxs-lookup"><span data-stu-id="2628d-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="2628d-113">重新映射作業時，服務布節點會先停用，然後再重新為 vm 重新製作成動畫，並再次啟用它們一旦恢復使用。</span><span class="sxs-lookup"><span data-stu-id="2628d-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="2628d-114">如果是在主要節點類型上完成此工作，可能需要一些時間，因為可能不會同時重新製作所有節點的映射。</span><span class="sxs-lookup"><span data-stu-id="2628d-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="2628d-115">即使服務結構無法停用節點，使用 -ForceReimage 還是會強制執行作業，但請小心使用，因為如果節點上執行有狀態的工作量，可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="2628d-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="2628d-116">例子</span><span class="sxs-lookup"><span data-stu-id="2628d-116">EXAMPLES</span></span>

### <span data-ttu-id="2628d-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="2628d-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="2628d-118">更新節點類型的實例計數。</span><span class="sxs-lookup"><span data-stu-id="2628d-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="2628d-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="2628d-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="2628d-120">更新節點類型的位置適當位置。</span><span class="sxs-lookup"><span data-stu-id="2628d-120">Update placement properites of the node type.</span></span> <span data-ttu-id="2628d-121">這將會覆寫較舊的放置適當位置 ，如果有。</span><span class="sxs-lookup"><span data-stu-id="2628d-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="2628d-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="2628d-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="2628d-123">重新映射節點類型上的節點 0 和 3。</span><span class="sxs-lookup"><span data-stu-id="2628d-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="2628d-124">範例 4</span><span class="sxs-lookup"><span data-stu-id="2628d-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="2628d-125">使用管線更新節點類型的實例計數。</span><span class="sxs-lookup"><span data-stu-id="2628d-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="2628d-126">參數</span><span class="sxs-lookup"><span data-stu-id="2628d-126">PARAMETERS</span></span>

### <span data-ttu-id="2628d-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="2628d-127">-ApplicationEndPort</span></span>
<span data-ttu-id="2628d-128">埠範圍的應用程式結束埠。</span><span class="sxs-lookup"><span data-stu-id="2628d-128">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="2628d-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="2628d-129">-ApplicationStartPort</span></span>
<span data-ttu-id="2628d-130">一系列埠的應用程式啟動埠。</span><span class="sxs-lookup"><span data-stu-id="2628d-130">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="2628d-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2628d-131">-AsJob</span></span>
<span data-ttu-id="2628d-132">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="2628d-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2628d-133">-容量</span><span class="sxs-lookup"><span data-stu-id="2628d-133">-Capacity</span></span>
<span data-ttu-id="2628d-134">將節點類型中的節點所使用容量標記當做金鑰/值組時，集區資源管理員會使用這些標記來瞭解節點有多少資源。</span><span class="sxs-lookup"><span data-stu-id="2628d-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="2628d-135">更新此選項會優先于目前的值。</span><span class="sxs-lookup"><span data-stu-id="2628d-135">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="2628d-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2628d-136">-ClusterName</span></span>
<span data-ttu-id="2628d-137">指定組名。</span><span class="sxs-lookup"><span data-stu-id="2628d-137">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2628d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2628d-138">-DefaultProfile</span></span>
<span data-ttu-id="2628d-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2628d-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2628d-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="2628d-140">-EphemeralEndPort</span></span>
<span data-ttu-id="2628d-141">一系列埠的暫時結束埠。</span><span class="sxs-lookup"><span data-stu-id="2628d-141">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="2628d-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="2628d-142">-EphemeralStartPort</span></span>
<span data-ttu-id="2628d-143">一系列埠的暫時啟動埠。</span><span class="sxs-lookup"><span data-stu-id="2628d-143">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="2628d-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="2628d-144">-ForceReimage</span></span>
<span data-ttu-id="2628d-145">使用此旗標會強制移除，即使服務結構無法停用節點。</span><span class="sxs-lookup"><span data-stu-id="2628d-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="2628d-146">請小心使用，如果節點上執行狀態工作負載，可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="2628d-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

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

### <span data-ttu-id="2628d-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2628d-147">-InputObject</span></span>
<span data-ttu-id="2628d-148">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="2628d-148">Node type resource</span></span>

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

### <span data-ttu-id="2628d-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="2628d-149">-InstanceCount</span></span>
<span data-ttu-id="2628d-150">節點類型的節點數目。</span><span class="sxs-lookup"><span data-stu-id="2628d-150">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="2628d-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="2628d-151">-Name</span></span>
<span data-ttu-id="2628d-152">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="2628d-152">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="2628d-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="2628d-153">-NodeName</span></span>
<span data-ttu-id="2628d-154">作業的節點名稱清單。</span><span class="sxs-lookup"><span data-stu-id="2628d-154">List of node names for the operation.</span></span>

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

### <span data-ttu-id="2628d-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2628d-155">-PassThru</span></span>
<span data-ttu-id="2628d-156">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2628d-156">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2628d-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="2628d-157">-PlacementProperty</span></span>
<span data-ttu-id="2628d-158">在節點類型中，將節點所使用的位置標記當做金鑰/值組，可用來指出應在何處執行特定服務 (工作負載) 位置。</span><span class="sxs-lookup"><span data-stu-id="2628d-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="2628d-159">更新此選項會優先于目前的值。</span><span class="sxs-lookup"><span data-stu-id="2628d-159">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="2628d-160">-重新映射</span><span class="sxs-lookup"><span data-stu-id="2628d-160">-Reimage</span></span>
<span data-ttu-id="2628d-161">指定為節點類型上的節點重新製作動畫。</span><span class="sxs-lookup"><span data-stu-id="2628d-161">Specify to reimage nodes on the node type.</span></span>

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

### <span data-ttu-id="2628d-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2628d-162">-ResourceGroupName</span></span>
<span data-ttu-id="2628d-163">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2628d-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2628d-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2628d-164">-ResourceId</span></span>
<span data-ttu-id="2628d-165">節點類型資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2628d-165">Node type resource id</span></span>

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

### <span data-ttu-id="2628d-166">-確認</span><span class="sxs-lookup"><span data-stu-id="2628d-166">-Confirm</span></span>
<span data-ttu-id="2628d-167">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2628d-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2628d-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2628d-168">-WhatIf</span></span>
<span data-ttu-id="2628d-169">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2628d-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2628d-170">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2628d-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2628d-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2628d-171">CommonParameters</span></span>
<span data-ttu-id="2628d-172">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2628d-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2628d-173">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2628d-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2628d-174">輸入</span><span class="sxs-lookup"><span data-stu-id="2628d-174">INPUTS</span></span>

### <span data-ttu-id="2628d-175">System.String</span><span class="sxs-lookup"><span data-stu-id="2628d-175">System.String</span></span>

## <span data-ttu-id="2628d-176">輸出</span><span class="sxs-lookup"><span data-stu-id="2628d-176">OUTPUTS</span></span>

### <span data-ttu-id="2628d-177">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2628d-177">System.Boolean</span></span>

## <span data-ttu-id="2628d-178">筆記</span><span class="sxs-lookup"><span data-stu-id="2628d-178">NOTES</span></span>

## <span data-ttu-id="2628d-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="2628d-179">RELATED LINKS</span></span>

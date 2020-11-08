---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129248"
---
# <span data-ttu-id="92977-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="92977-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="92977-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92977-102">SYNOPSIS</span></span>
<span data-ttu-id="92977-103">移除節點類型或節點類型中的特定節點。</span><span class="sxs-lookup"><span data-stu-id="92977-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="92977-104">句法</span><span class="sxs-lookup"><span data-stu-id="92977-104">SYNTAX</span></span>

### <span data-ttu-id="92977-105">DeleteNodeTypeByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="92977-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92977-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="92977-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92977-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="92977-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92977-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="92977-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92977-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="92977-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92977-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="92977-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92977-111">說明</span><span class="sxs-lookup"><span data-stu-id="92977-111">DESCRIPTION</span></span>
<span data-ttu-id="92977-112">移除節點類型或節點類型中的特定節點。</span><span class="sxs-lookup"><span data-stu-id="92977-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="92977-113">如果使用 paremter-NodeName，則只會移除指定的節點。</span><span class="sxs-lookup"><span data-stu-id="92977-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="92977-114">示例</span><span class="sxs-lookup"><span data-stu-id="92977-114">EXAMPLES</span></span>

### <span data-ttu-id="92977-115">範例1</span><span class="sxs-lookup"><span data-stu-id="92977-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="92977-116">移除節點類型。</span><span class="sxs-lookup"><span data-stu-id="92977-116">Remove node type.</span></span>

### <span data-ttu-id="92977-117">範例2</span><span class="sxs-lookup"><span data-stu-id="92977-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="92977-118">使用管道移除節點類型。</span><span class="sxs-lookup"><span data-stu-id="92977-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="92977-119">範例3</span><span class="sxs-lookup"><span data-stu-id="92977-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="92977-120">從節點類型移除2個節點。</span><span class="sxs-lookup"><span data-stu-id="92977-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="92977-121">範例4</span><span class="sxs-lookup"><span data-stu-id="92977-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="92977-122">使用管道從節點類型移除2個節點。</span><span class="sxs-lookup"><span data-stu-id="92977-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="92977-123">參數</span><span class="sxs-lookup"><span data-stu-id="92977-123">PARAMETERS</span></span>

### <span data-ttu-id="92977-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92977-124">-AsJob</span></span>
<span data-ttu-id="92977-125">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="92977-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="92977-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="92977-126">-ClusterName</span></span>
<span data-ttu-id="92977-127">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="92977-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92977-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92977-128">-DefaultProfile</span></span>
<span data-ttu-id="92977-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92977-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92977-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="92977-130">-ForceRemoveNode</span></span>
<span data-ttu-id="92977-131">即使服務結構無法停用節點，使用這個標誌也會強制移除。</span><span class="sxs-lookup"><span data-stu-id="92977-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="92977-132">謹慎使用：如果在節點上執行狀態工作負荷，可能會導致資料遺失，或者，如果 opearion 之後沒有足夠的種子節點，也可能會將群集移到最下層。</span><span class="sxs-lookup"><span data-stu-id="92977-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92977-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92977-133">-InputObject</span></span>
<span data-ttu-id="92977-134">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="92977-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92977-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="92977-135">-Name</span></span>
<span data-ttu-id="92977-136">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="92977-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92977-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="92977-137">-NodeName</span></span>
<span data-ttu-id="92977-138">操作的節點名稱清單。</span><span class="sxs-lookup"><span data-stu-id="92977-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92977-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92977-139">-PassThru</span></span>
<span data-ttu-id="92977-140">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="92977-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="92977-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92977-141">-ResourceGroupName</span></span>
<span data-ttu-id="92977-142">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92977-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92977-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92977-143">-ResourceId</span></span>
<span data-ttu-id="92977-144">節點類型資源識別碼</span><span class="sxs-lookup"><span data-stu-id="92977-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92977-145">-確認</span><span class="sxs-lookup"><span data-stu-id="92977-145">-Confirm</span></span>
<span data-ttu-id="92977-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92977-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92977-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92977-147">-WhatIf</span></span>
<span data-ttu-id="92977-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92977-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92977-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92977-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92977-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92977-150">CommonParameters</span></span>
<span data-ttu-id="92977-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92977-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92977-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="92977-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92977-153">輸入</span><span class="sxs-lookup"><span data-stu-id="92977-153">INPUTS</span></span>

### <span data-ttu-id="92977-154">System.object</span><span class="sxs-lookup"><span data-stu-id="92977-154">System.String</span></span>

## <span data-ttu-id="92977-155">輸出</span><span class="sxs-lookup"><span data-stu-id="92977-155">OUTPUTS</span></span>

### <span data-ttu-id="92977-156">System.object</span><span class="sxs-lookup"><span data-stu-id="92977-156">System.Boolean</span></span>

## <span data-ttu-id="92977-157">筆記</span><span class="sxs-lookup"><span data-stu-id="92977-157">NOTES</span></span>

## <span data-ttu-id="92977-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="92977-158">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5cb0e5bf8dce38a8552514835d2e16d19c3cc833
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915822"
---
# <span data-ttu-id="f7e33-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f7e33-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="f7e33-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7e33-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e33-103">移除節點類型或節點類型中的特定節點。</span><span class="sxs-lookup"><span data-stu-id="f7e33-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="f7e33-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7e33-104">SYNTAX</span></span>

### <span data-ttu-id="f7e33-105">DeleteNodeTypeByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="f7e33-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7e33-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="f7e33-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7e33-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="f7e33-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7e33-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="f7e33-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7e33-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="f7e33-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7e33-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="f7e33-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7e33-111">描述</span><span class="sxs-lookup"><span data-stu-id="f7e33-111">DESCRIPTION</span></span>
<span data-ttu-id="f7e33-112">移除節點類型或節點類型中的特定節點。</span><span class="sxs-lookup"><span data-stu-id="f7e33-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="f7e33-113">如果使用 paremter -NodeName，則只會移除指定的節點。</span><span class="sxs-lookup"><span data-stu-id="f7e33-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="f7e33-114">例子</span><span class="sxs-lookup"><span data-stu-id="f7e33-114">EXAMPLES</span></span>

### <span data-ttu-id="f7e33-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="f7e33-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="f7e33-116">移除節點類型。</span><span class="sxs-lookup"><span data-stu-id="f7e33-116">Remove node type.</span></span>

### <span data-ttu-id="f7e33-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="f7e33-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="f7e33-118">移除節點類型，包含管線。</span><span class="sxs-lookup"><span data-stu-id="f7e33-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="f7e33-119">範例 3</span><span class="sxs-lookup"><span data-stu-id="f7e33-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="f7e33-120">從節點類型移除 2 個節點。</span><span class="sxs-lookup"><span data-stu-id="f7e33-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="f7e33-121">範例 4</span><span class="sxs-lookup"><span data-stu-id="f7e33-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="f7e33-122">使用管線從節點類型移除 2 個節點。</span><span class="sxs-lookup"><span data-stu-id="f7e33-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="f7e33-123">參數</span><span class="sxs-lookup"><span data-stu-id="f7e33-123">PARAMETERS</span></span>

### <span data-ttu-id="f7e33-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7e33-124">-AsJob</span></span>
<span data-ttu-id="f7e33-125">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="f7e33-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f7e33-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f7e33-126">-ClusterName</span></span>
<span data-ttu-id="f7e33-127">指定組名。</span><span class="sxs-lookup"><span data-stu-id="f7e33-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f7e33-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e33-128">-DefaultProfile</span></span>
<span data-ttu-id="f7e33-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7e33-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7e33-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="f7e33-130">-ForceRemoveNode</span></span>
<span data-ttu-id="f7e33-131">使用此旗標會強制移除，即使服務結構無法停用節點。</span><span class="sxs-lookup"><span data-stu-id="f7e33-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="f7e33-132">請小心使用，如果節點上執行有狀態的工作量，可能會導致資料遺失，或如果執行之後沒有足夠的子節點，可能會導致該組組降低。</span><span class="sxs-lookup"><span data-stu-id="f7e33-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="f7e33-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7e33-133">-InputObject</span></span>
<span data-ttu-id="f7e33-134">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="f7e33-134">Node type resource</span></span>

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

### <span data-ttu-id="f7e33-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7e33-135">-Name</span></span>
<span data-ttu-id="f7e33-136">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e33-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="f7e33-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="f7e33-137">-NodeName</span></span>
<span data-ttu-id="f7e33-138">作業的節點名稱清單。</span><span class="sxs-lookup"><span data-stu-id="f7e33-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="f7e33-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7e33-139">-PassThru</span></span>
<span data-ttu-id="f7e33-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="f7e33-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f7e33-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e33-141">-ResourceGroupName</span></span>
<span data-ttu-id="f7e33-142">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e33-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f7e33-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7e33-143">-ResourceId</span></span>
<span data-ttu-id="f7e33-144">節點類型資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f7e33-144">Node type resource id</span></span>

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

### <span data-ttu-id="f7e33-145">-確認</span><span class="sxs-lookup"><span data-stu-id="f7e33-145">-Confirm</span></span>
<span data-ttu-id="f7e33-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f7e33-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e33-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e33-147">-WhatIf</span></span>
<span data-ttu-id="f7e33-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7e33-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e33-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7e33-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e33-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e33-150">CommonParameters</span></span>
<span data-ttu-id="f7e33-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7e33-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e33-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7e33-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e33-153">輸入</span><span class="sxs-lookup"><span data-stu-id="f7e33-153">INPUTS</span></span>

### <span data-ttu-id="f7e33-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f7e33-154">System.String</span></span>

## <span data-ttu-id="f7e33-155">輸出</span><span class="sxs-lookup"><span data-stu-id="f7e33-155">OUTPUTS</span></span>

### <span data-ttu-id="f7e33-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7e33-156">System.Boolean</span></span>

## <span data-ttu-id="f7e33-157">筆記</span><span class="sxs-lookup"><span data-stu-id="f7e33-157">NOTES</span></span>

## <span data-ttu-id="f7e33-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7e33-158">RELATED LINKS</span></span>

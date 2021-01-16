---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: e9c4c68f794b5ea0c20b0e1fe57677b329b02622
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279044"
---
# <span data-ttu-id="e44be-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e44be-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="e44be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e44be-102">SYNOPSIS</span></span>
<span data-ttu-id="e44be-103">刪除 Synapse Analytics SQL pool 還原點。</span><span class="sxs-lookup"><span data-stu-id="e44be-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="e44be-104">句法</span><span class="sxs-lookup"><span data-stu-id="e44be-104">SYNTAX</span></span>

### <span data-ttu-id="e44be-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e44be-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String> -Name <String> 
[-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e44be-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e44be-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -Name <String> -SqlPoolObject <PSSynapseSqlPool> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e44be-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e44be-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e44be-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e44be-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e44be-109">說明</span><span class="sxs-lookup"><span data-stu-id="e44be-109">DESCRIPTION</span></span>
<span data-ttu-id="e44be-110">**AzSynapseSqlPoolRestorePoint** Cmdlet 會永久刪除 Azure SYNAPSE 分析 SQL pool 還原點。</span><span class="sxs-lookup"><span data-stu-id="e44be-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="e44be-111">示例</span><span class="sxs-lookup"><span data-stu-id="e44be-111">EXAMPLES</span></span>

### <span data-ttu-id="e44be-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e44be-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="e44be-113">這個命令會刪除 Azure Synapse Analytics SQL pool 還原點。</span><span class="sxs-lookup"><span data-stu-id="e44be-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="e44be-114">範例2</span><span class="sxs-lookup"><span data-stu-id="e44be-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="e44be-115">這個命令會透過管線刪除 Azure Synapse Analytics SQL pool 還原點。</span><span class="sxs-lookup"><span data-stu-id="e44be-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="e44be-116">範例3</span><span class="sxs-lookup"><span data-stu-id="e44be-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="e44be-117">這個命令會透過管線刪除 Azure Synapse Analytics SQL pool 還原點。</span><span class="sxs-lookup"><span data-stu-id="e44be-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="e44be-118">範例4</span><span class="sxs-lookup"><span data-stu-id="e44be-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="e44be-119">此命令會刪除具有指定資源識別碼的 Azure Synapse Analytics SQL pool 還原點。</span><span class="sxs-lookup"><span data-stu-id="e44be-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="e44be-120">參數</span><span class="sxs-lookup"><span data-stu-id="e44be-120">PARAMETERS</span></span>

### <span data-ttu-id="e44be-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e44be-121">-AsJob</span></span>
<span data-ttu-id="e44be-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e44be-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e44be-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e44be-123">-Force</span></span>
<span data-ttu-id="e44be-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="e44be-124">Do not ask for confirmation.</span></span>

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


### <span data-ttu-id="e44be-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e44be-125">-InputObject</span></span>
<span data-ttu-id="e44be-126">SQL pool 還原點建立時間輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e44be-126">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e44be-127">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="e44be-127">-RestorePointCreationDate</span></span>
<span data-ttu-id="e44be-128">SQL 還原點建立日期 Synapse 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e44be-128">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44be-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e44be-129">-PassThru</span></span>
<span data-ttu-id="e44be-130">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="e44be-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e44be-131">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e44be-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e44be-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44be-132">-ResourceGroupName</span></span>
<span data-ttu-id="e44be-133">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e44be-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44be-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e44be-134">-ResourceId</span></span>
<span data-ttu-id="e44be-135">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e44be-135">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e44be-136">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e44be-136">-SqlPoolName</span></span>
<span data-ttu-id="e44be-137">Synapse Sql pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e44be-137">Name of Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44be-138">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e44be-138">-SqlPoolObject</span></span>
<span data-ttu-id="e44be-139">Sql Pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e44be-139">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e44be-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e44be-140">-WorkspaceName</span></span>
<span data-ttu-id="e44be-141">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e44be-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44be-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e44be-142">-WorkspaceObject</span></span>
<span data-ttu-id="e44be-143">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e44be-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e44be-144">-確認</span><span class="sxs-lookup"><span data-stu-id="e44be-144">-Confirm</span></span>
<span data-ttu-id="e44be-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e44be-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e44be-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44be-146">-WhatIf</span></span>
<span data-ttu-id="e44be-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e44be-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44be-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e44be-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e44be-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44be-149">CommonParameters</span></span>
<span data-ttu-id="e44be-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e44be-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44be-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e44be-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44be-152">輸入</span><span class="sxs-lookup"><span data-stu-id="e44be-152">INPUTS</span></span>

### <span data-ttu-id="e44be-153">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e44be-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e44be-154">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e44be-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="e44be-155">PSRestorePoint 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e44be-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="e44be-156">System.object</span><span class="sxs-lookup"><span data-stu-id="e44be-156">System.String</span></span>

## <span data-ttu-id="e44be-157">輸出</span><span class="sxs-lookup"><span data-stu-id="e44be-157">OUTPUTS</span></span>

### <span data-ttu-id="e44be-158">System.object</span><span class="sxs-lookup"><span data-stu-id="e44be-158">System.Boolean</span></span>

## <span data-ttu-id="e44be-159">筆記</span><span class="sxs-lookup"><span data-stu-id="e44be-159">NOTES</span></span>

## <span data-ttu-id="e44be-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="e44be-160">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129399"
---
# <span data-ttu-id="d9605-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d9605-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="d9605-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9605-102">SYNOPSIS</span></span>
<span data-ttu-id="d9605-103">更新 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="d9605-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d9605-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9605-104">SYNTAX</span></span>

### <span data-ttu-id="d9605-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d9605-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9605-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9605-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9605-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9605-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9605-117">說明</span><span class="sxs-lookup"><span data-stu-id="d9605-117">DESCRIPTION</span></span>
<span data-ttu-id="d9605-118">**AzSynapseSqlPool** Cmdlet 會更新 Azure SYNAPSE Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="d9605-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d9605-119">示例</span><span class="sxs-lookup"><span data-stu-id="d9605-119">EXAMPLES</span></span>

### <span data-ttu-id="d9605-120">範例1</span><span class="sxs-lookup"><span data-stu-id="d9605-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="d9605-121">這個命令會更新 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="d9605-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="d9605-122">範例2</span><span class="sxs-lookup"><span data-stu-id="d9605-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="d9605-123">這個命令會透過管線更新 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="d9605-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="d9605-124">範例3</span><span class="sxs-lookup"><span data-stu-id="d9605-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="d9605-125">這個命令會透過管線更新 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="d9605-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="d9605-126">範例4</span><span class="sxs-lookup"><span data-stu-id="d9605-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="d9605-127">這個命令會更新 Azure Synapse Analytics SQL pool 與資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9605-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="d9605-128">參數</span><span class="sxs-lookup"><span data-stu-id="d9605-128">PARAMETERS</span></span>

### <span data-ttu-id="d9605-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9605-129">-AsJob</span></span>
<span data-ttu-id="d9605-130">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d9605-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9605-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9605-131">-DefaultProfile</span></span>
<span data-ttu-id="d9605-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9605-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9605-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9605-133">-InputObject</span></span>
<span data-ttu-id="d9605-134">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d9605-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9605-135">-Name</span></span>
<span data-ttu-id="d9605-136">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9605-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9605-137">-PassThru</span></span>
<span data-ttu-id="d9605-138">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="d9605-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d9605-139">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="d9605-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d9605-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="d9605-140">-PerformanceLevel</span></span>
<span data-ttu-id="d9605-141">要指派給 SQL pool 的 SQL 服務層級和效能等級。</span><span class="sxs-lookup"><span data-stu-id="d9605-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="d9605-142">例如，DW2000c。</span><span class="sxs-lookup"><span data-stu-id="d9605-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9605-143">-ResourceGroupName</span></span>
<span data-ttu-id="d9605-144">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d9605-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9605-145">-ResourceId</span></span>
<span data-ttu-id="d9605-146">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9605-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-147">-簡歷</span><span class="sxs-lookup"><span data-stu-id="d9605-147">-Resume</span></span>
<span data-ttu-id="d9605-148">指示要繼續 SQL pool</span><span class="sxs-lookup"><span data-stu-id="d9605-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-149">-暫停</span><span class="sxs-lookup"><span data-stu-id="d9605-149">-Suspend</span></span>
<span data-ttu-id="d9605-150">指示暫停 SQL 池</span><span class="sxs-lookup"><span data-stu-id="d9605-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9605-151">-Tag</span></span>
<span data-ttu-id="d9605-152">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="d9605-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-153">-版本</span><span class="sxs-lookup"><span data-stu-id="d9605-153">-Version</span></span>
<span data-ttu-id="d9605-154">Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="d9605-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="d9605-155">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="d9605-155">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-156">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d9605-156">-WorkspaceName</span></span>
<span data-ttu-id="d9605-157">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9605-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-158">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d9605-158">-WorkspaceObject</span></span>
<span data-ttu-id="d9605-159">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d9605-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9605-160">-確認</span><span class="sxs-lookup"><span data-stu-id="d9605-160">-Confirm</span></span>
<span data-ttu-id="d9605-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9605-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9605-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9605-162">-WhatIf</span></span>
<span data-ttu-id="d9605-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9605-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9605-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9605-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9605-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9605-165">CommonParameters</span></span>
<span data-ttu-id="d9605-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9605-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9605-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9605-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9605-168">輸入</span><span class="sxs-lookup"><span data-stu-id="d9605-168">INPUTS</span></span>

### <span data-ttu-id="d9605-169">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d9605-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d9605-170">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d9605-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d9605-171">輸出</span><span class="sxs-lookup"><span data-stu-id="d9605-171">OUTPUTS</span></span>

### <span data-ttu-id="d9605-172">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d9605-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d9605-173">筆記</span><span class="sxs-lookup"><span data-stu-id="d9605-173">NOTES</span></span>

## <span data-ttu-id="d9605-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9605-174">RELATED LINKS</span></span>

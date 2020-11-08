---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137761"
---
# <span data-ttu-id="e0c39-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e0c39-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e0c39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0c39-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c39-103">更新 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="e0c39-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e0c39-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0c39-104">SYNTAX</span></span>

### <span data-ttu-id="e0c39-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e0c39-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0c39-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0c39-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0c39-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0c39-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0c39-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0c39-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0c39-109">說明</span><span class="sxs-lookup"><span data-stu-id="e0c39-109">DESCRIPTION</span></span>
<span data-ttu-id="e0c39-110">**AzSynapseSqlPool** Cmdlet 會更新 Azure SYNAPSE Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="e0c39-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e0c39-111">示例</span><span class="sxs-lookup"><span data-stu-id="e0c39-111">EXAMPLES</span></span>

### <span data-ttu-id="e0c39-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e0c39-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="e0c39-113">這個命令會更新 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="e0c39-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="e0c39-114">範例2</span><span class="sxs-lookup"><span data-stu-id="e0c39-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="e0c39-115">這個命令會透過管線更新 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="e0c39-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="e0c39-116">範例3</span><span class="sxs-lookup"><span data-stu-id="e0c39-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="e0c39-117">這個命令會透過管線更新 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="e0c39-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="e0c39-118">範例4</span><span class="sxs-lookup"><span data-stu-id="e0c39-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="e0c39-119">這個命令會更新 Azure Synapse Analytics SQL pool 與資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0c39-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="e0c39-120">參數</span><span class="sxs-lookup"><span data-stu-id="e0c39-120">PARAMETERS</span></span>

### <span data-ttu-id="e0c39-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0c39-121">-AsJob</span></span>
<span data-ttu-id="e0c39-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e0c39-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0c39-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c39-123">-DefaultProfile</span></span>
<span data-ttu-id="e0c39-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0c39-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c39-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0c39-125">-InputObject</span></span>
<span data-ttu-id="e0c39-126">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e0c39-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c39-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0c39-127">-Name</span></span>
<span data-ttu-id="e0c39-128">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0c39-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c39-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0c39-129">-PassThru</span></span>
<span data-ttu-id="e0c39-130">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="e0c39-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e0c39-131">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e0c39-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e0c39-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="e0c39-132">-PerformanceLevel</span></span>
<span data-ttu-id="e0c39-133">要指派給 SQL pool 的 SQL 服務層級和效能等級。</span><span class="sxs-lookup"><span data-stu-id="e0c39-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="e0c39-134">例如，DW2000c。</span><span class="sxs-lookup"><span data-stu-id="e0c39-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c39-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0c39-135">-ResourceGroupName</span></span>
<span data-ttu-id="e0c39-136">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e0c39-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c39-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0c39-137">-ResourceId</span></span>
<span data-ttu-id="e0c39-138">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0c39-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c39-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0c39-139">-Tag</span></span>
<span data-ttu-id="e0c39-140">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="e0c39-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c39-141">-版本</span><span class="sxs-lookup"><span data-stu-id="e0c39-141">-Version</span></span>
<span data-ttu-id="e0c39-142">Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="e0c39-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e0c39-143">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="e0c39-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="e0c39-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0c39-144">-WorkspaceName</span></span>
<span data-ttu-id="e0c39-145">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0c39-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c39-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e0c39-146">-WorkspaceObject</span></span>
<span data-ttu-id="e0c39-147">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e0c39-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c39-148">-確認</span><span class="sxs-lookup"><span data-stu-id="e0c39-148">-Confirm</span></span>
<span data-ttu-id="e0c39-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e0c39-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0c39-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c39-150">-WhatIf</span></span>
<span data-ttu-id="e0c39-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0c39-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0c39-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0c39-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0c39-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c39-153">CommonParameters</span></span>
<span data-ttu-id="e0c39-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0c39-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c39-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e0c39-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c39-156">輸入</span><span class="sxs-lookup"><span data-stu-id="e0c39-156">INPUTS</span></span>

### <span data-ttu-id="e0c39-157">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e0c39-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e0c39-158">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e0c39-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e0c39-159">輸出</span><span class="sxs-lookup"><span data-stu-id="e0c39-159">OUTPUTS</span></span>

### <span data-ttu-id="e0c39-160">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e0c39-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e0c39-161">筆記</span><span class="sxs-lookup"><span data-stu-id="e0c39-161">NOTES</span></span>

## <span data-ttu-id="e0c39-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0c39-162">RELATED LINKS</span></span>

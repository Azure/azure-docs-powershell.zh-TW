---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: fe13a82a6662b0f8e9578f4f0fd5143b350538c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903910"
---
# <span data-ttu-id="185f7-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="185f7-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="185f7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="185f7-102">SYNOPSIS</span></span>
<span data-ttu-id="185f7-103">更新 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="185f7-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="185f7-104">語法</span><span class="sxs-lookup"><span data-stu-id="185f7-104">SYNTAX</span></span>

### <span data-ttu-id="185f7-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="185f7-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="185f7-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="185f7-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="185f7-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="185f7-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="185f7-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="185f7-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="185f7-109">描述</span><span class="sxs-lookup"><span data-stu-id="185f7-109">DESCRIPTION</span></span>
<span data-ttu-id="185f7-110">**Update-AzSynapseSqlPool** Cmdlet 會更新 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="185f7-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="185f7-111">例子</span><span class="sxs-lookup"><span data-stu-id="185f7-111">EXAMPLES</span></span>

### <span data-ttu-id="185f7-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="185f7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="185f7-113">此命令會更新 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="185f7-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="185f7-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="185f7-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="185f7-115">此命令會透過管線更新 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="185f7-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="185f7-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="185f7-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="185f7-117">此命令會透過管線更新 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="185f7-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="185f7-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="185f7-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="185f7-119">此命令會以資源識別碼更新 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="185f7-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="185f7-120">參數</span><span class="sxs-lookup"><span data-stu-id="185f7-120">PARAMETERS</span></span>

### <span data-ttu-id="185f7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="185f7-121">-AsJob</span></span>
<span data-ttu-id="185f7-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="185f7-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="185f7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185f7-123">-DefaultProfile</span></span>
<span data-ttu-id="185f7-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="185f7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="185f7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="185f7-125">-InputObject</span></span>
<span data-ttu-id="185f7-126">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="185f7-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="185f7-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="185f7-127">-Name</span></span>
<span data-ttu-id="185f7-128">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="185f7-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="185f7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="185f7-129">-PassThru</span></span>
<span data-ttu-id="185f7-130">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="185f7-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="185f7-131">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="185f7-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="185f7-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="185f7-132">-PerformanceLevel</span></span>
<span data-ttu-id="185f7-133">要指派給 SQL 資料庫的 SQL 服務層級和績效等級。</span><span class="sxs-lookup"><span data-stu-id="185f7-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="185f7-134">例如，2000c。</span><span class="sxs-lookup"><span data-stu-id="185f7-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="185f7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="185f7-135">-ResourceGroupName</span></span>
<span data-ttu-id="185f7-136">資源組名。</span><span class="sxs-lookup"><span data-stu-id="185f7-136">Resource group name.</span></span>

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

### <span data-ttu-id="185f7-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="185f7-137">-ResourceId</span></span>
<span data-ttu-id="185f7-138">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="185f7-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="185f7-139">-標記</span><span class="sxs-lookup"><span data-stu-id="185f7-139">-Tag</span></span>
<span data-ttu-id="185f7-140">與資源關聯的標記字串字典。</span><span class="sxs-lookup"><span data-stu-id="185f7-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="185f7-141">-版本</span><span class="sxs-lookup"><span data-stu-id="185f7-141">-Version</span></span>
<span data-ttu-id="185f7-142">Synapse SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="185f7-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="185f7-143">例如 2 或 3。</span><span class="sxs-lookup"><span data-stu-id="185f7-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="185f7-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="185f7-144">-WorkspaceName</span></span>
<span data-ttu-id="185f7-145">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="185f7-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="185f7-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="185f7-146">-WorkspaceObject</span></span>
<span data-ttu-id="185f7-147">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="185f7-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="185f7-148">-確認</span><span class="sxs-lookup"><span data-stu-id="185f7-148">-Confirm</span></span>
<span data-ttu-id="185f7-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="185f7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="185f7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="185f7-150">-WhatIf</span></span>
<span data-ttu-id="185f7-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="185f7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="185f7-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="185f7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="185f7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185f7-153">CommonParameters</span></span>
<span data-ttu-id="185f7-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="185f7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185f7-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="185f7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185f7-156">輸入</span><span class="sxs-lookup"><span data-stu-id="185f7-156">INPUTS</span></span>

### <span data-ttu-id="185f7-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="185f7-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="185f7-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="185f7-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="185f7-159">輸出</span><span class="sxs-lookup"><span data-stu-id="185f7-159">OUTPUTS</span></span>

### <span data-ttu-id="185f7-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="185f7-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="185f7-161">筆記</span><span class="sxs-lookup"><span data-stu-id="185f7-161">NOTES</span></span>

## <span data-ttu-id="185f7-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="185f7-162">RELATED LINKS</span></span>

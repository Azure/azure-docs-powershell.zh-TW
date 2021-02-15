---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138187"
---
# <span data-ttu-id="99b8b-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="99b8b-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="99b8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="99b8b-103">刪除 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="99b8b-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="99b8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="99b8b-104">SYNTAX</span></span>

### <span data-ttu-id="99b8b-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="99b8b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99b8b-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b8b-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99b8b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b8b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99b8b-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99b8b-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99b8b-109">說明</span><span class="sxs-lookup"><span data-stu-id="99b8b-109">DESCRIPTION</span></span>
<span data-ttu-id="99b8b-110">**AzSynapseSqlPool** Cmdlet 會永久刪除 Azure SYNAPSE 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="99b8b-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="99b8b-111">示例</span><span class="sxs-lookup"><span data-stu-id="99b8b-111">EXAMPLES</span></span>

### <span data-ttu-id="99b8b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="99b8b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="99b8b-113">這個命令會刪除 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="99b8b-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="99b8b-114">範例2</span><span class="sxs-lookup"><span data-stu-id="99b8b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="99b8b-115">這個命令會透過管線刪除 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="99b8b-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="99b8b-116">範例3</span><span class="sxs-lookup"><span data-stu-id="99b8b-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="99b8b-117">這個命令會透過管線刪除 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="99b8b-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="99b8b-118">範例4</span><span class="sxs-lookup"><span data-stu-id="99b8b-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="99b8b-119">這個命令會刪除具有指定資源識別碼的 Azure Synapse 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="99b8b-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="99b8b-120">參數</span><span class="sxs-lookup"><span data-stu-id="99b8b-120">PARAMETERS</span></span>

### <span data-ttu-id="99b8b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99b8b-121">-AsJob</span></span>
<span data-ttu-id="99b8b-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="99b8b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99b8b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b8b-123">-DefaultProfile</span></span>
<span data-ttu-id="99b8b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99b8b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99b8b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="99b8b-125">-Force</span></span>
<span data-ttu-id="99b8b-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="99b8b-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="99b8b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99b8b-127">-InputObject</span></span>
<span data-ttu-id="99b8b-128">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="99b8b-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99b8b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="99b8b-129">-Name</span></span>
<span data-ttu-id="99b8b-130">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="99b8b-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b8b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99b8b-131">-PassThru</span></span>
<span data-ttu-id="99b8b-132">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="99b8b-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="99b8b-133">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="99b8b-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="99b8b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b8b-134">-ResourceGroupName</span></span>
<span data-ttu-id="99b8b-135">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="99b8b-135">Resource group name.</span></span>

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

### <span data-ttu-id="99b8b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99b8b-136">-ResourceId</span></span>
<span data-ttu-id="99b8b-137">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="99b8b-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="99b8b-138">-版本</span><span class="sxs-lookup"><span data-stu-id="99b8b-138">-Version</span></span>
<span data-ttu-id="99b8b-139">Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="99b8b-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="99b8b-140">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="99b8b-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="99b8b-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="99b8b-141">-WorkspaceName</span></span>
<span data-ttu-id="99b8b-142">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="99b8b-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="99b8b-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="99b8b-143">-WorkspaceObject</span></span>
<span data-ttu-id="99b8b-144">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="99b8b-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="99b8b-145">-確認</span><span class="sxs-lookup"><span data-stu-id="99b8b-145">-Confirm</span></span>
<span data-ttu-id="99b8b-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99b8b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b8b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99b8b-147">-WhatIf</span></span>
<span data-ttu-id="99b8b-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99b8b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99b8b-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99b8b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b8b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b8b-150">CommonParameters</span></span>
<span data-ttu-id="99b8b-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99b8b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b8b-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="99b8b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b8b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="99b8b-153">INPUTS</span></span>

### <span data-ttu-id="99b8b-154">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="99b8b-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="99b8b-155">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="99b8b-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="99b8b-156">System.object</span><span class="sxs-lookup"><span data-stu-id="99b8b-156">System.String</span></span>

## <span data-ttu-id="99b8b-157">輸出</span><span class="sxs-lookup"><span data-stu-id="99b8b-157">OUTPUTS</span></span>

### <span data-ttu-id="99b8b-158">System.object</span><span class="sxs-lookup"><span data-stu-id="99b8b-158">System.Boolean</span></span>

## <span data-ttu-id="99b8b-159">筆記</span><span class="sxs-lookup"><span data-stu-id="99b8b-159">NOTES</span></span>

## <span data-ttu-id="99b8b-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="99b8b-160">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129101"
---
# <span data-ttu-id="6289d-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6289d-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="6289d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6289d-102">SYNOPSIS</span></span>
<span data-ttu-id="6289d-103">刪除 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="6289d-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6289d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6289d-104">SYNTAX</span></span>

### <span data-ttu-id="6289d-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6289d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6289d-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6289d-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6289d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6289d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6289d-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6289d-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6289d-109">說明</span><span class="sxs-lookup"><span data-stu-id="6289d-109">DESCRIPTION</span></span>
<span data-ttu-id="6289d-110">**AzSynapseSqlPool** Cmdlet 會永久刪除 Azure SYNAPSE 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="6289d-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6289d-111">示例</span><span class="sxs-lookup"><span data-stu-id="6289d-111">EXAMPLES</span></span>

### <span data-ttu-id="6289d-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6289d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="6289d-113">這個命令會刪除 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="6289d-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="6289d-114">範例2</span><span class="sxs-lookup"><span data-stu-id="6289d-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="6289d-115">這個命令會透過管線刪除 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="6289d-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="6289d-116">範例3</span><span class="sxs-lookup"><span data-stu-id="6289d-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="6289d-117">這個命令會透過管線刪除 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="6289d-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="6289d-118">範例4</span><span class="sxs-lookup"><span data-stu-id="6289d-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="6289d-119">這個命令會刪除具有指定資源識別碼的 Azure Synapse 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="6289d-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="6289d-120">參數</span><span class="sxs-lookup"><span data-stu-id="6289d-120">PARAMETERS</span></span>

### <span data-ttu-id="6289d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6289d-121">-AsJob</span></span>
<span data-ttu-id="6289d-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6289d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6289d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6289d-123">-DefaultProfile</span></span>
<span data-ttu-id="6289d-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6289d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6289d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6289d-125">-InputObject</span></span>
<span data-ttu-id="6289d-126">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6289d-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6289d-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6289d-127">-Name</span></span>
<span data-ttu-id="6289d-128">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6289d-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="6289d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6289d-129">-PassThru</span></span>
<span data-ttu-id="6289d-130">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="6289d-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6289d-131">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6289d-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6289d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6289d-132">-ResourceGroupName</span></span>
<span data-ttu-id="6289d-133">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6289d-133">Resource group name.</span></span>

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

### <span data-ttu-id="6289d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6289d-134">-ResourceId</span></span>
<span data-ttu-id="6289d-135">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6289d-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="6289d-136">-版本</span><span class="sxs-lookup"><span data-stu-id="6289d-136">-Version</span></span>
<span data-ttu-id="6289d-137">Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="6289d-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="6289d-138">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="6289d-138">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="6289d-139">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6289d-139">-WorkspaceName</span></span>
<span data-ttu-id="6289d-140">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6289d-140">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6289d-141">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6289d-141">-WorkspaceObject</span></span>
<span data-ttu-id="6289d-142">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6289d-142">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6289d-143">-確認</span><span class="sxs-lookup"><span data-stu-id="6289d-143">-Confirm</span></span>
<span data-ttu-id="6289d-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6289d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6289d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6289d-145">-WhatIf</span></span>
<span data-ttu-id="6289d-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6289d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6289d-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6289d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6289d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6289d-148">CommonParameters</span></span>
<span data-ttu-id="6289d-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6289d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6289d-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6289d-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6289d-151">輸入</span><span class="sxs-lookup"><span data-stu-id="6289d-151">INPUTS</span></span>

### <span data-ttu-id="6289d-152">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6289d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6289d-153">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6289d-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="6289d-154">System.object</span><span class="sxs-lookup"><span data-stu-id="6289d-154">System.String</span></span>

## <span data-ttu-id="6289d-155">輸出</span><span class="sxs-lookup"><span data-stu-id="6289d-155">OUTPUTS</span></span>

### <span data-ttu-id="6289d-156">System.object</span><span class="sxs-lookup"><span data-stu-id="6289d-156">System.Boolean</span></span>

## <span data-ttu-id="6289d-157">筆記</span><span class="sxs-lookup"><span data-stu-id="6289d-157">NOTES</span></span>

## <span data-ttu-id="6289d-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="6289d-158">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 298077ced1b7cb308bae4a8a5d27e13893c4b4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914242"
---
# <span data-ttu-id="023f5-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="023f5-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="023f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="023f5-102">SYNOPSIS</span></span>
<span data-ttu-id="023f5-103">刪除 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="023f5-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="023f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="023f5-104">SYNTAX</span></span>

### <span data-ttu-id="023f5-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="023f5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="023f5-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="023f5-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="023f5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="023f5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="023f5-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="023f5-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="023f5-109">描述</span><span class="sxs-lookup"><span data-stu-id="023f5-109">DESCRIPTION</span></span>
<span data-ttu-id="023f5-110">**Remove-AzSynapseSqlPool** Cmdlet 會永久刪除 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="023f5-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="023f5-111">例子</span><span class="sxs-lookup"><span data-stu-id="023f5-111">EXAMPLES</span></span>

### <span data-ttu-id="023f5-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="023f5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="023f5-113">此命令會刪除 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="023f5-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="023f5-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="023f5-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="023f5-115">此命令會透過管線刪除 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="023f5-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="023f5-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="023f5-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="023f5-117">此命令會透過管線刪除 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="023f5-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="023f5-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="023f5-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="023f5-119">此命令會刪除具有指定資源識別碼的 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="023f5-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="023f5-120">參數</span><span class="sxs-lookup"><span data-stu-id="023f5-120">PARAMETERS</span></span>

### <span data-ttu-id="023f5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="023f5-121">-AsJob</span></span>
<span data-ttu-id="023f5-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="023f5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="023f5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="023f5-123">-DefaultProfile</span></span>
<span data-ttu-id="023f5-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="023f5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="023f5-125">-強制</span><span class="sxs-lookup"><span data-stu-id="023f5-125">-Force</span></span>
<span data-ttu-id="023f5-126">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="023f5-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="023f5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="023f5-127">-InputObject</span></span>
<span data-ttu-id="023f5-128">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="023f5-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="023f5-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="023f5-129">-Name</span></span>
<span data-ttu-id="023f5-130">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="023f5-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="023f5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="023f5-131">-PassThru</span></span>
<span data-ttu-id="023f5-132">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="023f5-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="023f5-133">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="023f5-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="023f5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="023f5-134">-ResourceGroupName</span></span>
<span data-ttu-id="023f5-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="023f5-135">Resource group name.</span></span>

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

### <span data-ttu-id="023f5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="023f5-136">-ResourceId</span></span>
<span data-ttu-id="023f5-137">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="023f5-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="023f5-138">-版本</span><span class="sxs-lookup"><span data-stu-id="023f5-138">-Version</span></span>
<span data-ttu-id="023f5-139">Synapse SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="023f5-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="023f5-140">例如 2 或 3。</span><span class="sxs-lookup"><span data-stu-id="023f5-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="023f5-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="023f5-141">-WorkspaceName</span></span>
<span data-ttu-id="023f5-142">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="023f5-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="023f5-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="023f5-143">-WorkspaceObject</span></span>
<span data-ttu-id="023f5-144">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="023f5-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="023f5-145">-確認</span><span class="sxs-lookup"><span data-stu-id="023f5-145">-Confirm</span></span>
<span data-ttu-id="023f5-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="023f5-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="023f5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="023f5-147">-WhatIf</span></span>
<span data-ttu-id="023f5-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="023f5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="023f5-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="023f5-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="023f5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="023f5-150">CommonParameters</span></span>
<span data-ttu-id="023f5-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="023f5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="023f5-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="023f5-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="023f5-153">輸入</span><span class="sxs-lookup"><span data-stu-id="023f5-153">INPUTS</span></span>

### <span data-ttu-id="023f5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="023f5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="023f5-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="023f5-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="023f5-156">System.String</span><span class="sxs-lookup"><span data-stu-id="023f5-156">System.String</span></span>

## <span data-ttu-id="023f5-157">輸出</span><span class="sxs-lookup"><span data-stu-id="023f5-157">OUTPUTS</span></span>

### <span data-ttu-id="023f5-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="023f5-158">System.Boolean</span></span>

## <span data-ttu-id="023f5-159">筆記</span><span class="sxs-lookup"><span data-stu-id="023f5-159">NOTES</span></span>

## <span data-ttu-id="023f5-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="023f5-160">RELATED LINKS</span></span>

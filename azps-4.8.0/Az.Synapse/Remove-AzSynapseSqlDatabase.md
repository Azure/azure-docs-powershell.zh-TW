---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971575"
---
# <span data-ttu-id="e9761-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9761-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="e9761-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9761-102">SYNOPSIS</span></span>
<span data-ttu-id="e9761-103">刪除 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9761-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e9761-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9761-104">SYNTAX</span></span>

### <span data-ttu-id="e9761-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e9761-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9761-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9761-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9761-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9761-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9761-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9761-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9761-109">說明</span><span class="sxs-lookup"><span data-stu-id="e9761-109">DESCRIPTION</span></span>
<span data-ttu-id="e9761-110">**AzSynapseSqlPool** Cmdlet 會永久刪除 Azure SYNAPSE 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9761-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="e9761-111">示例</span><span class="sxs-lookup"><span data-stu-id="e9761-111">EXAMPLES</span></span>

### <span data-ttu-id="e9761-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e9761-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="e9761-113">這個命令會刪除 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9761-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="e9761-114">範例2</span><span class="sxs-lookup"><span data-stu-id="e9761-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="e9761-115">這個命令會透過管線刪除 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9761-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="e9761-116">範例3</span><span class="sxs-lookup"><span data-stu-id="e9761-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="e9761-117">這個命令會透過管線刪除 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9761-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="e9761-118">範例4</span><span class="sxs-lookup"><span data-stu-id="e9761-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="e9761-119">這個命令會刪除具有指定資源識別碼的 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9761-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="e9761-120">參數</span><span class="sxs-lookup"><span data-stu-id="e9761-120">PARAMETERS</span></span>

### <span data-ttu-id="e9761-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9761-121">-AsJob</span></span>
<span data-ttu-id="e9761-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e9761-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9761-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9761-123">-DefaultProfile</span></span>
<span data-ttu-id="e9761-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9761-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9761-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9761-125">-InputObject</span></span>
<span data-ttu-id="e9761-126">SQL 資料庫輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e9761-126">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9761-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9761-127">-Name</span></span>
<span data-ttu-id="e9761-128">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9761-128">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e9761-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9761-129">-PassThru</span></span>
<span data-ttu-id="e9761-130">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="e9761-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e9761-131">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e9761-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e9761-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9761-132">-ResourceGroupName</span></span>
<span data-ttu-id="e9761-133">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e9761-133">Resource group name.</span></span>

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

### <span data-ttu-id="e9761-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9761-134">-ResourceId</span></span>
<span data-ttu-id="e9761-135">Synapse SQL 資料庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9761-135">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e9761-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9761-136">-WorkspaceName</span></span>
<span data-ttu-id="e9761-137">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9761-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9761-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e9761-138">-WorkspaceObject</span></span>
<span data-ttu-id="e9761-139">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e9761-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9761-140">-確認</span><span class="sxs-lookup"><span data-stu-id="e9761-140">-Confirm</span></span>
<span data-ttu-id="e9761-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9761-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9761-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9761-142">-WhatIf</span></span>
<span data-ttu-id="e9761-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9761-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9761-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9761-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9761-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9761-145">CommonParameters</span></span>
<span data-ttu-id="e9761-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9761-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9761-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9761-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9761-148">輸入</span><span class="sxs-lookup"><span data-stu-id="e9761-148">INPUTS</span></span>

### <span data-ttu-id="e9761-149">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e9761-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e9761-150">PSSynapseSqlDatabase 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e9761-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="e9761-151">System.object</span><span class="sxs-lookup"><span data-stu-id="e9761-151">System.String</span></span>

## <span data-ttu-id="e9761-152">輸出</span><span class="sxs-lookup"><span data-stu-id="e9761-152">OUTPUTS</span></span>

### <span data-ttu-id="e9761-153">System.object</span><span class="sxs-lookup"><span data-stu-id="e9761-153">System.Boolean</span></span>

## <span data-ttu-id="e9761-154">筆記</span><span class="sxs-lookup"><span data-stu-id="e9761-154">NOTES</span></span>

## <span data-ttu-id="e9761-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9761-155">RELATED LINKS</span></span>

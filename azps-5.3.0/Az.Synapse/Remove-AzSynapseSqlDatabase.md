---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 4951fbe707dbae8c1fdff34e828e468a2d3168bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288123"
---
# <span data-ttu-id="0b943-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b943-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="0b943-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b943-102">SYNOPSIS</span></span>
<span data-ttu-id="0b943-103">刪除 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b943-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0b943-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b943-104">SYNTAX</span></span>

### <span data-ttu-id="0b943-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0b943-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b943-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b943-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b943-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b943-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b943-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b943-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b943-109">說明</span><span class="sxs-lookup"><span data-stu-id="0b943-109">DESCRIPTION</span></span>
<span data-ttu-id="0b943-110">**AzSynapseSqlPool** Cmdlet 會永久刪除 Azure SYNAPSE 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b943-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0b943-111">示例</span><span class="sxs-lookup"><span data-stu-id="0b943-111">EXAMPLES</span></span>

### <span data-ttu-id="0b943-112">範例1</span><span class="sxs-lookup"><span data-stu-id="0b943-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="0b943-113">這個命令會刪除 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b943-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="0b943-114">範例2</span><span class="sxs-lookup"><span data-stu-id="0b943-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="0b943-115">這個命令會透過管線刪除 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b943-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="0b943-116">範例3</span><span class="sxs-lookup"><span data-stu-id="0b943-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="0b943-117">這個命令會透過管線刪除 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b943-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="0b943-118">範例4</span><span class="sxs-lookup"><span data-stu-id="0b943-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="0b943-119">這個命令會刪除具有指定資源識別碼的 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b943-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="0b943-120">參數</span><span class="sxs-lookup"><span data-stu-id="0b943-120">PARAMETERS</span></span>

### <span data-ttu-id="0b943-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b943-121">-AsJob</span></span>
<span data-ttu-id="0b943-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0b943-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b943-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b943-123">-DefaultProfile</span></span>
<span data-ttu-id="0b943-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b943-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b943-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0b943-125">-Force</span></span>
<span data-ttu-id="0b943-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0b943-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0b943-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b943-127">-InputObject</span></span>
<span data-ttu-id="0b943-128">SQL 資料庫輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0b943-128">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0b943-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b943-129">-Name</span></span>
<span data-ttu-id="0b943-130">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b943-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="0b943-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b943-131">-PassThru</span></span>
<span data-ttu-id="0b943-132">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="0b943-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0b943-133">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="0b943-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0b943-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b943-134">-ResourceGroupName</span></span>
<span data-ttu-id="0b943-135">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0b943-135">Resource group name.</span></span>

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

### <span data-ttu-id="0b943-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b943-136">-ResourceId</span></span>
<span data-ttu-id="0b943-137">Synapse SQL 資料庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b943-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="0b943-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0b943-138">-WorkspaceName</span></span>
<span data-ttu-id="0b943-139">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b943-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0b943-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0b943-140">-WorkspaceObject</span></span>
<span data-ttu-id="0b943-141">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0b943-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0b943-142">-確認</span><span class="sxs-lookup"><span data-stu-id="0b943-142">-Confirm</span></span>
<span data-ttu-id="0b943-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b943-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b943-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b943-144">-WhatIf</span></span>
<span data-ttu-id="0b943-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b943-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b943-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b943-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b943-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b943-147">CommonParameters</span></span>
<span data-ttu-id="0b943-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b943-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b943-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b943-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b943-150">輸入</span><span class="sxs-lookup"><span data-stu-id="0b943-150">INPUTS</span></span>

### <span data-ttu-id="0b943-151">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0b943-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0b943-152">PSSynapseSqlDatabase 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0b943-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="0b943-153">System.object</span><span class="sxs-lookup"><span data-stu-id="0b943-153">System.String</span></span>

## <span data-ttu-id="0b943-154">輸出</span><span class="sxs-lookup"><span data-stu-id="0b943-154">OUTPUTS</span></span>

### <span data-ttu-id="0b943-155">System.object</span><span class="sxs-lookup"><span data-stu-id="0b943-155">System.Boolean</span></span>

## <span data-ttu-id="0b943-156">筆記</span><span class="sxs-lookup"><span data-stu-id="0b943-156">NOTES</span></span>

## <span data-ttu-id="0b943-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b943-157">RELATED LINKS</span></span>

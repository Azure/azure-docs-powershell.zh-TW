---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: a60bcb20610449b9f76ff3e62684da43a2a792c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903917"
---
# <span data-ttu-id="b5a4d-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5a4d-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="b5a4d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a4d-103">刪除 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="b5a4d-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5a4d-104">SYNTAX</span></span>

### <span data-ttu-id="b5a4d-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b5a4d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5a4d-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5a4d-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5a4d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5a4d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5a4d-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5a4d-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5a4d-109">描述</span><span class="sxs-lookup"><span data-stu-id="b5a4d-109">DESCRIPTION</span></span>
<span data-ttu-id="b5a4d-110">**Remove-AzSynapseSqlPool** Cmdlet 會永久刪除 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="b5a4d-111">例子</span><span class="sxs-lookup"><span data-stu-id="b5a4d-111">EXAMPLES</span></span>

### <span data-ttu-id="b5a4d-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="b5a4d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="b5a4d-113">此命令會刪除 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="b5a4d-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="b5a4d-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="b5a4d-115">此命令會透過管線刪除 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="b5a4d-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="b5a4d-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="b5a4d-117">此命令會透過管線刪除 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="b5a4d-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="b5a4d-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="b5a4d-119">此命令會刪除具有指定資源識別碼的 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="b5a4d-120">參數</span><span class="sxs-lookup"><span data-stu-id="b5a4d-120">PARAMETERS</span></span>

### <span data-ttu-id="b5a4d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5a4d-121">-AsJob</span></span>
<span data-ttu-id="b5a4d-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5a4d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5a4d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a4d-123">-DefaultProfile</span></span>
<span data-ttu-id="b5a4d-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5a4d-125">-強制</span><span class="sxs-lookup"><span data-stu-id="b5a4d-125">-Force</span></span>
<span data-ttu-id="b5a4d-126">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b5a4d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5a4d-127">-InputObject</span></span>
<span data-ttu-id="b5a4d-128">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-128">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b5a4d-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5a4d-129">-Name</span></span>
<span data-ttu-id="b5a4d-130">Synapse SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="b5a4d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5a4d-131">-PassThru</span></span>
<span data-ttu-id="b5a4d-132">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b5a4d-133">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b5a4d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a4d-134">-ResourceGroupName</span></span>
<span data-ttu-id="b5a4d-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-135">Resource group name.</span></span>

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

### <span data-ttu-id="b5a4d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5a4d-136">-ResourceId</span></span>
<span data-ttu-id="b5a4d-137">Synapse SQL Database 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="b5a4d-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5a4d-138">-WorkspaceName</span></span>
<span data-ttu-id="b5a4d-139">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b5a4d-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b5a4d-140">-WorkspaceObject</span></span>
<span data-ttu-id="b5a4d-141">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b5a4d-142">-確認</span><span class="sxs-lookup"><span data-stu-id="b5a4d-142">-Confirm</span></span>
<span data-ttu-id="b5a4d-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a4d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a4d-144">-WhatIf</span></span>
<span data-ttu-id="b5a4d-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5a4d-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a4d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a4d-147">CommonParameters</span></span>
<span data-ttu-id="b5a4d-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5a4d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a4d-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5a4d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a4d-150">輸入</span><span class="sxs-lookup"><span data-stu-id="b5a4d-150">INPUTS</span></span>

### <span data-ttu-id="b5a4d-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5a4d-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b5a4d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5a4d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="b5a4d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b5a4d-153">System.String</span></span>

## <span data-ttu-id="b5a4d-154">輸出</span><span class="sxs-lookup"><span data-stu-id="b5a4d-154">OUTPUTS</span></span>

### <span data-ttu-id="b5a4d-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5a4d-155">System.Boolean</span></span>

## <span data-ttu-id="b5a4d-156">筆記</span><span class="sxs-lookup"><span data-stu-id="b5a4d-156">NOTES</span></span>

## <span data-ttu-id="b5a4d-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5a4d-157">RELATED LINKS</span></span>

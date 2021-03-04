---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: a939ef485976a746e705de10a4706b03c63f910e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912162"
---
# <span data-ttu-id="0f6fe-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0f6fe-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="0f6fe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f6fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6fe-103">更新 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0f6fe-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f6fe-104">SYNTAX</span></span>

### <span data-ttu-id="0f6fe-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0f6fe-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fe-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f6fe-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f6fe-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f6fe-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fe-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f6fe-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f6fe-109">描述</span><span class="sxs-lookup"><span data-stu-id="0f6fe-109">DESCRIPTION</span></span>
<span data-ttu-id="0f6fe-110">**Update-AzSynapseSqlDatabase** Cmdlet 會更新 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0f6fe-111">例子</span><span class="sxs-lookup"><span data-stu-id="0f6fe-111">EXAMPLES</span></span>

### <span data-ttu-id="0f6fe-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0f6fe-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="0f6fe-113">此命令會更新 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0f6fe-114">參數</span><span class="sxs-lookup"><span data-stu-id="0f6fe-114">PARAMETERS</span></span>

### <span data-ttu-id="0f6fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f6fe-115">-AsJob</span></span>
<span data-ttu-id="0f6fe-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0f6fe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f6fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6fe-117">-DefaultProfile</span></span>
<span data-ttu-id="0f6fe-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f6fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f6fe-119">-InputObject</span></span>
<span data-ttu-id="0f6fe-120">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fe-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="0f6fe-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="0f6fe-122">指定資料庫的大小上限 ，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fe-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f6fe-123">-Name</span></span>
<span data-ttu-id="0f6fe-124">Synapse SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="0f6fe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f6fe-125">-PassThru</span></span>
<span data-ttu-id="0f6fe-126">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0f6fe-127">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0f6fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f6fe-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-129">Resource group name.</span></span>

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

### <span data-ttu-id="0f6fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f6fe-130">-ResourceId</span></span>
<span data-ttu-id="0f6fe-131">Synapse SQL Database 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="0f6fe-132">-標記</span><span class="sxs-lookup"><span data-stu-id="0f6fe-132">-Tag</span></span>
<span data-ttu-id="0f6fe-133">與資源關聯的標記字串字典。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="0f6fe-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f6fe-134">-WorkspaceName</span></span>
<span data-ttu-id="0f6fe-135">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0f6fe-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0f6fe-136">-WorkspaceObject</span></span>
<span data-ttu-id="0f6fe-137">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0f6fe-138">-確認</span><span class="sxs-lookup"><span data-stu-id="0f6fe-138">-Confirm</span></span>
<span data-ttu-id="0f6fe-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6fe-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6fe-140">-WhatIf</span></span>
<span data-ttu-id="0f6fe-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f6fe-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f6fe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6fe-143">CommonParameters</span></span>
<span data-ttu-id="0f6fe-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f6fe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6fe-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f6fe-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6fe-146">輸入</span><span class="sxs-lookup"><span data-stu-id="0f6fe-146">INPUTS</span></span>

### <span data-ttu-id="0f6fe-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f6fe-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0f6fe-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0f6fe-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="0f6fe-149">輸出</span><span class="sxs-lookup"><span data-stu-id="0f6fe-149">OUTPUTS</span></span>

### <span data-ttu-id="0f6fe-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0f6fe-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="0f6fe-151">筆記</span><span class="sxs-lookup"><span data-stu-id="0f6fe-151">NOTES</span></span>

## <span data-ttu-id="0f6fe-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f6fe-152">RELATED LINKS</span></span>

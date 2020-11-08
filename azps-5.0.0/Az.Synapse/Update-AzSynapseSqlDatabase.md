---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137605"
---
# <span data-ttu-id="a57f6-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a57f6-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="a57f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a57f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a57f6-103">更新 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="a57f6-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a57f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a57f6-104">SYNTAX</span></span>

### <span data-ttu-id="a57f6-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a57f6-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57f6-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57f6-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a57f6-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57f6-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57f6-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57f6-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57f6-109">說明</span><span class="sxs-lookup"><span data-stu-id="a57f6-109">DESCRIPTION</span></span>
<span data-ttu-id="a57f6-110">**AzSynapseSqlDatabase** Cmdlet 會更新 Azure SYNAPSE 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="a57f6-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a57f6-111">示例</span><span class="sxs-lookup"><span data-stu-id="a57f6-111">EXAMPLES</span></span>

### <span data-ttu-id="a57f6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a57f6-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="a57f6-113">這個命令會更新 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="a57f6-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a57f6-114">參數</span><span class="sxs-lookup"><span data-stu-id="a57f6-114">PARAMETERS</span></span>

### <span data-ttu-id="a57f6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a57f6-115">-AsJob</span></span>
<span data-ttu-id="a57f6-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a57f6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a57f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57f6-117">-DefaultProfile</span></span>
<span data-ttu-id="a57f6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a57f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a57f6-119">-InputObject</span></span>
<span data-ttu-id="a57f6-120">SQL 資料庫輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a57f6-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a57f6-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="a57f6-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="a57f6-122">指定資料庫的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a57f6-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="a57f6-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a57f6-123">-Name</span></span>
<span data-ttu-id="a57f6-124">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a57f6-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="a57f6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a57f6-125">-PassThru</span></span>
<span data-ttu-id="a57f6-126">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a57f6-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a57f6-127">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a57f6-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a57f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="a57f6-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a57f6-129">Resource group name.</span></span>

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

### <span data-ttu-id="a57f6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a57f6-130">-ResourceId</span></span>
<span data-ttu-id="a57f6-131">Synapse SQL 資料庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a57f6-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="a57f6-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="a57f6-132">-Tag</span></span>
<span data-ttu-id="a57f6-133">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="a57f6-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="a57f6-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a57f6-134">-WorkspaceName</span></span>
<span data-ttu-id="a57f6-135">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a57f6-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a57f6-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a57f6-136">-WorkspaceObject</span></span>
<span data-ttu-id="a57f6-137">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a57f6-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a57f6-138">-確認</span><span class="sxs-lookup"><span data-stu-id="a57f6-138">-Confirm</span></span>
<span data-ttu-id="a57f6-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a57f6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57f6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57f6-140">-WhatIf</span></span>
<span data-ttu-id="a57f6-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a57f6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57f6-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a57f6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57f6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57f6-143">CommonParameters</span></span>
<span data-ttu-id="a57f6-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a57f6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57f6-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a57f6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57f6-146">輸入</span><span class="sxs-lookup"><span data-stu-id="a57f6-146">INPUTS</span></span>

### <span data-ttu-id="a57f6-147">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a57f6-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a57f6-148">PSSynapseSqlDatabase 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a57f6-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="a57f6-149">輸出</span><span class="sxs-lookup"><span data-stu-id="a57f6-149">OUTPUTS</span></span>

### <span data-ttu-id="a57f6-150">PSSynapseSqlDatabase 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a57f6-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="a57f6-151">筆記</span><span class="sxs-lookup"><span data-stu-id="a57f6-151">NOTES</span></span>

## <span data-ttu-id="a57f6-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a57f6-152">RELATED LINKS</span></span>
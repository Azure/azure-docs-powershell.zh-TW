---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: d0249098c8414a38adecc4112449174496656b78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916835"
---
# <span data-ttu-id="24683-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="24683-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="24683-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24683-102">SYNOPSIS</span></span>
<span data-ttu-id="24683-103">暫停 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="24683-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="24683-104">語法</span><span class="sxs-lookup"><span data-stu-id="24683-104">SYNTAX</span></span>

### <span data-ttu-id="24683-105">SuspendByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="24683-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24683-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24683-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24683-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24683-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24683-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24683-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24683-109">描述</span><span class="sxs-lookup"><span data-stu-id="24683-109">DESCRIPTION</span></span>
<span data-ttu-id="24683-110">**Suspend-AzSynapseSqlPool** Cmdlet 會暫停 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="24683-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="24683-111">例子</span><span class="sxs-lookup"><span data-stu-id="24683-111">EXAMPLES</span></span>

### <span data-ttu-id="24683-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="24683-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="24683-113">此命令會暫停使用中的 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="24683-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="24683-114">參數</span><span class="sxs-lookup"><span data-stu-id="24683-114">PARAMETERS</span></span>

### <span data-ttu-id="24683-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24683-115">-AsJob</span></span>
<span data-ttu-id="24683-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24683-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24683-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24683-117">-DefaultProfile</span></span>
<span data-ttu-id="24683-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24683-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24683-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24683-119">-InputObject</span></span>
<span data-ttu-id="24683-120">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="24683-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24683-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="24683-121">-Name</span></span>
<span data-ttu-id="24683-122">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="24683-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24683-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24683-123">-PassThru</span></span>
<span data-ttu-id="24683-124">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="24683-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="24683-125">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="24683-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="24683-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24683-126">-ResourceGroupName</span></span>
<span data-ttu-id="24683-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="24683-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24683-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24683-128">-ResourceId</span></span>
<span data-ttu-id="24683-129">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24683-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24683-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="24683-130">-WorkspaceName</span></span>
<span data-ttu-id="24683-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="24683-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24683-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="24683-132">-WorkspaceObject</span></span>
<span data-ttu-id="24683-133">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="24683-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24683-134">-確認</span><span class="sxs-lookup"><span data-stu-id="24683-134">-Confirm</span></span>
<span data-ttu-id="24683-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="24683-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24683-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24683-136">-WhatIf</span></span>
<span data-ttu-id="24683-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24683-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24683-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24683-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24683-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24683-139">CommonParameters</span></span>
<span data-ttu-id="24683-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24683-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24683-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24683-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24683-142">輸入</span><span class="sxs-lookup"><span data-stu-id="24683-142">INPUTS</span></span>

### <span data-ttu-id="24683-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="24683-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="24683-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="24683-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="24683-145">輸出</span><span class="sxs-lookup"><span data-stu-id="24683-145">OUTPUTS</span></span>

### <span data-ttu-id="24683-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="24683-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="24683-147">筆記</span><span class="sxs-lookup"><span data-stu-id="24683-147">NOTES</span></span>

## <span data-ttu-id="24683-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="24683-148">RELATED LINKS</span></span>

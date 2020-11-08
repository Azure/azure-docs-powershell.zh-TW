---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136609"
---
# <span data-ttu-id="6351d-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6351d-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="6351d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6351d-102">SYNOPSIS</span></span>
<span data-ttu-id="6351d-103">暫停 Synapse 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="6351d-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6351d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6351d-104">SYNTAX</span></span>

### <span data-ttu-id="6351d-105">SuspendByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6351d-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6351d-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6351d-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6351d-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6351d-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6351d-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6351d-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6351d-109">說明</span><span class="sxs-lookup"><span data-stu-id="6351d-109">DESCRIPTION</span></span>
<span data-ttu-id="6351d-110">**AzSynapseSqlPool** Cmdlet 會暫停 Azure SYNAPSE 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="6351d-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6351d-111">示例</span><span class="sxs-lookup"><span data-stu-id="6351d-111">EXAMPLES</span></span>

### <span data-ttu-id="6351d-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6351d-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="6351d-113">這個命令會暫停 active Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="6351d-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6351d-114">參數</span><span class="sxs-lookup"><span data-stu-id="6351d-114">PARAMETERS</span></span>

### <span data-ttu-id="6351d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6351d-115">-AsJob</span></span>
<span data-ttu-id="6351d-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6351d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6351d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6351d-117">-DefaultProfile</span></span>
<span data-ttu-id="6351d-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6351d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6351d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6351d-119">-InputObject</span></span>
<span data-ttu-id="6351d-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6351d-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6351d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6351d-121">-Name</span></span>
<span data-ttu-id="6351d-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6351d-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6351d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6351d-123">-PassThru</span></span>
<span data-ttu-id="6351d-124">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="6351d-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6351d-125">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6351d-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6351d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6351d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6351d-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6351d-127">Resource group name.</span></span>

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

### <span data-ttu-id="6351d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6351d-128">-ResourceId</span></span>
<span data-ttu-id="6351d-129">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6351d-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="6351d-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6351d-130">-WorkspaceName</span></span>
<span data-ttu-id="6351d-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6351d-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6351d-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6351d-132">-WorkspaceObject</span></span>
<span data-ttu-id="6351d-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6351d-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6351d-134">-確認</span><span class="sxs-lookup"><span data-stu-id="6351d-134">-Confirm</span></span>
<span data-ttu-id="6351d-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6351d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6351d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6351d-136">-WhatIf</span></span>
<span data-ttu-id="6351d-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6351d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6351d-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6351d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6351d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6351d-139">CommonParameters</span></span>
<span data-ttu-id="6351d-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6351d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6351d-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6351d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6351d-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6351d-142">INPUTS</span></span>

### <span data-ttu-id="6351d-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6351d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6351d-144">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6351d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6351d-145">輸出</span><span class="sxs-lookup"><span data-stu-id="6351d-145">OUTPUTS</span></span>

### <span data-ttu-id="6351d-146">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6351d-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6351d-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6351d-147">NOTES</span></span>

## <span data-ttu-id="6351d-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6351d-148">RELATED LINKS</span></span>

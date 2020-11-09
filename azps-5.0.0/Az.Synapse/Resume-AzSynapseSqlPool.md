---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ea27b23174d9555e4153dc5ef8c4d053ef5a49b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286723"
---
# <span data-ttu-id="a2025-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a2025-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a2025-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2025-102">SYNOPSIS</span></span>
<span data-ttu-id="a2025-103">繼續 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="a2025-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a2025-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2025-104">SYNTAX</span></span>

### <span data-ttu-id="a2025-105">ResumeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a2025-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2025-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2025-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2025-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2025-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2025-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2025-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2025-109">說明</span><span class="sxs-lookup"><span data-stu-id="a2025-109">DESCRIPTION</span></span>
<span data-ttu-id="a2025-110">**Resume AzSynapseSqlPool** Cmdlet 會繼續 Azure SYNAPSE 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="a2025-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a2025-111">示例</span><span class="sxs-lookup"><span data-stu-id="a2025-111">EXAMPLES</span></span>

### <span data-ttu-id="a2025-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a2025-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a2025-113">這個命令會繼續執行暫停的 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="a2025-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a2025-114">參數</span><span class="sxs-lookup"><span data-stu-id="a2025-114">PARAMETERS</span></span>

### <span data-ttu-id="a2025-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2025-115">-AsJob</span></span>
<span data-ttu-id="a2025-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2025-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2025-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2025-117">-DefaultProfile</span></span>
<span data-ttu-id="a2025-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2025-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2025-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2025-119">-InputObject</span></span>
<span data-ttu-id="a2025-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a2025-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2025-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2025-121">-Name</span></span>
<span data-ttu-id="a2025-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2025-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2025-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2025-123">-PassThru</span></span>
<span data-ttu-id="a2025-124">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a2025-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a2025-125">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a2025-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a2025-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2025-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2025-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a2025-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2025-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2025-128">-ResourceId</span></span>
<span data-ttu-id="a2025-129">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2025-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2025-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2025-130">-WorkspaceName</span></span>
<span data-ttu-id="a2025-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2025-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2025-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a2025-132">-WorkspaceObject</span></span>
<span data-ttu-id="a2025-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a2025-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2025-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a2025-134">-Confirm</span></span>
<span data-ttu-id="a2025-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2025-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2025-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2025-136">-WhatIf</span></span>
<span data-ttu-id="a2025-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2025-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2025-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2025-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2025-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2025-139">CommonParameters</span></span>
<span data-ttu-id="a2025-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2025-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2025-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2025-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2025-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a2025-142">INPUTS</span></span>

### <span data-ttu-id="a2025-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a2025-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a2025-144">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a2025-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a2025-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a2025-145">OUTPUTS</span></span>

### <span data-ttu-id="a2025-146">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a2025-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a2025-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a2025-147">NOTES</span></span>

## <span data-ttu-id="a2025-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2025-148">RELATED LINKS</span></span>

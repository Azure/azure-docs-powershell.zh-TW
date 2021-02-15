---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ff2a68d7e0ae0ad94f685bbe1cfb795f7cd6a706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130354"
---
# <span data-ttu-id="a158b-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a158b-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a158b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a158b-102">SYNOPSIS</span></span>
<span data-ttu-id="a158b-103">繼續 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="a158b-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a158b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a158b-104">SYNTAX</span></span>

### <span data-ttu-id="a158b-105">ResumeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a158b-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a158b-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a158b-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a158b-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a158b-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a158b-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a158b-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a158b-109">說明</span><span class="sxs-lookup"><span data-stu-id="a158b-109">DESCRIPTION</span></span>
<span data-ttu-id="a158b-110">**Resume AzSynapseSqlPool** Cmdlet 會繼續 Azure SYNAPSE 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="a158b-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a158b-111">示例</span><span class="sxs-lookup"><span data-stu-id="a158b-111">EXAMPLES</span></span>

### <span data-ttu-id="a158b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a158b-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a158b-113">這個命令會繼續執行暫停的 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="a158b-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a158b-114">參數</span><span class="sxs-lookup"><span data-stu-id="a158b-114">PARAMETERS</span></span>

### <span data-ttu-id="a158b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a158b-115">-AsJob</span></span>
<span data-ttu-id="a158b-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a158b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a158b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a158b-117">-DefaultProfile</span></span>
<span data-ttu-id="a158b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a158b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a158b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a158b-119">-InputObject</span></span>
<span data-ttu-id="a158b-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a158b-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a158b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a158b-121">-Name</span></span>
<span data-ttu-id="a158b-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a158b-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a158b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a158b-123">-PassThru</span></span>
<span data-ttu-id="a158b-124">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a158b-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a158b-125">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a158b-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a158b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a158b-126">-ResourceGroupName</span></span>
<span data-ttu-id="a158b-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a158b-127">Resource group name.</span></span>

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

### <span data-ttu-id="a158b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a158b-128">-ResourceId</span></span>
<span data-ttu-id="a158b-129">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a158b-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a158b-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a158b-130">-WorkspaceName</span></span>
<span data-ttu-id="a158b-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a158b-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a158b-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a158b-132">-WorkspaceObject</span></span>
<span data-ttu-id="a158b-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a158b-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a158b-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a158b-134">-Confirm</span></span>
<span data-ttu-id="a158b-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a158b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a158b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a158b-136">-WhatIf</span></span>
<span data-ttu-id="a158b-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a158b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a158b-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a158b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a158b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a158b-139">CommonParameters</span></span>
<span data-ttu-id="a158b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a158b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a158b-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a158b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a158b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a158b-142">INPUTS</span></span>

### <span data-ttu-id="a158b-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a158b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a158b-144">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a158b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a158b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a158b-145">OUTPUTS</span></span>

### <span data-ttu-id="a158b-146">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a158b-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a158b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a158b-147">NOTES</span></span>

## <span data-ttu-id="a158b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a158b-148">RELATED LINKS</span></span>

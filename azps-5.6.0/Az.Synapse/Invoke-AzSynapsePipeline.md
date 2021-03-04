---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: 756db1072eec6546f6e495b3ec2115ca77389a73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909922"
---
# <span data-ttu-id="a03f6-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="a03f6-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="a03f6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a03f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a03f6-103">會啟動管線以開始執行。</span><span class="sxs-lookup"><span data-stu-id="a03f6-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="a03f6-104">語法</span><span class="sxs-lookup"><span data-stu-id="a03f6-104">SYNTAX</span></span>

### <span data-ttu-id="a03f6-105">NewByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a03f6-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a03f6-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="a03f6-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a03f6-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="a03f6-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a03f6-108">描述</span><span class="sxs-lookup"><span data-stu-id="a03f6-108">DESCRIPTION</span></span>
<span data-ttu-id="a03f6-109">**Invoke-AzSynapsePipeline 命令** 會啟動指定管線上的執行，並針對該執行過程返回識別碼。</span><span class="sxs-lookup"><span data-stu-id="a03f6-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="a03f6-110">此 GUID 可以傳遞至 **Get-AzSynapsePipelineRun** 或 **Get-AzSynapseActivityRun，** 以取得有關此執行的進一步詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a03f6-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="a03f6-111">例子</span><span class="sxs-lookup"><span data-stu-id="a03f6-111">EXAMPLES</span></span>

### <span data-ttu-id="a03f6-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="a03f6-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="a03f6-113">此命令會啟動工作區 ContosoWorkspace 中名為 ContosoPipeline 的管線執行。</span><span class="sxs-lookup"><span data-stu-id="a03f6-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a03f6-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="a03f6-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="a03f6-115">此命令會啟動在工作區 ContosoWorkspace 中透過管線執行名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="a03f6-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a03f6-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="a03f6-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="a03f6-117">此命令會啟動在工作區 ContosoWorkspace 中透過管線執行名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="a03f6-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a03f6-118">參數</span><span class="sxs-lookup"><span data-stu-id="a03f6-118">PARAMETERS</span></span>

### <span data-ttu-id="a03f6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a03f6-119">-AsJob</span></span>
<span data-ttu-id="a03f6-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a03f6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a03f6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03f6-121">-DefaultProfile</span></span>
<span data-ttu-id="a03f6-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a03f6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a03f6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a03f6-123">-InputObject</span></span>
<span data-ttu-id="a03f6-124">管線執行相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a03f6-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a03f6-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="a03f6-125">-IsRecovery</span></span>
<span data-ttu-id="a03f6-126">復原模式標標。</span><span class="sxs-lookup"><span data-stu-id="a03f6-126">Recovery mode flag.</span></span>
<span data-ttu-id="a03f6-127">如果復原模式設為 True，則指定的參照管線執行與新執行會在同一個 groupId 下分組。</span><span class="sxs-lookup"><span data-stu-id="a03f6-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="a03f6-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a03f6-128">-Parameter</span></span>
<span data-ttu-id="a03f6-129">管線執行的參數。</span><span class="sxs-lookup"><span data-stu-id="a03f6-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="a03f6-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="a03f6-130">-ParameterFile</span></span>
<span data-ttu-id="a03f6-131">具有管線執行參數的檔案名。</span><span class="sxs-lookup"><span data-stu-id="a03f6-131">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03f6-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a03f6-132">-PipelineName</span></span>
<span data-ttu-id="a03f6-133">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="a03f6-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03f6-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a03f6-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="a03f6-135">要重新執行的管線執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="a03f6-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="a03f6-136">如果指定執行識別碼，將會使用指定執行的參數來建立新執行。</span><span class="sxs-lookup"><span data-stu-id="a03f6-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03f6-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="a03f6-137">-StartActivityName</span></span>
<span data-ttu-id="a03f6-138">在復原模式中，重新執行會從此活動開始。</span><span class="sxs-lookup"><span data-stu-id="a03f6-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="a03f6-139">如果未指定，將會執行所有活動。</span><span class="sxs-lookup"><span data-stu-id="a03f6-139">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03f6-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a03f6-140">-WorkspaceName</span></span>
<span data-ttu-id="a03f6-141">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a03f6-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03f6-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a03f6-142">-WorkspaceObject</span></span>
<span data-ttu-id="a03f6-143">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="a03f6-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a03f6-144">-確認</span><span class="sxs-lookup"><span data-stu-id="a03f6-144">-Confirm</span></span>
<span data-ttu-id="a03f6-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a03f6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a03f6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a03f6-146">-WhatIf</span></span>
<span data-ttu-id="a03f6-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a03f6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a03f6-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a03f6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a03f6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03f6-149">CommonParameters</span></span>
<span data-ttu-id="a03f6-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a03f6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03f6-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a03f6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03f6-152">輸入</span><span class="sxs-lookup"><span data-stu-id="a03f6-152">INPUTS</span></span>

### <span data-ttu-id="a03f6-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="a03f6-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="a03f6-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a03f6-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a03f6-155">輸出</span><span class="sxs-lookup"><span data-stu-id="a03f6-155">OUTPUTS</span></span>

### <span data-ttu-id="a03f6-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="a03f6-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="a03f6-157">筆記</span><span class="sxs-lookup"><span data-stu-id="a03f6-157">NOTES</span></span>

## <span data-ttu-id="a03f6-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="a03f6-158">RELATED LINKS</span></span>

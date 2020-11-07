---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968922"
---
# <span data-ttu-id="8d741-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="8d741-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="8d741-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d741-102">SYNOPSIS</span></span>
<span data-ttu-id="8d741-103">調用管線以啟動它的執行。</span><span class="sxs-lookup"><span data-stu-id="8d741-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="8d741-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d741-104">SYNTAX</span></span>

### <span data-ttu-id="8d741-105">NewByName (預設) </span><span class="sxs-lookup"><span data-stu-id="8d741-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d741-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="8d741-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d741-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="8d741-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d741-108">說明</span><span class="sxs-lookup"><span data-stu-id="8d741-108">DESCRIPTION</span></span>
<span data-ttu-id="8d741-109">**Invoke AzSynapsePipeline** 命令會在指定的管線上啟動執行，並傳回該執行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d741-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="8d741-110">此 GUID 可以傳送至 **AzSynapsePipelineRun** 或 **AzSynapseActivityRun** ，以取得此執行的進一步詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8d741-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="8d741-111">示例</span><span class="sxs-lookup"><span data-stu-id="8d741-111">EXAMPLES</span></span>

### <span data-ttu-id="8d741-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8d741-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="8d741-113">這個命令會在工作區 ContosoWorkspace 中啟動名為 ContosoPipeline 的管道執行。</span><span class="sxs-lookup"><span data-stu-id="8d741-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="8d741-114">範例2</span><span class="sxs-lookup"><span data-stu-id="8d741-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="8d741-115">這個命令會在工作區 ContosoWorkspace 透過管線啟動稱為 ContosoPipeline 的管道執行。</span><span class="sxs-lookup"><span data-stu-id="8d741-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="8d741-116">範例3</span><span class="sxs-lookup"><span data-stu-id="8d741-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="8d741-117">這個命令會在工作區 ContosoWorkspace 透過管線啟動稱為 ContosoPipeline 的管道執行。</span><span class="sxs-lookup"><span data-stu-id="8d741-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="8d741-118">參數</span><span class="sxs-lookup"><span data-stu-id="8d741-118">PARAMETERS</span></span>

### <span data-ttu-id="8d741-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d741-119">-AsJob</span></span>
<span data-ttu-id="8d741-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8d741-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d741-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d741-121">-DefaultProfile</span></span>
<span data-ttu-id="8d741-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d741-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d741-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d741-123">-InputObject</span></span>
<span data-ttu-id="8d741-124">執行管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8d741-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="8d741-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="8d741-125">-IsRecovery</span></span>
<span data-ttu-id="8d741-126">[復原模式] 旗標。</span><span class="sxs-lookup"><span data-stu-id="8d741-126">Recovery mode flag.</span></span>
<span data-ttu-id="8d741-127">如果將 [復原模式] 設定為 true，則會執行指定的參照管線，而新的執行將會群組為相同的 groupId。</span><span class="sxs-lookup"><span data-stu-id="8d741-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="8d741-128">-參數</span><span class="sxs-lookup"><span data-stu-id="8d741-128">-Parameter</span></span>
<span data-ttu-id="8d741-129">管線執行的參數。</span><span class="sxs-lookup"><span data-stu-id="8d741-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="8d741-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="8d741-130">-ParameterFile</span></span>
<span data-ttu-id="8d741-131">含有管線執行參數的檔案名。</span><span class="sxs-lookup"><span data-stu-id="8d741-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="8d741-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="8d741-132">-PipelineName</span></span>
<span data-ttu-id="8d741-133">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="8d741-133">The pipeline name.</span></span>

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

### <span data-ttu-id="8d741-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="8d741-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="8d741-135">要重新執行的管線執行 ID。</span><span class="sxs-lookup"><span data-stu-id="8d741-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="8d741-136">如果指定了 [執行識別碼]，則會使用指定執行的參數來建立新的執行。</span><span class="sxs-lookup"><span data-stu-id="8d741-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="8d741-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="8d741-137">-StartActivityName</span></span>
<span data-ttu-id="8d741-138">在 [恢復] 模式中，[重新執行] 就會從這個活動開始。</span><span class="sxs-lookup"><span data-stu-id="8d741-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="8d741-139">如果未指定，所有活動將會執行。</span><span class="sxs-lookup"><span data-stu-id="8d741-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="8d741-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8d741-140">-WorkspaceName</span></span>
<span data-ttu-id="8d741-141">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d741-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8d741-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8d741-142">-WorkspaceObject</span></span>
<span data-ttu-id="8d741-143">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="8d741-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8d741-144">-確認</span><span class="sxs-lookup"><span data-stu-id="8d741-144">-Confirm</span></span>
<span data-ttu-id="8d741-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d741-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d741-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d741-146">-WhatIf</span></span>
<span data-ttu-id="8d741-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d741-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d741-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d741-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d741-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d741-149">CommonParameters</span></span>
<span data-ttu-id="8d741-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d741-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d741-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d741-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d741-152">輸入</span><span class="sxs-lookup"><span data-stu-id="8d741-152">INPUTS</span></span>

### <span data-ttu-id="8d741-153">PSPipelineResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="8d741-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="8d741-154">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="8d741-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8d741-155">輸出</span><span class="sxs-lookup"><span data-stu-id="8d741-155">OUTPUTS</span></span>

### <span data-ttu-id="8d741-156">PSCreateRunResponse 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="8d741-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="8d741-157">筆記</span><span class="sxs-lookup"><span data-stu-id="8d741-157">NOTES</span></span>

## <span data-ttu-id="8d741-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d741-158">RELATED LINKS</span></span>

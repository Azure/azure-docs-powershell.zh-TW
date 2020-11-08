---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138046"
---
# <span data-ttu-id="7a6a1-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="7a6a1-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="7a6a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6a1-103">停止在工作區中執行管線。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="7a6a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a6a1-104">SYNTAX</span></span>

### <span data-ttu-id="7a6a1-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="7a6a1-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a6a1-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7a6a1-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a6a1-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a6a1-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a6a1-108">說明</span><span class="sxs-lookup"><span data-stu-id="7a6a1-108">DESCRIPTION</span></span>
<span data-ttu-id="7a6a1-109">**AzSynapsePipelineRun** Cmdlet 會停止在使用管線執行 ID 指定的工作區中執行管線。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="7a6a1-110">示例</span><span class="sxs-lookup"><span data-stu-id="7a6a1-110">EXAMPLES</span></span>

### <span data-ttu-id="7a6a1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7a6a1-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="7a6a1-112">這個命令會在工作區 ContosoWorkspace 中停止執行 id 為 b9730a13-aa12-4926-a8b3-8e3a974ab0bd 的管道。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7a6a1-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7a6a1-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="7a6a1-114">這個命令會在工作區 ContosoWorkspace 透過管線停止執行含有 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd 的管道。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7a6a1-115">範例3</span><span class="sxs-lookup"><span data-stu-id="7a6a1-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="7a6a1-116">這個命令會在工作區 ContosoWorkspace 透過管線停止執行含有 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd 的管道。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7a6a1-117">參數</span><span class="sxs-lookup"><span data-stu-id="7a6a1-117">PARAMETERS</span></span>

### <span data-ttu-id="7a6a1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a6a1-118">-AsJob</span></span>
<span data-ttu-id="7a6a1-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a6a1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a6a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6a1-120">-DefaultProfile</span></span>
<span data-ttu-id="7a6a1-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a6a1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a6a1-122">-InputObject</span></span>
<span data-ttu-id="7a6a1-123">執行管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6a1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a6a1-124">-PassThru</span></span>
<span data-ttu-id="7a6a1-125">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7a6a1-126">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7a6a1-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="7a6a1-127">-PipelineRunId</span></span>
<span data-ttu-id="7a6a1-128">管線執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6a1-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a6a1-129">-WorkspaceName</span></span>
<span data-ttu-id="7a6a1-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6a1-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7a6a1-131">-WorkspaceObject</span></span>
<span data-ttu-id="7a6a1-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6a1-133">-確認</span><span class="sxs-lookup"><span data-stu-id="7a6a1-133">-Confirm</span></span>
<span data-ttu-id="7a6a1-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a6a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a6a1-135">-WhatIf</span></span>
<span data-ttu-id="7a6a1-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a6a1-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a6a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6a1-138">CommonParameters</span></span>
<span data-ttu-id="7a6a1-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6a1-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6a1-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7a6a1-141">INPUTS</span></span>

### <span data-ttu-id="7a6a1-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7a6a1-143">PSPipelineRun 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="7a6a1-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="7a6a1-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7a6a1-144">OUTPUTS</span></span>

### <span data-ttu-id="7a6a1-145">System.object</span><span class="sxs-lookup"><span data-stu-id="7a6a1-145">System.Boolean</span></span>

## <span data-ttu-id="7a6a1-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7a6a1-146">NOTES</span></span>

## <span data-ttu-id="7a6a1-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a6a1-147">RELATED LINKS</span></span>
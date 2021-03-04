---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: 607b251deff02ae6a74f0ceb5fc4f88a9c899688
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912194"
---
# <span data-ttu-id="bc858-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="bc858-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="bc858-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bc858-102">SYNOPSIS</span></span>
<span data-ttu-id="bc858-103">停止在工作區中執行管線。</span><span class="sxs-lookup"><span data-stu-id="bc858-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="bc858-104">語法</span><span class="sxs-lookup"><span data-stu-id="bc858-104">SYNTAX</span></span>

### <span data-ttu-id="bc858-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="bc858-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc858-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="bc858-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc858-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="bc858-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc858-108">描述</span><span class="sxs-lookup"><span data-stu-id="bc858-108">DESCRIPTION</span></span>
<span data-ttu-id="bc858-109">**Stop-AzSynapsePipelineRun** Cmdlet 會停止以管線執行識別碼指定的工作區中的管線執行。</span><span class="sxs-lookup"><span data-stu-id="bc858-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="bc858-110">例子</span><span class="sxs-lookup"><span data-stu-id="bc858-110">EXAMPLES</span></span>

### <span data-ttu-id="bc858-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bc858-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="bc858-112">此命令會停止使用工作區 ContosoWorkspace 中的 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd 執行管線。</span><span class="sxs-lookup"><span data-stu-id="bc858-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="bc858-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="bc858-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="bc858-114">此命令會以 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd 在工作區 ContosoWorkspace 中透過管線停止管線執行。</span><span class="sxs-lookup"><span data-stu-id="bc858-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="bc858-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="bc858-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="bc858-116">此命令會以 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd 在工作區 ContosoWorkspace 中透過管線停止管線執行。</span><span class="sxs-lookup"><span data-stu-id="bc858-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="bc858-117">參數</span><span class="sxs-lookup"><span data-stu-id="bc858-117">PARAMETERS</span></span>

### <span data-ttu-id="bc858-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc858-118">-AsJob</span></span>
<span data-ttu-id="bc858-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bc858-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc858-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc858-120">-DefaultProfile</span></span>
<span data-ttu-id="bc858-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc858-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc858-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc858-122">-InputObject</span></span>
<span data-ttu-id="bc858-123">管線執行相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bc858-123">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="bc858-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc858-124">-PassThru</span></span>
<span data-ttu-id="bc858-125">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="bc858-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bc858-126">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="bc858-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bc858-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="bc858-127">-PipelineRunId</span></span>
<span data-ttu-id="bc858-128">管線執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc858-128">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="bc858-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bc858-129">-WorkspaceName</span></span>
<span data-ttu-id="bc858-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc858-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bc858-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bc858-131">-WorkspaceObject</span></span>
<span data-ttu-id="bc858-132">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="bc858-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bc858-133">-確認</span><span class="sxs-lookup"><span data-stu-id="bc858-133">-Confirm</span></span>
<span data-ttu-id="bc858-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bc858-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc858-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc858-135">-WhatIf</span></span>
<span data-ttu-id="bc858-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc858-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc858-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc858-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc858-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc858-138">CommonParameters</span></span>
<span data-ttu-id="bc858-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bc858-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc858-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc858-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc858-141">輸入</span><span class="sxs-lookup"><span data-stu-id="bc858-141">INPUTS</span></span>

### <span data-ttu-id="bc858-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bc858-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bc858-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="bc858-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="bc858-144">輸出</span><span class="sxs-lookup"><span data-stu-id="bc858-144">OUTPUTS</span></span>

### <span data-ttu-id="bc858-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc858-145">System.Boolean</span></span>

## <span data-ttu-id="bc858-146">筆記</span><span class="sxs-lookup"><span data-stu-id="bc858-146">NOTES</span></span>

## <span data-ttu-id="bc858-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc858-147">RELATED LINKS</span></span>

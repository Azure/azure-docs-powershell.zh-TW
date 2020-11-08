---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139372"
---
# <span data-ttu-id="a1f09-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="a1f09-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="a1f09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1f09-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f09-103">從工作區移除管線。</span><span class="sxs-lookup"><span data-stu-id="a1f09-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="a1f09-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1f09-104">SYNTAX</span></span>

### <span data-ttu-id="a1f09-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a1f09-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a1f09-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1f09-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1f09-108">說明</span><span class="sxs-lookup"><span data-stu-id="a1f09-108">DESCRIPTION</span></span>
<span data-ttu-id="a1f09-109">**AzSynapsePipeline** Cmdlet 會從工作區移除管線。</span><span class="sxs-lookup"><span data-stu-id="a1f09-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="a1f09-110">示例</span><span class="sxs-lookup"><span data-stu-id="a1f09-110">EXAMPLES</span></span>

### <span data-ttu-id="a1f09-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a1f09-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="a1f09-112">這個 Cmdlet 會從名為 ContosoWorkspace 的工作區移除名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="a1f09-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a1f09-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a1f09-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="a1f09-114">這個 Cmdlet 會從名為 ContosoWorkspace 的工作區，移除名為 ContosoPipeline 的管道。</span><span class="sxs-lookup"><span data-stu-id="a1f09-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a1f09-115">範例3</span><span class="sxs-lookup"><span data-stu-id="a1f09-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="a1f09-116">這個 Cmdlet 會從名為 ContosoWorkspace 的工作區，移除名為 ContosoPipeline 的管道。</span><span class="sxs-lookup"><span data-stu-id="a1f09-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a1f09-117">參數</span><span class="sxs-lookup"><span data-stu-id="a1f09-117">PARAMETERS</span></span>

### <span data-ttu-id="a1f09-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1f09-118">-AsJob</span></span>
<span data-ttu-id="a1f09-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a1f09-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1f09-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f09-120">-DefaultProfile</span></span>
<span data-ttu-id="a1f09-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1f09-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1f09-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1f09-122">-InputObject</span></span>
<span data-ttu-id="a1f09-123">管線物件。</span><span class="sxs-lookup"><span data-stu-id="a1f09-123">The pipeline object.</span></span>

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

### <span data-ttu-id="a1f09-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1f09-124">-Name</span></span>
<span data-ttu-id="a1f09-125">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="a1f09-125">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1f09-126">-PassThru</span></span>
<span data-ttu-id="a1f09-127">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a1f09-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a1f09-128">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a1f09-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a1f09-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1f09-129">-WorkspaceName</span></span>
<span data-ttu-id="a1f09-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1f09-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a1f09-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a1f09-131">-WorkspaceObject</span></span>
<span data-ttu-id="a1f09-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a1f09-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1f09-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a1f09-133">-Confirm</span></span>
<span data-ttu-id="a1f09-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1f09-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f09-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f09-135">-WhatIf</span></span>
<span data-ttu-id="a1f09-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1f09-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1f09-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1f09-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1f09-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f09-138">CommonParameters</span></span>
<span data-ttu-id="a1f09-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1f09-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f09-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1f09-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f09-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a1f09-141">INPUTS</span></span>

### <span data-ttu-id="a1f09-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a1f09-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a1f09-143">PSPipelineResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a1f09-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="a1f09-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a1f09-144">OUTPUTS</span></span>

### <span data-ttu-id="a1f09-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a1f09-145">System.Boolean</span></span>

## <span data-ttu-id="a1f09-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a1f09-146">NOTES</span></span>

## <span data-ttu-id="a1f09-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1f09-147">RELATED LINKS</span></span>

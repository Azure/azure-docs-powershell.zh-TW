---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: b7bd7866ec6c6ff41a6ef7474b71cfc880e28f49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909373"
---
# <span data-ttu-id="d0b36-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="d0b36-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="d0b36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d0b36-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b36-103">從工作區移除管線。</span><span class="sxs-lookup"><span data-stu-id="d0b36-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="d0b36-104">語法</span><span class="sxs-lookup"><span data-stu-id="d0b36-104">SYNTAX</span></span>

### <span data-ttu-id="d0b36-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d0b36-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b36-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="d0b36-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b36-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0b36-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0b36-108">描述</span><span class="sxs-lookup"><span data-stu-id="d0b36-108">DESCRIPTION</span></span>
<span data-ttu-id="d0b36-109">**Remove-AzSynapsePipeline** Cmdlet 會從工作區移除管線。</span><span class="sxs-lookup"><span data-stu-id="d0b36-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="d0b36-110">例子</span><span class="sxs-lookup"><span data-stu-id="d0b36-110">EXAMPLES</span></span>

### <span data-ttu-id="d0b36-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d0b36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="d0b36-112">此 Cmdlet 會從名為 ContosoWorkspace 的工作區移除名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="d0b36-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d0b36-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="d0b36-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="d0b36-114">此 Cmdlet 會從名為 ContosoWorkspace 的工作區透過管線移除名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="d0b36-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="d0b36-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="d0b36-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="d0b36-116">此 Cmdlet 會從名為 ContosoWorkspace 的工作區透過管線移除名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="d0b36-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d0b36-117">參數</span><span class="sxs-lookup"><span data-stu-id="d0b36-117">PARAMETERS</span></span>

### <span data-ttu-id="d0b36-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0b36-118">-AsJob</span></span>
<span data-ttu-id="d0b36-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d0b36-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0b36-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b36-120">-DefaultProfile</span></span>
<span data-ttu-id="d0b36-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0b36-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b36-122">-強制</span><span class="sxs-lookup"><span data-stu-id="d0b36-122">-Force</span></span>
<span data-ttu-id="d0b36-123">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="d0b36-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d0b36-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0b36-124">-InputObject</span></span>
<span data-ttu-id="d0b36-125">管線物件。</span><span class="sxs-lookup"><span data-stu-id="d0b36-125">The pipeline object.</span></span>

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

### <span data-ttu-id="d0b36-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0b36-126">-Name</span></span>
<span data-ttu-id="d0b36-127">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="d0b36-127">The pipeline name.</span></span>

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

### <span data-ttu-id="d0b36-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0b36-128">-PassThru</span></span>
<span data-ttu-id="d0b36-129">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="d0b36-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d0b36-130">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="d0b36-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d0b36-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d0b36-131">-WorkspaceName</span></span>
<span data-ttu-id="d0b36-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0b36-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d0b36-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d0b36-133">-WorkspaceObject</span></span>
<span data-ttu-id="d0b36-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="d0b36-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d0b36-135">-確認</span><span class="sxs-lookup"><span data-stu-id="d0b36-135">-Confirm</span></span>
<span data-ttu-id="d0b36-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d0b36-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0b36-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b36-137">-WhatIf</span></span>
<span data-ttu-id="d0b36-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0b36-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b36-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0b36-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0b36-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b36-140">CommonParameters</span></span>
<span data-ttu-id="d0b36-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d0b36-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b36-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0b36-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b36-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d0b36-143">INPUTS</span></span>

### <span data-ttu-id="d0b36-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0b36-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d0b36-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="d0b36-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="d0b36-146">輸出</span><span class="sxs-lookup"><span data-stu-id="d0b36-146">OUTPUTS</span></span>

### <span data-ttu-id="d0b36-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0b36-147">System.Boolean</span></span>

## <span data-ttu-id="d0b36-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d0b36-148">NOTES</span></span>

## <span data-ttu-id="d0b36-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0b36-149">RELATED LINKS</span></span>

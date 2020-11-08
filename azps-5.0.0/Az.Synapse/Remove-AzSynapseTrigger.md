---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 0882789e230c012fe9f23dcdbeeb5378e9b91781
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138581"
---
# <span data-ttu-id="45959-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="45959-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="45959-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45959-102">SYNOPSIS</span></span>
<span data-ttu-id="45959-103">從工作區移除觸發程式。</span><span class="sxs-lookup"><span data-stu-id="45959-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="45959-104">句法</span><span class="sxs-lookup"><span data-stu-id="45959-104">SYNTAX</span></span>

### <span data-ttu-id="45959-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="45959-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45959-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="45959-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45959-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="45959-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45959-108">說明</span><span class="sxs-lookup"><span data-stu-id="45959-108">DESCRIPTION</span></span>
<span data-ttu-id="45959-109">AzSynapseTrigger Cmdlet 會從工作區中移除觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="45959-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="45959-110">示例</span><span class="sxs-lookup"><span data-stu-id="45959-110">EXAMPLES</span></span>

### <span data-ttu-id="45959-111">範例1</span><span class="sxs-lookup"><span data-stu-id="45959-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="45959-112">從工作區 ContosoWorkspace 中移除名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="45959-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="45959-113">範例2</span><span class="sxs-lookup"><span data-stu-id="45959-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="45959-114">從工作區 ContosoWorkspace 透過管線移除稱為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="45959-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="45959-115">範例3</span><span class="sxs-lookup"><span data-stu-id="45959-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="45959-116">從工作區 ContosoWorkspace 透過管線移除稱為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="45959-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="45959-117">參數</span><span class="sxs-lookup"><span data-stu-id="45959-117">PARAMETERS</span></span>

### <span data-ttu-id="45959-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45959-118">-AsJob</span></span>
<span data-ttu-id="45959-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="45959-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45959-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45959-120">-DefaultProfile</span></span>
<span data-ttu-id="45959-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45959-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45959-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45959-122">-InputObject</span></span>
<span data-ttu-id="45959-123">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="45959-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45959-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="45959-124">-Name</span></span>
<span data-ttu-id="45959-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="45959-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45959-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45959-126">-PassThru</span></span>
<span data-ttu-id="45959-127">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="45959-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="45959-128">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="45959-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="45959-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="45959-129">-WorkspaceName</span></span>
<span data-ttu-id="45959-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="45959-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="45959-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="45959-131">-WorkspaceObject</span></span>
<span data-ttu-id="45959-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="45959-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="45959-133">-確認</span><span class="sxs-lookup"><span data-stu-id="45959-133">-Confirm</span></span>
<span data-ttu-id="45959-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45959-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45959-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45959-135">-WhatIf</span></span>
<span data-ttu-id="45959-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45959-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45959-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45959-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45959-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45959-138">CommonParameters</span></span>
<span data-ttu-id="45959-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45959-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45959-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="45959-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45959-141">輸入</span><span class="sxs-lookup"><span data-stu-id="45959-141">INPUTS</span></span>

### <span data-ttu-id="45959-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="45959-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="45959-143">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="45959-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="45959-144">輸出</span><span class="sxs-lookup"><span data-stu-id="45959-144">OUTPUTS</span></span>

### <span data-ttu-id="45959-145">System.object</span><span class="sxs-lookup"><span data-stu-id="45959-145">System.Boolean</span></span>

## <span data-ttu-id="45959-146">筆記</span><span class="sxs-lookup"><span data-stu-id="45959-146">NOTES</span></span>

## <span data-ttu-id="45959-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="45959-147">RELATED LINKS</span></span>

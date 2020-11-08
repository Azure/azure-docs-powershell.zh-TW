---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138580"
---
# <span data-ttu-id="ef52f-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="ef52f-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="ef52f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef52f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef52f-103">將事件觸發程式取消訂閱至外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="ef52f-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="ef52f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef52f-104">SYNTAX</span></span>

### <span data-ttu-id="ef52f-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="ef52f-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef52f-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ef52f-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef52f-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef52f-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef52f-108">說明</span><span class="sxs-lookup"><span data-stu-id="ef52f-108">DESCRIPTION</span></span>
<span data-ttu-id="ef52f-109">**AzSynapseTriggerSubscription** Cmdlet 會將事件觸發程式從觸發程式的指定取消預訂給指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="ef52f-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="ef52f-110">示例</span><span class="sxs-lookup"><span data-stu-id="ef52f-110">EXAMPLES</span></span>

### <span data-ttu-id="ef52f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ef52f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="ef52f-112">這個命令會將觸發程式 ContosoTrigger 的觸發程式從觸發程式的指定取消訂閱至指定事件。</span><span class="sxs-lookup"><span data-stu-id="ef52f-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="ef52f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ef52f-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="ef52f-114">這個命令會將觸發程式 ContosoTrigger 的觸發程式從觸發程式中的指定事件取消訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef52f-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="ef52f-115">範例3</span><span class="sxs-lookup"><span data-stu-id="ef52f-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="ef52f-116">這個命令會將觸發程式 ContosoTrigger 的觸發程式從觸發程式中的指定事件取消訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef52f-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="ef52f-117">參數</span><span class="sxs-lookup"><span data-stu-id="ef52f-117">PARAMETERS</span></span>

### <span data-ttu-id="ef52f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef52f-118">-AsJob</span></span>
<span data-ttu-id="ef52f-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef52f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef52f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef52f-120">-DefaultProfile</span></span>
<span data-ttu-id="ef52f-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef52f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef52f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef52f-122">-InputObject</span></span>
<span data-ttu-id="ef52f-123">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="ef52f-123">The trigger object.</span></span>

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

### <span data-ttu-id="ef52f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef52f-124">-Name</span></span>
<span data-ttu-id="ef52f-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="ef52f-125">The trigger name.</span></span>

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

### <span data-ttu-id="ef52f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef52f-126">-PassThru</span></span>
<span data-ttu-id="ef52f-127">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="ef52f-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ef52f-128">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="ef52f-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ef52f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ef52f-129">-WorkspaceName</span></span>
<span data-ttu-id="ef52f-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef52f-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ef52f-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ef52f-131">-WorkspaceObject</span></span>
<span data-ttu-id="ef52f-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="ef52f-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ef52f-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ef52f-133">-Confirm</span></span>
<span data-ttu-id="ef52f-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef52f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef52f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef52f-135">-WhatIf</span></span>
<span data-ttu-id="ef52f-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef52f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef52f-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef52f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef52f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef52f-138">CommonParameters</span></span>
<span data-ttu-id="ef52f-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef52f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef52f-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ef52f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef52f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ef52f-141">INPUTS</span></span>

### <span data-ttu-id="ef52f-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="ef52f-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ef52f-143">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="ef52f-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="ef52f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ef52f-144">OUTPUTS</span></span>

### <span data-ttu-id="ef52f-145">System.object</span><span class="sxs-lookup"><span data-stu-id="ef52f-145">System.Boolean</span></span>

## <span data-ttu-id="ef52f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ef52f-146">NOTES</span></span>

## <span data-ttu-id="ef52f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef52f-147">RELATED LINKS</span></span>

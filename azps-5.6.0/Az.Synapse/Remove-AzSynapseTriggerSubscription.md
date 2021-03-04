---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: f331cad857fba20d72ffdd34f84f70a5d6392bff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914986"
---
# <span data-ttu-id="709aa-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="709aa-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="709aa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="709aa-102">SYNOPSIS</span></span>
<span data-ttu-id="709aa-103">取消訂閱外部服務事件的事件觸發。</span><span class="sxs-lookup"><span data-stu-id="709aa-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="709aa-104">語法</span><span class="sxs-lookup"><span data-stu-id="709aa-104">SYNTAX</span></span>

### <span data-ttu-id="709aa-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="709aa-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709aa-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="709aa-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="709aa-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="709aa-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="709aa-108">描述</span><span class="sxs-lookup"><span data-stu-id="709aa-108">DESCRIPTION</span></span>
<span data-ttu-id="709aa-109">**Remove-AzSynapseTriggerSubscription** Cmdlet 會取消訂閱觸發程式所指定外部服務事件的事件觸發程式。</span><span class="sxs-lookup"><span data-stu-id="709aa-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="709aa-110">例子</span><span class="sxs-lookup"><span data-stu-id="709aa-110">EXAMPLES</span></span>

### <span data-ttu-id="709aa-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="709aa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="709aa-112">此命令會取消訂閱名為 ContosoTrigger 的觸發程式，以從觸發程式觸發指定事件。</span><span class="sxs-lookup"><span data-stu-id="709aa-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="709aa-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="709aa-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="709aa-114">此命令會從觸發程式透過管道取消訂閱，將名為 ContosoTrigger 的事件觸發至指定的事件。</span><span class="sxs-lookup"><span data-stu-id="709aa-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="709aa-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="709aa-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="709aa-116">此命令會從觸發程式透過管道取消訂閱，將名為 ContosoTrigger 的事件觸發至指定的事件。</span><span class="sxs-lookup"><span data-stu-id="709aa-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="709aa-117">參數</span><span class="sxs-lookup"><span data-stu-id="709aa-117">PARAMETERS</span></span>

### <span data-ttu-id="709aa-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="709aa-118">-AsJob</span></span>
<span data-ttu-id="709aa-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="709aa-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="709aa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709aa-120">-DefaultProfile</span></span>
<span data-ttu-id="709aa-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="709aa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="709aa-122">-強制</span><span class="sxs-lookup"><span data-stu-id="709aa-122">-Force</span></span>
<span data-ttu-id="709aa-123">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="709aa-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="709aa-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="709aa-124">-InputObject</span></span>
<span data-ttu-id="709aa-125">觸發物件。</span><span class="sxs-lookup"><span data-stu-id="709aa-125">The trigger object.</span></span>

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

### <span data-ttu-id="709aa-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="709aa-126">-Name</span></span>
<span data-ttu-id="709aa-127">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="709aa-127">The trigger name.</span></span>

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

### <span data-ttu-id="709aa-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="709aa-128">-PassThru</span></span>
<span data-ttu-id="709aa-129">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="709aa-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="709aa-130">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="709aa-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="709aa-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="709aa-131">-WorkspaceName</span></span>
<span data-ttu-id="709aa-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="709aa-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="709aa-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="709aa-133">-WorkspaceObject</span></span>
<span data-ttu-id="709aa-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="709aa-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="709aa-135">-確認</span><span class="sxs-lookup"><span data-stu-id="709aa-135">-Confirm</span></span>
<span data-ttu-id="709aa-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="709aa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="709aa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="709aa-137">-WhatIf</span></span>
<span data-ttu-id="709aa-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="709aa-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="709aa-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="709aa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="709aa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709aa-140">CommonParameters</span></span>
<span data-ttu-id="709aa-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="709aa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709aa-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="709aa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709aa-143">輸入</span><span class="sxs-lookup"><span data-stu-id="709aa-143">INPUTS</span></span>

### <span data-ttu-id="709aa-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="709aa-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="709aa-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="709aa-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="709aa-146">輸出</span><span class="sxs-lookup"><span data-stu-id="709aa-146">OUTPUTS</span></span>

### <span data-ttu-id="709aa-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="709aa-147">System.Boolean</span></span>

## <span data-ttu-id="709aa-148">筆記</span><span class="sxs-lookup"><span data-stu-id="709aa-148">NOTES</span></span>

## <span data-ttu-id="709aa-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="709aa-149">RELATED LINKS</span></span>

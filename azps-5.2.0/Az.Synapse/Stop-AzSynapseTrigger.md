---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274471"
---
# <span data-ttu-id="221ef-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="221ef-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="221ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="221ef-102">SYNOPSIS</span></span>
<span data-ttu-id="221ef-103">停止工作區中的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="221ef-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="221ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="221ef-104">SYNTAX</span></span>

### <span data-ttu-id="221ef-105">StopByName (預設) </span><span class="sxs-lookup"><span data-stu-id="221ef-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="221ef-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="221ef-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="221ef-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="221ef-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="221ef-108">說明</span><span class="sxs-lookup"><span data-stu-id="221ef-108">DESCRIPTION</span></span>
<span data-ttu-id="221ef-109">**AzSynapseTrigger** Cmdlet 會在工作區中停止觸發程式。</span><span class="sxs-lookup"><span data-stu-id="221ef-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="221ef-110">如果觸發程式處於「已啟動」狀態，則該 Cmdlet 會停止觸發程式，而且不會再叫管線。</span><span class="sxs-lookup"><span data-stu-id="221ef-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="221ef-111">如果觸發程式已處於「已停止」狀態，則此 Cmdlet 沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="221ef-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="221ef-112">示例</span><span class="sxs-lookup"><span data-stu-id="221ef-112">EXAMPLES</span></span>

### <span data-ttu-id="221ef-113">範例1</span><span class="sxs-lookup"><span data-stu-id="221ef-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="221ef-114">在工作區 ContosoWorkspace 中停止名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="221ef-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="221ef-115">範例2</span><span class="sxs-lookup"><span data-stu-id="221ef-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="221ef-116">在工作區 ContosoWorkspace 透過管線停止名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="221ef-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="221ef-117">範例3</span><span class="sxs-lookup"><span data-stu-id="221ef-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="221ef-118">在工作區 ContosoWorkspace 透過管線停止名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="221ef-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="221ef-119">參數</span><span class="sxs-lookup"><span data-stu-id="221ef-119">PARAMETERS</span></span>

### <span data-ttu-id="221ef-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="221ef-120">-AsJob</span></span>
<span data-ttu-id="221ef-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="221ef-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="221ef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="221ef-122">-DefaultProfile</span></span>
<span data-ttu-id="221ef-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="221ef-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="221ef-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="221ef-124">-InputObject</span></span>
<span data-ttu-id="221ef-125">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="221ef-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="221ef-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="221ef-126">-Name</span></span>
<span data-ttu-id="221ef-127">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="221ef-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="221ef-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="221ef-128">-PassThru</span></span>
<span data-ttu-id="221ef-129">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="221ef-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="221ef-130">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="221ef-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="221ef-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="221ef-131">-WorkspaceName</span></span>
<span data-ttu-id="221ef-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="221ef-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="221ef-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="221ef-133">-WorkspaceObject</span></span>
<span data-ttu-id="221ef-134">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="221ef-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="221ef-135">-確認</span><span class="sxs-lookup"><span data-stu-id="221ef-135">-Confirm</span></span>
<span data-ttu-id="221ef-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="221ef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="221ef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="221ef-137">-WhatIf</span></span>
<span data-ttu-id="221ef-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="221ef-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="221ef-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="221ef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="221ef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="221ef-140">CommonParameters</span></span>
<span data-ttu-id="221ef-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="221ef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="221ef-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="221ef-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="221ef-143">輸入</span><span class="sxs-lookup"><span data-stu-id="221ef-143">INPUTS</span></span>

### <span data-ttu-id="221ef-144">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="221ef-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="221ef-145">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="221ef-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="221ef-146">輸出</span><span class="sxs-lookup"><span data-stu-id="221ef-146">OUTPUTS</span></span>

### <span data-ttu-id="221ef-147">System.object</span><span class="sxs-lookup"><span data-stu-id="221ef-147">System.Boolean</span></span>

## <span data-ttu-id="221ef-148">筆記</span><span class="sxs-lookup"><span data-stu-id="221ef-148">NOTES</span></span>

## <span data-ttu-id="221ef-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="221ef-149">RELATED LINKS</span></span>

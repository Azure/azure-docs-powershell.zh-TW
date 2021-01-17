---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438912"
---
# <span data-ttu-id="cb727-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="cb727-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="cb727-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb727-102">SYNOPSIS</span></span>
<span data-ttu-id="cb727-103">在工作區中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="cb727-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="cb727-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb727-104">SYNTAX</span></span>

### <span data-ttu-id="cb727-105">StartByName (預設) </span><span class="sxs-lookup"><span data-stu-id="cb727-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb727-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="cb727-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb727-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb727-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb727-108">說明</span><span class="sxs-lookup"><span data-stu-id="cb727-108">DESCRIPTION</span></span>
<span data-ttu-id="cb727-109">**Start AzSynapseTrigger** Cmdlet 會在工作區中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="cb727-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="cb727-110">如果觸發程式處於「已停止」狀態，則該 Cmdlet 會啟動觸發程式，而且最終會根據其定義來調用管線。</span><span class="sxs-lookup"><span data-stu-id="cb727-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="cb727-111">如果觸發程式已處於「已啟動」狀態，則此 Cmdlet 不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="cb727-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="cb727-112">示例</span><span class="sxs-lookup"><span data-stu-id="cb727-112">EXAMPLES</span></span>

### <span data-ttu-id="cb727-113">範例1</span><span class="sxs-lookup"><span data-stu-id="cb727-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="cb727-114">在工作區 ContosoWorkspace 中啟動名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="cb727-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cb727-115">範例2</span><span class="sxs-lookup"><span data-stu-id="cb727-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="cb727-116">在工作區 ContosoWorkspace 透過管線啟動名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="cb727-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="cb727-117">範例3</span><span class="sxs-lookup"><span data-stu-id="cb727-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="cb727-118">在工作區 ContosoWorkspace 透過管線啟動名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="cb727-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cb727-119">參數</span><span class="sxs-lookup"><span data-stu-id="cb727-119">PARAMETERS</span></span>

### <span data-ttu-id="cb727-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb727-120">-AsJob</span></span>
<span data-ttu-id="cb727-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb727-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb727-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb727-122">-DefaultProfile</span></span>
<span data-ttu-id="cb727-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb727-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb727-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb727-124">-InputObject</span></span>
<span data-ttu-id="cb727-125">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="cb727-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb727-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb727-126">-Name</span></span>
<span data-ttu-id="cb727-127">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="cb727-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb727-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb727-128">-PassThru</span></span>
<span data-ttu-id="cb727-129">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="cb727-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cb727-130">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="cb727-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cb727-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb727-131">-WorkspaceName</span></span>
<span data-ttu-id="cb727-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb727-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb727-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cb727-133">-WorkspaceObject</span></span>
<span data-ttu-id="cb727-134">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="cb727-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb727-135">-確認</span><span class="sxs-lookup"><span data-stu-id="cb727-135">-Confirm</span></span>
<span data-ttu-id="cb727-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb727-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb727-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb727-137">-WhatIf</span></span>
<span data-ttu-id="cb727-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb727-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb727-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb727-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb727-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb727-140">CommonParameters</span></span>
<span data-ttu-id="cb727-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb727-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb727-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb727-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb727-143">輸入</span><span class="sxs-lookup"><span data-stu-id="cb727-143">INPUTS</span></span>

### <span data-ttu-id="cb727-144">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="cb727-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cb727-145">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="cb727-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="cb727-146">輸出</span><span class="sxs-lookup"><span data-stu-id="cb727-146">OUTPUTS</span></span>

### <span data-ttu-id="cb727-147">System.object</span><span class="sxs-lookup"><span data-stu-id="cb727-147">System.Boolean</span></span>

## <span data-ttu-id="cb727-148">筆記</span><span class="sxs-lookup"><span data-stu-id="cb727-148">NOTES</span></span>

## <span data-ttu-id="cb727-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb727-149">RELATED LINKS</span></span>

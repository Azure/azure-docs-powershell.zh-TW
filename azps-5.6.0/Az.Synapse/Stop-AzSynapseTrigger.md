---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 94773a882a4bb2d29712fff6796d34cff6254df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912182"
---
# <span data-ttu-id="7f88e-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="7f88e-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="7f88e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7f88e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f88e-103">停止工作區中的觸發。</span><span class="sxs-lookup"><span data-stu-id="7f88e-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="7f88e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7f88e-104">SYNTAX</span></span>

### <span data-ttu-id="7f88e-105">StopByName (預設) </span><span class="sxs-lookup"><span data-stu-id="7f88e-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f88e-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="7f88e-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f88e-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="7f88e-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f88e-108">描述</span><span class="sxs-lookup"><span data-stu-id="7f88e-108">DESCRIPTION</span></span>
<span data-ttu-id="7f88e-109">**Stop-AzSynapseTrigger Cmdlet** 會停止工作區中的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="7f88e-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="7f88e-110">如果觸發程式位於 'Started' 狀態，Cmdlet 會停止觸發程式，不再會啟動管線。</span><span class="sxs-lookup"><span data-stu-id="7f88e-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="7f88e-111">如果觸發人已經進入 '已停止' 狀態，此 Cmdlet 沒有作用。</span><span class="sxs-lookup"><span data-stu-id="7f88e-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="7f88e-112">例子</span><span class="sxs-lookup"><span data-stu-id="7f88e-112">EXAMPLES</span></span>

### <span data-ttu-id="7f88e-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="7f88e-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="7f88e-114">在工作區 ContosoWorkspace 中停止名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="7f88e-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7f88e-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="7f88e-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="7f88e-116">在工作區 ContosoWorkspace 中透過管線停止名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="7f88e-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7f88e-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="7f88e-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="7f88e-118">在工作區 ContosoWorkspace 中透過管線停止名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="7f88e-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7f88e-119">參數</span><span class="sxs-lookup"><span data-stu-id="7f88e-119">PARAMETERS</span></span>

### <span data-ttu-id="7f88e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f88e-120">-AsJob</span></span>
<span data-ttu-id="7f88e-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7f88e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f88e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f88e-122">-DefaultProfile</span></span>
<span data-ttu-id="7f88e-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f88e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f88e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f88e-124">-InputObject</span></span>
<span data-ttu-id="7f88e-125">觸發物件。</span><span class="sxs-lookup"><span data-stu-id="7f88e-125">The trigger object.</span></span>

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

### <span data-ttu-id="7f88e-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f88e-126">-Name</span></span>
<span data-ttu-id="7f88e-127">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="7f88e-127">The trigger name.</span></span>

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

### <span data-ttu-id="7f88e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f88e-128">-PassThru</span></span>
<span data-ttu-id="7f88e-129">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="7f88e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7f88e-130">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="7f88e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7f88e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7f88e-131">-WorkspaceName</span></span>
<span data-ttu-id="7f88e-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f88e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7f88e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7f88e-133">-WorkspaceObject</span></span>
<span data-ttu-id="7f88e-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="7f88e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7f88e-135">-確認</span><span class="sxs-lookup"><span data-stu-id="7f88e-135">-Confirm</span></span>
<span data-ttu-id="7f88e-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7f88e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f88e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f88e-137">-WhatIf</span></span>
<span data-ttu-id="7f88e-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f88e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f88e-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f88e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f88e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f88e-140">CommonParameters</span></span>
<span data-ttu-id="7f88e-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7f88e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f88e-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f88e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f88e-143">輸入</span><span class="sxs-lookup"><span data-stu-id="7f88e-143">INPUTS</span></span>

### <span data-ttu-id="7f88e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7f88e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7f88e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="7f88e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="7f88e-146">輸出</span><span class="sxs-lookup"><span data-stu-id="7f88e-146">OUTPUTS</span></span>

### <span data-ttu-id="7f88e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f88e-147">System.Boolean</span></span>

## <span data-ttu-id="7f88e-148">筆記</span><span class="sxs-lookup"><span data-stu-id="7f88e-148">NOTES</span></span>

## <span data-ttu-id="7f88e-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f88e-149">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: 39801db0d1cd400fa88868b87098260c9148daa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912197"
---
# <span data-ttu-id="36b1d-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="36b1d-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="36b1d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="36b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="36b1d-103">在工作區中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="36b1d-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="36b1d-104">語法</span><span class="sxs-lookup"><span data-stu-id="36b1d-104">SYNTAX</span></span>

### <span data-ttu-id="36b1d-105">StartByName (預設) </span><span class="sxs-lookup"><span data-stu-id="36b1d-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b1d-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="36b1d-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b1d-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="36b1d-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b1d-108">描述</span><span class="sxs-lookup"><span data-stu-id="36b1d-108">DESCRIPTION</span></span>
<span data-ttu-id="36b1d-109">**Start-AzSynapseTrigger Cmdlet** 會啟動工作區中的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="36b1d-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="36b1d-110">如果觸發程式為 '已停止' 狀態，Cmdlet 會啟動觸發程式，最後會根據定義來叫用管線。</span><span class="sxs-lookup"><span data-stu-id="36b1d-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="36b1d-111">如果觸發已進入 '開始' 狀態，此 Cmdlet 將無效。</span><span class="sxs-lookup"><span data-stu-id="36b1d-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="36b1d-112">例子</span><span class="sxs-lookup"><span data-stu-id="36b1d-112">EXAMPLES</span></span>

### <span data-ttu-id="36b1d-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="36b1d-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="36b1d-114">在工作區 ContosoWorkspace 中啟動名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="36b1d-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="36b1d-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="36b1d-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="36b1d-116">在工作區 ContosoWorkspace 中透過管線啟動名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="36b1d-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="36b1d-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="36b1d-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="36b1d-118">在工作區 ContosoWorkspace 中透過管線啟動名為 ContosoTrigger 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="36b1d-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="36b1d-119">參數</span><span class="sxs-lookup"><span data-stu-id="36b1d-119">PARAMETERS</span></span>

### <span data-ttu-id="36b1d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36b1d-120">-AsJob</span></span>
<span data-ttu-id="36b1d-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36b1d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36b1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b1d-122">-DefaultProfile</span></span>
<span data-ttu-id="36b1d-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="36b1d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36b1d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36b1d-124">-InputObject</span></span>
<span data-ttu-id="36b1d-125">觸發物件。</span><span class="sxs-lookup"><span data-stu-id="36b1d-125">The trigger object.</span></span>

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

### <span data-ttu-id="36b1d-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="36b1d-126">-Name</span></span>
<span data-ttu-id="36b1d-127">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="36b1d-127">The trigger name.</span></span>

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

### <span data-ttu-id="36b1d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36b1d-128">-PassThru</span></span>
<span data-ttu-id="36b1d-129">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="36b1d-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="36b1d-130">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="36b1d-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="36b1d-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="36b1d-131">-WorkspaceName</span></span>
<span data-ttu-id="36b1d-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="36b1d-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="36b1d-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="36b1d-133">-WorkspaceObject</span></span>
<span data-ttu-id="36b1d-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="36b1d-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="36b1d-135">-確認</span><span class="sxs-lookup"><span data-stu-id="36b1d-135">-Confirm</span></span>
<span data-ttu-id="36b1d-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="36b1d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36b1d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b1d-137">-WhatIf</span></span>
<span data-ttu-id="36b1d-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36b1d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36b1d-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36b1d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36b1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b1d-140">CommonParameters</span></span>
<span data-ttu-id="36b1d-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="36b1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b1d-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36b1d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b1d-143">輸入</span><span class="sxs-lookup"><span data-stu-id="36b1d-143">INPUTS</span></span>

### <span data-ttu-id="36b1d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="36b1d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="36b1d-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="36b1d-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="36b1d-146">輸出</span><span class="sxs-lookup"><span data-stu-id="36b1d-146">OUTPUTS</span></span>

### <span data-ttu-id="36b1d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36b1d-147">System.Boolean</span></span>

## <span data-ttu-id="36b1d-148">筆記</span><span class="sxs-lookup"><span data-stu-id="36b1d-148">NOTES</span></span>

## <span data-ttu-id="36b1d-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="36b1d-149">RELATED LINKS</span></span>

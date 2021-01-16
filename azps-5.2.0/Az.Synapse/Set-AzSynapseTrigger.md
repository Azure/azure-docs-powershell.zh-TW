---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281552"
---
# <span data-ttu-id="c0c49-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="c0c49-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="c0c49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0c49-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c49-103">在工作區中建立觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0c49-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="c0c49-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0c49-104">SYNTAX</span></span>

### <span data-ttu-id="c0c49-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="c0c49-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c49-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="c0c49-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c49-107">說明</span><span class="sxs-lookup"><span data-stu-id="c0c49-107">DESCRIPTION</span></span>
<span data-ttu-id="c0c49-108">**AzSynapseTrigger** Cmdlet 會在工作區中建立觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0c49-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="c0c49-109">觸發程式是在「已停止」狀態中建立，這表示它們不會立即開始喚醒它們所參照的管線。</span><span class="sxs-lookup"><span data-stu-id="c0c49-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="c0c49-110">示例</span><span class="sxs-lookup"><span data-stu-id="c0c49-110">EXAMPLES</span></span>

### <span data-ttu-id="c0c49-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c0c49-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="c0c49-112">在工作區 ContosoWorkspace 中建立名為 ContosoTrigger 的新觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0c49-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="c0c49-113">觸發程式是以「已停止」狀態建立，表示它不會立即啟動。</span><span class="sxs-lookup"><span data-stu-id="c0c49-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="c0c49-114">您可以使用 Cmdlet 來啟動觸發程式 `Start-AzDataFactoryV2Trigger` 。</span><span class="sxs-lookup"><span data-stu-id="c0c49-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="c0c49-115">範例2</span><span class="sxs-lookup"><span data-stu-id="c0c49-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="c0c49-116">透過管線在工作區 ContosoWorkspace 中建立名為 ContosoTrigger 的新觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0c49-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="c0c49-117">觸發程式是以「已停止」狀態建立，表示它不會立即啟動。</span><span class="sxs-lookup"><span data-stu-id="c0c49-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="c0c49-118">您可以使用 Cmdlet 來啟動觸發程式 `Start-AzDataFactoryV2Trigger` 。</span><span class="sxs-lookup"><span data-stu-id="c0c49-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="c0c49-119">參數</span><span class="sxs-lookup"><span data-stu-id="c0c49-119">PARAMETERS</span></span>

### <span data-ttu-id="c0c49-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0c49-120">-AsJob</span></span>
<span data-ttu-id="c0c49-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0c49-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0c49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c49-122">-DefaultProfile</span></span>
<span data-ttu-id="c0c49-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0c49-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c49-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c0c49-124">-DefinitionFile</span></span>
<span data-ttu-id="c0c49-125">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="c0c49-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c49-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0c49-126">-Name</span></span>
<span data-ttu-id="c0c49-127">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="c0c49-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c49-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0c49-128">-WorkspaceName</span></span>
<span data-ttu-id="c0c49-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0c49-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c49-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0c49-130">-WorkspaceObject</span></span>
<span data-ttu-id="c0c49-131">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="c0c49-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c49-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c0c49-132">-Confirm</span></span>
<span data-ttu-id="c0c49-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0c49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c49-134">-WhatIf</span></span>
<span data-ttu-id="c0c49-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0c49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c49-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0c49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c49-137">CommonParameters</span></span>
<span data-ttu-id="c0c49-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0c49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c49-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0c49-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c49-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c0c49-140">INPUTS</span></span>

### <span data-ttu-id="c0c49-141">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c0c49-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c0c49-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c0c49-142">OUTPUTS</span></span>

### <span data-ttu-id="c0c49-143">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c0c49-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="c0c49-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c0c49-144">NOTES</span></span>

## <span data-ttu-id="c0c49-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0c49-145">RELATED LINKS</span></span>

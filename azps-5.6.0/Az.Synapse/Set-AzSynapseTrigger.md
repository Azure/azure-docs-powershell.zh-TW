---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 0852cbbce26e1f95bfb75975418fae30038316ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912209"
---
# <span data-ttu-id="225d0-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="225d0-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="225d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="225d0-102">SYNOPSIS</span></span>
<span data-ttu-id="225d0-103">在工作區中建立觸發。</span><span class="sxs-lookup"><span data-stu-id="225d0-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="225d0-104">語法</span><span class="sxs-lookup"><span data-stu-id="225d0-104">SYNTAX</span></span>

### <span data-ttu-id="225d0-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="225d0-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="225d0-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="225d0-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="225d0-107">描述</span><span class="sxs-lookup"><span data-stu-id="225d0-107">DESCRIPTION</span></span>
<span data-ttu-id="225d0-108">**Set-AzSynapseTrigger Cmdlet** 會建立工作區中的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="225d0-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="225d0-109">觸發會以 '已停止' 狀態建立，這表示它們不會立即開始叫用他們參照的管道。</span><span class="sxs-lookup"><span data-stu-id="225d0-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="225d0-110">例子</span><span class="sxs-lookup"><span data-stu-id="225d0-110">EXAMPLES</span></span>

### <span data-ttu-id="225d0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="225d0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="225d0-112">在工作區 ContosoWorkspace 中建立名為 ContosoTrigger 的新觸發程式。</span><span class="sxs-lookup"><span data-stu-id="225d0-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="225d0-113">觸發會以 '已停止' 狀態建立，這表示它不會立即開始。</span><span class="sxs-lookup"><span data-stu-id="225d0-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="225d0-114">可以使用 `Start-AzDataFactoryV2Trigger` Cmdlet 啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="225d0-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="225d0-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="225d0-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="225d0-116">透過管線在工作區 ContosoWorkspace 中建立名為 ContosoTrigger 的新觸發程式。</span><span class="sxs-lookup"><span data-stu-id="225d0-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="225d0-117">觸發會以 '已停止' 狀態建立，這表示它不會立即開始。</span><span class="sxs-lookup"><span data-stu-id="225d0-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="225d0-118">可以使用 `Start-AzDataFactoryV2Trigger` Cmdlet 啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="225d0-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="225d0-119">參數</span><span class="sxs-lookup"><span data-stu-id="225d0-119">PARAMETERS</span></span>

### <span data-ttu-id="225d0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="225d0-120">-AsJob</span></span>
<span data-ttu-id="225d0-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="225d0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="225d0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225d0-122">-DefaultProfile</span></span>
<span data-ttu-id="225d0-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="225d0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="225d0-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="225d0-124">-DefinitionFile</span></span>
<span data-ttu-id="225d0-125">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="225d0-125">The JSON file path.</span></span>

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

### <span data-ttu-id="225d0-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="225d0-126">-Name</span></span>
<span data-ttu-id="225d0-127">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="225d0-127">The trigger name.</span></span>

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

### <span data-ttu-id="225d0-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="225d0-128">-WorkspaceName</span></span>
<span data-ttu-id="225d0-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="225d0-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="225d0-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="225d0-130">-WorkspaceObject</span></span>
<span data-ttu-id="225d0-131">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="225d0-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="225d0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="225d0-132">-Confirm</span></span>
<span data-ttu-id="225d0-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="225d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="225d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="225d0-134">-WhatIf</span></span>
<span data-ttu-id="225d0-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="225d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="225d0-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="225d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="225d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225d0-137">CommonParameters</span></span>
<span data-ttu-id="225d0-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="225d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225d0-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="225d0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225d0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="225d0-140">INPUTS</span></span>

### <span data-ttu-id="225d0-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="225d0-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="225d0-142">輸出</span><span class="sxs-lookup"><span data-stu-id="225d0-142">OUTPUTS</span></span>

### <span data-ttu-id="225d0-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="225d0-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="225d0-144">筆記</span><span class="sxs-lookup"><span data-stu-id="225d0-144">NOTES</span></span>

## <span data-ttu-id="225d0-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="225d0-145">RELATED LINKS</span></span>

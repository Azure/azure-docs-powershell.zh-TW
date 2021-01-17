---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288347"
---
# <span data-ttu-id="a0997-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="a0997-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="a0997-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0997-102">SYNOPSIS</span></span>
<span data-ttu-id="a0997-103">為外部服務事件訂閱事件觸發程式。</span><span class="sxs-lookup"><span data-stu-id="a0997-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="a0997-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0997-104">SYNTAX</span></span>

### <span data-ttu-id="a0997-105">AddByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a0997-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0997-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="a0997-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0997-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0997-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0997-108">說明</span><span class="sxs-lookup"><span data-stu-id="a0997-108">DESCRIPTION</span></span>
<span data-ttu-id="a0997-109">**AzSynapseTriggerSubscription** Cmdlet 會將事件觸發程式從觸發程式的指定訂閱至指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="a0997-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="a0997-110">示例</span><span class="sxs-lookup"><span data-stu-id="a0997-110">EXAMPLES</span></span>

### <span data-ttu-id="a0997-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a0997-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="a0997-112">這個命令會將觸發程式（名為 ContosoTrigger 的觸發程式）訂閱到觸發程式的指定事件。</span><span class="sxs-lookup"><span data-stu-id="a0997-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="a0997-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a0997-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="a0997-114">這個命令會將觸發程式（名為 ContosoTrigger 的觸發程式）從觸發程式（透過管線）的指定事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0997-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="a0997-115">範例3</span><span class="sxs-lookup"><span data-stu-id="a0997-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="a0997-116">這個命令會將觸發程式（名為 ContosoTrigger 的觸發程式）從觸發程式（透過管線）的指定事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0997-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="a0997-117">參數</span><span class="sxs-lookup"><span data-stu-id="a0997-117">PARAMETERS</span></span>

### <span data-ttu-id="a0997-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0997-118">-AsJob</span></span>
<span data-ttu-id="a0997-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0997-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0997-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0997-120">-DefaultProfile</span></span>
<span data-ttu-id="a0997-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0997-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0997-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0997-122">-InputObject</span></span>
<span data-ttu-id="a0997-123">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="a0997-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0997-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0997-124">-Name</span></span>
<span data-ttu-id="a0997-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="a0997-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0997-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a0997-126">-WorkspaceName</span></span>
<span data-ttu-id="a0997-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0997-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0997-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a0997-128">-WorkspaceObject</span></span>
<span data-ttu-id="a0997-129">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a0997-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0997-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a0997-130">-Confirm</span></span>
<span data-ttu-id="a0997-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0997-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0997-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0997-132">-WhatIf</span></span>
<span data-ttu-id="a0997-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0997-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0997-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0997-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0997-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0997-135">CommonParameters</span></span>
<span data-ttu-id="a0997-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0997-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0997-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0997-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0997-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a0997-138">INPUTS</span></span>

### <span data-ttu-id="a0997-139">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a0997-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a0997-140">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a0997-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="a0997-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a0997-141">OUTPUTS</span></span>

### <span data-ttu-id="a0997-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a0997-142">System.Object</span></span>
## <span data-ttu-id="a0997-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a0997-143">NOTES</span></span>

## <span data-ttu-id="a0997-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0997-144">RELATED LINKS</span></span>

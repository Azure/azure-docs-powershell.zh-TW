---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130419"
---
# <span data-ttu-id="902f3-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="902f3-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="902f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="902f3-102">SYNOPSIS</span></span>
<span data-ttu-id="902f3-103">為外部服務事件訂閱事件觸發程式。</span><span class="sxs-lookup"><span data-stu-id="902f3-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="902f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="902f3-104">SYNTAX</span></span>

### <span data-ttu-id="902f3-105">AddByName (預設) </span><span class="sxs-lookup"><span data-stu-id="902f3-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902f3-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="902f3-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902f3-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="902f3-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="902f3-108">說明</span><span class="sxs-lookup"><span data-stu-id="902f3-108">DESCRIPTION</span></span>
<span data-ttu-id="902f3-109">**AzSynapseTriggerSubscription** Cmdlet 會將事件觸發程式從觸發程式的指定訂閱至指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="902f3-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="902f3-110">示例</span><span class="sxs-lookup"><span data-stu-id="902f3-110">EXAMPLES</span></span>

### <span data-ttu-id="902f3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="902f3-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="902f3-112">這個命令會將觸發程式（名為 ContosoTrigger 的觸發程式）訂閱到觸發程式的指定事件。</span><span class="sxs-lookup"><span data-stu-id="902f3-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="902f3-113">範例2</span><span class="sxs-lookup"><span data-stu-id="902f3-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="902f3-114">這個命令會將觸發程式（名為 ContosoTrigger 的觸發程式）從觸發程式（透過管線）的指定事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="902f3-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="902f3-115">範例3</span><span class="sxs-lookup"><span data-stu-id="902f3-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="902f3-116">這個命令會將觸發程式（名為 ContosoTrigger 的觸發程式）從觸發程式（透過管線）的指定事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="902f3-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="902f3-117">參數</span><span class="sxs-lookup"><span data-stu-id="902f3-117">PARAMETERS</span></span>

### <span data-ttu-id="902f3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="902f3-118">-AsJob</span></span>
<span data-ttu-id="902f3-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="902f3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="902f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902f3-120">-DefaultProfile</span></span>
<span data-ttu-id="902f3-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="902f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="902f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="902f3-122">-InputObject</span></span>
<span data-ttu-id="902f3-123">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="902f3-123">The trigger object.</span></span>

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

### <span data-ttu-id="902f3-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="902f3-124">-Name</span></span>
<span data-ttu-id="902f3-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="902f3-125">The trigger name.</span></span>

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

### <span data-ttu-id="902f3-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="902f3-126">-WorkspaceName</span></span>
<span data-ttu-id="902f3-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="902f3-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="902f3-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="902f3-128">-WorkspaceObject</span></span>
<span data-ttu-id="902f3-129">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="902f3-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="902f3-130">-確認</span><span class="sxs-lookup"><span data-stu-id="902f3-130">-Confirm</span></span>
<span data-ttu-id="902f3-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="902f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="902f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="902f3-132">-WhatIf</span></span>
<span data-ttu-id="902f3-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="902f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="902f3-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="902f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="902f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902f3-135">CommonParameters</span></span>
<span data-ttu-id="902f3-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="902f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902f3-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="902f3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902f3-138">輸入</span><span class="sxs-lookup"><span data-stu-id="902f3-138">INPUTS</span></span>

### <span data-ttu-id="902f3-139">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="902f3-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="902f3-140">PSTriggerResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="902f3-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="902f3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="902f3-141">OUTPUTS</span></span>

### <span data-ttu-id="902f3-142">System.object</span><span class="sxs-lookup"><span data-stu-id="902f3-142">System.Object</span></span>
## <span data-ttu-id="902f3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="902f3-143">NOTES</span></span>

## <span data-ttu-id="902f3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="902f3-144">RELATED LINKS</span></span>

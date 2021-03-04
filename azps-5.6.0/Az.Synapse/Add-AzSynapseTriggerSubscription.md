---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: d9ff2e46b7b4ccf7b3d2fafd1aa8142efd0675b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909266"
---
# <span data-ttu-id="53a4b-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="53a4b-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="53a4b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="53a4b-103">訂閱事件觸發事件至外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="53a4b-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="53a4b-104">語法</span><span class="sxs-lookup"><span data-stu-id="53a4b-104">SYNTAX</span></span>

### <span data-ttu-id="53a4b-105">AddByName (預設) </span><span class="sxs-lookup"><span data-stu-id="53a4b-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a4b-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="53a4b-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a4b-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="53a4b-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a4b-108">描述</span><span class="sxs-lookup"><span data-stu-id="53a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="53a4b-109">**Add-AzSynapseTriggerSubscription** Cmdlet 會從觸發程式訂閱事件觸發程式所指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="53a4b-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="53a4b-110">例子</span><span class="sxs-lookup"><span data-stu-id="53a4b-110">EXAMPLES</span></span>

### <span data-ttu-id="53a4b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="53a4b-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="53a4b-112">此命令會訂閱觸發程式 ContosoTri用觸發程式，以從觸發程式指定事件。</span><span class="sxs-lookup"><span data-stu-id="53a4b-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="53a4b-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="53a4b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="53a4b-114">此命令會訂閱名為 ContosoTrigger 的觸發程式，以透過管道從觸發程式觸發特定事件。</span><span class="sxs-lookup"><span data-stu-id="53a4b-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="53a4b-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="53a4b-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="53a4b-116">此命令會訂閱名為 ContosoTrigger 的觸發程式，以透過管道從觸發程式觸發特定事件。</span><span class="sxs-lookup"><span data-stu-id="53a4b-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="53a4b-117">參數</span><span class="sxs-lookup"><span data-stu-id="53a4b-117">PARAMETERS</span></span>

### <span data-ttu-id="53a4b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53a4b-118">-AsJob</span></span>
<span data-ttu-id="53a4b-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="53a4b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53a4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a4b-120">-DefaultProfile</span></span>
<span data-ttu-id="53a4b-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53a4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53a4b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53a4b-122">-InputObject</span></span>
<span data-ttu-id="53a4b-123">觸發物件。</span><span class="sxs-lookup"><span data-stu-id="53a4b-123">The trigger object.</span></span>

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

### <span data-ttu-id="53a4b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="53a4b-124">-Name</span></span>
<span data-ttu-id="53a4b-125">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="53a4b-125">The trigger name.</span></span>

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

### <span data-ttu-id="53a4b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53a4b-126">-WorkspaceName</span></span>
<span data-ttu-id="53a4b-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="53a4b-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="53a4b-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53a4b-128">-WorkspaceObject</span></span>
<span data-ttu-id="53a4b-129">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="53a4b-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="53a4b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="53a4b-130">-Confirm</span></span>
<span data-ttu-id="53a4b-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="53a4b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a4b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a4b-132">-WhatIf</span></span>
<span data-ttu-id="53a4b-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53a4b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a4b-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53a4b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a4b-135">CommonParameters</span></span>
<span data-ttu-id="53a4b-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53a4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a4b-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53a4b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a4b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="53a4b-138">INPUTS</span></span>

### <span data-ttu-id="53a4b-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="53a4b-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="53a4b-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="53a4b-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="53a4b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="53a4b-141">OUTPUTS</span></span>

### <span data-ttu-id="53a4b-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="53a4b-142">System.Object</span></span>
## <span data-ttu-id="53a4b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="53a4b-143">NOTES</span></span>

## <span data-ttu-id="53a4b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="53a4b-144">RELATED LINKS</span></span>

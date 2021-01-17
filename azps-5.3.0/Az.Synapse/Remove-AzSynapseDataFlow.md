---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438968"
---
# <span data-ttu-id="357c1-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="357c1-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="357c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="357c1-102">SYNOPSIS</span></span>
<span data-ttu-id="357c1-103">移除工作區的資料流程。</span><span class="sxs-lookup"><span data-stu-id="357c1-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="357c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="357c1-104">SYNTAX</span></span>

### <span data-ttu-id="357c1-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="357c1-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="357c1-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="357c1-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="357c1-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="357c1-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="357c1-108">說明</span><span class="sxs-lookup"><span data-stu-id="357c1-108">DESCRIPTION</span></span>
<span data-ttu-id="357c1-109">**AzSynapseDataFlow** Cmdlet 會從工作區移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="357c1-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="357c1-110">示例</span><span class="sxs-lookup"><span data-stu-id="357c1-110">EXAMPLES</span></span>

### <span data-ttu-id="357c1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="357c1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="357c1-112">這個命令會從名為 [ContosoWorkspace] 的工作區中移除名為 ContosoDataFlow 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="357c1-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="357c1-113">參數</span><span class="sxs-lookup"><span data-stu-id="357c1-113">PARAMETERS</span></span>

### <span data-ttu-id="357c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="357c1-114">-AsJob</span></span>
<span data-ttu-id="357c1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="357c1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="357c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357c1-116">-DefaultProfile</span></span>
<span data-ttu-id="357c1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="357c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="357c1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="357c1-118">-Force</span></span>
<span data-ttu-id="357c1-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="357c1-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="357c1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="357c1-120">-InputObject</span></span>
<span data-ttu-id="357c1-121">資料流程程物件。</span><span class="sxs-lookup"><span data-stu-id="357c1-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="357c1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="357c1-122">-Name</span></span>
<span data-ttu-id="357c1-123">資料流程程名稱。</span><span class="sxs-lookup"><span data-stu-id="357c1-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357c1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="357c1-124">-PassThru</span></span>
<span data-ttu-id="357c1-125">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="357c1-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="357c1-126">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="357c1-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="357c1-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="357c1-127">-WorkspaceName</span></span>
<span data-ttu-id="357c1-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="357c1-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="357c1-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="357c1-129">-WorkspaceObject</span></span>
<span data-ttu-id="357c1-130">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="357c1-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="357c1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="357c1-131">-Confirm</span></span>
<span data-ttu-id="357c1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="357c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="357c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="357c1-133">-WhatIf</span></span>
<span data-ttu-id="357c1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="357c1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="357c1-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="357c1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="357c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357c1-136">CommonParameters</span></span>
<span data-ttu-id="357c1-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="357c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357c1-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="357c1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357c1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="357c1-139">INPUTS</span></span>

### <span data-ttu-id="357c1-140">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="357c1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="357c1-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="357c1-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="357c1-142">輸出</span><span class="sxs-lookup"><span data-stu-id="357c1-142">OUTPUTS</span></span>

### <span data-ttu-id="357c1-143">System.object</span><span class="sxs-lookup"><span data-stu-id="357c1-143">System.Boolean</span></span>

## <span data-ttu-id="357c1-144">筆記</span><span class="sxs-lookup"><span data-stu-id="357c1-144">NOTES</span></span>

## <span data-ttu-id="357c1-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="357c1-145">RELATED LINKS</span></span>

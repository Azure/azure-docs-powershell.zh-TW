---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 68da67d2a29b6f05ed50adc9eb8aef343a7e973b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284000"
---
# <span data-ttu-id="fb63a-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="fb63a-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="fb63a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb63a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb63a-103">移除工作區中的資料集。</span><span class="sxs-lookup"><span data-stu-id="fb63a-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="fb63a-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb63a-104">SYNTAX</span></span>

### <span data-ttu-id="fb63a-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="fb63a-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb63a-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="fb63a-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb63a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb63a-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb63a-108">說明</span><span class="sxs-lookup"><span data-stu-id="fb63a-108">DESCRIPTION</span></span>
<span data-ttu-id="fb63a-109">**AzSynapseDataset** Cmdlet 會從工作區移除資料集。</span><span class="sxs-lookup"><span data-stu-id="fb63a-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="fb63a-110">示例</span><span class="sxs-lookup"><span data-stu-id="fb63a-110">EXAMPLES</span></span>

### <span data-ttu-id="fb63a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fb63a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="fb63a-112">這個命令會從名為 [ContosoWorkspace] 的工作區中移除名為 ContosoDataset 的資料集。</span><span class="sxs-lookup"><span data-stu-id="fb63a-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fb63a-113">參數</span><span class="sxs-lookup"><span data-stu-id="fb63a-113">PARAMETERS</span></span>

### <span data-ttu-id="fb63a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb63a-114">-AsJob</span></span>
<span data-ttu-id="fb63a-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb63a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb63a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb63a-116">-DefaultProfile</span></span>
<span data-ttu-id="fb63a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb63a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb63a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fb63a-118">-Force</span></span>
<span data-ttu-id="fb63a-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="fb63a-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fb63a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb63a-120">-InputObject</span></span>
<span data-ttu-id="fb63a-121">資料集物件。</span><span class="sxs-lookup"><span data-stu-id="fb63a-121">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb63a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb63a-122">-Name</span></span>
<span data-ttu-id="fb63a-123">資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="fb63a-123">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb63a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb63a-124">-PassThru</span></span>
<span data-ttu-id="fb63a-125">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="fb63a-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fb63a-126">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="fb63a-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fb63a-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb63a-127">-WorkspaceName</span></span>
<span data-ttu-id="fb63a-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb63a-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fb63a-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fb63a-129">-WorkspaceObject</span></span>
<span data-ttu-id="fb63a-130">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="fb63a-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fb63a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="fb63a-131">-Confirm</span></span>
<span data-ttu-id="fb63a-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb63a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb63a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb63a-133">-WhatIf</span></span>
<span data-ttu-id="fb63a-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb63a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb63a-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb63a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb63a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb63a-136">CommonParameters</span></span>
<span data-ttu-id="fb63a-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb63a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb63a-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fb63a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb63a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="fb63a-139">INPUTS</span></span>

### <span data-ttu-id="fb63a-140">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="fb63a-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fb63a-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="fb63a-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="fb63a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="fb63a-142">OUTPUTS</span></span>

### <span data-ttu-id="fb63a-143">System.object</span><span class="sxs-lookup"><span data-stu-id="fb63a-143">System.Boolean</span></span>

## <span data-ttu-id="fb63a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="fb63a-144">NOTES</span></span>

## <span data-ttu-id="fb63a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb63a-145">RELATED LINKS</span></span>

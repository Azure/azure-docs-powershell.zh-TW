---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: b70c30b7652c331571030917057339a9d2d7de3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904786"
---
# <span data-ttu-id="4604b-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="4604b-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="4604b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4604b-102">SYNOPSIS</span></span>
<span data-ttu-id="4604b-103">從工作區移除資料集。</span><span class="sxs-lookup"><span data-stu-id="4604b-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="4604b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4604b-104">SYNTAX</span></span>

### <span data-ttu-id="4604b-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="4604b-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4604b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4604b-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4604b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4604b-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4604b-108">描述</span><span class="sxs-lookup"><span data-stu-id="4604b-108">DESCRIPTION</span></span>
<span data-ttu-id="4604b-109">**Remove-AzSynapseDataset** Cmdlet 會從工作區移除資料集。</span><span class="sxs-lookup"><span data-stu-id="4604b-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="4604b-110">例子</span><span class="sxs-lookup"><span data-stu-id="4604b-110">EXAMPLES</span></span>

### <span data-ttu-id="4604b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4604b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="4604b-112">此命令會從名為 ContosoWorkspace 的工作區移除名為 ContosoDataset 的資料集。</span><span class="sxs-lookup"><span data-stu-id="4604b-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4604b-113">參數</span><span class="sxs-lookup"><span data-stu-id="4604b-113">PARAMETERS</span></span>

### <span data-ttu-id="4604b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4604b-114">-AsJob</span></span>
<span data-ttu-id="4604b-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4604b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4604b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4604b-116">-DefaultProfile</span></span>
<span data-ttu-id="4604b-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4604b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4604b-118">-強制</span><span class="sxs-lookup"><span data-stu-id="4604b-118">-Force</span></span>
<span data-ttu-id="4604b-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="4604b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4604b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4604b-120">-InputObject</span></span>
<span data-ttu-id="4604b-121">資料集物件。</span><span class="sxs-lookup"><span data-stu-id="4604b-121">The dataset object.</span></span>

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

### <span data-ttu-id="4604b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4604b-122">-Name</span></span>
<span data-ttu-id="4604b-123">資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="4604b-123">The dataset name.</span></span>

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

### <span data-ttu-id="4604b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4604b-124">-PassThru</span></span>
<span data-ttu-id="4604b-125">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="4604b-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4604b-126">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="4604b-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4604b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4604b-127">-WorkspaceName</span></span>
<span data-ttu-id="4604b-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="4604b-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4604b-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4604b-129">-WorkspaceObject</span></span>
<span data-ttu-id="4604b-130">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="4604b-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4604b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4604b-131">-Confirm</span></span>
<span data-ttu-id="4604b-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4604b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4604b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4604b-133">-WhatIf</span></span>
<span data-ttu-id="4604b-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4604b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4604b-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4604b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4604b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4604b-136">CommonParameters</span></span>
<span data-ttu-id="4604b-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4604b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4604b-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4604b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4604b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4604b-139">INPUTS</span></span>

### <span data-ttu-id="4604b-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4604b-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4604b-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="4604b-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="4604b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4604b-142">OUTPUTS</span></span>

### <span data-ttu-id="4604b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4604b-143">System.Boolean</span></span>

## <span data-ttu-id="4604b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4604b-144">NOTES</span></span>

## <span data-ttu-id="4604b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4604b-145">RELATED LINKS</span></span>

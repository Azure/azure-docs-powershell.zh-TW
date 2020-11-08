---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139374"
---
# <span data-ttu-id="5f105-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="5f105-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="5f105-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f105-102">SYNOPSIS</span></span>
<span data-ttu-id="5f105-103">從工作區移除筆記本。</span><span class="sxs-lookup"><span data-stu-id="5f105-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="5f105-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f105-104">SYNTAX</span></span>

### <span data-ttu-id="5f105-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="5f105-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f105-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="5f105-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f105-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f105-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f105-108">說明</span><span class="sxs-lookup"><span data-stu-id="5f105-108">DESCRIPTION</span></span>
<span data-ttu-id="5f105-109">**AzSynapseNotebook** Cmdlet 會從工作區移除筆記本。</span><span class="sxs-lookup"><span data-stu-id="5f105-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="5f105-110">示例</span><span class="sxs-lookup"><span data-stu-id="5f105-110">EXAMPLES</span></span>

### <span data-ttu-id="5f105-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5f105-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="5f105-112">從工作區 ContosoWorkspace 中移除名為 ContosoNotebook 的筆記本。</span><span class="sxs-lookup"><span data-stu-id="5f105-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="5f105-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5f105-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="5f105-114">透過管線從工作區 ContosoWorkspace 移除稱為 ContosoNotebook 的筆記本。</span><span class="sxs-lookup"><span data-stu-id="5f105-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="5f105-115">範例3</span><span class="sxs-lookup"><span data-stu-id="5f105-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="5f105-116">透過管線從工作區 ContosoWorkspace 移除稱為 ContosoNotebook 的筆記本。</span><span class="sxs-lookup"><span data-stu-id="5f105-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5f105-117">參數</span><span class="sxs-lookup"><span data-stu-id="5f105-117">PARAMETERS</span></span>

### <span data-ttu-id="5f105-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f105-118">-AsJob</span></span>
<span data-ttu-id="5f105-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5f105-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f105-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f105-120">-DefaultProfile</span></span>
<span data-ttu-id="5f105-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f105-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f105-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f105-122">-InputObject</span></span>
<span data-ttu-id="5f105-123">[筆記本] 物件。</span><span class="sxs-lookup"><span data-stu-id="5f105-123">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f105-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f105-124">-Name</span></span>
<span data-ttu-id="5f105-125">筆記本名稱。</span><span class="sxs-lookup"><span data-stu-id="5f105-125">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f105-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f105-126">-PassThru</span></span>
<span data-ttu-id="5f105-127">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="5f105-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5f105-128">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="5f105-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5f105-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f105-129">-WorkspaceName</span></span>
<span data-ttu-id="5f105-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f105-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5f105-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5f105-131">-WorkspaceObject</span></span>
<span data-ttu-id="5f105-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="5f105-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5f105-133">-確認</span><span class="sxs-lookup"><span data-stu-id="5f105-133">-Confirm</span></span>
<span data-ttu-id="5f105-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f105-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f105-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f105-135">-WhatIf</span></span>
<span data-ttu-id="5f105-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f105-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f105-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f105-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f105-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f105-138">CommonParameters</span></span>
<span data-ttu-id="5f105-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f105-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f105-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5f105-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f105-141">輸入</span><span class="sxs-lookup"><span data-stu-id="5f105-141">INPUTS</span></span>

### <span data-ttu-id="5f105-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5f105-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5f105-143">PSNotebookResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5f105-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="5f105-144">輸出</span><span class="sxs-lookup"><span data-stu-id="5f105-144">OUTPUTS</span></span>

### <span data-ttu-id="5f105-145">System.object</span><span class="sxs-lookup"><span data-stu-id="5f105-145">System.Boolean</span></span>

## <span data-ttu-id="5f105-146">筆記</span><span class="sxs-lookup"><span data-stu-id="5f105-146">NOTES</span></span>

## <span data-ttu-id="5f105-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f105-147">RELATED LINKS</span></span>

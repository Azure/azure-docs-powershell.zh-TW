---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 6203143eb2d386b627d0208730987709b1dd68c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909909"
---
# <span data-ttu-id="3fcf1-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="3fcf1-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="3fcf1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3fcf1-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcf1-103">從工作區移除筆記本。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="3fcf1-104">語法</span><span class="sxs-lookup"><span data-stu-id="3fcf1-104">SYNTAX</span></span>

### <span data-ttu-id="3fcf1-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="3fcf1-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcf1-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3fcf1-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fcf1-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3fcf1-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fcf1-108">描述</span><span class="sxs-lookup"><span data-stu-id="3fcf1-108">DESCRIPTION</span></span>
<span data-ttu-id="3fcf1-109">**Remove-AzSynapseNotebook** Cmdlet 會從工作區移除筆記本。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="3fcf1-110">例子</span><span class="sxs-lookup"><span data-stu-id="3fcf1-110">EXAMPLES</span></span>

### <span data-ttu-id="3fcf1-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3fcf1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="3fcf1-112">從工作區 ContosoWorkspace 移除名為 ContosoNotebook 的筆記本。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="3fcf1-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="3fcf1-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="3fcf1-114">透過管線從工作區 ContosoWorkspace 移除名為 ContosoNotebook 的筆記本。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="3fcf1-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="3fcf1-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="3fcf1-116">透過管線從工作區 ContosoWorkspace 移除名為 ContosoNotebook 的筆記本。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3fcf1-117">參數</span><span class="sxs-lookup"><span data-stu-id="3fcf1-117">PARAMETERS</span></span>

### <span data-ttu-id="3fcf1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fcf1-118">-AsJob</span></span>
<span data-ttu-id="3fcf1-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3fcf1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fcf1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fcf1-120">-DefaultProfile</span></span>
<span data-ttu-id="3fcf1-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fcf1-122">-強制</span><span class="sxs-lookup"><span data-stu-id="3fcf1-122">-Force</span></span>
<span data-ttu-id="3fcf1-123">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3fcf1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fcf1-124">-InputObject</span></span>
<span data-ttu-id="3fcf1-125">筆記本物件。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-125">The notebook object.</span></span>

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

### <span data-ttu-id="3fcf1-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fcf1-126">-Name</span></span>
<span data-ttu-id="3fcf1-127">筆記本名稱。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-127">The notebook name.</span></span>

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

### <span data-ttu-id="3fcf1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fcf1-128">-PassThru</span></span>
<span data-ttu-id="3fcf1-129">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3fcf1-130">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3fcf1-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3fcf1-131">-WorkspaceName</span></span>
<span data-ttu-id="3fcf1-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3fcf1-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3fcf1-133">-WorkspaceObject</span></span>
<span data-ttu-id="3fcf1-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3fcf1-135">-確認</span><span class="sxs-lookup"><span data-stu-id="3fcf1-135">-Confirm</span></span>
<span data-ttu-id="3fcf1-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fcf1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fcf1-137">-WhatIf</span></span>
<span data-ttu-id="3fcf1-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fcf1-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fcf1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcf1-140">CommonParameters</span></span>
<span data-ttu-id="3fcf1-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3fcf1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcf1-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fcf1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcf1-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3fcf1-143">INPUTS</span></span>

### <span data-ttu-id="3fcf1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fcf1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3fcf1-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="3fcf1-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="3fcf1-146">輸出</span><span class="sxs-lookup"><span data-stu-id="3fcf1-146">OUTPUTS</span></span>

### <span data-ttu-id="3fcf1-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fcf1-147">System.Boolean</span></span>

## <span data-ttu-id="3fcf1-148">筆記</span><span class="sxs-lookup"><span data-stu-id="3fcf1-148">NOTES</span></span>

## <span data-ttu-id="3fcf1-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fcf1-149">RELATED LINKS</span></span>

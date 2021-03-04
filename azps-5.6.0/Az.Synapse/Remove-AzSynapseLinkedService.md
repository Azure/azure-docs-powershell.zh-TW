---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: 640992f0070d6cff14852000b07ecd8eddc61c1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910909"
---
# <span data-ttu-id="51ed7-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="51ed7-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="51ed7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="51ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="51ed7-103">從工作區移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="51ed7-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="51ed7-104">語法</span><span class="sxs-lookup"><span data-stu-id="51ed7-104">SYNTAX</span></span>

### <span data-ttu-id="51ed7-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="51ed7-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51ed7-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="51ed7-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51ed7-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="51ed7-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51ed7-108">描述</span><span class="sxs-lookup"><span data-stu-id="51ed7-108">DESCRIPTION</span></span>
<span data-ttu-id="51ed7-109">**Remove-AzSynapseLinkedService** Cmdlet 會從工作區移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="51ed7-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="51ed7-110">例子</span><span class="sxs-lookup"><span data-stu-id="51ed7-110">EXAMPLES</span></span>

### <span data-ttu-id="51ed7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="51ed7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="51ed7-112">此命令會從名為 ContosoWorkspace 的工作區移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="51ed7-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="51ed7-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="51ed7-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="51ed7-114">此命令會透過管線從名為 ContosoWorkspace 的工作區移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="51ed7-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="51ed7-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="51ed7-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="51ed7-116">此命令會透過管線從名為 ContosoWorkspace 的工作區移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="51ed7-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="51ed7-117">參數</span><span class="sxs-lookup"><span data-stu-id="51ed7-117">PARAMETERS</span></span>

### <span data-ttu-id="51ed7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51ed7-118">-AsJob</span></span>
<span data-ttu-id="51ed7-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="51ed7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51ed7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ed7-120">-DefaultProfile</span></span>
<span data-ttu-id="51ed7-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="51ed7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51ed7-122">-強制</span><span class="sxs-lookup"><span data-stu-id="51ed7-122">-Force</span></span>
<span data-ttu-id="51ed7-123">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="51ed7-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="51ed7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51ed7-124">-InputObject</span></span>
<span data-ttu-id="51ed7-125">連結的服務物件。</span><span class="sxs-lookup"><span data-stu-id="51ed7-125">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51ed7-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="51ed7-126">-Name</span></span>
<span data-ttu-id="51ed7-127">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="51ed7-127">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ed7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51ed7-128">-PassThru</span></span>
<span data-ttu-id="51ed7-129">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="51ed7-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="51ed7-130">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="51ed7-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="51ed7-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="51ed7-131">-WorkspaceName</span></span>
<span data-ttu-id="51ed7-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="51ed7-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="51ed7-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="51ed7-133">-WorkspaceObject</span></span>
<span data-ttu-id="51ed7-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="51ed7-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="51ed7-135">-確認</span><span class="sxs-lookup"><span data-stu-id="51ed7-135">-Confirm</span></span>
<span data-ttu-id="51ed7-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="51ed7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51ed7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51ed7-137">-WhatIf</span></span>
<span data-ttu-id="51ed7-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51ed7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51ed7-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51ed7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51ed7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ed7-140">CommonParameters</span></span>
<span data-ttu-id="51ed7-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="51ed7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ed7-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51ed7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ed7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="51ed7-143">INPUTS</span></span>

### <span data-ttu-id="51ed7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="51ed7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="51ed7-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="51ed7-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="51ed7-146">輸出</span><span class="sxs-lookup"><span data-stu-id="51ed7-146">OUTPUTS</span></span>

### <span data-ttu-id="51ed7-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="51ed7-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="51ed7-148">筆記</span><span class="sxs-lookup"><span data-stu-id="51ed7-148">NOTES</span></span>

## <span data-ttu-id="51ed7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="51ed7-149">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136810"
---
# <span data-ttu-id="a2d53-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="a2d53-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="a2d53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2d53-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d53-103">從工作區移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="a2d53-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="a2d53-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2d53-104">SYNTAX</span></span>

### <span data-ttu-id="a2d53-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a2d53-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d53-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a2d53-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d53-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2d53-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d53-108">說明</span><span class="sxs-lookup"><span data-stu-id="a2d53-108">DESCRIPTION</span></span>
<span data-ttu-id="a2d53-109">**AzSynapseLinkedService** Cmdlet 會從工作區移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="a2d53-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="a2d53-110">示例</span><span class="sxs-lookup"><span data-stu-id="a2d53-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d53-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a2d53-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="a2d53-112">這個命令會從名為 [ContosoWorkspace] 的工作區中，移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="a2d53-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a2d53-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a2d53-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="a2d53-114">這個命令會從名為 ContosoWorkspace 的工作區，從 [透過管線] 中移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="a2d53-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a2d53-115">範例3</span><span class="sxs-lookup"><span data-stu-id="a2d53-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="a2d53-116">這個命令會從名為 ContosoWorkspace 的工作區，從 [透過管線] 中移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="a2d53-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a2d53-117">參數</span><span class="sxs-lookup"><span data-stu-id="a2d53-117">PARAMETERS</span></span>

### <span data-ttu-id="a2d53-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2d53-118">-AsJob</span></span>
<span data-ttu-id="a2d53-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2d53-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2d53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d53-120">-DefaultProfile</span></span>
<span data-ttu-id="a2d53-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2d53-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d53-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a2d53-122">-Force</span></span>
<span data-ttu-id="a2d53-123">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a2d53-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a2d53-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2d53-124">-InputObject</span></span>
<span data-ttu-id="a2d53-125">連結的服務物件。</span><span class="sxs-lookup"><span data-stu-id="a2d53-125">The linked service object.</span></span>

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

### <span data-ttu-id="a2d53-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2d53-126">-Name</span></span>
<span data-ttu-id="a2d53-127">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a2d53-127">The linked service name.</span></span>

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

### <span data-ttu-id="a2d53-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2d53-128">-PassThru</span></span>
<span data-ttu-id="a2d53-129">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a2d53-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a2d53-130">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a2d53-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a2d53-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2d53-131">-WorkspaceName</span></span>
<span data-ttu-id="a2d53-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2d53-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2d53-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a2d53-133">-WorkspaceObject</span></span>
<span data-ttu-id="a2d53-134">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a2d53-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a2d53-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a2d53-135">-Confirm</span></span>
<span data-ttu-id="a2d53-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2d53-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d53-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d53-137">-WhatIf</span></span>
<span data-ttu-id="a2d53-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2d53-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2d53-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2d53-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d53-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d53-140">CommonParameters</span></span>
<span data-ttu-id="a2d53-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2d53-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d53-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2d53-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d53-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a2d53-143">INPUTS</span></span>

### <span data-ttu-id="a2d53-144">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a2d53-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a2d53-145">PSLinkedServiceResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a2d53-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="a2d53-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a2d53-146">OUTPUTS</span></span>

### <span data-ttu-id="a2d53-147">PSLinkedServiceResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a2d53-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="a2d53-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a2d53-148">NOTES</span></span>

## <span data-ttu-id="a2d53-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2d53-149">RELATED LINKS</span></span>

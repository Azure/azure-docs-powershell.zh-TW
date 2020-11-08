---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971357"
---
# <span data-ttu-id="74d95-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="74d95-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="74d95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74d95-102">SYNOPSIS</span></span>
<span data-ttu-id="74d95-103">從工作區移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="74d95-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="74d95-104">句法</span><span class="sxs-lookup"><span data-stu-id="74d95-104">SYNTAX</span></span>

### <span data-ttu-id="74d95-105">RemoveByName (預設) </span><span class="sxs-lookup"><span data-stu-id="74d95-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d95-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="74d95-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d95-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="74d95-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74d95-108">說明</span><span class="sxs-lookup"><span data-stu-id="74d95-108">DESCRIPTION</span></span>
<span data-ttu-id="74d95-109">**AzSynapseLinkedService** Cmdlet 會從工作區移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="74d95-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="74d95-110">示例</span><span class="sxs-lookup"><span data-stu-id="74d95-110">EXAMPLES</span></span>

### <span data-ttu-id="74d95-111">範例1</span><span class="sxs-lookup"><span data-stu-id="74d95-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="74d95-112">這個命令會從名為 [ContosoWorkspace] 的工作區中，移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="74d95-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="74d95-113">範例2</span><span class="sxs-lookup"><span data-stu-id="74d95-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="74d95-114">這個命令會從名為 ContosoWorkspace 的工作區，從 [透過管線] 中移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="74d95-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="74d95-115">範例3</span><span class="sxs-lookup"><span data-stu-id="74d95-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="74d95-116">這個命令會從名為 ContosoWorkspace 的工作區，從 [透過管線] 中移除名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="74d95-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="74d95-117">參數</span><span class="sxs-lookup"><span data-stu-id="74d95-117">PARAMETERS</span></span>

### <span data-ttu-id="74d95-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74d95-118">-AsJob</span></span>
<span data-ttu-id="74d95-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="74d95-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74d95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d95-120">-DefaultProfile</span></span>
<span data-ttu-id="74d95-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74d95-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d95-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74d95-122">-InputObject</span></span>
<span data-ttu-id="74d95-123">連結的服務物件。</span><span class="sxs-lookup"><span data-stu-id="74d95-123">The linked service object.</span></span>

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

### <span data-ttu-id="74d95-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="74d95-124">-Name</span></span>
<span data-ttu-id="74d95-125">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="74d95-125">The linked service name.</span></span>

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

### <span data-ttu-id="74d95-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74d95-126">-PassThru</span></span>
<span data-ttu-id="74d95-127">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="74d95-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="74d95-128">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="74d95-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="74d95-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74d95-129">-WorkspaceName</span></span>
<span data-ttu-id="74d95-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="74d95-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="74d95-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="74d95-131">-WorkspaceObject</span></span>
<span data-ttu-id="74d95-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="74d95-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="74d95-133">-確認</span><span class="sxs-lookup"><span data-stu-id="74d95-133">-Confirm</span></span>
<span data-ttu-id="74d95-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74d95-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d95-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d95-135">-WhatIf</span></span>
<span data-ttu-id="74d95-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74d95-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74d95-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74d95-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d95-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d95-138">CommonParameters</span></span>
<span data-ttu-id="74d95-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74d95-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d95-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74d95-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d95-141">輸入</span><span class="sxs-lookup"><span data-stu-id="74d95-141">INPUTS</span></span>

### <span data-ttu-id="74d95-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="74d95-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="74d95-143">PSLinkedServiceResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="74d95-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="74d95-144">輸出</span><span class="sxs-lookup"><span data-stu-id="74d95-144">OUTPUTS</span></span>

### <span data-ttu-id="74d95-145">PSLinkedServiceResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="74d95-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="74d95-146">筆記</span><span class="sxs-lookup"><span data-stu-id="74d95-146">NOTES</span></span>

## <span data-ttu-id="74d95-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="74d95-147">RELATED LINKS</span></span>

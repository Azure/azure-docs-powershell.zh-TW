---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437876"
---
# <span data-ttu-id="e5da8-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="e5da8-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="e5da8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5da8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5da8-103">更新自託管的整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="e5da8-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="e5da8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5da8-104">SYNTAX</span></span>

### <span data-ttu-id="e5da8-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e5da8-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5da8-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5da8-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5da8-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5da8-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5da8-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5da8-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5da8-109">說明</span><span class="sxs-lookup"><span data-stu-id="e5da8-109">DESCRIPTION</span></span>
<span data-ttu-id="e5da8-110">**AzSynapseIntegrationRuntimeNode** Cmdlet 會更新工作區中自行託管整合執行時間節點的屬性。</span><span class="sxs-lookup"><span data-stu-id="e5da8-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="e5da8-111">目前僅支援更新 ' ConcurrentJobsLimit」。</span><span class="sxs-lookup"><span data-stu-id="e5da8-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="e5da8-112">示例</span><span class="sxs-lookup"><span data-stu-id="e5da8-112">EXAMPLES</span></span>

### <span data-ttu-id="e5da8-113">範例1</span><span class="sxs-lookup"><span data-stu-id="e5da8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="e5da8-114">在自行託管整合執行時間 "test-selfhost-ir" 中，Cmdlet 會將節點 "Node_1" 的 [ConcurrentJobsLimit "更新為3。</span><span class="sxs-lookup"><span data-stu-id="e5da8-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="e5da8-115">參數</span><span class="sxs-lookup"><span data-stu-id="e5da8-115">PARAMETERS</span></span>

### <span data-ttu-id="e5da8-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="e5da8-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="e5da8-117">允許在整合執行時間節點上執行的併發作業數目。</span><span class="sxs-lookup"><span data-stu-id="e5da8-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="e5da8-118">允許介於1和 maxConcurrentJobs 之間的值。</span><span class="sxs-lookup"><span data-stu-id="e5da8-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5da8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5da8-119">-DefaultProfile</span></span>
<span data-ttu-id="e5da8-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5da8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5da8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5da8-121">-InputObject</span></span>
<span data-ttu-id="e5da8-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="e5da8-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5da8-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e5da8-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e5da8-124">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="e5da8-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5da8-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5da8-125">-Name</span></span>
<span data-ttu-id="e5da8-126">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="e5da8-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5da8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5da8-127">-ResourceGroupName</span></span>
<span data-ttu-id="e5da8-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e5da8-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5da8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5da8-129">-ResourceId</span></span>
<span data-ttu-id="e5da8-130">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5da8-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5da8-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5da8-131">-WorkspaceName</span></span>
<span data-ttu-id="e5da8-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5da8-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5da8-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e5da8-133">-WorkspaceObject</span></span>
<span data-ttu-id="e5da8-134">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e5da8-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5da8-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e5da8-135">-Confirm</span></span>
<span data-ttu-id="e5da8-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5da8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5da8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5da8-137">-WhatIf</span></span>
<span data-ttu-id="e5da8-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5da8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5da8-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5da8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5da8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5da8-140">CommonParameters</span></span>
<span data-ttu-id="e5da8-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5da8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5da8-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5da8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5da8-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e5da8-143">INPUTS</span></span>

### <span data-ttu-id="e5da8-144">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e5da8-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e5da8-145">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e5da8-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e5da8-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e5da8-146">OUTPUTS</span></span>

### <span data-ttu-id="e5da8-147">PSSelfHostedIntegrationRuntimeStatus 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e5da8-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="e5da8-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e5da8-148">NOTES</span></span>

## <span data-ttu-id="e5da8-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5da8-149">RELATED LINKS</span></span>

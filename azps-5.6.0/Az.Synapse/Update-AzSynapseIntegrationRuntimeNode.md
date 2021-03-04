---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5c2d7c8aa81cb45b6b49898c95b27256aa504b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904781"
---
# <span data-ttu-id="7e45b-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="7e45b-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="7e45b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e45b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e45b-103">更新自我託管的整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="7e45b-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="7e45b-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e45b-104">SYNTAX</span></span>

### <span data-ttu-id="7e45b-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7e45b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e45b-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e45b-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e45b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e45b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e45b-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e45b-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e45b-109">描述</span><span class="sxs-lookup"><span data-stu-id="7e45b-109">DESCRIPTION</span></span>
<span data-ttu-id="7e45b-110">**Update-AzSynapse RuntimeRuntimeNode** Cmdlet 會更新工作區中自我託管整合執行時間節點的屬性。</span><span class="sxs-lookup"><span data-stu-id="7e45b-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="7e45b-111">目前僅支援更新 'ConcurrentJobsLimit'。</span><span class="sxs-lookup"><span data-stu-id="7e45b-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="7e45b-112">例子</span><span class="sxs-lookup"><span data-stu-id="7e45b-112">EXAMPLES</span></span>

### <span data-ttu-id="7e45b-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="7e45b-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="7e45b-114">Cmdlet 會針對自我託管整合執行時間 "test-selfhost-ir" 中的節點 "Node_1" 將 "ConcurrentJobsLimit" 更新為 3。</span><span class="sxs-lookup"><span data-stu-id="7e45b-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="7e45b-115">參數</span><span class="sxs-lookup"><span data-stu-id="7e45b-115">PARAMETERS</span></span>

### <span data-ttu-id="7e45b-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="7e45b-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="7e45b-117">在整合執行時間節點上允許執行並行工作的數量。</span><span class="sxs-lookup"><span data-stu-id="7e45b-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="7e45b-118">允許介於 1 到 maxConcurrentJobs 之間的值。</span><span class="sxs-lookup"><span data-stu-id="7e45b-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="7e45b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e45b-119">-DefaultProfile</span></span>
<span data-ttu-id="7e45b-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e45b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e45b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e45b-121">-InputObject</span></span>
<span data-ttu-id="7e45b-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="7e45b-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="7e45b-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="7e45b-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="7e45b-124">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="7e45b-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="7e45b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e45b-125">-Name</span></span>
<span data-ttu-id="7e45b-126">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="7e45b-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="7e45b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e45b-127">-ResourceGroupName</span></span>
<span data-ttu-id="7e45b-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7e45b-128">Resource group name.</span></span>

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

### <span data-ttu-id="7e45b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e45b-129">-ResourceId</span></span>
<span data-ttu-id="7e45b-130">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e45b-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="7e45b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e45b-131">-WorkspaceName</span></span>
<span data-ttu-id="7e45b-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e45b-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7e45b-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7e45b-133">-WorkspaceObject</span></span>
<span data-ttu-id="7e45b-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="7e45b-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7e45b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="7e45b-135">-Confirm</span></span>
<span data-ttu-id="7e45b-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7e45b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e45b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e45b-137">-WhatIf</span></span>
<span data-ttu-id="7e45b-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e45b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e45b-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e45b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e45b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e45b-140">CommonParameters</span></span>
<span data-ttu-id="7e45b-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e45b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e45b-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e45b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e45b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="7e45b-143">INPUTS</span></span>

### <span data-ttu-id="7e45b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e45b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7e45b-145">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="7e45b-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7e45b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="7e45b-146">OUTPUTS</span></span>

### <span data-ttu-id="7e45b-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHosted方格RuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="7e45b-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="7e45b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="7e45b-148">NOTES</span></span>

## <span data-ttu-id="7e45b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e45b-149">RELATED LINKS</span></span>

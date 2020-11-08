---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136592"
---
# <span data-ttu-id="5bc83-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5bc83-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="5bc83-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bc83-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc83-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="5bc83-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="5bc83-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bc83-104">SYNTAX</span></span>

### <span data-ttu-id="5bc83-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5bc83-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc83-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc83-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc83-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc83-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bc83-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc83-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bc83-109">說明</span><span class="sxs-lookup"><span data-stu-id="5bc83-109">DESCRIPTION</span></span>
<span data-ttu-id="5bc83-110">**更新-AzSynapseIntegrationRuntime** Cmdlet 會更新整合執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="5bc83-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="5bc83-111">目前這個 Cmdlet 只支援針對自行託管的執行時間更新「自動更新」和「AutoUpdateDelayOffset」。</span><span class="sxs-lookup"><span data-stu-id="5bc83-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="5bc83-112">示例</span><span class="sxs-lookup"><span data-stu-id="5bc83-112">EXAMPLES</span></span>

### <span data-ttu-id="5bc83-113">範例1</span><span class="sxs-lookup"><span data-stu-id="5bc83-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="5bc83-114">此 Cmdlet 會更新名為「test-selfhost-ir」的自託管集成執行時間。</span><span class="sxs-lookup"><span data-stu-id="5bc83-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="5bc83-115">參數</span><span class="sxs-lookup"><span data-stu-id="5bc83-115">PARAMETERS</span></span>

### <span data-ttu-id="5bc83-116">-自動更新</span><span class="sxs-lookup"><span data-stu-id="5bc83-116">-AutoUpdate</span></span>
<span data-ttu-id="5bc83-117">啟用或停用自託管的集成執行時間自動更新。</span><span class="sxs-lookup"><span data-stu-id="5bc83-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc83-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="5bc83-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="5bc83-119">自託管的執行時間自動更新一天的時間。</span><span class="sxs-lookup"><span data-stu-id="5bc83-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc83-120">-DefaultProfile</span></span>
<span data-ttu-id="5bc83-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bc83-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bc83-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bc83-122">-InputObject</span></span>
<span data-ttu-id="5bc83-123">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="5bc83-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="5bc83-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5bc83-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="5bc83-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc83-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="5bc83-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc83-126">-ResourceGroupName</span></span>
<span data-ttu-id="5bc83-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc83-127">Resource group name.</span></span>

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

### <span data-ttu-id="5bc83-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bc83-128">-ResourceId</span></span>
<span data-ttu-id="5bc83-129">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5bc83-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="5bc83-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5bc83-130">-WorkspaceName</span></span>
<span data-ttu-id="5bc83-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc83-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5bc83-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5bc83-132">-WorkspaceObject</span></span>
<span data-ttu-id="5bc83-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="5bc83-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5bc83-134">-確認</span><span class="sxs-lookup"><span data-stu-id="5bc83-134">-Confirm</span></span>
<span data-ttu-id="5bc83-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5bc83-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bc83-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc83-136">-WhatIf</span></span>
<span data-ttu-id="5bc83-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5bc83-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bc83-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5bc83-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bc83-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc83-139">CommonParameters</span></span>
<span data-ttu-id="5bc83-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bc83-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc83-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5bc83-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc83-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5bc83-142">INPUTS</span></span>

### <span data-ttu-id="5bc83-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5bc83-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5bc83-144">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5bc83-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5bc83-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5bc83-145">OUTPUTS</span></span>

### <span data-ttu-id="5bc83-146">PSSelfHostedIntegrationRuntimeStatus 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5bc83-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="5bc83-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5bc83-147">NOTES</span></span>

## <span data-ttu-id="5bc83-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bc83-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 004cfc8e0bd22be1f57a320cf10aa7d7f53cbb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911826"
---
# <span data-ttu-id="6eecc-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6eecc-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="6eecc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6eecc-102">SYNOPSIS</span></span>
<span data-ttu-id="6eecc-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="6eecc-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="6eecc-104">語法</span><span class="sxs-lookup"><span data-stu-id="6eecc-104">SYNTAX</span></span>

### <span data-ttu-id="6eecc-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6eecc-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eecc-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eecc-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eecc-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eecc-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6eecc-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eecc-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6eecc-109">描述</span><span class="sxs-lookup"><span data-stu-id="6eecc-109">DESCRIPTION</span></span>
<span data-ttu-id="6eecc-110">**Update-AzSynapse RuntimeRuntime** Cmdlet 會更新整合執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="6eecc-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="6eecc-111">目前，Cmdlet 僅支援更新自我託管整合執行時間的 'AutoUpdate' 和 'AutoUpdateDelayOffset'。</span><span class="sxs-lookup"><span data-stu-id="6eecc-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="6eecc-112">例子</span><span class="sxs-lookup"><span data-stu-id="6eecc-112">EXAMPLES</span></span>

### <span data-ttu-id="6eecc-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="6eecc-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="6eecc-114">Cmdlet 會更新名為'test-selfhost-ir'的自我託管整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="6eecc-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6eecc-115">參數</span><span class="sxs-lookup"><span data-stu-id="6eecc-115">PARAMETERS</span></span>

### <span data-ttu-id="6eecc-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="6eecc-116">-AutoUpdate</span></span>
<span data-ttu-id="6eecc-117">啟用或停用自行託管的整合執行時間自動更新。</span><span class="sxs-lookup"><span data-stu-id="6eecc-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="6eecc-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="6eecc-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="6eecc-119">自動託管整合執行時間自動更新的一天中時間。</span><span class="sxs-lookup"><span data-stu-id="6eecc-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="6eecc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eecc-120">-DefaultProfile</span></span>
<span data-ttu-id="6eecc-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6eecc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eecc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eecc-122">-InputObject</span></span>
<span data-ttu-id="6eecc-123">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="6eecc-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="6eecc-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6eecc-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6eecc-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="6eecc-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="6eecc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eecc-126">-ResourceGroupName</span></span>
<span data-ttu-id="6eecc-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6eecc-127">Resource group name.</span></span>

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

### <span data-ttu-id="6eecc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eecc-128">-ResourceId</span></span>
<span data-ttu-id="6eecc-129">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6eecc-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6eecc-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6eecc-130">-WorkspaceName</span></span>
<span data-ttu-id="6eecc-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6eecc-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6eecc-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6eecc-132">-WorkspaceObject</span></span>
<span data-ttu-id="6eecc-133">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="6eecc-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6eecc-134">-確認</span><span class="sxs-lookup"><span data-stu-id="6eecc-134">-Confirm</span></span>
<span data-ttu-id="6eecc-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6eecc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eecc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eecc-136">-WhatIf</span></span>
<span data-ttu-id="6eecc-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6eecc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eecc-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eecc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eecc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eecc-139">CommonParameters</span></span>
<span data-ttu-id="6eecc-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6eecc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eecc-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eecc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eecc-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6eecc-142">INPUTS</span></span>

### <span data-ttu-id="6eecc-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6eecc-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6eecc-144">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="6eecc-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6eecc-145">輸出</span><span class="sxs-lookup"><span data-stu-id="6eecc-145">OUTPUTS</span></span>

### <span data-ttu-id="6eecc-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHosted方格RuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="6eecc-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="6eecc-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6eecc-147">NOTES</span></span>

## <span data-ttu-id="6eecc-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6eecc-148">RELATED LINKS</span></span>

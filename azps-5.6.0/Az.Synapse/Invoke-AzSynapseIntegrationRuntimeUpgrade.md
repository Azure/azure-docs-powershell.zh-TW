---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: ad5b23e29eb2d13fcad6aaf2659940dace83f4eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909933"
---
# <span data-ttu-id="0e8bc-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="0e8bc-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="0e8bc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8bc-103">升級自行託管的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="0e8bc-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e8bc-104">SYNTAX</span></span>

### <span data-ttu-id="0e8bc-105">InvokeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0e8bc-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8bc-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e8bc-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8bc-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e8bc-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8bc-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e8bc-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8bc-109">描述</span><span class="sxs-lookup"><span data-stu-id="0e8bc-109">DESCRIPTION</span></span>
<span data-ttu-id="0e8bc-110">如果 **新版本可用，則 Invoke-AzSynapse RuntimeRuntimeUpgrade** Cmdlet 會升級自行託管的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="0e8bc-111">例子</span><span class="sxs-lookup"><span data-stu-id="0e8bc-111">EXAMPLES</span></span>

### <span data-ttu-id="0e8bc-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0e8bc-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="0e8bc-113">Cmdlet 會升級工作區 ContosoWorkspace 中名為"test-selfhost-ir"的自行託管整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="0e8bc-114">參數</span><span class="sxs-lookup"><span data-stu-id="0e8bc-114">PARAMETERS</span></span>

### <span data-ttu-id="0e8bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8bc-115">-DefaultProfile</span></span>
<span data-ttu-id="0e8bc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e8bc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e8bc-117">-InputObject</span></span>
<span data-ttu-id="0e8bc-118">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8bc-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e8bc-119">-Name</span></span>
<span data-ttu-id="0e8bc-120">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e8bc-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8bc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e8bc-123">-ResourceId</span></span>
<span data-ttu-id="0e8bc-124">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8bc-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0e8bc-125">-WorkspaceName</span></span>
<span data-ttu-id="0e8bc-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8bc-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0e8bc-127">-WorkspaceObject</span></span>
<span data-ttu-id="0e8bc-128">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8bc-129">-確認</span><span class="sxs-lookup"><span data-stu-id="0e8bc-129">-Confirm</span></span>
<span data-ttu-id="0e8bc-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8bc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8bc-131">-WhatIf</span></span>
<span data-ttu-id="0e8bc-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8bc-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8bc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8bc-134">CommonParameters</span></span>
<span data-ttu-id="0e8bc-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e8bc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8bc-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e8bc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8bc-137">輸入</span><span class="sxs-lookup"><span data-stu-id="0e8bc-137">INPUTS</span></span>

### <span data-ttu-id="0e8bc-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e8bc-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0e8bc-139">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="0e8bc-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0e8bc-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0e8bc-140">OUTPUTS</span></span>

### <span data-ttu-id="0e8bc-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="0e8bc-141">System.Void</span></span>

## <span data-ttu-id="0e8bc-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0e8bc-142">NOTES</span></span>

## <span data-ttu-id="0e8bc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e8bc-143">RELATED LINKS</span></span>

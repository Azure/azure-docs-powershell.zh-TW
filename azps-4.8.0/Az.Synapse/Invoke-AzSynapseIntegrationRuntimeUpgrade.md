---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126665"
---
# <span data-ttu-id="c5c05-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="c5c05-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="c5c05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5c05-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c05-103">升級自託管的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="c5c05-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="c5c05-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5c05-104">SYNTAX</span></span>

### <span data-ttu-id="c5c05-105">InvokeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c5c05-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c05-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c05-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c05-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c05-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c05-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c05-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5c05-109">說明</span><span class="sxs-lookup"><span data-stu-id="c5c05-109">DESCRIPTION</span></span>
<span data-ttu-id="c5c05-110">如果有新的版本， **AzSynapseIntegrationRuntimeUpgrade** Cmdlet 會升級自託管整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="c5c05-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="c5c05-111">示例</span><span class="sxs-lookup"><span data-stu-id="c5c05-111">EXAMPLES</span></span>

### <span data-ttu-id="c5c05-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c5c05-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="c5c05-113">Cmdlet 會在工作區 ContosoWorkspace 中升級一個名為「test-selfhost-ir」的 self 託管執行時間。</span><span class="sxs-lookup"><span data-stu-id="c5c05-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="c5c05-114">參數</span><span class="sxs-lookup"><span data-stu-id="c5c05-114">PARAMETERS</span></span>

### <span data-ttu-id="c5c05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c05-115">-DefaultProfile</span></span>
<span data-ttu-id="c5c05-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5c05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5c05-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5c05-117">-InputObject</span></span>
<span data-ttu-id="c5c05-118">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="c5c05-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="c5c05-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5c05-119">-Name</span></span>
<span data-ttu-id="c5c05-120">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="c5c05-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="c5c05-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c05-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5c05-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c5c05-122">Resource group name.</span></span>

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

### <span data-ttu-id="c5c05-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c05-123">-ResourceId</span></span>
<span data-ttu-id="c5c05-124">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5c05-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="c5c05-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5c05-125">-WorkspaceName</span></span>
<span data-ttu-id="c5c05-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5c05-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c5c05-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c5c05-127">-WorkspaceObject</span></span>
<span data-ttu-id="c5c05-128">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="c5c05-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c5c05-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c5c05-129">-Confirm</span></span>
<span data-ttu-id="c5c05-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c5c05-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5c05-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c05-131">-WhatIf</span></span>
<span data-ttu-id="c5c05-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5c05-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5c05-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5c05-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5c05-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c05-134">CommonParameters</span></span>
<span data-ttu-id="c5c05-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5c05-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c05-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c5c05-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c05-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c5c05-137">INPUTS</span></span>

### <span data-ttu-id="c5c05-138">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c5c05-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c5c05-139">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c5c05-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c5c05-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c5c05-140">OUTPUTS</span></span>

### <span data-ttu-id="c5c05-141">System.void</span><span class="sxs-lookup"><span data-stu-id="c5c05-141">System.Void</span></span>

## <span data-ttu-id="c5c05-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c5c05-142">NOTES</span></span>

## <span data-ttu-id="c5c05-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5c05-143">RELATED LINKS</span></span>

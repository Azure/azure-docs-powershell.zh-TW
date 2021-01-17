---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288151"
---
# <span data-ttu-id="6077e-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6077e-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="6077e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6077e-102">SYNOPSIS</span></span>
<span data-ttu-id="6077e-103">在整合執行時間中移除具有指定名稱的節點。</span><span class="sxs-lookup"><span data-stu-id="6077e-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="6077e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6077e-104">SYNTAX</span></span>

### <span data-ttu-id="6077e-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6077e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6077e-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6077e-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6077e-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6077e-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6077e-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6077e-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6077e-109">說明</span><span class="sxs-lookup"><span data-stu-id="6077e-109">DESCRIPTION</span></span>
<span data-ttu-id="6077e-110">**AzSynapseIntegrationRuntimeNode** Cmdlet 會移除整合執行時間中的節點。</span><span class="sxs-lookup"><span data-stu-id="6077e-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="6077e-111">示例</span><span class="sxs-lookup"><span data-stu-id="6077e-111">EXAMPLES</span></span>

### <span data-ttu-id="6077e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6077e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="6077e-113">在整合執行時間中移除具有指定名稱的節點。</span><span class="sxs-lookup"><span data-stu-id="6077e-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="6077e-114">參數</span><span class="sxs-lookup"><span data-stu-id="6077e-114">PARAMETERS</span></span>

### <span data-ttu-id="6077e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6077e-115">-DefaultProfile</span></span>
<span data-ttu-id="6077e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6077e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6077e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6077e-117">-Force</span></span>
<span data-ttu-id="6077e-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="6077e-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6077e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6077e-119">-InputObject</span></span>
<span data-ttu-id="6077e-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="6077e-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6077e-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6077e-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6077e-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="6077e-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6077e-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="6077e-123">-NodeName</span></span>
<span data-ttu-id="6077e-124">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="6077e-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6077e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6077e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6077e-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6077e-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6077e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6077e-127">-ResourceId</span></span>
<span data-ttu-id="6077e-128">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6077e-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6077e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6077e-129">-WorkspaceName</span></span>
<span data-ttu-id="6077e-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6077e-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6077e-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6077e-131">-WorkspaceObject</span></span>
<span data-ttu-id="6077e-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6077e-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6077e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="6077e-133">-Confirm</span></span>
<span data-ttu-id="6077e-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6077e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6077e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6077e-135">-WhatIf</span></span>
<span data-ttu-id="6077e-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6077e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6077e-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6077e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6077e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6077e-138">CommonParameters</span></span>
<span data-ttu-id="6077e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6077e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6077e-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6077e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6077e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="6077e-141">INPUTS</span></span>

### <span data-ttu-id="6077e-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6077e-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6077e-143">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6077e-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="6077e-144">System.object</span><span class="sxs-lookup"><span data-stu-id="6077e-144">System.String</span></span>

## <span data-ttu-id="6077e-145">輸出</span><span class="sxs-lookup"><span data-stu-id="6077e-145">OUTPUTS</span></span>

### <span data-ttu-id="6077e-146">System.void</span><span class="sxs-lookup"><span data-stu-id="6077e-146">System.Void</span></span>

## <span data-ttu-id="6077e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6077e-147">NOTES</span></span>

## <span data-ttu-id="6077e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6077e-148">RELATED LINKS</span></span>

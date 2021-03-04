---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 07b1b36222f0d1a31d4a4a7374957336246f0073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916839"
---
# <span data-ttu-id="331aa-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="331aa-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="331aa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="331aa-102">SYNOPSIS</span></span>
<span data-ttu-id="331aa-103">移除整合執行時間上具有指定名稱的節點。</span><span class="sxs-lookup"><span data-stu-id="331aa-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="331aa-104">語法</span><span class="sxs-lookup"><span data-stu-id="331aa-104">SYNTAX</span></span>

### <span data-ttu-id="331aa-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="331aa-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="331aa-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="331aa-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="331aa-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="331aa-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="331aa-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="331aa-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="331aa-109">描述</span><span class="sxs-lookup"><span data-stu-id="331aa-109">DESCRIPTION</span></span>
<span data-ttu-id="331aa-110">**Remove-AzSynapse RuntimeRuntimeNode** Cmdlet 會移除整合執行時間中的節點。</span><span class="sxs-lookup"><span data-stu-id="331aa-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="331aa-111">例子</span><span class="sxs-lookup"><span data-stu-id="331aa-111">EXAMPLES</span></span>

### <span data-ttu-id="331aa-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="331aa-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="331aa-113">移除整合執行時間上具有指定名稱的節點。</span><span class="sxs-lookup"><span data-stu-id="331aa-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="331aa-114">參數</span><span class="sxs-lookup"><span data-stu-id="331aa-114">PARAMETERS</span></span>

### <span data-ttu-id="331aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331aa-115">-DefaultProfile</span></span>
<span data-ttu-id="331aa-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="331aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="331aa-117">-強制</span><span class="sxs-lookup"><span data-stu-id="331aa-117">-Force</span></span>
<span data-ttu-id="331aa-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="331aa-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="331aa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="331aa-119">-InputObject</span></span>
<span data-ttu-id="331aa-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="331aa-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="331aa-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="331aa-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="331aa-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="331aa-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="331aa-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="331aa-123">-NodeName</span></span>
<span data-ttu-id="331aa-124">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="331aa-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="331aa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331aa-125">-ResourceGroupName</span></span>
<span data-ttu-id="331aa-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="331aa-126">Resource group name.</span></span>

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

### <span data-ttu-id="331aa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="331aa-127">-ResourceId</span></span>
<span data-ttu-id="331aa-128">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="331aa-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="331aa-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="331aa-129">-WorkspaceName</span></span>
<span data-ttu-id="331aa-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="331aa-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="331aa-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="331aa-131">-WorkspaceObject</span></span>
<span data-ttu-id="331aa-132">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="331aa-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="331aa-133">-確認</span><span class="sxs-lookup"><span data-stu-id="331aa-133">-Confirm</span></span>
<span data-ttu-id="331aa-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="331aa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="331aa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="331aa-135">-WhatIf</span></span>
<span data-ttu-id="331aa-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="331aa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="331aa-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="331aa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="331aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331aa-138">CommonParameters</span></span>
<span data-ttu-id="331aa-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="331aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331aa-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="331aa-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331aa-141">輸入</span><span class="sxs-lookup"><span data-stu-id="331aa-141">INPUTS</span></span>

### <span data-ttu-id="331aa-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="331aa-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="331aa-143">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="331aa-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="331aa-144">System.String</span><span class="sxs-lookup"><span data-stu-id="331aa-144">System.String</span></span>

## <span data-ttu-id="331aa-145">輸出</span><span class="sxs-lookup"><span data-stu-id="331aa-145">OUTPUTS</span></span>

### <span data-ttu-id="331aa-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="331aa-146">System.Void</span></span>

## <span data-ttu-id="331aa-147">筆記</span><span class="sxs-lookup"><span data-stu-id="331aa-147">NOTES</span></span>

## <span data-ttu-id="331aa-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="331aa-148">RELATED LINKS</span></span>

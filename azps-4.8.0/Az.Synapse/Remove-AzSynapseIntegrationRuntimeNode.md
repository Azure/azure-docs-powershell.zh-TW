---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971358"
---
# <span data-ttu-id="f2021-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f2021-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="f2021-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2021-102">SYNOPSIS</span></span>
<span data-ttu-id="f2021-103">在整合執行時間中移除具有指定名稱的節點。</span><span class="sxs-lookup"><span data-stu-id="f2021-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="f2021-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2021-104">SYNTAX</span></span>

### <span data-ttu-id="f2021-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f2021-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2021-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2021-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2021-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2021-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2021-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2021-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2021-109">說明</span><span class="sxs-lookup"><span data-stu-id="f2021-109">DESCRIPTION</span></span>
<span data-ttu-id="f2021-110">**AzSynapseIntegrationRuntimeNode** Cmdlet 會移除整合執行時間中的節點。</span><span class="sxs-lookup"><span data-stu-id="f2021-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="f2021-111">示例</span><span class="sxs-lookup"><span data-stu-id="f2021-111">EXAMPLES</span></span>

### <span data-ttu-id="f2021-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f2021-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="f2021-113">在整合執行時間中移除具有指定名稱的節點。</span><span class="sxs-lookup"><span data-stu-id="f2021-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="f2021-114">參數</span><span class="sxs-lookup"><span data-stu-id="f2021-114">PARAMETERS</span></span>

### <span data-ttu-id="f2021-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2021-115">-DefaultProfile</span></span>
<span data-ttu-id="f2021-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2021-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2021-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f2021-117">-Force</span></span>
<span data-ttu-id="f2021-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f2021-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f2021-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2021-119">-InputObject</span></span>
<span data-ttu-id="f2021-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="f2021-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="f2021-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f2021-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f2021-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="f2021-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="f2021-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="f2021-123">-NodeName</span></span>
<span data-ttu-id="f2021-124">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="f2021-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="f2021-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2021-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2021-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f2021-126">Resource group name.</span></span>

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

### <span data-ttu-id="f2021-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2021-127">-ResourceId</span></span>
<span data-ttu-id="f2021-128">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2021-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="f2021-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f2021-129">-WorkspaceName</span></span>
<span data-ttu-id="f2021-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2021-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f2021-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f2021-131">-WorkspaceObject</span></span>
<span data-ttu-id="f2021-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="f2021-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f2021-133">-確認</span><span class="sxs-lookup"><span data-stu-id="f2021-133">-Confirm</span></span>
<span data-ttu-id="f2021-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f2021-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2021-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2021-135">-WhatIf</span></span>
<span data-ttu-id="f2021-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2021-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2021-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2021-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2021-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2021-138">CommonParameters</span></span>
<span data-ttu-id="f2021-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2021-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2021-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f2021-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2021-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f2021-141">INPUTS</span></span>

### <span data-ttu-id="f2021-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="f2021-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f2021-143">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="f2021-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="f2021-144">System.object</span><span class="sxs-lookup"><span data-stu-id="f2021-144">System.String</span></span>

## <span data-ttu-id="f2021-145">輸出</span><span class="sxs-lookup"><span data-stu-id="f2021-145">OUTPUTS</span></span>

### <span data-ttu-id="f2021-146">System.void</span><span class="sxs-lookup"><span data-stu-id="f2021-146">System.Void</span></span>

## <span data-ttu-id="f2021-147">筆記</span><span class="sxs-lookup"><span data-stu-id="f2021-147">NOTES</span></span>

## <span data-ttu-id="f2021-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2021-148">RELATED LINKS</span></span>

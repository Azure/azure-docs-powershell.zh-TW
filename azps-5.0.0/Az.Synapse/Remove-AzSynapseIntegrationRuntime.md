---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139360"
---
# <span data-ttu-id="d357e-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d357e-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="d357e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d357e-102">SYNOPSIS</span></span>
<span data-ttu-id="d357e-103">移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="d357e-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="d357e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d357e-104">SYNTAX</span></span>

### <span data-ttu-id="d357e-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d357e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d357e-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d357e-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d357e-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d357e-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d357e-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d357e-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d357e-109">說明</span><span class="sxs-lookup"><span data-stu-id="d357e-109">DESCRIPTION</span></span>
<span data-ttu-id="d357e-110">**AzSynapseIntegrationRuntime** Cmdlet 會移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="d357e-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="d357e-111">示例</span><span class="sxs-lookup"><span data-stu-id="d357e-111">EXAMPLES</span></span>

### <span data-ttu-id="d357e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d357e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="d357e-113">這個命令會從名為 ContosoWorkspace 的工作區中，移除名為「test reserved-ir」的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="d357e-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d357e-114">參數</span><span class="sxs-lookup"><span data-stu-id="d357e-114">PARAMETERS</span></span>

### <span data-ttu-id="d357e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d357e-115">-DefaultProfile</span></span>
<span data-ttu-id="d357e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d357e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d357e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d357e-117">-Force</span></span>
<span data-ttu-id="d357e-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="d357e-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d357e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d357e-119">-InputObject</span></span>
<span data-ttu-id="d357e-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="d357e-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="d357e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d357e-121">-Name</span></span>
<span data-ttu-id="d357e-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="d357e-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d357e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d357e-123">-ResourceGroupName</span></span>
<span data-ttu-id="d357e-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d357e-124">Resource group name.</span></span>

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

### <span data-ttu-id="d357e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d357e-125">-ResourceId</span></span>
<span data-ttu-id="d357e-126">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d357e-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="d357e-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d357e-127">-WorkspaceName</span></span>
<span data-ttu-id="d357e-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d357e-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d357e-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d357e-129">-WorkspaceObject</span></span>
<span data-ttu-id="d357e-130">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d357e-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d357e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="d357e-131">-Confirm</span></span>
<span data-ttu-id="d357e-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d357e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d357e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d357e-133">-WhatIf</span></span>
<span data-ttu-id="d357e-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d357e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d357e-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d357e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d357e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d357e-136">CommonParameters</span></span>
<span data-ttu-id="d357e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d357e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d357e-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d357e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d357e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="d357e-139">INPUTS</span></span>

### <span data-ttu-id="d357e-140">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d357e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d357e-141">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d357e-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d357e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d357e-142">OUTPUTS</span></span>

### <span data-ttu-id="d357e-143">System.void</span><span class="sxs-lookup"><span data-stu-id="d357e-143">System.Void</span></span>

## <span data-ttu-id="d357e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d357e-144">NOTES</span></span>

## <span data-ttu-id="d357e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d357e-145">RELATED LINKS</span></span>
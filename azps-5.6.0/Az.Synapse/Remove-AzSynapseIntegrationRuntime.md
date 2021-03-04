---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: bf15d0f533f54de589ef354d92c4cf2f600b12cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904193"
---
# <span data-ttu-id="60767-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="60767-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="60767-102">簡介</span><span class="sxs-lookup"><span data-stu-id="60767-102">SYNOPSIS</span></span>
<span data-ttu-id="60767-103">移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="60767-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="60767-104">語法</span><span class="sxs-lookup"><span data-stu-id="60767-104">SYNTAX</span></span>

### <span data-ttu-id="60767-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="60767-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60767-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60767-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60767-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60767-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60767-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60767-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60767-109">描述</span><span class="sxs-lookup"><span data-stu-id="60767-109">DESCRIPTION</span></span>
<span data-ttu-id="60767-110">**Remove-AzSynapse RuntimeRuntime** Cmdlet 會移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="60767-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="60767-111">例子</span><span class="sxs-lookup"><span data-stu-id="60767-111">EXAMPLES</span></span>

### <span data-ttu-id="60767-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="60767-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="60767-113">此命令會從名為 ContosoWorkspace 的工作區移除名為"test-reserved-ir"的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="60767-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="60767-114">參數</span><span class="sxs-lookup"><span data-stu-id="60767-114">PARAMETERS</span></span>

### <span data-ttu-id="60767-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60767-115">-DefaultProfile</span></span>
<span data-ttu-id="60767-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="60767-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60767-117">-強制</span><span class="sxs-lookup"><span data-stu-id="60767-117">-Force</span></span>
<span data-ttu-id="60767-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="60767-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="60767-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60767-119">-InputObject</span></span>
<span data-ttu-id="60767-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="60767-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="60767-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="60767-121">-Name</span></span>
<span data-ttu-id="60767-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="60767-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="60767-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60767-123">-ResourceGroupName</span></span>
<span data-ttu-id="60767-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="60767-124">Resource group name.</span></span>

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

### <span data-ttu-id="60767-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60767-125">-ResourceId</span></span>
<span data-ttu-id="60767-126">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="60767-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="60767-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="60767-127">-WorkspaceName</span></span>
<span data-ttu-id="60767-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="60767-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="60767-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="60767-129">-WorkspaceObject</span></span>
<span data-ttu-id="60767-130">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="60767-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="60767-131">-確認</span><span class="sxs-lookup"><span data-stu-id="60767-131">-Confirm</span></span>
<span data-ttu-id="60767-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="60767-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60767-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60767-133">-WhatIf</span></span>
<span data-ttu-id="60767-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60767-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60767-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60767-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60767-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60767-136">CommonParameters</span></span>
<span data-ttu-id="60767-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="60767-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60767-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60767-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60767-139">輸入</span><span class="sxs-lookup"><span data-stu-id="60767-139">INPUTS</span></span>

### <span data-ttu-id="60767-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="60767-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="60767-141">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="60767-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="60767-142">輸出</span><span class="sxs-lookup"><span data-stu-id="60767-142">OUTPUTS</span></span>

### <span data-ttu-id="60767-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="60767-143">System.Void</span></span>

## <span data-ttu-id="60767-144">筆記</span><span class="sxs-lookup"><span data-stu-id="60767-144">NOTES</span></span>

## <span data-ttu-id="60767-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="60767-145">RELATED LINKS</span></span>

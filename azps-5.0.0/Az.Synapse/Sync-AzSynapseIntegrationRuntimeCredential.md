---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136606"
---
# <span data-ttu-id="0db07-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="0db07-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="0db07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0db07-102">SYNOPSIS</span></span>
<span data-ttu-id="0db07-103">在整合執行時間節點之間同步處理認證。</span><span class="sxs-lookup"><span data-stu-id="0db07-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="0db07-104">句法</span><span class="sxs-lookup"><span data-stu-id="0db07-104">SYNTAX</span></span>

### <span data-ttu-id="0db07-105">StopByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0db07-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0db07-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db07-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0db07-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db07-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db07-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db07-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db07-109">說明</span><span class="sxs-lookup"><span data-stu-id="0db07-109">DESCRIPTION</span></span>
<span data-ttu-id="0db07-110">**AzSynapseIntegrationRuntimeCredential** Cmdlet 會同步處理整合執行時間節點中的內部部署認證，這會強制在所有節點中都有相同的認證。</span><span class="sxs-lookup"><span data-stu-id="0db07-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="0db07-111">示例</span><span class="sxs-lookup"><span data-stu-id="0db07-111">EXAMPLES</span></span>

### <span data-ttu-id="0db07-112">範例1</span><span class="sxs-lookup"><span data-stu-id="0db07-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="0db07-113">在整合執行時間節點之間同步處理認證。</span><span class="sxs-lookup"><span data-stu-id="0db07-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="0db07-114">參數</span><span class="sxs-lookup"><span data-stu-id="0db07-114">PARAMETERS</span></span>

### <span data-ttu-id="0db07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db07-115">-DefaultProfile</span></span>
<span data-ttu-id="0db07-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0db07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db07-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0db07-117">-Force</span></span>
<span data-ttu-id="0db07-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0db07-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0db07-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0db07-119">-InputObject</span></span>
<span data-ttu-id="0db07-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="0db07-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0db07-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="0db07-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="0db07-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="0db07-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db07-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db07-123">-ResourceGroupName</span></span>
<span data-ttu-id="0db07-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0db07-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db07-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0db07-125">-ResourceId</span></span>
<span data-ttu-id="0db07-126">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0db07-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db07-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0db07-127">-WorkspaceName</span></span>
<span data-ttu-id="0db07-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0db07-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db07-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0db07-129">-WorkspaceObject</span></span>
<span data-ttu-id="0db07-130">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0db07-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0db07-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0db07-131">-Confirm</span></span>
<span data-ttu-id="0db07-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0db07-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db07-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db07-133">-WhatIf</span></span>
<span data-ttu-id="0db07-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0db07-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db07-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0db07-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db07-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db07-136">CommonParameters</span></span>
<span data-ttu-id="0db07-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0db07-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db07-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0db07-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db07-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0db07-139">INPUTS</span></span>

### <span data-ttu-id="0db07-140">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0db07-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0db07-141">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0db07-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0db07-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0db07-142">OUTPUTS</span></span>

### <span data-ttu-id="0db07-143">System.void</span><span class="sxs-lookup"><span data-stu-id="0db07-143">System.Void</span></span>

## <span data-ttu-id="0db07-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0db07-144">NOTES</span></span>

## <span data-ttu-id="0db07-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0db07-145">RELATED LINKS</span></span>

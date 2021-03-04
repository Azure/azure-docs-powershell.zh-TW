---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: d183506538bb2063a21eaf33df088ba613a2d3ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916834"
---
# <span data-ttu-id="0131c-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="0131c-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="0131c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0131c-102">SYNOPSIS</span></span>
<span data-ttu-id="0131c-103">同步處理整合執行時間節點之間的認證。</span><span class="sxs-lookup"><span data-stu-id="0131c-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="0131c-104">語法</span><span class="sxs-lookup"><span data-stu-id="0131c-104">SYNTAX</span></span>

### <span data-ttu-id="0131c-105">StopByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0131c-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0131c-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0131c-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0131c-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0131c-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0131c-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0131c-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0131c-109">描述</span><span class="sxs-lookup"><span data-stu-id="0131c-109">DESCRIPTION</span></span>
<span data-ttu-id="0131c-110">**Sync-AzSynapse RuntimeRuntimeCredential Cmdlet** 會同步處理整合執行時間節點之間的內部部署認證，這強制在所有節點中認證完全相同。</span><span class="sxs-lookup"><span data-stu-id="0131c-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="0131c-111">例子</span><span class="sxs-lookup"><span data-stu-id="0131c-111">EXAMPLES</span></span>

### <span data-ttu-id="0131c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0131c-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="0131c-113">同步處理整合執行時間節點之間的認證。</span><span class="sxs-lookup"><span data-stu-id="0131c-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="0131c-114">參數</span><span class="sxs-lookup"><span data-stu-id="0131c-114">PARAMETERS</span></span>

### <span data-ttu-id="0131c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0131c-115">-DefaultProfile</span></span>
<span data-ttu-id="0131c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0131c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0131c-117">-強制</span><span class="sxs-lookup"><span data-stu-id="0131c-117">-Force</span></span>
<span data-ttu-id="0131c-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="0131c-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0131c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0131c-119">-InputObject</span></span>
<span data-ttu-id="0131c-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="0131c-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="0131c-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="0131c-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="0131c-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="0131c-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="0131c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0131c-123">-ResourceGroupName</span></span>
<span data-ttu-id="0131c-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0131c-124">Resource group name.</span></span>

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

### <span data-ttu-id="0131c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0131c-125">-ResourceId</span></span>
<span data-ttu-id="0131c-126">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0131c-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="0131c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0131c-127">-WorkspaceName</span></span>
<span data-ttu-id="0131c-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0131c-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0131c-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0131c-129">-WorkspaceObject</span></span>
<span data-ttu-id="0131c-130">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="0131c-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0131c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0131c-131">-Confirm</span></span>
<span data-ttu-id="0131c-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0131c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0131c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0131c-133">-WhatIf</span></span>
<span data-ttu-id="0131c-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0131c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0131c-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0131c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0131c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0131c-136">CommonParameters</span></span>
<span data-ttu-id="0131c-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0131c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0131c-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0131c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0131c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0131c-139">INPUTS</span></span>

### <span data-ttu-id="0131c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0131c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0131c-141">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="0131c-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0131c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0131c-142">OUTPUTS</span></span>

### <span data-ttu-id="0131c-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="0131c-143">System.Void</span></span>

## <span data-ttu-id="0131c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0131c-144">NOTES</span></span>

## <span data-ttu-id="0131c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0131c-145">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438956"
---
# <span data-ttu-id="d545e-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="d545e-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="d545e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d545e-102">SYNOPSIS</span></span>
<span data-ttu-id="d545e-103">從 SQL pool 中移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="d545e-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="d545e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d545e-104">SYNTAX</span></span>

### <span data-ttu-id="d545e-105">ClearByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d545e-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d545e-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d545e-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d545e-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d545e-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d545e-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d545e-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d545e-109">說明</span><span class="sxs-lookup"><span data-stu-id="d545e-109">DESCRIPTION</span></span>
<span data-ttu-id="d545e-110">**Reset AzSynapseSqlPoolAdvancedThreatProtectionSetting** Cmdlet 會從 Azure SYNAPSE Analytics SQL pool 中移除高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="d545e-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d545e-111">示例</span><span class="sxs-lookup"><span data-stu-id="d545e-111">EXAMPLES</span></span>

### <span data-ttu-id="d545e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d545e-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="d545e-113">這個命令會從名為 ContosoWorkspace 的工作區下，從名為 ContosoSqlPool 的 SQL pool 中移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="d545e-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d545e-114">參數</span><span class="sxs-lookup"><span data-stu-id="d545e-114">PARAMETERS</span></span>

### <span data-ttu-id="d545e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d545e-115">-AsJob</span></span>
<span data-ttu-id="d545e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d545e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d545e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d545e-117">-DefaultProfile</span></span>
<span data-ttu-id="d545e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d545e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d545e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d545e-119">-InputObject</span></span>
<span data-ttu-id="d545e-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d545e-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d545e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d545e-121">-Name</span></span>
<span data-ttu-id="d545e-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d545e-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet, ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d545e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d545e-123">-PassThru</span></span>
<span data-ttu-id="d545e-124">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="d545e-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d545e-125">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="d545e-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d545e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d545e-126">-ResourceGroupName</span></span>
<span data-ttu-id="d545e-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d545e-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d545e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d545e-128">-ResourceId</span></span>
<span data-ttu-id="d545e-129">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d545e-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d545e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d545e-130">-WorkspaceName</span></span>
<span data-ttu-id="d545e-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d545e-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d545e-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d545e-132">-WorkspaceObject</span></span>
<span data-ttu-id="d545e-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d545e-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d545e-134">-確認</span><span class="sxs-lookup"><span data-stu-id="d545e-134">-Confirm</span></span>
<span data-ttu-id="d545e-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d545e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d545e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d545e-136">-WhatIf</span></span>
<span data-ttu-id="d545e-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d545e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d545e-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d545e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d545e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d545e-139">CommonParameters</span></span>
<span data-ttu-id="d545e-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d545e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d545e-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d545e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d545e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d545e-142">INPUTS</span></span>

### <span data-ttu-id="d545e-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d545e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d545e-144">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d545e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d545e-145">輸出</span><span class="sxs-lookup"><span data-stu-id="d545e-145">OUTPUTS</span></span>

### <span data-ttu-id="d545e-146">System.object</span><span class="sxs-lookup"><span data-stu-id="d545e-146">System.Boolean</span></span>

## <span data-ttu-id="d545e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="d545e-147">NOTES</span></span>

## <span data-ttu-id="d545e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="d545e-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142858"
---
# <span data-ttu-id="a4615-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a4615-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a4615-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4615-102">SYNOPSIS</span></span>
<span data-ttu-id="a4615-103">從 SQL pool 中移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="a4615-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="a4615-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4615-104">SYNTAX</span></span>

### <span data-ttu-id="a4615-105">ClearByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4615-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4615-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4615-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4615-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4615-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4615-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4615-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4615-109">說明</span><span class="sxs-lookup"><span data-stu-id="a4615-109">DESCRIPTION</span></span>
<span data-ttu-id="a4615-110">**Reset AzSynapseSqlPoolAdvancedThreatProtectionSetting** Cmdlet 會從 Azure SYNAPSE Analytics SQL pool 中移除高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="a4615-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a4615-111">示例</span><span class="sxs-lookup"><span data-stu-id="a4615-111">EXAMPLES</span></span>

### <span data-ttu-id="a4615-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a4615-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a4615-113">這個命令會從名為 ContosoWorkspace 的工作區下，從名為 ContosoSqlPool 的 SQL pool 中移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="a4615-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a4615-114">參數</span><span class="sxs-lookup"><span data-stu-id="a4615-114">PARAMETERS</span></span>

### <span data-ttu-id="a4615-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4615-115">-AsJob</span></span>
<span data-ttu-id="a4615-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a4615-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4615-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4615-117">-DefaultProfile</span></span>
<span data-ttu-id="a4615-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4615-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4615-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4615-119">-InputObject</span></span>
<span data-ttu-id="a4615-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a4615-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a4615-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4615-121">-Name</span></span>
<span data-ttu-id="a4615-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4615-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a4615-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4615-123">-PassThru</span></span>
<span data-ttu-id="a4615-124">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a4615-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a4615-125">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a4615-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a4615-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4615-126">-ResourceGroupName</span></span>
<span data-ttu-id="a4615-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a4615-127">Resource group name.</span></span>

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

### <span data-ttu-id="a4615-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4615-128">-ResourceId</span></span>
<span data-ttu-id="a4615-129">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4615-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a4615-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a4615-130">-WorkspaceName</span></span>
<span data-ttu-id="a4615-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4615-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a4615-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a4615-132">-WorkspaceObject</span></span>
<span data-ttu-id="a4615-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a4615-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a4615-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a4615-134">-Confirm</span></span>
<span data-ttu-id="a4615-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4615-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4615-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4615-136">-WhatIf</span></span>
<span data-ttu-id="a4615-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4615-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4615-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4615-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4615-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4615-139">CommonParameters</span></span>
<span data-ttu-id="a4615-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4615-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4615-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4615-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4615-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a4615-142">INPUTS</span></span>

### <span data-ttu-id="a4615-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a4615-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a4615-144">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a4615-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a4615-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a4615-145">OUTPUTS</span></span>

### <span data-ttu-id="a4615-146">System.object</span><span class="sxs-lookup"><span data-stu-id="a4615-146">System.Boolean</span></span>

## <span data-ttu-id="a4615-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a4615-147">NOTES</span></span>

## <span data-ttu-id="a4615-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4615-148">RELATED LINKS</span></span>

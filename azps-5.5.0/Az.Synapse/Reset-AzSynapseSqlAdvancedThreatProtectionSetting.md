---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142867"
---
# <span data-ttu-id="54cc3-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="54cc3-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="54cc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="54cc3-103">移除工作區中的 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="54cc3-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="54cc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="54cc3-104">SYNTAX</span></span>

### <span data-ttu-id="54cc3-105">ClearByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="54cc3-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54cc3-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54cc3-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54cc3-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54cc3-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54cc3-108">說明</span><span class="sxs-lookup"><span data-stu-id="54cc3-108">DESCRIPTION</span></span>
<span data-ttu-id="54cc3-109">**Reset AzSynapseSqlAdvancedThreatProtectionSetting** Cmdlet 會從 Azure Synapse Analytics 工作區中移除高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="54cc3-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="54cc3-110">示例</span><span class="sxs-lookup"><span data-stu-id="54cc3-110">EXAMPLES</span></span>

### <span data-ttu-id="54cc3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="54cc3-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="54cc3-112">這個命令會從名為 ContosoWorkspace 的工作區移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="54cc3-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="54cc3-113">參數</span><span class="sxs-lookup"><span data-stu-id="54cc3-113">PARAMETERS</span></span>

### <span data-ttu-id="54cc3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54cc3-114">-AsJob</span></span>
<span data-ttu-id="54cc3-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54cc3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54cc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cc3-116">-DefaultProfile</span></span>
<span data-ttu-id="54cc3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54cc3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54cc3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54cc3-118">-InputObject</span></span>
<span data-ttu-id="54cc3-119">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="54cc3-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54cc3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54cc3-120">-PassThru</span></span>
<span data-ttu-id="54cc3-121">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="54cc3-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="54cc3-122">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="54cc3-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="54cc3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54cc3-123">-ResourceGroupName</span></span>
<span data-ttu-id="54cc3-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="54cc3-124">Resource group name.</span></span>

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

### <span data-ttu-id="54cc3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54cc3-125">-ResourceId</span></span>
<span data-ttu-id="54cc3-126">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="54cc3-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="54cc3-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54cc3-127">-WorkspaceName</span></span>
<span data-ttu-id="54cc3-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="54cc3-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="54cc3-129">-確認</span><span class="sxs-lookup"><span data-stu-id="54cc3-129">-Confirm</span></span>
<span data-ttu-id="54cc3-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54cc3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54cc3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54cc3-131">-WhatIf</span></span>
<span data-ttu-id="54cc3-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54cc3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54cc3-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54cc3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54cc3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cc3-134">CommonParameters</span></span>
<span data-ttu-id="54cc3-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54cc3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cc3-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="54cc3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cc3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="54cc3-137">INPUTS</span></span>

### <span data-ttu-id="54cc3-138">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="54cc3-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="54cc3-139">輸出</span><span class="sxs-lookup"><span data-stu-id="54cc3-139">OUTPUTS</span></span>

### <span data-ttu-id="54cc3-140">System.object</span><span class="sxs-lookup"><span data-stu-id="54cc3-140">System.Boolean</span></span>

## <span data-ttu-id="54cc3-141">筆記</span><span class="sxs-lookup"><span data-stu-id="54cc3-141">NOTES</span></span>

## <span data-ttu-id="54cc3-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="54cc3-142">RELATED LINKS</span></span>

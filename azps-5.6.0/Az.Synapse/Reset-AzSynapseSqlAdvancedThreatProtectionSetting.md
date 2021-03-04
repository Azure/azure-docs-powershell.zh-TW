---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9b4e55f701b956fc653cf08cddb87997a998315e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910901"
---
# <span data-ttu-id="978b9-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="978b9-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="978b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="978b9-102">SYNOPSIS</span></span>
<span data-ttu-id="978b9-103">從工作區移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="978b9-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="978b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="978b9-104">SYNTAX</span></span>

### <span data-ttu-id="978b9-105">ClearByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="978b9-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="978b9-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="978b9-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="978b9-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="978b9-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978b9-108">描述</span><span class="sxs-lookup"><span data-stu-id="978b9-108">DESCRIPTION</span></span>
<span data-ttu-id="978b9-109">**Reset-AzSynapseSqlAdvancedThreatProtectionSetting** Cmdlet 會從 Azure Synapse Analytics Workspace 移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="978b9-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="978b9-110">例子</span><span class="sxs-lookup"><span data-stu-id="978b9-110">EXAMPLES</span></span>

### <span data-ttu-id="978b9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="978b9-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="978b9-112">此命令會從名為 ContosoWorkspace 的工作區移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="978b9-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="978b9-113">參數</span><span class="sxs-lookup"><span data-stu-id="978b9-113">PARAMETERS</span></span>

### <span data-ttu-id="978b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="978b9-114">-AsJob</span></span>
<span data-ttu-id="978b9-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="978b9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="978b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978b9-116">-DefaultProfile</span></span>
<span data-ttu-id="978b9-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="978b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="978b9-118">-InputObject</span></span>
<span data-ttu-id="978b9-119">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="978b9-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="978b9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="978b9-120">-PassThru</span></span>
<span data-ttu-id="978b9-121">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="978b9-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="978b9-122">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="978b9-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="978b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="978b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="978b9-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="978b9-124">Resource group name.</span></span>

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

### <span data-ttu-id="978b9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="978b9-125">-ResourceId</span></span>
<span data-ttu-id="978b9-126">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="978b9-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="978b9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="978b9-127">-WorkspaceName</span></span>
<span data-ttu-id="978b9-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="978b9-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="978b9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="978b9-129">-Confirm</span></span>
<span data-ttu-id="978b9-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="978b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978b9-131">-WhatIf</span></span>
<span data-ttu-id="978b9-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="978b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="978b9-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="978b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978b9-134">CommonParameters</span></span>
<span data-ttu-id="978b9-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="978b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978b9-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="978b9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978b9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="978b9-137">INPUTS</span></span>

### <span data-ttu-id="978b9-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="978b9-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="978b9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="978b9-139">OUTPUTS</span></span>

### <span data-ttu-id="978b9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="978b9-140">System.Boolean</span></span>

## <span data-ttu-id="978b9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="978b9-141">NOTES</span></span>

## <span data-ttu-id="978b9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="978b9-142">RELATED LINKS</span></span>

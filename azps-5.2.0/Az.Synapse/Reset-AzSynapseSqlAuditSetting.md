---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: b25ca2a026cf5d82aa25f69868ca8605fd75bced
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276503"
---
# <span data-ttu-id="1757f-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="1757f-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="1757f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1757f-102">SYNOPSIS</span></span>
<span data-ttu-id="1757f-103">移除 Azure Synapse Analytics 工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="1757f-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="1757f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1757f-104">SYNTAX</span></span>

### <span data-ttu-id="1757f-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1757f-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1757f-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1757f-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1757f-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1757f-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1757f-108">說明</span><span class="sxs-lookup"><span data-stu-id="1757f-108">DESCRIPTION</span></span>
<span data-ttu-id="1757f-109">**Reset AzSynapseSqlAuditSetting** Cmdlet 會移除 Azure Synapse Analytics 工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="1757f-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="1757f-110">示例</span><span class="sxs-lookup"><span data-stu-id="1757f-110">EXAMPLES</span></span>

### <span data-ttu-id="1757f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1757f-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1757f-112">這個命令會移除名為 ContosoWorkspace 的 Azure Synapse Analytics 工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="1757f-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1757f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1757f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="1757f-114">這個命令會移除名為 ContosoWorkspace 的 Azure Synapse Analytics 工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="1757f-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1757f-115">參數</span><span class="sxs-lookup"><span data-stu-id="1757f-115">PARAMETERS</span></span>

### <span data-ttu-id="1757f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1757f-116">-AsJob</span></span>
<span data-ttu-id="1757f-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1757f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1757f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1757f-118">-DefaultProfile</span></span>
<span data-ttu-id="1757f-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1757f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1757f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1757f-120">-InputObject</span></span>
<span data-ttu-id="1757f-121">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="1757f-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1757f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1757f-122">-PassThru</span></span>
<span data-ttu-id="1757f-123">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="1757f-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1757f-124">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="1757f-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1757f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1757f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1757f-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1757f-126">Resource group name.</span></span>

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

### <span data-ttu-id="1757f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1757f-127">-ResourceId</span></span>
<span data-ttu-id="1757f-128">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1757f-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="1757f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1757f-129">-WorkspaceName</span></span>
<span data-ttu-id="1757f-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1757f-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1757f-131">-確認</span><span class="sxs-lookup"><span data-stu-id="1757f-131">-Confirm</span></span>
<span data-ttu-id="1757f-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1757f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1757f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1757f-133">-WhatIf</span></span>
<span data-ttu-id="1757f-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1757f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1757f-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1757f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1757f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1757f-136">CommonParameters</span></span>
<span data-ttu-id="1757f-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1757f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1757f-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1757f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1757f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="1757f-139">INPUTS</span></span>

### <span data-ttu-id="1757f-140">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="1757f-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1757f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1757f-141">OUTPUTS</span></span>

### <span data-ttu-id="1757f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1757f-142">System.Boolean</span></span>

## <span data-ttu-id="1757f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1757f-143">NOTES</span></span>

## <span data-ttu-id="1757f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1757f-144">RELATED LINKS</span></span>

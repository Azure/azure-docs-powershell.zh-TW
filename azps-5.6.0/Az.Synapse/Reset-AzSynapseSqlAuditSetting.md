---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 00d9682eb6562cfbfb9d06a4c8a6bac3b149cea1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907349"
---
# <span data-ttu-id="d6332-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="d6332-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="d6332-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6332-102">SYNOPSIS</span></span>
<span data-ttu-id="d6332-103">移除 Azure Synapse Analytics Workspace 的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="d6332-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="d6332-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6332-104">SYNTAX</span></span>

### <span data-ttu-id="d6332-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d6332-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6332-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6332-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6332-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6332-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6332-108">描述</span><span class="sxs-lookup"><span data-stu-id="d6332-108">DESCRIPTION</span></span>
<span data-ttu-id="d6332-109">**Reset-AzSynapseSqlAuditSetting** Cmdlet 會移除 Azure Synapse Analytics Workspace 的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="d6332-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="d6332-110">例子</span><span class="sxs-lookup"><span data-stu-id="d6332-110">EXAMPLES</span></span>

### <span data-ttu-id="d6332-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d6332-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d6332-112">此命令會移除名為 ContosoWorkspace 的 Azure Synapse Analytics Workspace 的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="d6332-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d6332-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="d6332-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="d6332-114">此命令會透過管道移除名為 ContosoWorkspace 的 Azure Synapse Analytics Workspace 的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="d6332-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d6332-115">參數</span><span class="sxs-lookup"><span data-stu-id="d6332-115">PARAMETERS</span></span>

### <span data-ttu-id="d6332-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6332-116">-AsJob</span></span>
<span data-ttu-id="d6332-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6332-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6332-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6332-118">-DefaultProfile</span></span>
<span data-ttu-id="d6332-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6332-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6332-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6332-120">-InputObject</span></span>
<span data-ttu-id="d6332-121">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="d6332-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d6332-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6332-122">-PassThru</span></span>
<span data-ttu-id="d6332-123">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="d6332-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d6332-124">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="d6332-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d6332-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6332-125">-ResourceGroupName</span></span>
<span data-ttu-id="d6332-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d6332-126">Resource group name.</span></span>

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

### <span data-ttu-id="d6332-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6332-127">-ResourceId</span></span>
<span data-ttu-id="d6332-128">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6332-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="d6332-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d6332-129">-WorkspaceName</span></span>
<span data-ttu-id="d6332-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6332-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d6332-131">-確認</span><span class="sxs-lookup"><span data-stu-id="d6332-131">-Confirm</span></span>
<span data-ttu-id="d6332-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d6332-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6332-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6332-133">-WhatIf</span></span>
<span data-ttu-id="d6332-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6332-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6332-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6332-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6332-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6332-136">CommonParameters</span></span>
<span data-ttu-id="d6332-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6332-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6332-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6332-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6332-139">輸入</span><span class="sxs-lookup"><span data-stu-id="d6332-139">INPUTS</span></span>

### <span data-ttu-id="d6332-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6332-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d6332-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d6332-141">OUTPUTS</span></span>

### <span data-ttu-id="d6332-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6332-142">System.Boolean</span></span>

## <span data-ttu-id="d6332-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d6332-143">NOTES</span></span>

## <span data-ttu-id="d6332-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6332-144">RELATED LINKS</span></span>

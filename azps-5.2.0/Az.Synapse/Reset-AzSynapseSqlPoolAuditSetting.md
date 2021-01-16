---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274940"
---
# <span data-ttu-id="fb803-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="fb803-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="fb803-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb803-102">SYNOPSIS</span></span>
<span data-ttu-id="fb803-103">移除 Azure Synapse Analytics SQL pool 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="fb803-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fb803-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb803-104">SYNTAX</span></span>

### <span data-ttu-id="fb803-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fb803-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb803-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb803-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb803-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb803-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb803-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb803-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb803-109">說明</span><span class="sxs-lookup"><span data-stu-id="fb803-109">DESCRIPTION</span></span>
<span data-ttu-id="fb803-110">**Reset AzSynapseSqlPoolAuditSetting** Cmdlet 會移除 Azure SYNAPSE Analytics SQL pool 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="fb803-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fb803-111">示例</span><span class="sxs-lookup"><span data-stu-id="fb803-111">EXAMPLES</span></span>

### <span data-ttu-id="fb803-112">範例1</span><span class="sxs-lookup"><span data-stu-id="fb803-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="fb803-113">這個命令會移除工作區 ContosoWorkspace 中稱為 ContosoSqlPool 的 SQL 池的審核設定。</span><span class="sxs-lookup"><span data-stu-id="fb803-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="fb803-114">範例2</span><span class="sxs-lookup"><span data-stu-id="fb803-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="fb803-115">這個命令會在工作區 ContosoWorkspace 透過管線中移除稱為 ContosoSqlPool 的 SQL 池的審核設定。</span><span class="sxs-lookup"><span data-stu-id="fb803-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="fb803-116">參數</span><span class="sxs-lookup"><span data-stu-id="fb803-116">PARAMETERS</span></span>

### <span data-ttu-id="fb803-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb803-117">-AsJob</span></span>
<span data-ttu-id="fb803-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb803-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb803-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb803-119">-DefaultProfile</span></span>
<span data-ttu-id="fb803-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb803-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb803-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb803-121">-InputObject</span></span>
<span data-ttu-id="fb803-122">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="fb803-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb803-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb803-123">-Name</span></span>
<span data-ttu-id="fb803-124">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb803-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb803-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb803-125">-PassThru</span></span>
<span data-ttu-id="fb803-126">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="fb803-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fb803-127">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="fb803-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fb803-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb803-128">-ResourceGroupName</span></span>
<span data-ttu-id="fb803-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fb803-129">Resource group name.</span></span>

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

### <span data-ttu-id="fb803-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb803-130">-ResourceId</span></span>
<span data-ttu-id="fb803-131">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb803-131">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="fb803-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb803-132">-WorkspaceName</span></span>
<span data-ttu-id="fb803-133">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb803-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fb803-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fb803-134">-WorkspaceObject</span></span>
<span data-ttu-id="fb803-135">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="fb803-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fb803-136">-確認</span><span class="sxs-lookup"><span data-stu-id="fb803-136">-Confirm</span></span>
<span data-ttu-id="fb803-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb803-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb803-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb803-138">-WhatIf</span></span>
<span data-ttu-id="fb803-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb803-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb803-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb803-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb803-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb803-141">CommonParameters</span></span>
<span data-ttu-id="fb803-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb803-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb803-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fb803-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb803-144">輸入</span><span class="sxs-lookup"><span data-stu-id="fb803-144">INPUTS</span></span>

### <span data-ttu-id="fb803-145">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="fb803-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fb803-146">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="fb803-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fb803-147">輸出</span><span class="sxs-lookup"><span data-stu-id="fb803-147">OUTPUTS</span></span>

### <span data-ttu-id="fb803-148">System.object</span><span class="sxs-lookup"><span data-stu-id="fb803-148">System.Boolean</span></span>

## <span data-ttu-id="fb803-149">筆記</span><span class="sxs-lookup"><span data-stu-id="fb803-149">NOTES</span></span>

## <span data-ttu-id="fb803-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb803-150">RELATED LINKS</span></span>

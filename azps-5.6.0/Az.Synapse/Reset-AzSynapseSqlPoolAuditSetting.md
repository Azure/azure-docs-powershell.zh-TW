---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 8b47466c2f40ff769c1755ea1d59873a120e5d5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916694"
---
# <span data-ttu-id="d1944-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="d1944-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="d1944-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1944-102">SYNOPSIS</span></span>
<span data-ttu-id="d1944-103">移除 Azure Synapse Analytics SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="d1944-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d1944-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1944-104">SYNTAX</span></span>

### <span data-ttu-id="d1944-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d1944-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1944-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1944-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1944-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1944-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1944-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1944-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1944-109">描述</span><span class="sxs-lookup"><span data-stu-id="d1944-109">DESCRIPTION</span></span>
<span data-ttu-id="d1944-110">**Reset-AzSynapseSqlPoolAuditSetting** Cmdlet 會移除 Azure Synapse Analytics SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="d1944-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d1944-111">例子</span><span class="sxs-lookup"><span data-stu-id="d1944-111">EXAMPLES</span></span>

### <span data-ttu-id="d1944-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d1944-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="d1944-113">此命令會移除工作區 ContosoWorkspace 中名為 ContosoSqlPool 的 SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="d1944-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d1944-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="d1944-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="d1944-115">此命令會透過管線移除工作區 ContosoWorkspace 中稱為 ContosoSqlPool 的 SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="d1944-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d1944-116">參數</span><span class="sxs-lookup"><span data-stu-id="d1944-116">PARAMETERS</span></span>

### <span data-ttu-id="d1944-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1944-117">-AsJob</span></span>
<span data-ttu-id="d1944-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d1944-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1944-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1944-119">-DefaultProfile</span></span>
<span data-ttu-id="d1944-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1944-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1944-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1944-121">-InputObject</span></span>
<span data-ttu-id="d1944-122">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="d1944-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d1944-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1944-123">-Name</span></span>
<span data-ttu-id="d1944-124">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1944-124">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="d1944-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1944-125">-PassThru</span></span>
<span data-ttu-id="d1944-126">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="d1944-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d1944-127">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="d1944-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d1944-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1944-128">-ResourceGroupName</span></span>
<span data-ttu-id="d1944-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d1944-129">Resource group name.</span></span>

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

### <span data-ttu-id="d1944-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1944-130">-ResourceId</span></span>
<span data-ttu-id="d1944-131">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1944-131">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="d1944-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d1944-132">-WorkspaceName</span></span>
<span data-ttu-id="d1944-133">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1944-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d1944-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d1944-134">-WorkspaceObject</span></span>
<span data-ttu-id="d1944-135">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="d1944-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d1944-136">-確認</span><span class="sxs-lookup"><span data-stu-id="d1944-136">-Confirm</span></span>
<span data-ttu-id="d1944-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1944-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1944-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1944-138">-WhatIf</span></span>
<span data-ttu-id="d1944-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1944-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1944-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1944-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1944-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1944-141">CommonParameters</span></span>
<span data-ttu-id="d1944-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1944-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1944-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1944-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1944-144">輸入</span><span class="sxs-lookup"><span data-stu-id="d1944-144">INPUTS</span></span>

### <span data-ttu-id="d1944-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d1944-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d1944-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d1944-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d1944-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d1944-147">OUTPUTS</span></span>

### <span data-ttu-id="d1944-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1944-148">System.Boolean</span></span>

## <span data-ttu-id="d1944-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d1944-149">NOTES</span></span>

## <span data-ttu-id="d1944-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1944-150">RELATED LINKS</span></span>

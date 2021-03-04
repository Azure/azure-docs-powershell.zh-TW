---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: cfcfb283887e221db02c894f7a7712203e516996
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905710"
---
# <span data-ttu-id="8ba0c-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8ba0c-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="8ba0c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8ba0c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba0c-103">繼續 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8ba0c-104">語法</span><span class="sxs-lookup"><span data-stu-id="8ba0c-104">SYNTAX</span></span>

### <span data-ttu-id="8ba0c-105">ResumeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8ba0c-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba0c-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba0c-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba0c-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba0c-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba0c-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba0c-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba0c-109">描述</span><span class="sxs-lookup"><span data-stu-id="8ba0c-109">DESCRIPTION</span></span>
<span data-ttu-id="8ba0c-110">**Resume-AzSynapseSqlPool** Cmdlet 會恢復 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8ba0c-111">例子</span><span class="sxs-lookup"><span data-stu-id="8ba0c-111">EXAMPLES</span></span>

### <span data-ttu-id="8ba0c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="8ba0c-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="8ba0c-113">此命令會恢復暫停的 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8ba0c-114">參數</span><span class="sxs-lookup"><span data-stu-id="8ba0c-114">PARAMETERS</span></span>

### <span data-ttu-id="8ba0c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ba0c-115">-AsJob</span></span>
<span data-ttu-id="8ba0c-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ba0c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ba0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba0c-117">-DefaultProfile</span></span>
<span data-ttu-id="8ba0c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ba0c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba0c-119">-InputObject</span></span>
<span data-ttu-id="8ba0c-120">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba0c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ba0c-121">-Name</span></span>
<span data-ttu-id="8ba0c-122">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba0c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ba0c-123">-PassThru</span></span>
<span data-ttu-id="8ba0c-124">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8ba0c-125">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8ba0c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba0c-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ba0c-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba0c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ba0c-128">-ResourceId</span></span>
<span data-ttu-id="8ba0c-129">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba0c-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8ba0c-130">-WorkspaceName</span></span>
<span data-ttu-id="8ba0c-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba0c-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8ba0c-132">-WorkspaceObject</span></span>
<span data-ttu-id="8ba0c-133">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba0c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="8ba0c-134">-Confirm</span></span>
<span data-ttu-id="8ba0c-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba0c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba0c-136">-WhatIf</span></span>
<span data-ttu-id="8ba0c-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba0c-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba0c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba0c-139">CommonParameters</span></span>
<span data-ttu-id="8ba0c-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8ba0c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba0c-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ba0c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba0c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="8ba0c-142">INPUTS</span></span>

### <span data-ttu-id="8ba0c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8ba0c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8ba0c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8ba0c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8ba0c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8ba0c-145">OUTPUTS</span></span>

### <span data-ttu-id="8ba0c-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8ba0c-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8ba0c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8ba0c-147">NOTES</span></span>

## <span data-ttu-id="8ba0c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ba0c-148">RELATED LINKS</span></span>

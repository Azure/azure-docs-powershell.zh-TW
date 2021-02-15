---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: a278b316a62639c6c33d4f05491e314a2b9a1e85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130367"
---
# <span data-ttu-id="0d36f-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="0d36f-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="0d36f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d36f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d36f-103">移除 SQL 池中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="0d36f-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="0d36f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d36f-104">SYNTAX</span></span>

### <span data-ttu-id="0d36f-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0d36f-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d36f-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d36f-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d36f-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d36f-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d36f-108">說明</span><span class="sxs-lookup"><span data-stu-id="0d36f-108">DESCRIPTION</span></span>
<span data-ttu-id="0d36f-109">Remove-AzSynapseSqlPoolSensitivityClassification Cmdlet 會移除 SQL 池中各欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="0d36f-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="0d36f-110">示例</span><span class="sxs-lookup"><span data-stu-id="0d36f-110">EXAMPLES</span></span>

### <span data-ttu-id="0d36f-111">範例1：移除 Azure Synapse SQL pool 中資料行的資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="0d36f-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="0d36f-112">範例2：使用 [管道] 移除 Azure Synapse SQL pool 中資料行的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="0d36f-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="0d36f-113">範例3：使用 [管道] 移除 Azure Synapse SQL pool 中資料行的資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="0d36f-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="0d36f-114">參數</span><span class="sxs-lookup"><span data-stu-id="0d36f-114">PARAMETERS</span></span>

### <span data-ttu-id="0d36f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d36f-115">-AsJob</span></span>
<span data-ttu-id="0d36f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0d36f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d36f-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="0d36f-117">-ClassificationObject</span></span>
<span data-ttu-id="0d36f-118">代表 SQL Pool 敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="0d36f-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d36f-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0d36f-119">-ColumnName</span></span>
<span data-ttu-id="0d36f-120">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d36f-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d36f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d36f-121">-DefaultProfile</span></span>
<span data-ttu-id="0d36f-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d36f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d36f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d36f-123">-PassThru</span></span>
<span data-ttu-id="0d36f-124">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="0d36f-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0d36f-125">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="0d36f-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0d36f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d36f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0d36f-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0d36f-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d36f-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0d36f-128">-SchemaName</span></span>
<span data-ttu-id="0d36f-129">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d36f-129">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d36f-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="0d36f-130">-SqlPoolName</span></span>
<span data-ttu-id="0d36f-131">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d36f-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d36f-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="0d36f-132">-SqlPoolObject</span></span>
<span data-ttu-id="0d36f-133">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0d36f-133">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d36f-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="0d36f-134">-TableName</span></span>
<span data-ttu-id="0d36f-135">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d36f-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d36f-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d36f-136">-WorkspaceName</span></span>
<span data-ttu-id="0d36f-137">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d36f-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d36f-138">-確認</span><span class="sxs-lookup"><span data-stu-id="0d36f-138">-Confirm</span></span>
<span data-ttu-id="0d36f-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d36f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d36f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d36f-140">-WhatIf</span></span>
<span data-ttu-id="0d36f-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d36f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d36f-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d36f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d36f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d36f-143">CommonParameters</span></span>
<span data-ttu-id="0d36f-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d36f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d36f-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d36f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d36f-146">輸入</span><span class="sxs-lookup"><span data-stu-id="0d36f-146">INPUTS</span></span>

### <span data-ttu-id="0d36f-147">Synapse DataClassification. SqlPoolSensitivityClassificationModel （）</span><span class="sxs-lookup"><span data-stu-id="0d36f-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="0d36f-148">System.object</span><span class="sxs-lookup"><span data-stu-id="0d36f-148">System.String</span></span>

### <span data-ttu-id="0d36f-149">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0d36f-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0d36f-150">輸出</span><span class="sxs-lookup"><span data-stu-id="0d36f-150">OUTPUTS</span></span>

### <span data-ttu-id="0d36f-151">System.object</span><span class="sxs-lookup"><span data-stu-id="0d36f-151">System.Boolean</span></span>

## <span data-ttu-id="0d36f-152">筆記</span><span class="sxs-lookup"><span data-stu-id="0d36f-152">NOTES</span></span>

## <span data-ttu-id="0d36f-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d36f-153">RELATED LINKS</span></span>

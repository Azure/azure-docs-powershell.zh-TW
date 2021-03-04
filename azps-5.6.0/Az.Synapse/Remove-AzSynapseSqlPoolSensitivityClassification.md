---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 58ef691f5f109f301ffae2636d739405000754ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903914"
---
# <span data-ttu-id="4644a-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4644a-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="4644a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4644a-102">SYNOPSIS</span></span>
<span data-ttu-id="4644a-103">移除 SQL 資料庫中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="4644a-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="4644a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4644a-104">SYNTAX</span></span>

### <span data-ttu-id="4644a-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4644a-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4644a-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4644a-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4644a-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4644a-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4644a-108">描述</span><span class="sxs-lookup"><span data-stu-id="4644a-108">DESCRIPTION</span></span>
<span data-ttu-id="4644a-109">Cmdlet Remove-AzSynapseSqlPoolSensitivityClassification移除 SQL 資料庫中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="4644a-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="4644a-110">例子</span><span class="sxs-lookup"><span data-stu-id="4644a-110">EXAMPLES</span></span>

### <span data-ttu-id="4644a-111">範例 1：移除 Azure Synapse SQL 資料庫中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="4644a-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="4644a-112">範例 2：使用管道移除 Azure Synapse SQL 集區中欄的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="4644a-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="4644a-113">範例 3：使用管道移除 Azure Synapse SQL 資料庫中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="4644a-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="4644a-114">參數</span><span class="sxs-lookup"><span data-stu-id="4644a-114">PARAMETERS</span></span>

### <span data-ttu-id="4644a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4644a-115">-AsJob</span></span>
<span data-ttu-id="4644a-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4644a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4644a-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="4644a-117">-ClassificationObject</span></span>
<span data-ttu-id="4644a-118">代表 SQL 資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="4644a-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="4644a-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4644a-119">-ColumnName</span></span>
<span data-ttu-id="4644a-120">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="4644a-120">Name of column.</span></span>

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

### <span data-ttu-id="4644a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4644a-121">-DefaultProfile</span></span>
<span data-ttu-id="4644a-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4644a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4644a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4644a-123">-PassThru</span></span>
<span data-ttu-id="4644a-124">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="4644a-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4644a-125">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="4644a-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4644a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4644a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4644a-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4644a-127">Resource group name.</span></span>

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

### <span data-ttu-id="4644a-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4644a-128">-SchemaName</span></span>
<span data-ttu-id="4644a-129">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="4644a-129">Name of schema.</span></span>

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

### <span data-ttu-id="4644a-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="4644a-130">-SqlPoolName</span></span>
<span data-ttu-id="4644a-131">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4644a-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="4644a-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="4644a-132">-SqlPoolObject</span></span>
<span data-ttu-id="4644a-133">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="4644a-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4644a-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="4644a-134">-TableName</span></span>
<span data-ttu-id="4644a-135">資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="4644a-135">Name of table.</span></span>

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

### <span data-ttu-id="4644a-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4644a-136">-WorkspaceName</span></span>
<span data-ttu-id="4644a-137">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="4644a-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4644a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="4644a-138">-Confirm</span></span>
<span data-ttu-id="4644a-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4644a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4644a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4644a-140">-WhatIf</span></span>
<span data-ttu-id="4644a-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4644a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4644a-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4644a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4644a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4644a-143">CommonParameters</span></span>
<span data-ttu-id="4644a-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4644a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4644a-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4644a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4644a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="4644a-146">INPUTS</span></span>

### <span data-ttu-id="4644a-147">Microsoft.Azure.Commands.Synapse.models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="4644a-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="4644a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="4644a-148">System.String</span></span>

### <span data-ttu-id="4644a-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4644a-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4644a-150">輸出</span><span class="sxs-lookup"><span data-stu-id="4644a-150">OUTPUTS</span></span>

### <span data-ttu-id="4644a-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4644a-151">System.Boolean</span></span>

## <span data-ttu-id="4644a-152">筆記</span><span class="sxs-lookup"><span data-stu-id="4644a-152">NOTES</span></span>

## <span data-ttu-id="4644a-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="4644a-153">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 40d1fe07db7720bfb9fdad061ac3d57298d86a8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908410"
---
# <span data-ttu-id="3ee4b-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3ee4b-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="3ee4b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ee4b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee4b-103">啟用欄的敏感度建議 (在 SQL 資料庫內的所有資料行上預設) 啟用建議。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="3ee4b-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ee4b-104">SYNTAX</span></span>

### <span data-ttu-id="3ee4b-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3ee4b-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ee4b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ee4b-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ee4b-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ee4b-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee4b-108">描述</span><span class="sxs-lookup"><span data-stu-id="3ee4b-108">DESCRIPTION</span></span>
<span data-ttu-id="3ee4b-109">此Enable-AzSynapseSqlPoolSensitivityRecommendation Cmdlet 可在 SQL 資料庫的欄上啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="3ee4b-110">例子</span><span class="sxs-lookup"><span data-stu-id="3ee4b-110">EXAMPLES</span></span>

### <span data-ttu-id="3ee4b-111">範例 1：在 Azure Synapse SQL 資料庫的一個給定資料行上啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="3ee4b-112">範例 2：使用管道在給定資料行 Azure Synapse SQL 資料庫上啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="3ee4b-113">參數</span><span class="sxs-lookup"><span data-stu-id="3ee4b-113">PARAMETERS</span></span>

### <span data-ttu-id="3ee4b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ee4b-114">-AsJob</span></span>
<span data-ttu-id="3ee4b-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3ee4b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ee4b-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3ee4b-116">-ColumnName</span></span>
<span data-ttu-id="3ee4b-117">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-117">Name of column.</span></span>

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

### <span data-ttu-id="3ee4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee4b-118">-DefaultProfile</span></span>
<span data-ttu-id="3ee4b-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ee4b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ee4b-120">-InputObject</span></span>
<span data-ttu-id="3ee4b-121">代表 SQL 資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee4b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ee4b-122">-PassThru</span></span>
<span data-ttu-id="3ee4b-123">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3ee4b-124">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3ee4b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee4b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ee4b-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-126">Resource group name.</span></span>

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

### <span data-ttu-id="3ee4b-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3ee4b-127">-SchemaName</span></span>
<span data-ttu-id="3ee4b-128">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-128">Name of schema.</span></span>

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

### <span data-ttu-id="3ee4b-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="3ee4b-129">-SqlPoolName</span></span>
<span data-ttu-id="3ee4b-130">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="3ee4b-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="3ee4b-131">-SqlPoolObject</span></span>
<span data-ttu-id="3ee4b-132">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-132">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3ee4b-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="3ee4b-133">-TableName</span></span>
<span data-ttu-id="3ee4b-134">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-134">Name of table.</span></span>

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

### <span data-ttu-id="3ee4b-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ee4b-135">-WorkspaceName</span></span>
<span data-ttu-id="3ee4b-136">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3ee4b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="3ee4b-137">-Confirm</span></span>
<span data-ttu-id="3ee4b-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ee4b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee4b-139">-WhatIf</span></span>
<span data-ttu-id="3ee4b-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ee4b-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ee4b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee4b-142">CommonParameters</span></span>
<span data-ttu-id="3ee4b-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ee4b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee4b-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ee4b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee4b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="3ee4b-145">INPUTS</span></span>

### <span data-ttu-id="3ee4b-146">Microsoft.Azure.Commands.Synapse.models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="3ee4b-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="3ee4b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3ee4b-147">System.String</span></span>

### <span data-ttu-id="3ee4b-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3ee4b-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="3ee4b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="3ee4b-149">OUTPUTS</span></span>

### <span data-ttu-id="3ee4b-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ee4b-150">System.Boolean</span></span>

## <span data-ttu-id="3ee4b-151">筆記</span><span class="sxs-lookup"><span data-stu-id="3ee4b-151">NOTES</span></span>

## <span data-ttu-id="3ee4b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ee4b-152">RELATED LINKS</span></span>

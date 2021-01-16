---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285803"
---
# <span data-ttu-id="fc78c-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="fc78c-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="fc78c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc78c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc78c-103">針對資料行啟用敏感度建議 (建議預設會在資料庫中的所有資料行上啟用) 建議。</span><span class="sxs-lookup"><span data-stu-id="fc78c-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="fc78c-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc78c-104">SYNTAX</span></span>

### <span data-ttu-id="fc78c-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc78c-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc78c-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc78c-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc78c-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc78c-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc78c-108">說明</span><span class="sxs-lookup"><span data-stu-id="fc78c-108">DESCRIPTION</span></span>
<span data-ttu-id="fc78c-109">Enable-AzSqlDatabaseSensitivityRecommendation Cmdlet 可在資料庫中的資料行上啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="fc78c-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="fc78c-110">示例</span><span class="sxs-lookup"><span data-stu-id="fc78c-110">EXAMPLES</span></span>

### <span data-ttu-id="fc78c-111">範例1：針對 Azure SQL 資料庫中的特定資料行啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="fc78c-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="fc78c-112">範例2：使用管道在特定欄的 Azure SQL 資料庫上啟用靈敏度建議。</span><span class="sxs-lookup"><span data-stu-id="fc78c-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="fc78c-113">參數</span><span class="sxs-lookup"><span data-stu-id="fc78c-113">PARAMETERS</span></span>

### <span data-ttu-id="fc78c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc78c-114">-AsJob</span></span>
<span data-ttu-id="fc78c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fc78c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc78c-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="fc78c-116">-ColumnName</span></span>
<span data-ttu-id="fc78c-117">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc78c-117">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc78c-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc78c-118">-DatabaseName</span></span>
<span data-ttu-id="fc78c-119">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc78c-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="fc78c-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fc78c-120">-DatabaseObject</span></span>
<span data-ttu-id="fc78c-121">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="fc78c-121">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc78c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc78c-122">-DefaultProfile</span></span>
<span data-ttu-id="fc78c-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc78c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc78c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc78c-124">-InputObject</span></span>
<span data-ttu-id="fc78c-125">代表 SQL 資料庫靈敏度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="fc78c-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc78c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc78c-126">-PassThru</span></span>
<span data-ttu-id="fc78c-127">指定是否要在 Cmdlet 執行結束時輸出靈敏度分類模型</span><span class="sxs-lookup"><span data-stu-id="fc78c-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="fc78c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc78c-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc78c-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc78c-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="fc78c-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fc78c-130">-SchemaName</span></span>
<span data-ttu-id="fc78c-131">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc78c-131">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc78c-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc78c-132">-ServerName</span></span>
<span data-ttu-id="fc78c-133">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="fc78c-133">SQL server name.</span></span>

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

### <span data-ttu-id="fc78c-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="fc78c-134">-TableName</span></span>
<span data-ttu-id="fc78c-135">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc78c-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc78c-136">-確認</span><span class="sxs-lookup"><span data-stu-id="fc78c-136">-Confirm</span></span>
<span data-ttu-id="fc78c-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc78c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc78c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc78c-138">-WhatIf</span></span>
<span data-ttu-id="fc78c-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc78c-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc78c-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc78c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc78c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc78c-141">CommonParameters</span></span>
<span data-ttu-id="fc78c-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc78c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc78c-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fc78c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc78c-144">輸入</span><span class="sxs-lookup"><span data-stu-id="fc78c-144">INPUTS</span></span>

### <span data-ttu-id="fc78c-145">SqlDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="fc78c-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="fc78c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="fc78c-146">OUTPUTS</span></span>

### <span data-ttu-id="fc78c-147">System.object</span><span class="sxs-lookup"><span data-stu-id="fc78c-147">System.Boolean</span></span>

## <span data-ttu-id="fc78c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="fc78c-148">NOTES</span></span>

## <span data-ttu-id="fc78c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc78c-149">RELATED LINKS</span></span>

[<span data-ttu-id="fc78c-150">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="fc78c-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
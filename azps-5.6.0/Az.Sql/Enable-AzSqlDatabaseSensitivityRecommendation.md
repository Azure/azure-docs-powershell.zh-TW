---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e7e13e62407018559835f4703d0b94edeced930b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910586"
---
# <span data-ttu-id="c6b69-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="c6b69-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="c6b69-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6b69-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b69-103">啟用欄的敏感度建議 (資料庫中所有欄上預設) 啟用建議。</span><span class="sxs-lookup"><span data-stu-id="c6b69-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="c6b69-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6b69-104">SYNTAX</span></span>

### <span data-ttu-id="c6b69-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c6b69-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6b69-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6b69-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6b69-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6b69-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6b69-108">描述</span><span class="sxs-lookup"><span data-stu-id="c6b69-108">DESCRIPTION</span></span>
<span data-ttu-id="c6b69-109">此Enable-AzSqlDatabaseSensitivityRecommendation Cmdlet 可針對資料庫中的資料行啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="c6b69-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="c6b69-110">例子</span><span class="sxs-lookup"><span data-stu-id="c6b69-110">EXAMPLES</span></span>

### <span data-ttu-id="c6b69-111">範例 1：在 Azure SQL Database 中為一個欄位啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="c6b69-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="c6b69-112">範例 2：使用管道在給定欄 Azure SQL 資料庫上啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="c6b69-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="c6b69-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6b69-113">PARAMETERS</span></span>

### <span data-ttu-id="c6b69-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6b69-114">-AsJob</span></span>
<span data-ttu-id="c6b69-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c6b69-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6b69-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c6b69-116">-ColumnName</span></span>
<span data-ttu-id="c6b69-117">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6b69-117">Name of column.</span></span>

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

### <span data-ttu-id="c6b69-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6b69-118">-DatabaseName</span></span>
<span data-ttu-id="c6b69-119">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6b69-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="c6b69-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c6b69-120">-DatabaseObject</span></span>
<span data-ttu-id="c6b69-121">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="c6b69-121">The SQL database object.</span></span>

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

### <span data-ttu-id="c6b69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b69-122">-DefaultProfile</span></span>
<span data-ttu-id="c6b69-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6b69-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6b69-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6b69-124">-InputObject</span></span>
<span data-ttu-id="c6b69-125">代表 SQL 資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="c6b69-125">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="c6b69-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6b69-126">-PassThru</span></span>
<span data-ttu-id="c6b69-127">指定是否要在 Cmdlet 執行結束時輸出敏感度分類模型</span><span class="sxs-lookup"><span data-stu-id="c6b69-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="c6b69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b69-128">-ResourceGroupName</span></span>
<span data-ttu-id="c6b69-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6b69-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6b69-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c6b69-130">-SchemaName</span></span>
<span data-ttu-id="c6b69-131">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="c6b69-131">Name of schema.</span></span>

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

### <span data-ttu-id="c6b69-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6b69-132">-ServerName</span></span>
<span data-ttu-id="c6b69-133">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c6b69-133">SQL server name.</span></span>

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

### <span data-ttu-id="c6b69-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="c6b69-134">-TableName</span></span>
<span data-ttu-id="c6b69-135">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6b69-135">Name of table.</span></span>

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

### <span data-ttu-id="c6b69-136">-確認</span><span class="sxs-lookup"><span data-stu-id="c6b69-136">-Confirm</span></span>
<span data-ttu-id="c6b69-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6b69-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b69-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b69-138">-WhatIf</span></span>
<span data-ttu-id="c6b69-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6b69-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6b69-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6b69-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b69-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b69-141">CommonParameters</span></span>
<span data-ttu-id="c6b69-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6b69-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b69-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6b69-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b69-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c6b69-144">INPUTS</span></span>

### <span data-ttu-id="c6b69-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="c6b69-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="c6b69-146">輸出</span><span class="sxs-lookup"><span data-stu-id="c6b69-146">OUTPUTS</span></span>

### <span data-ttu-id="c6b69-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6b69-147">System.Boolean</span></span>

## <span data-ttu-id="c6b69-148">筆記</span><span class="sxs-lookup"><span data-stu-id="c6b69-148">NOTES</span></span>

## <span data-ttu-id="c6b69-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6b69-149">RELATED LINKS</span></span>

[<span data-ttu-id="c6b69-150">深入瞭解 Azure SQL Database 資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="c6b69-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
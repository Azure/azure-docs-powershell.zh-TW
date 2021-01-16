---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283911"
---
# <span data-ttu-id="e2e3b-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="e2e3b-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="e2e3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e3b-103">針對資料庫中的資料行停用 (關閉) 敏感性建議。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="e2e3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2e3b-104">SYNTAX</span></span>

### <span data-ttu-id="e2e3b-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e2e3b-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e3b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2e3b-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e3b-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2e3b-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e3b-108">說明</span><span class="sxs-lookup"><span data-stu-id="e2e3b-108">DESCRIPTION</span></span>
<span data-ttu-id="e2e3b-109">Disable-AzSqlDatabaseSensitivityRecommendation Cmdlet 會停用資料庫中資料行的 (關閉) 敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="e2e3b-110">示例</span><span class="sxs-lookup"><span data-stu-id="e2e3b-110">EXAMPLES</span></span>

### <span data-ttu-id="e2e3b-111">範例1：停用 Azure SQL 資料庫中指定資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="e2e3b-112">範例2：在使用管道的 Azure SQL 資料庫的欄上，停用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="e2e3b-113">範例3：使用管道針對 Azure SQL 資料庫中的特定欄停用靈敏度建議。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="e2e3b-114">參數</span><span class="sxs-lookup"><span data-stu-id="e2e3b-114">PARAMETERS</span></span>

### <span data-ttu-id="e2e3b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2e3b-115">-AsJob</span></span>
<span data-ttu-id="e2e3b-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2e3b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2e3b-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e2e3b-117">-ColumnName</span></span>
<span data-ttu-id="e2e3b-118">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-118">Name of column.</span></span>

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

### <span data-ttu-id="e2e3b-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2e3b-119">-DatabaseName</span></span>
<span data-ttu-id="e2e3b-120">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="e2e3b-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e2e3b-121">-DatabaseObject</span></span>
<span data-ttu-id="e2e3b-122">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-122">The SQL database object.</span></span>

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

### <span data-ttu-id="e2e3b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e3b-123">-DefaultProfile</span></span>
<span data-ttu-id="e2e3b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e3b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2e3b-125">-InputObject</span></span>
<span data-ttu-id="e2e3b-126">代表 SQL 資料庫靈敏度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="e2e3b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2e3b-127">-PassThru</span></span>
<span data-ttu-id="e2e3b-128">指定是否要在 Cmdlet 執行結束時輸出靈敏度分類模型</span><span class="sxs-lookup"><span data-stu-id="e2e3b-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e2e3b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e3b-129">-ResourceGroupName</span></span>
<span data-ttu-id="e2e3b-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2e3b-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e2e3b-131">-SchemaName</span></span>
<span data-ttu-id="e2e3b-132">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-132">Name of schema.</span></span>

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

### <span data-ttu-id="e2e3b-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e2e3b-133">-ServerName</span></span>
<span data-ttu-id="e2e3b-134">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-134">SQL server name.</span></span>

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

### <span data-ttu-id="e2e3b-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="e2e3b-135">-TableName</span></span>
<span data-ttu-id="e2e3b-136">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-136">Name of table.</span></span>

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

### <span data-ttu-id="e2e3b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e2e3b-137">-Confirm</span></span>
<span data-ttu-id="e2e3b-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2e3b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e3b-139">-WhatIf</span></span>
<span data-ttu-id="e2e3b-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2e3b-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2e3b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e3b-142">CommonParameters</span></span>
<span data-ttu-id="e2e3b-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e3b-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e2e3b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e3b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e2e3b-145">INPUTS</span></span>

### <span data-ttu-id="e2e3b-146">SqlDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="e2e3b-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="e2e3b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e2e3b-147">OUTPUTS</span></span>

### <span data-ttu-id="e2e3b-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e2e3b-148">System.Boolean</span></span>

## <span data-ttu-id="e2e3b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e2e3b-149">NOTES</span></span>

## <span data-ttu-id="e2e3b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2e3b-150">RELATED LINKS</span></span>

[<span data-ttu-id="e2e3b-151">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="e2e3b-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
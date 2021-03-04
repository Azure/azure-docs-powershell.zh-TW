---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 88e08a15c864386d2e073f83f437d0db537f2ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915209"
---
# <span data-ttu-id="c0405-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="c0405-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="c0405-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0405-102">SYNOPSIS</span></span>
<span data-ttu-id="c0405-103">設定資料庫中資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c0405-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="c0405-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0405-104">SYNTAX</span></span>

### <span data-ttu-id="c0405-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c0405-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0405-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0405-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0405-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0405-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0405-108">描述</span><span class="sxs-lookup"><span data-stu-id="c0405-108">DESCRIPTION</span></span>
<span data-ttu-id="c0405-109">此Set-AzSqlDatabaseSensitivityClassification Cmdlet 會設定資料庫中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c0405-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="c0405-110">例子</span><span class="sxs-lookup"><span data-stu-id="c0405-110">EXAMPLES</span></span>

### <span data-ttu-id="c0405-111">範例 1：在 Azure SQL 資料庫中設定資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c0405-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="c0405-112">範例 2：在 Azure SQL 資料庫中設定欄的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c0405-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="c0405-113">範例 3：在 Azure SQL 資料庫中使用管線設定資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c0405-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="c0405-114">參數</span><span class="sxs-lookup"><span data-stu-id="c0405-114">PARAMETERS</span></span>

### <span data-ttu-id="c0405-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0405-115">-AsJob</span></span>
<span data-ttu-id="c0405-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0405-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0405-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="c0405-117">-ClassificationObject</span></span>
<span data-ttu-id="c0405-118">代表 SQL 資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="c0405-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0405-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c0405-119">-ColumnName</span></span>
<span data-ttu-id="c0405-120">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0405-120">Name of column.</span></span>

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

### <span data-ttu-id="c0405-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0405-121">-DatabaseName</span></span>
<span data-ttu-id="c0405-122">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0405-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="c0405-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c0405-123">-DatabaseObject</span></span>
<span data-ttu-id="c0405-124">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="c0405-124">The SQL database object.</span></span>

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

### <span data-ttu-id="c0405-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0405-125">-DefaultProfile</span></span>
<span data-ttu-id="c0405-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0405-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0405-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="c0405-127">-InformationType</span></span>
<span data-ttu-id="c0405-128">描述資料行中儲存之資料之資訊類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0405-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0405-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0405-129">-PassThru</span></span>
<span data-ttu-id="c0405-130">指定是否要在 Cmdlet 執行結束時輸出敏感度分類模型</span><span class="sxs-lookup"><span data-stu-id="c0405-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="c0405-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0405-131">-ResourceGroupName</span></span>
<span data-ttu-id="c0405-132">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0405-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0405-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c0405-133">-SchemaName</span></span>
<span data-ttu-id="c0405-134">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="c0405-134">Name of schema.</span></span>

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

### <span data-ttu-id="c0405-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="c0405-135">-SensitivityLabel</span></span>
<span data-ttu-id="c0405-136">描述資料行中儲存之資料的敏感度的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0405-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0405-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c0405-137">-ServerName</span></span>
<span data-ttu-id="c0405-138">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c0405-138">SQL server name.</span></span>

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

### <span data-ttu-id="c0405-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="c0405-139">-TableName</span></span>
<span data-ttu-id="c0405-140">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0405-140">Name of table.</span></span>

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

### <span data-ttu-id="c0405-141">-確認</span><span class="sxs-lookup"><span data-stu-id="c0405-141">-Confirm</span></span>
<span data-ttu-id="c0405-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0405-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0405-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0405-143">-WhatIf</span></span>
<span data-ttu-id="c0405-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0405-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0405-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0405-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0405-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0405-146">CommonParameters</span></span>
<span data-ttu-id="c0405-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0405-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0405-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0405-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0405-149">輸入</span><span class="sxs-lookup"><span data-stu-id="c0405-149">INPUTS</span></span>

### <span data-ttu-id="c0405-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="c0405-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="c0405-151">輸出</span><span class="sxs-lookup"><span data-stu-id="c0405-151">OUTPUTS</span></span>

### <span data-ttu-id="c0405-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0405-152">System.Boolean</span></span>

## <span data-ttu-id="c0405-153">筆記</span><span class="sxs-lookup"><span data-stu-id="c0405-153">NOTES</span></span>

## <span data-ttu-id="c0405-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0405-154">RELATED LINKS</span></span>

[<span data-ttu-id="c0405-155">深入瞭解 Azure SQL Database 資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="c0405-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)

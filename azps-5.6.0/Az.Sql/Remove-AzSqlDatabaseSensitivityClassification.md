---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 3cc73a3f359207db947c03bf42aafb3c7beff11e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904262"
---
# <span data-ttu-id="88265-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="88265-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="88265-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88265-102">SYNOPSIS</span></span>
<span data-ttu-id="88265-103">移除資料庫中資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88265-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="88265-104">語法</span><span class="sxs-lookup"><span data-stu-id="88265-104">SYNTAX</span></span>

### <span data-ttu-id="88265-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="88265-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88265-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="88265-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88265-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="88265-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88265-108">描述</span><span class="sxs-lookup"><span data-stu-id="88265-108">DESCRIPTION</span></span>
<span data-ttu-id="88265-109">Cmdlet Remove-AzSqlDatabaseSensitivityClassification移除資料庫中資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88265-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="88265-110">例子</span><span class="sxs-lookup"><span data-stu-id="88265-110">EXAMPLES</span></span>

### <span data-ttu-id="88265-111">範例 1：移除 Azure SQL Database 中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88265-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="88265-112">範例 2：使用管道移除 Azure SQL 資料庫中資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88265-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="88265-113">範例 3：使用管道移除 Azure SQL 資料庫中資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88265-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="88265-114">參數</span><span class="sxs-lookup"><span data-stu-id="88265-114">PARAMETERS</span></span>

### <span data-ttu-id="88265-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88265-115">-AsJob</span></span>
<span data-ttu-id="88265-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88265-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88265-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="88265-117">-ClassificationObject</span></span>
<span data-ttu-id="88265-118">代表 SQL 資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="88265-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="88265-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="88265-119">-ColumnName</span></span>
<span data-ttu-id="88265-120">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="88265-120">Name of column.</span></span>

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

### <span data-ttu-id="88265-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88265-121">-DatabaseName</span></span>
<span data-ttu-id="88265-122">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="88265-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="88265-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="88265-123">-DatabaseObject</span></span>
<span data-ttu-id="88265-124">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="88265-124">The SQL database object.</span></span>

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

### <span data-ttu-id="88265-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88265-125">-DefaultProfile</span></span>
<span data-ttu-id="88265-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88265-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88265-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88265-127">-PassThru</span></span>
<span data-ttu-id="88265-128">指定是否要在 Cmdlet 執行結束時輸出敏感度分類模型</span><span class="sxs-lookup"><span data-stu-id="88265-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="88265-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88265-129">-ResourceGroupName</span></span>
<span data-ttu-id="88265-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88265-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="88265-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="88265-131">-SchemaName</span></span>
<span data-ttu-id="88265-132">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="88265-132">Name of schema.</span></span>

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

### <span data-ttu-id="88265-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="88265-133">-ServerName</span></span>
<span data-ttu-id="88265-134">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="88265-134">SQL server name.</span></span>

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

### <span data-ttu-id="88265-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="88265-135">-TableName</span></span>
<span data-ttu-id="88265-136">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="88265-136">Name of table.</span></span>

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

### <span data-ttu-id="88265-137">-確認</span><span class="sxs-lookup"><span data-stu-id="88265-137">-Confirm</span></span>
<span data-ttu-id="88265-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="88265-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88265-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88265-139">-WhatIf</span></span>
<span data-ttu-id="88265-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88265-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88265-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88265-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88265-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88265-142">CommonParameters</span></span>
<span data-ttu-id="88265-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88265-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88265-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88265-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88265-145">輸入</span><span class="sxs-lookup"><span data-stu-id="88265-145">INPUTS</span></span>

### <span data-ttu-id="88265-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="88265-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="88265-147">輸出</span><span class="sxs-lookup"><span data-stu-id="88265-147">OUTPUTS</span></span>

### <span data-ttu-id="88265-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88265-148">System.Boolean</span></span>

## <span data-ttu-id="88265-149">筆記</span><span class="sxs-lookup"><span data-stu-id="88265-149">NOTES</span></span>

## <span data-ttu-id="88265-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="88265-150">RELATED LINKS</span></span>

[<span data-ttu-id="88265-151">深入瞭解 Azure SQL Database 資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="88265-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)

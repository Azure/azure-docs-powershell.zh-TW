---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 50bd23f0c0be638683dae4acb5b43165a8c5b4f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620463"
---
# <span data-ttu-id="f8c86-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f8c86-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="f8c86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8c86-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c86-103">取得資料庫中資料行的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="f8c86-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="f8c86-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8c86-104">SYNTAX</span></span>

### <span data-ttu-id="f8c86-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f8c86-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c86-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8c86-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c86-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8c86-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c86-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8c86-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8c86-109">說明</span><span class="sxs-lookup"><span data-stu-id="f8c86-109">DESCRIPTION</span></span>
<span data-ttu-id="f8c86-110">Get-AzSqlDatabaseSensitivityClassification Cmdlet 會傳回 Azure SQL 資料庫中資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="f8c86-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="f8c86-111">示例</span><span class="sxs-lookup"><span data-stu-id="f8c86-111">EXAMPLES</span></span>

### <span data-ttu-id="f8c86-112">範例1：取得 Azure SQL 資料庫的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="f8c86-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="f8c86-113">範例2：使用管道取得 Azure SQL 資料庫的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="f8c86-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="f8c86-114">範例3：取得 Azure SQL 資料庫特定資料行的目前資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="f8c86-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="f8c86-115">範例4：使用管道取得 Azure SQL Database 之特定資料行的目前資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="f8c86-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="f8c86-116">參數</span><span class="sxs-lookup"><span data-stu-id="f8c86-116">PARAMETERS</span></span>

### <span data-ttu-id="f8c86-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8c86-117">-AsJob</span></span>
<span data-ttu-id="f8c86-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f8c86-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8c86-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f8c86-119">-ColumnName</span></span>
<span data-ttu-id="f8c86-120">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8c86-120">Name of column.</span></span>

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

### <span data-ttu-id="f8c86-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8c86-121">-DatabaseName</span></span>
<span data-ttu-id="f8c86-122">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8c86-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8c86-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f8c86-123">-DatabaseObject</span></span>
<span data-ttu-id="f8c86-124">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="f8c86-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8c86-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c86-125">-DefaultProfile</span></span>
<span data-ttu-id="f8c86-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8c86-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c86-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8c86-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8c86-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8c86-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f8c86-129">-SchemaName</span></span>
<span data-ttu-id="f8c86-130">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8c86-130">Name of schema.</span></span>

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

### <span data-ttu-id="f8c86-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f8c86-131">-ServerName</span></span>
<span data-ttu-id="f8c86-132">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="f8c86-132">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8c86-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="f8c86-133">-TableName</span></span>
<span data-ttu-id="f8c86-134">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8c86-134">Name of table.</span></span>

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

### <span data-ttu-id="f8c86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c86-135">CommonParameters</span></span>
<span data-ttu-id="f8c86-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8c86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c86-137">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8c86-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c86-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f8c86-138">INPUTS</span></span>

### <span data-ttu-id="f8c86-139">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="f8c86-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f8c86-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f8c86-140">OUTPUTS</span></span>

### <span data-ttu-id="f8c86-141">SqlDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="f8c86-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="f8c86-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f8c86-142">NOTES</span></span>

## <span data-ttu-id="f8c86-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8c86-143">RELATED LINKS</span></span>

[<span data-ttu-id="f8c86-144">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="f8c86-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)

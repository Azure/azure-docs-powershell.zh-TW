---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 32459ad76bb118e97ba29e1730c6006a69b4a3b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917606"
---
# <span data-ttu-id="b1bdb-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="b1bdb-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="b1bdb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="b1bdb-103">在資料庫中獲取資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="b1bdb-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1bdb-104">SYNTAX</span></span>

### <span data-ttu-id="b1bdb-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1bdb-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1bdb-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1bdb-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1bdb-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1bdb-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1bdb-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1bdb-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1bdb-109">描述</span><span class="sxs-lookup"><span data-stu-id="b1bdb-109">DESCRIPTION</span></span>
<span data-ttu-id="b1bdb-110">此Get-AzSqlDatabaseSensitivityClassification Cmdlet 會返回 Azure SQL 資料庫中資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="b1bdb-111">例子</span><span class="sxs-lookup"><span data-stu-id="b1bdb-111">EXAMPLES</span></span>

### <span data-ttu-id="b1bdb-112">範例 1：取得 Azure SQL Database 的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="b1bdb-113">範例 2：使用管道取得 Azure SQL 資料庫的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="b1bdb-114">範例 3：取得 Azure SQL Database 特定資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="b1bdb-115">範例 4：使用管道取得 Azure SQL 資料庫特定資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="b1bdb-116">參數</span><span class="sxs-lookup"><span data-stu-id="b1bdb-116">PARAMETERS</span></span>

### <span data-ttu-id="b1bdb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1bdb-117">-AsJob</span></span>
<span data-ttu-id="b1bdb-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b1bdb-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1bdb-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b1bdb-119">-ColumnName</span></span>
<span data-ttu-id="b1bdb-120">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-120">Name of column.</span></span>

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

### <span data-ttu-id="b1bdb-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1bdb-121">-DatabaseName</span></span>
<span data-ttu-id="b1bdb-122">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="b1bdb-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b1bdb-123">-DatabaseObject</span></span>
<span data-ttu-id="b1bdb-124">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-124">The SQL database object.</span></span>

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

### <span data-ttu-id="b1bdb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1bdb-125">-DefaultProfile</span></span>
<span data-ttu-id="b1bdb-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1bdb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1bdb-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1bdb-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1bdb-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b1bdb-129">-SchemaName</span></span>
<span data-ttu-id="b1bdb-130">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-130">Name of schema.</span></span>

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

### <span data-ttu-id="b1bdb-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b1bdb-131">-ServerName</span></span>
<span data-ttu-id="b1bdb-132">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-132">SQL server name.</span></span>

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

### <span data-ttu-id="b1bdb-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="b1bdb-133">-TableName</span></span>
<span data-ttu-id="b1bdb-134">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-134">Name of table.</span></span>

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

### <span data-ttu-id="b1bdb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1bdb-135">CommonParameters</span></span>
<span data-ttu-id="b1bdb-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1bdb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1bdb-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1bdb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1bdb-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b1bdb-138">INPUTS</span></span>

### <span data-ttu-id="b1bdb-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b1bdb-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b1bdb-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b1bdb-140">OUTPUTS</span></span>

### <span data-ttu-id="b1bdb-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b1bdb-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b1bdb-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b1bdb-142">NOTES</span></span>

## <span data-ttu-id="b1bdb-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1bdb-143">RELATED LINKS</span></span>

[<span data-ttu-id="b1bdb-144">深入瞭解 Azure SQL Database 資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="b1bdb-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)

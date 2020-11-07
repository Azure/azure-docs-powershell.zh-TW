---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: ba8229bcddf27a2a14d50efc2cbd32e6e47015c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792533"
---
# <span data-ttu-id="5dccc-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="5dccc-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="5dccc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5dccc-102">SYNOPSIS</span></span>
<span data-ttu-id="5dccc-103">取得資料庫中資料行的建議資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5dccc-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="5dccc-104">句法</span><span class="sxs-lookup"><span data-stu-id="5dccc-104">SYNTAX</span></span>

### <span data-ttu-id="5dccc-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5dccc-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dccc-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dccc-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dccc-107">說明</span><span class="sxs-lookup"><span data-stu-id="5dccc-107">DESCRIPTION</span></span>
<span data-ttu-id="5dccc-108">Get-AzSqlDatabaseSensitivityRecommendation Cmdlet 會傳回建議的資訊類型，以及資料庫中資料行的敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5dccc-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="5dccc-109">示例</span><span class="sxs-lookup"><span data-stu-id="5dccc-109">EXAMPLES</span></span>

### <span data-ttu-id="5dccc-110">範例1：取得 Azure SQL 資料庫的建議資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5dccc-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

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

### <span data-ttu-id="5dccc-111">範例2：使用管道取得 Azure SQL 資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5dccc-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

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

## <span data-ttu-id="5dccc-112">參數</span><span class="sxs-lookup"><span data-stu-id="5dccc-112">PARAMETERS</span></span>

### <span data-ttu-id="5dccc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5dccc-113">-AsJob</span></span>
<span data-ttu-id="5dccc-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5dccc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5dccc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5dccc-115">-DatabaseName</span></span>
<span data-ttu-id="5dccc-116">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dccc-116">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccc-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5dccc-117">-DatabaseObject</span></span>
<span data-ttu-id="5dccc-118">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="5dccc-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dccc-119">-DefaultProfile</span></span>
<span data-ttu-id="5dccc-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5dccc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dccc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dccc-121">-ResourceGroupName</span></span>
<span data-ttu-id="5dccc-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dccc-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccc-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5dccc-123">-ServerName</span></span>
<span data-ttu-id="5dccc-124">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="5dccc-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dccc-125">CommonParameters</span></span>
<span data-ttu-id="5dccc-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5dccc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dccc-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5dccc-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dccc-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5dccc-128">INPUTS</span></span>

### <span data-ttu-id="5dccc-129">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="5dccc-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5dccc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5dccc-130">OUTPUTS</span></span>

### <span data-ttu-id="5dccc-131">SqlDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="5dccc-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="5dccc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5dccc-132">NOTES</span></span>

## <span data-ttu-id="5dccc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dccc-133">RELATED LINKS</span></span>

[<span data-ttu-id="5dccc-134">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="5dccc-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)

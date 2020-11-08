---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129882"
---
# <span data-ttu-id="fc834-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="fc834-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="fc834-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc834-102">SYNOPSIS</span></span>
<span data-ttu-id="fc834-103">取得資料庫中資料行的建議資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="fc834-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="fc834-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc834-104">SYNTAX</span></span>

### <span data-ttu-id="fc834-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc834-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc834-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc834-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc834-107">說明</span><span class="sxs-lookup"><span data-stu-id="fc834-107">DESCRIPTION</span></span>
<span data-ttu-id="fc834-108">Get-AzSqlDatabaseSensitivityRecommendation Cmdlet 會傳回建議的資訊類型，以及資料庫中資料行的敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="fc834-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="fc834-109">示例</span><span class="sxs-lookup"><span data-stu-id="fc834-109">EXAMPLES</span></span>

### <span data-ttu-id="fc834-110">範例1：取得 Azure SQL 資料庫的建議資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="fc834-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

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

### <span data-ttu-id="fc834-111">範例2：使用管道取得 Azure SQL 資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="fc834-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

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

## <span data-ttu-id="fc834-112">參數</span><span class="sxs-lookup"><span data-stu-id="fc834-112">PARAMETERS</span></span>

### <span data-ttu-id="fc834-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc834-113">-AsJob</span></span>
<span data-ttu-id="fc834-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fc834-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc834-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc834-115">-DatabaseName</span></span>
<span data-ttu-id="fc834-116">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc834-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="fc834-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fc834-117">-DatabaseObject</span></span>
<span data-ttu-id="fc834-118">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="fc834-118">The SQL database object.</span></span>

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

### <span data-ttu-id="fc834-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc834-119">-DefaultProfile</span></span>
<span data-ttu-id="fc834-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc834-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc834-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc834-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc834-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc834-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="fc834-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc834-123">-ServerName</span></span>
<span data-ttu-id="fc834-124">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="fc834-124">SQL server name.</span></span>

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

### <span data-ttu-id="fc834-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc834-125">CommonParameters</span></span>
<span data-ttu-id="fc834-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc834-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc834-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fc834-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc834-128">輸入</span><span class="sxs-lookup"><span data-stu-id="fc834-128">INPUTS</span></span>

### <span data-ttu-id="fc834-129">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="fc834-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fc834-130">輸出</span><span class="sxs-lookup"><span data-stu-id="fc834-130">OUTPUTS</span></span>

### <span data-ttu-id="fc834-131">SqlDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="fc834-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="fc834-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fc834-132">NOTES</span></span>

## <span data-ttu-id="fc834-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc834-133">RELATED LINKS</span></span>

[<span data-ttu-id="fc834-134">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="fc834-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)

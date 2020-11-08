---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fe8cffb4ab9d79828795cc1148a3c109cfbfdddb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970126"
---
# <span data-ttu-id="c2e4d-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="c2e4d-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="c2e4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e4d-103">取得 Azure SQL managed 實例資料庫中資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="c2e4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2e4d-104">SYNTAX</span></span>

### <span data-ttu-id="c2e4d-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c2e4d-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2e4d-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2e4d-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2e4d-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2e4d-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2e4d-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2e4d-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2e4d-109">說明</span><span class="sxs-lookup"><span data-stu-id="c2e4d-109">DESCRIPTION</span></span>
<span data-ttu-id="c2e4d-110">Get-AzSqlInstanceDatabaseSensitivityClassification Cmdlet 會傳回 Azure SQL managed 實例資料庫中資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="c2e4d-111">示例</span><span class="sxs-lookup"><span data-stu-id="c2e4d-111">EXAMPLES</span></span>

### <span data-ttu-id="c2e4d-112">範例1：取得 Azure SQL managed 實例資料庫的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="c2e4d-113">範例2：使用管道取得 Azure SQL managed 實例資料庫的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="c2e4d-114">範例3：取得 Azure SQL managed 實例資料庫之特定資料行的目前資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="c2e4d-115">範例4：使用管道取得 Azure SQL managed 實例資料庫之特定資料行的目前資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="c2e4d-116">參數</span><span class="sxs-lookup"><span data-stu-id="c2e4d-116">PARAMETERS</span></span>

### <span data-ttu-id="c2e4d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2e4d-117">-AsJob</span></span>
<span data-ttu-id="c2e4d-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2e4d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2e4d-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c2e4d-119">-ColumnName</span></span>
<span data-ttu-id="c2e4d-120">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-120">Name of column.</span></span>

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

### <span data-ttu-id="c2e4d-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2e4d-121">-DatabaseName</span></span>
<span data-ttu-id="c2e4d-122">Azure SQL managed 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="c2e4d-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c2e4d-123">-DatabaseObject</span></span>
<span data-ttu-id="c2e4d-124">Azure SQL managed 實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e4d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e4d-125">-DefaultProfile</span></span>
<span data-ttu-id="c2e4d-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2e4d-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2e4d-127">-InstanceName</span></span>
<span data-ttu-id="c2e4d-128">Azure SQL managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="c2e4d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2e4d-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2e4d-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c2e4d-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c2e4d-131">-SchemaName</span></span>
<span data-ttu-id="c2e4d-132">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-132">Name of schema.</span></span>

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

### <span data-ttu-id="c2e4d-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="c2e4d-133">-TableName</span></span>
<span data-ttu-id="c2e4d-134">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-134">Name of table.</span></span>

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

### <span data-ttu-id="c2e4d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e4d-135">CommonParameters</span></span>
<span data-ttu-id="c2e4d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e4d-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c2e4d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e4d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c2e4d-138">INPUTS</span></span>

### <span data-ttu-id="c2e4d-139">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="c2e4d-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="c2e4d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c2e4d-140">OUTPUTS</span></span>

### <span data-ttu-id="c2e4d-141">ManagedDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="c2e4d-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="c2e4d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c2e4d-142">NOTES</span></span>

## <span data-ttu-id="c2e4d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2e4d-143">RELATED LINKS</span></span>

[<span data-ttu-id="c2e4d-144">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="c2e4d-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)

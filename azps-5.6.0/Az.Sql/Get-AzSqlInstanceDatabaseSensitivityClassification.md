---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 9a33504fb27d7c1cf623b03f6c4ea8fefb32c85f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914306"
---
# <span data-ttu-id="feb50-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="feb50-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="feb50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="feb50-102">SYNOPSIS</span></span>
<span data-ttu-id="feb50-103">在 Azure SQL 受管理的實例資料庫中，獲得資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="feb50-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="feb50-104">語法</span><span class="sxs-lookup"><span data-stu-id="feb50-104">SYNTAX</span></span>

### <span data-ttu-id="feb50-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="feb50-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb50-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb50-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb50-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb50-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb50-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb50-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb50-109">描述</span><span class="sxs-lookup"><span data-stu-id="feb50-109">DESCRIPTION</span></span>
<span data-ttu-id="feb50-110">Cmdlet Get-AzSqlInstanceDatabaseSensitivityClassification Azure SQL 受管理的實例資料庫中，會返回目前的資訊類型和欄的敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="feb50-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="feb50-111">例子</span><span class="sxs-lookup"><span data-stu-id="feb50-111">EXAMPLES</span></span>

### <span data-ttu-id="feb50-112">範例 1：取得 Azure SQL 受管理實例資料庫的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="feb50-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
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

### <span data-ttu-id="feb50-113">範例 2：取得 Azure SQL Managed Instance 資料庫的目前資訊類型和敏感度標籤與管道。</span><span class="sxs-lookup"><span data-stu-id="feb50-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
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

### <span data-ttu-id="feb50-114">範例 3：取得 Azure SQL 受管理實例資料庫特定資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="feb50-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
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

### <span data-ttu-id="feb50-115">範例 4：使用管道取得 Azure SQL 受管理實例資料庫特定資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="feb50-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
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

## <span data-ttu-id="feb50-116">參數</span><span class="sxs-lookup"><span data-stu-id="feb50-116">PARAMETERS</span></span>

### <span data-ttu-id="feb50-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="feb50-117">-AsJob</span></span>
<span data-ttu-id="feb50-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="feb50-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="feb50-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="feb50-119">-ColumnName</span></span>
<span data-ttu-id="feb50-120">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="feb50-120">Name of column.</span></span>

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

### <span data-ttu-id="feb50-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="feb50-121">-DatabaseName</span></span>
<span data-ttu-id="feb50-122">Azure SQL 受管理的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="feb50-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="feb50-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="feb50-123">-DatabaseObject</span></span>
<span data-ttu-id="feb50-124">Azure SQL 受管理的實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="feb50-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="feb50-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb50-125">-DefaultProfile</span></span>
<span data-ttu-id="feb50-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="feb50-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb50-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="feb50-127">-InstanceName</span></span>
<span data-ttu-id="feb50-128">Azure SQL 受管理的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="feb50-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="feb50-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb50-129">-ResourceGroupName</span></span>
<span data-ttu-id="feb50-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="feb50-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="feb50-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="feb50-131">-SchemaName</span></span>
<span data-ttu-id="feb50-132">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="feb50-132">Name of schema.</span></span>

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

### <span data-ttu-id="feb50-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="feb50-133">-TableName</span></span>
<span data-ttu-id="feb50-134">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="feb50-134">Name of table.</span></span>

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

### <span data-ttu-id="feb50-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb50-135">CommonParameters</span></span>
<span data-ttu-id="feb50-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="feb50-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb50-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="feb50-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb50-138">輸入</span><span class="sxs-lookup"><span data-stu-id="feb50-138">INPUTS</span></span>

### <span data-ttu-id="feb50-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="feb50-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="feb50-140">輸出</span><span class="sxs-lookup"><span data-stu-id="feb50-140">OUTPUTS</span></span>

### <span data-ttu-id="feb50-141">Microsoft.Azure.Commands.sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="feb50-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="feb50-142">筆記</span><span class="sxs-lookup"><span data-stu-id="feb50-142">NOTES</span></span>

## <span data-ttu-id="feb50-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="feb50-143">RELATED LINKS</span></span>

[<span data-ttu-id="feb50-144">深入瞭解 Azure SQL Database 資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="feb50-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: f8a31171309a9c869d29078ff09ce8903288e8bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792393"
---
# Set-AzSqlDatabaseAuditing

## 摘要
**重要：此 Cmdlet 已棄用，請將它取代為 [AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) 。**

變更 Azure SQL 資料庫的審核設定。

## 句法

### DefaultParameterSet (預設) 
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### StorageAccountSubscriptionIdSet
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EventHubSet
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LogAnalyticsSet
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BlobStorageByParentResourceSet
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### StorageAccountSubscriptionIdByParentResourceSet
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### EventHubByParentResourceSet
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LogAnalyticsByParentResourceSet
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**AzSqlDatabaseAuditing** Cmdlet 會變更 Azure SQL 資料庫的審核設定。
若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。
審計記錄目的地是透過指定下列其中一個切換參數來決定： BlobStorage、LogAnalytics 或 EventHub (如果沒有指定，則預設值為 BlobStorage) 。
使用 *State* 參數來啟用/停用原則。
當審核記錄目的地為 blob 儲存時，請指定 *StorageAccountName* 參數，以判斷審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。 您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。
如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了資料庫識別碼之外，它還會傳回描述目前審核設定的物件。
資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。

## 示例

### 範例1：啟用 Azure SQL 資料庫的 blob 儲存審核原則
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### 範例2：停用 Azure SQL 資料庫的 blob 儲存審核原則
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### 範例3：使用不同訂閱的儲存空間帳戶來啟用 Azure SQL 資料庫的 blob 儲存審核原則
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### 範例4：使用 T-sql 謂詞啟用高級篩選的 Azure SQL 資料庫的 blob 儲存審核原則
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### 範例5：從 Azure SQL 資料庫的 blob 儲存審核原則中移除 [高級篩選] 設定
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### 範例6：啟用 Azure SQL 資料庫的事件中心審核原則
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### 範例7：停用 Azure SQL 資料庫的事件中心審核原則
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### 範例8：啟用 Azure SQL 資料庫的 log analytics 審核原則
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### 範例9：停用 Azure SQL 資料庫的 log analytics 審核原則
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### 範例10：透過管線停用 Azure SQL 資料庫的 log analytics 審核原則
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## 參數

### -AsJob
在背景中執行 Cmdlet

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

### -AuditAction
一組審核動作。  
支援的審核動作包括：  
SELECT  
時更新  
插  
DELETE  
抓住  
接收  
參照定義要審核之動作的一般形式為： [[物件] 的 [動作] 依據 [主體] 請注意，上述格式中的 [物件] 可以參照表格、視圖或儲存程式，或整個資料庫或架構等物件。 在後一個情況下，系統會分別使用表單資料庫：： [dbname] 和架構：： [schemaname]。
例如：  
依公開選取 dbo. myTable  
選取 [在資料庫：：由公用 myDatabase]  
選取 [在架構：：由公用 mySchema]  
如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditActionGroup
建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：  
  
"BATCH_COMPLETED_GROUP"，  
"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，  
"FAILED_DATABASE_AUTHENTICATION_GROUP"  
上述組合也是預設設定的集合。 這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。
如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BlobStorage
指定審核記錄目的地為 blob 儲存空間

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
SQL 資料庫名稱。

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -EventHub
指定審核記錄目的地為事件中樞

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventHubAuthorizationRuleResourceId
事件中心授權規則的資源識別碼

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventHubName
事件中心的名稱。 如果在提供 EventHubAuthorizationRuleResourceId 時沒有指定，則會選取預設事件中樞。

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
要管理其審核原則的資料庫物件。

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogAnalytics
指定審核記錄目的地為 log analytics

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
指定是否要在 Cmdlet 執行結束時輸出審核原則

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

### -PredicateExpression
T-sql 謂語 (WHERE 子句) 用來篩選審核記錄。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
審計記錄的保留天數。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
SQL server 名稱。

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
原則的狀態。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
儲存空間帳戶的名稱。

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountSubscriptionId
儲存空間帳戶訂閱識別碼

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKeyType
指定要使用的儲存空間便捷鍵。

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceResourceId
您想要傳送審核記錄的 Log analytics 工作區) 的 [工作區識別碼] (資源識別碼。 範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

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

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### AzureSqlDatabaseModel （.Sql）的。

### AuditActionGroups [] （.Sql） .Sql。

### System.object []

### SwitchParameter 的系統管理功能

### Guid.empty

### 系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]

## 輸出

### DatabaseBlobAuditingSettingsModel （.Sql） .Sql。

## 筆記

## 相關連結

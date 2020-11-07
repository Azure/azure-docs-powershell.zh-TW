---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 0a9122f4869c1d1d68fe5fc0fcdc5f4151b47e66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792602"
---
# <span data-ttu-id="c8111-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c8111-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="c8111-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8111-102">SYNOPSIS</span></span>
<span data-ttu-id="c8111-103">變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="c8111-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="c8111-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8111-104">SYNTAX</span></span>

### <span data-ttu-id="c8111-105">DatabaseParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8111-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8111-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8111-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8111-107">說明</span><span class="sxs-lookup"><span data-stu-id="c8111-107">DESCRIPTION</span></span>
<span data-ttu-id="c8111-108">**AzSqlDatabaseAudit** Cmdlet 會變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="c8111-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="c8111-109">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="c8111-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c8111-110">當 blob 儲存為審核記錄的目的地時，請指定 *StorageAccountResourceId* 參數來判斷審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c8111-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="c8111-111">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="c8111-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="c8111-112">示例</span><span class="sxs-lookup"><span data-stu-id="c8111-112">EXAMPLES</span></span>

### <span data-ttu-id="c8111-113">範例1：啟用 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="c8111-114">範例2：停用 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="c8111-115">範例3.1：使用 T-sql 謂語，透過高級篩選啟用 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="c8111-116">範例3.2：從 Azure SQL 資料庫的審核原則中移除 [高級篩選] 設定</span><span class="sxs-lookup"><span data-stu-id="c8111-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="c8111-117">範例4：啟用 Azure SQL 資料庫的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-117">Example 4: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="c8111-118">範例5：停用 Azure SQL 資料庫的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-118">Example 5: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="c8111-119">範例6：啟用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-119">Example 6: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="c8111-120">範例7：停用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-120">Example 7: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="c8111-121">範例8：透過管線停用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="c8111-122">範例9：停用將 Azure SQL 資料庫的審核記錄傳送到 blob 儲存空間，並允許將其傳送至記錄分析。</span><span class="sxs-lookup"><span data-stu-id="c8111-122">Example 9: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="c8111-123">範例10：啟用將 Azure SQL 資料庫的審核記錄傳送到 blob 儲存體、事件中樞和記錄分析。</span><span class="sxs-lookup"><span data-stu-id="c8111-123">Example 10: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="c8111-124">參數</span><span class="sxs-lookup"><span data-stu-id="c8111-124">PARAMETERS</span></span>

### <span data-ttu-id="c8111-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="c8111-125">-AuditAction</span></span>
<span data-ttu-id="c8111-126">一組審核動作。</span><span class="sxs-lookup"><span data-stu-id="c8111-126">The set of audit actions.</span></span>  
<span data-ttu-id="c8111-127">支援的審核動作包括：</span><span class="sxs-lookup"><span data-stu-id="c8111-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="c8111-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="c8111-128">SELECT</span></span>  
<span data-ttu-id="c8111-129">時更新</span><span class="sxs-lookup"><span data-stu-id="c8111-129">UPDATE</span></span>  
<span data-ttu-id="c8111-130">插</span><span class="sxs-lookup"><span data-stu-id="c8111-130">INSERT</span></span>  
<span data-ttu-id="c8111-131">DELETE</span><span class="sxs-lookup"><span data-stu-id="c8111-131">DELETE</span></span>  
<span data-ttu-id="c8111-132">抓住</span><span class="sxs-lookup"><span data-stu-id="c8111-132">EXECUTE</span></span>  
<span data-ttu-id="c8111-133">接收</span><span class="sxs-lookup"><span data-stu-id="c8111-133">RECEIVE</span></span>  
<span data-ttu-id="c8111-134">提到</span><span class="sxs-lookup"><span data-stu-id="c8111-134">REFERENCES</span></span>  
<span data-ttu-id="c8111-135">定義要審核之動作的一般形式是： [[物件] 上的 [動作]，[主體] 請注意，上述格式中的 [物件] 可以參照表格、視圖或儲存程式，或整個資料庫或架構等物件。</span><span class="sxs-lookup"><span data-stu-id="c8111-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="c8111-136">在後一個情況下，系統會分別使用表單資料庫：： [dbname] 和架構：： [schemaname]。</span><span class="sxs-lookup"><span data-stu-id="c8111-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="c8111-137">例如：</span><span class="sxs-lookup"><span data-stu-id="c8111-137">For example:</span></span>  
<span data-ttu-id="c8111-138">依公開選取 dbo. myTable</span><span class="sxs-lookup"><span data-stu-id="c8111-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="c8111-139">選取 [在資料庫：：由公用 myDatabase]</span><span class="sxs-lookup"><span data-stu-id="c8111-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="c8111-140">選取 [在架構：：由公用 mySchema]</span><span class="sxs-lookup"><span data-stu-id="c8111-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="c8111-141">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。</span><span class="sxs-lookup"><span data-stu-id="c8111-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="c8111-142">-AuditActionGroup</span></span>
<span data-ttu-id="c8111-143">建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="c8111-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="c8111-144">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="c8111-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="c8111-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="c8111-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="c8111-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="c8111-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="c8111-147">上述組合也是預設設定的集合。</span><span class="sxs-lookup"><span data-stu-id="c8111-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="c8111-148">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="c8111-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="c8111-149">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="c8111-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="c8111-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="c8111-151">指出 [blob 儲存空間] 是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="c8111-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8111-152">-DatabaseName</span></span>
<span data-ttu-id="c8111-153">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c8111-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c8111-154">-DatabaseObject</span></span>
<span data-ttu-id="c8111-155">要管理其審核原則的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="c8111-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="c8111-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8111-156">-DefaultProfile</span></span>
<span data-ttu-id="c8111-157">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8111-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8111-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="c8111-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="c8111-159">事件中心授權規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c8111-159">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="c8111-160">-EventHubName</span></span>
<span data-ttu-id="c8111-161">事件中心的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8111-161">The name of the event hub.</span></span> <span data-ttu-id="c8111-162">如果在提供 EventHubAuthorizationRuleResourceId 時沒有指定，則會選取預設事件中樞。</span><span class="sxs-lookup"><span data-stu-id="c8111-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="c8111-163">-EventHubTargetState</span></span>
<span data-ttu-id="c8111-164">指出事件中樞是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="c8111-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="c8111-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="c8111-166">指出記錄分析是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="c8111-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8111-167">-PassThru</span></span>
<span data-ttu-id="c8111-168">指定是否要在 Cmdlet 執行結束時輸出審核原則</span><span class="sxs-lookup"><span data-stu-id="c8111-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="c8111-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="c8111-169">-PredicateExpression</span></span>
<span data-ttu-id="c8111-170">T-sql 謂語 (WHERE 子句) 用來篩選審核記錄。</span><span class="sxs-lookup"><span data-stu-id="c8111-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8111-171">-ResourceGroupName</span></span>
<span data-ttu-id="c8111-172">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8111-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c8111-173">-RetentionInDays</span></span>
<span data-ttu-id="c8111-174">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="c8111-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8111-175">-ServerName</span></span>
<span data-ttu-id="c8111-176">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c8111-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c8111-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="c8111-178">儲存空間帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c8111-178">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="c8111-179">-StorageKeyType</span></span>
<span data-ttu-id="c8111-180">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c8111-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="c8111-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="c8111-182">您想要傳送審核記錄的 Log analytics 工作區) 的 [工作區識別碼] (資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8111-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="c8111-183">範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="c8111-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8111-184">-確認</span><span class="sxs-lookup"><span data-stu-id="c8111-184">-Confirm</span></span>
<span data-ttu-id="c8111-185">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8111-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8111-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8111-186">-WhatIf</span></span>
<span data-ttu-id="c8111-187">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8111-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8111-188">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8111-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8111-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8111-189">CommonParameters</span></span>
<span data-ttu-id="c8111-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8111-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8111-191">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c8111-191">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8111-192">輸入</span><span class="sxs-lookup"><span data-stu-id="c8111-192">INPUTS</span></span>

### <span data-ttu-id="c8111-193">System.object</span><span class="sxs-lookup"><span data-stu-id="c8111-193">System.String</span></span>

### <span data-ttu-id="c8111-194">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="c8111-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="c8111-195">AuditActionGroups [] （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="c8111-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="c8111-196">System.object []</span><span class="sxs-lookup"><span data-stu-id="c8111-196">System.String[]</span></span>

### <span data-ttu-id="c8111-197">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="c8111-197">System.Guid</span></span>

### <span data-ttu-id="c8111-198">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8111-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c8111-199">DatabaseAuditModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="c8111-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="c8111-200">輸出</span><span class="sxs-lookup"><span data-stu-id="c8111-200">OUTPUTS</span></span>

### <span data-ttu-id="c8111-201">System.object</span><span class="sxs-lookup"><span data-stu-id="c8111-201">System.Boolean</span></span>

## <span data-ttu-id="c8111-202">筆記</span><span class="sxs-lookup"><span data-stu-id="c8111-202">NOTES</span></span>

## <span data-ttu-id="c8111-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8111-203">RELATED LINKS</span></span>

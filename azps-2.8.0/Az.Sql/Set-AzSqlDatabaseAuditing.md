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
# <span data-ttu-id="d3e8e-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d3e8e-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="d3e8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e8e-103">**重要：此 Cmdlet 已棄用，請將它取代為 [AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) 。**</span><span class="sxs-lookup"><span data-stu-id="d3e8e-103">**Important: This cmdlet is deprecated, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="d3e8e-104">變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-104">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="d3e8e-105">句法</span><span class="sxs-lookup"><span data-stu-id="d3e8e-105">SYNTAX</span></span>

### <span data-ttu-id="d3e8e-106">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d3e8e-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e8e-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="d3e8e-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e8e-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="d3e8e-108">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e8e-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="d3e8e-109">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e8e-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="d3e8e-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e8e-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="d3e8e-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3e8e-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="d3e8e-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e8e-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="d3e8e-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e8e-114">說明</span><span class="sxs-lookup"><span data-stu-id="d3e8e-114">DESCRIPTION</span></span>
<span data-ttu-id="d3e8e-115">**AzSqlDatabaseAuditing** Cmdlet 會變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-115">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="d3e8e-116">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-116">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d3e8e-117">審計記錄目的地是透過指定下列其中一個切換參數來決定： BlobStorage、LogAnalytics 或 EventHub (如果沒有指定，則預設值為 BlobStorage) 。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="d3e8e-118">使用 *State* 參數來啟用/停用原則。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="d3e8e-119">當審核記錄目的地為 blob 儲存時，請指定 *StorageAccountName* 參數，以判斷審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="d3e8e-120">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="d3e8e-121">如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了資料庫識別碼之外，它還會傳回描述目前審核設定的物件。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="d3e8e-122">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-122">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="d3e8e-123">示例</span><span class="sxs-lookup"><span data-stu-id="d3e8e-123">EXAMPLES</span></span>

### <span data-ttu-id="d3e8e-124">範例1：啟用 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-124">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="d3e8e-125">範例2：停用 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-125">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="d3e8e-126">範例3：使用不同訂閱的儲存空間帳戶來啟用 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-126">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="d3e8e-127">範例4：使用 T-sql 謂詞啟用高級篩選的 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-127">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="d3e8e-128">範例5：從 Azure SQL 資料庫的 blob 儲存審核原則中移除 [高級篩選] 設定</span><span class="sxs-lookup"><span data-stu-id="d3e8e-128">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="d3e8e-129">範例6：啟用 Azure SQL 資料庫的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-129">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="d3e8e-130">範例7：停用 Azure SQL 資料庫的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-130">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="d3e8e-131">範例8：啟用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-131">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="d3e8e-132">範例9：停用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-132">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="d3e8e-133">範例10：透過管線停用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="d3e8e-134">參數</span><span class="sxs-lookup"><span data-stu-id="d3e8e-134">PARAMETERS</span></span>

### <span data-ttu-id="d3e8e-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3e8e-135">-AsJob</span></span>
<span data-ttu-id="d3e8e-136">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d3e8e-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3e8e-137">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="d3e8e-137">-AuditAction</span></span>
<span data-ttu-id="d3e8e-138">一組審核動作。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-138">The set of audit actions.</span></span>  
<span data-ttu-id="d3e8e-139">支援的審核動作包括：</span><span class="sxs-lookup"><span data-stu-id="d3e8e-139">The supported actions to audit are:</span></span>  
<span data-ttu-id="d3e8e-140">SELECT</span><span class="sxs-lookup"><span data-stu-id="d3e8e-140">SELECT</span></span>  
<span data-ttu-id="d3e8e-141">時更新</span><span class="sxs-lookup"><span data-stu-id="d3e8e-141">UPDATE</span></span>  
<span data-ttu-id="d3e8e-142">插</span><span class="sxs-lookup"><span data-stu-id="d3e8e-142">INSERT</span></span>  
<span data-ttu-id="d3e8e-143">DELETE</span><span class="sxs-lookup"><span data-stu-id="d3e8e-143">DELETE</span></span>  
<span data-ttu-id="d3e8e-144">抓住</span><span class="sxs-lookup"><span data-stu-id="d3e8e-144">EXECUTE</span></span>  
<span data-ttu-id="d3e8e-145">接收</span><span class="sxs-lookup"><span data-stu-id="d3e8e-145">RECEIVE</span></span>  
<span data-ttu-id="d3e8e-146">參照定義要審核之動作的一般形式為： [[物件] 的 [動作] 依據 [主體] 請注意，上述格式中的 [物件] 可以參照表格、視圖或儲存程式，或整個資料庫或架構等物件。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-146">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="d3e8e-147">在後一個情況下，系統會分別使用表單資料庫：： [dbname] 和架構：： [schemaname]。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-147">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="d3e8e-148">例如：</span><span class="sxs-lookup"><span data-stu-id="d3e8e-148">For example:</span></span>  
<span data-ttu-id="d3e8e-149">依公開選取 dbo. myTable</span><span class="sxs-lookup"><span data-stu-id="d3e8e-149">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="d3e8e-150">選取 [在資料庫：：由公用 myDatabase]</span><span class="sxs-lookup"><span data-stu-id="d3e8e-150">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="d3e8e-151">選取 [在架構：：由公用 mySchema]</span><span class="sxs-lookup"><span data-stu-id="d3e8e-151">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="d3e8e-152">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-152">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="d3e8e-153">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d3e8e-153">-AuditActionGroup</span></span>
<span data-ttu-id="d3e8e-154">建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="d3e8e-154">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="d3e8e-155">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="d3e8e-155">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="d3e8e-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="d3e8e-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="d3e8e-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="d3e8e-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="d3e8e-158">上述組合也是預設設定的集合。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-158">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="d3e8e-159">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-159">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="d3e8e-160">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-160">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="d3e8e-161">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="d3e8e-161">-BlobStorage</span></span>
<span data-ttu-id="d3e8e-162">指定審核記錄目的地為 blob 儲存空間</span><span class="sxs-lookup"><span data-stu-id="d3e8e-162">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="d3e8e-163">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3e8e-163">-DatabaseName</span></span>
<span data-ttu-id="d3e8e-164">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-164">SQL Database name.</span></span>

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

### <span data-ttu-id="d3e8e-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e8e-165">-DefaultProfile</span></span>
<span data-ttu-id="d3e8e-166">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-166">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e8e-167">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d3e8e-167">-EventHub</span></span>
<span data-ttu-id="d3e8e-168">指定審核記錄目的地為事件中樞</span><span class="sxs-lookup"><span data-stu-id="d3e8e-168">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="d3e8e-169">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e8e-169">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="d3e8e-170">事件中心授權規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d3e8e-170">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="d3e8e-171">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="d3e8e-171">-EventHubName</span></span>
<span data-ttu-id="d3e8e-172">事件中心的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-172">The name of the event hub.</span></span> <span data-ttu-id="d3e8e-173">如果在提供 EventHubAuthorizationRuleResourceId 時沒有指定，則會選取預設事件中樞。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-173">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="d3e8e-174">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3e8e-174">-InputObject</span></span>
<span data-ttu-id="d3e8e-175">要管理其審核原則的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-175">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="d3e8e-176">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="d3e8e-176">-LogAnalytics</span></span>
<span data-ttu-id="d3e8e-177">指定審核記錄目的地為 log analytics</span><span class="sxs-lookup"><span data-stu-id="d3e8e-177">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="d3e8e-178">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3e8e-178">-PassThru</span></span>
<span data-ttu-id="d3e8e-179">指定是否要在 Cmdlet 執行結束時輸出審核原則</span><span class="sxs-lookup"><span data-stu-id="d3e8e-179">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="d3e8e-180">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="d3e8e-180">-PredicateExpression</span></span>
<span data-ttu-id="d3e8e-181">T-sql 謂語 (WHERE 子句) 用來篩選審核記錄。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-181">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="d3e8e-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e8e-182">-ResourceGroupName</span></span>
<span data-ttu-id="d3e8e-183">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-183">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3e8e-184">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d3e8e-184">-RetentionInDays</span></span>
<span data-ttu-id="d3e8e-185">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-185">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="d3e8e-186">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3e8e-186">-ServerName</span></span>
<span data-ttu-id="d3e8e-187">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-187">SQL server name.</span></span>

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

### <span data-ttu-id="d3e8e-188">-State</span><span class="sxs-lookup"><span data-stu-id="d3e8e-188">-State</span></span>
<span data-ttu-id="d3e8e-189">原則的狀態。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-189">The state of the policy.</span></span>

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

### <span data-ttu-id="d3e8e-190">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d3e8e-190">-StorageAccountName</span></span>
<span data-ttu-id="d3e8e-191">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-191">The name of the storage account.</span></span>

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

### <span data-ttu-id="d3e8e-192">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3e8e-192">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="d3e8e-193">儲存空間帳戶訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="d3e8e-193">The storage account subscription id</span></span>

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

### <span data-ttu-id="d3e8e-194">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d3e8e-194">-StorageKeyType</span></span>
<span data-ttu-id="d3e8e-195">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-195">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="d3e8e-196">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e8e-196">-WorkspaceResourceId</span></span>
<span data-ttu-id="d3e8e-197">您想要傳送審核記錄的 Log analytics 工作區) 的 [工作區識別碼] (資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-197">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="d3e8e-198">範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="d3e8e-198">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="d3e8e-199">-確認</span><span class="sxs-lookup"><span data-stu-id="d3e8e-199">-Confirm</span></span>
<span data-ttu-id="d3e8e-200">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e8e-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e8e-201">-WhatIf</span></span>
<span data-ttu-id="d3e8e-202">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3e8e-203">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e8e-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e8e-204">CommonParameters</span></span>
<span data-ttu-id="d3e8e-205">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e8e-206">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e8e-207">輸入</span><span class="sxs-lookup"><span data-stu-id="d3e8e-207">INPUTS</span></span>

### <span data-ttu-id="d3e8e-208">System.object</span><span class="sxs-lookup"><span data-stu-id="d3e8e-208">System.String</span></span>

### <span data-ttu-id="d3e8e-209">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-209">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="d3e8e-210">AuditActionGroups [] （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-210">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="d3e8e-211">System.object []</span><span class="sxs-lookup"><span data-stu-id="d3e8e-211">System.String[]</span></span>

### <span data-ttu-id="d3e8e-212">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d3e8e-212">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d3e8e-213">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="d3e8e-213">System.Guid</span></span>

### <span data-ttu-id="d3e8e-214">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d3e8e-214">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d3e8e-215">輸出</span><span class="sxs-lookup"><span data-stu-id="d3e8e-215">OUTPUTS</span></span>

### <span data-ttu-id="d3e8e-216">DatabaseBlobAuditingSettingsModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="d3e8e-216">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="d3e8e-217">筆記</span><span class="sxs-lookup"><span data-stu-id="d3e8e-217">NOTES</span></span>

## <span data-ttu-id="d3e8e-218">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3e8e-218">RELATED LINKS</span></span>

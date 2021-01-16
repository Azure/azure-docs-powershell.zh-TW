---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: e13e97bd9f636de68344f83b600e440252431a22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276752"
---
# <span data-ttu-id="649eb-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="649eb-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="649eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="649eb-102">SYNOPSIS</span></span>
<span data-ttu-id="649eb-103">變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="649eb-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="649eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="649eb-104">SYNTAX</span></span>

### <span data-ttu-id="649eb-105">DatabaseParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="649eb-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="649eb-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="649eb-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="649eb-107">說明</span><span class="sxs-lookup"><span data-stu-id="649eb-107">DESCRIPTION</span></span>
<span data-ttu-id="649eb-108">**AzSqlDatabaseAudit** Cmdlet 會變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="649eb-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="649eb-109">若要使用 Cmdlet，請使用 [ *ResourceGroupName*]、[ *ServerName*] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="649eb-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="649eb-110">當 blob 儲存為審核記錄的目的地時，請指定 *StorageAccountResourceId* 參數來判斷審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="649eb-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="649eb-111">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="649eb-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="649eb-112">示例</span><span class="sxs-lookup"><span data-stu-id="649eb-112">EXAMPLES</span></span>

### <span data-ttu-id="649eb-113">範例1：啟用 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="649eb-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="649eb-114">範例2：停用 Azure SQL 資料庫的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="649eb-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="649eb-115">範例3：使用 T-sql 謂詞來啟用 Azure SQL 資料庫的 blob 儲存審核原則（含高級篩選）</span><span class="sxs-lookup"><span data-stu-id="649eb-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="649eb-116">範例4：從 Azure SQL 資料庫的審核原則中移除 [高級篩選] 設定</span><span class="sxs-lookup"><span data-stu-id="649eb-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="649eb-117">範例5：啟用 Azure SQL 資料庫的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="649eb-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="649eb-118">範例6：停用 Azure SQL 資料庫的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="649eb-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="649eb-119">範例7：啟用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="649eb-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="649eb-120">範例8：停用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="649eb-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="649eb-121">範例9：透過管線停用 Azure SQL 資料庫的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="649eb-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="649eb-122">範例10：停用將 Azure SQL 資料庫的審核記錄傳送到 blob 儲存空間，並允許將其傳送至記錄分析。</span><span class="sxs-lookup"><span data-stu-id="649eb-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="649eb-123">範例11：啟用將 Azure SQL 資料庫的審核記錄傳送到 blob 儲存體、事件中樞和記錄分析。</span><span class="sxs-lookup"><span data-stu-id="649eb-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="649eb-124">參數</span><span class="sxs-lookup"><span data-stu-id="649eb-124">PARAMETERS</span></span>

### <span data-ttu-id="649eb-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="649eb-125">-AuditAction</span></span>
<span data-ttu-id="649eb-126">一組審核動作。</span><span class="sxs-lookup"><span data-stu-id="649eb-126">The set of audit actions.</span></span>  
<span data-ttu-id="649eb-127">支援的審核動作包括：</span><span class="sxs-lookup"><span data-stu-id="649eb-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="649eb-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="649eb-128">SELECT</span></span>  
<span data-ttu-id="649eb-129">時更新</span><span class="sxs-lookup"><span data-stu-id="649eb-129">UPDATE</span></span>  
<span data-ttu-id="649eb-130">插</span><span class="sxs-lookup"><span data-stu-id="649eb-130">INSERT</span></span>  
<span data-ttu-id="649eb-131">DELETE</span><span class="sxs-lookup"><span data-stu-id="649eb-131">DELETE</span></span>  
<span data-ttu-id="649eb-132">抓住</span><span class="sxs-lookup"><span data-stu-id="649eb-132">EXECUTE</span></span>  
<span data-ttu-id="649eb-133">接收</span><span class="sxs-lookup"><span data-stu-id="649eb-133">RECEIVE</span></span>  
<span data-ttu-id="649eb-134">提到</span><span class="sxs-lookup"><span data-stu-id="649eb-134">REFERENCES</span></span>  
<span data-ttu-id="649eb-135">定義要審核之動作的一般形式是： [[物件] 上的 [動作]，[主體] 請注意，上述格式中的 [物件] 可以參照表格、視圖或儲存程式，或整個資料庫或架構等物件。</span><span class="sxs-lookup"><span data-stu-id="649eb-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="649eb-136">在後一個情況下，系統會分別使用表單資料庫：： [dbname] 和架構：： [schemaname]。</span><span class="sxs-lookup"><span data-stu-id="649eb-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="649eb-137">例如：</span><span class="sxs-lookup"><span data-stu-id="649eb-137">For example:</span></span>  
<span data-ttu-id="649eb-138">依公開選取 dbo. myTable</span><span class="sxs-lookup"><span data-stu-id="649eb-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="649eb-139">選取 [在資料庫：：由公用 myDatabase]</span><span class="sxs-lookup"><span data-stu-id="649eb-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="649eb-140">選取 [在架構：：由公用 mySchema]</span><span class="sxs-lookup"><span data-stu-id="649eb-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="649eb-141">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。</span><span class="sxs-lookup"><span data-stu-id="649eb-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="649eb-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="649eb-142">-AuditActionGroup</span></span>
<span data-ttu-id="649eb-143">建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="649eb-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="649eb-144">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="649eb-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="649eb-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="649eb-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="649eb-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="649eb-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="649eb-147">上述組合也是預設設定的集合。</span><span class="sxs-lookup"><span data-stu-id="649eb-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="649eb-148">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="649eb-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="649eb-149">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="649eb-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="649eb-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="649eb-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="649eb-151">指出 [blob 儲存空間] 是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="649eb-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="649eb-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="649eb-152">-DatabaseName</span></span>
<span data-ttu-id="649eb-153">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="649eb-153">SQL Database name.</span></span>

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

### <span data-ttu-id="649eb-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="649eb-154">-DatabaseObject</span></span>
<span data-ttu-id="649eb-155">要管理其審核原則的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="649eb-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="649eb-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="649eb-156">-DefaultProfile</span></span>
<span data-ttu-id="649eb-157">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="649eb-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="649eb-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="649eb-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="649eb-159">事件中心授權規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="649eb-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="649eb-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="649eb-160">-EventHubName</span></span>
<span data-ttu-id="649eb-161">事件中心的名稱。</span><span class="sxs-lookup"><span data-stu-id="649eb-161">The name of the event hub.</span></span> <span data-ttu-id="649eb-162">如果在提供 EventHubAuthorizationRuleResourceId 時沒有指定，則會選取預設事件中樞。</span><span class="sxs-lookup"><span data-stu-id="649eb-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="649eb-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="649eb-163">-EventHubTargetState</span></span>
<span data-ttu-id="649eb-164">指出事件中樞是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="649eb-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="649eb-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="649eb-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="649eb-166">指出記錄分析是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="649eb-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="649eb-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="649eb-167">-PassThru</span></span>
<span data-ttu-id="649eb-168">指定是否要在 Cmdlet 執行結束時輸出審核原則</span><span class="sxs-lookup"><span data-stu-id="649eb-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="649eb-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="649eb-169">-PredicateExpression</span></span>
<span data-ttu-id="649eb-170">T-sql 謂語 (WHERE 子句) 用來篩選審核記錄。</span><span class="sxs-lookup"><span data-stu-id="649eb-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="649eb-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="649eb-171">-ResourceGroupName</span></span>
<span data-ttu-id="649eb-172">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="649eb-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="649eb-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="649eb-173">-RetentionInDays</span></span>
<span data-ttu-id="649eb-174">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="649eb-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="649eb-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="649eb-175">-ServerName</span></span>
<span data-ttu-id="649eb-176">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="649eb-176">SQL server name.</span></span>

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

### <span data-ttu-id="649eb-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="649eb-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="649eb-178">儲存空間帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="649eb-178">The storage account resource id</span></span>

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

### <span data-ttu-id="649eb-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="649eb-179">-StorageKeyType</span></span>
<span data-ttu-id="649eb-180">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="649eb-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="649eb-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="649eb-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="649eb-182">您想要傳送審核記錄的 Log analytics 工作區) 的 [工作區識別碼] (資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="649eb-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="649eb-183">範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="649eb-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="649eb-184">-確認</span><span class="sxs-lookup"><span data-stu-id="649eb-184">-Confirm</span></span>
<span data-ttu-id="649eb-185">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="649eb-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="649eb-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="649eb-186">-WhatIf</span></span>
<span data-ttu-id="649eb-187">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="649eb-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="649eb-188">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="649eb-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="649eb-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="649eb-189">CommonParameters</span></span>
<span data-ttu-id="649eb-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="649eb-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="649eb-191">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="649eb-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="649eb-192">輸入</span><span class="sxs-lookup"><span data-stu-id="649eb-192">INPUTS</span></span>

### <span data-ttu-id="649eb-193">System.object</span><span class="sxs-lookup"><span data-stu-id="649eb-193">System.String</span></span>

### <span data-ttu-id="649eb-194">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="649eb-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="649eb-195">AuditActionGroups [] （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="649eb-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="649eb-196">System.object []</span><span class="sxs-lookup"><span data-stu-id="649eb-196">System.String[]</span></span>

### <span data-ttu-id="649eb-197">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="649eb-197">System.Guid</span></span>

### <span data-ttu-id="649eb-198">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="649eb-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="649eb-199">DatabaseAuditModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="649eb-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="649eb-200">輸出</span><span class="sxs-lookup"><span data-stu-id="649eb-200">OUTPUTS</span></span>

### <span data-ttu-id="649eb-201">System.object</span><span class="sxs-lookup"><span data-stu-id="649eb-201">System.Boolean</span></span>

## <span data-ttu-id="649eb-202">筆記</span><span class="sxs-lookup"><span data-stu-id="649eb-202">NOTES</span></span>

## <span data-ttu-id="649eb-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="649eb-203">RELATED LINKS</span></span>

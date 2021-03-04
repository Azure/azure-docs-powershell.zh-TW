---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 6e3c5c935f6703f5c4f29b2a4ae793fc48e9b16f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913054"
---
# <span data-ttu-id="22729-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="22729-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="22729-102">簡介</span><span class="sxs-lookup"><span data-stu-id="22729-102">SYNOPSIS</span></span>
<span data-ttu-id="22729-103">變更 Azure SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="22729-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="22729-104">語法</span><span class="sxs-lookup"><span data-stu-id="22729-104">SYNTAX</span></span>

### <span data-ttu-id="22729-105">DatabaseParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="22729-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22729-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22729-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22729-107">描述</span><span class="sxs-lookup"><span data-stu-id="22729-107">DESCRIPTION</span></span>
<span data-ttu-id="22729-108">**Set-AzSqlDatabaseAudit** Cmdlet 會變更 Azure SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="22729-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="22729-109">若要使用 Cmdlet，請使用 *ResourceGroupName、ServerName* 和 *DatabaseName* 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="22729-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="22729-110">當 Blob 儲存體是稽核記錄的目標時，請指定 *StorageAccountResourceId* 參數，以決定稽核記錄中的儲存帳戶，以及 *StorageKeyType* 參數來定義儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="22729-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="22729-111">您也可以設定 *RetentionInDays* 參數的值來定義稽核記錄期間，以定義稽核記錄保留。</span><span class="sxs-lookup"><span data-stu-id="22729-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="22729-112">例子</span><span class="sxs-lookup"><span data-stu-id="22729-112">EXAMPLES</span></span>

### <span data-ttu-id="22729-113">範例 1：啟用 Azure SQL 資料庫的 Blob 儲存稽核策略</span><span class="sxs-lookup"><span data-stu-id="22729-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="22729-114">範例 2：停用 Azure SQL 資料庫的 Blob 儲存稽核策略</span><span class="sxs-lookup"><span data-stu-id="22729-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="22729-115">範例 3：使用 T-SQL 詞詞啟用 Azure SQL 資料庫的 Blob 儲存稽核策略與篩選</span><span class="sxs-lookup"><span data-stu-id="22729-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "schema_name <> 'sys''" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="22729-116">範例 4：從 Azure SQL 資料庫的稽核策略移除篩選</span><span class="sxs-lookup"><span data-stu-id="22729-116">Example 4: Remove the filtering from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="22729-117">範例 5：啟用 Azure SQL 資料庫的事件中樞稽核策略</span><span class="sxs-lookup"><span data-stu-id="22729-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="22729-118">範例 6：停用 Azure SQL 資料庫的事件中樞稽核策略</span><span class="sxs-lookup"><span data-stu-id="22729-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="22729-119">範例 7：啟用 Azure SQL 資料庫的記錄分析稽核策略</span><span class="sxs-lookup"><span data-stu-id="22729-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="22729-120">範例 8：停用 Azure SQL 資料庫的記錄分析稽核策略</span><span class="sxs-lookup"><span data-stu-id="22729-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="22729-121">範例 9：透過管線停用 Azure SQL 資料庫的記錄分析稽核策略</span><span class="sxs-lookup"><span data-stu-id="22729-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="22729-122">範例 10：停用將 Azure SQL 資料庫的稽核記錄傳送至 Blob 儲存空間，並啟用傳送記錄分析。</span><span class="sxs-lookup"><span data-stu-id="22729-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="22729-123">範例 11：啟用將 Azure SQL 資料庫的稽核記錄傳送至 Blob 儲存體、事件中樞和記錄分析。</span><span class="sxs-lookup"><span data-stu-id="22729-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="22729-124">參數</span><span class="sxs-lookup"><span data-stu-id="22729-124">PARAMETERS</span></span>

### <span data-ttu-id="22729-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="22729-125">-AuditAction</span></span>
<span data-ttu-id="22729-126">稽核動作集。</span><span class="sxs-lookup"><span data-stu-id="22729-126">The set of audit actions.</span></span>  
<span data-ttu-id="22729-127">支援的稽核動作為：</span><span class="sxs-lookup"><span data-stu-id="22729-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="22729-128">選擇</span><span class="sxs-lookup"><span data-stu-id="22729-128">SELECT</span></span>  
<span data-ttu-id="22729-129">更新</span><span class="sxs-lookup"><span data-stu-id="22729-129">UPDATE</span></span>  
<span data-ttu-id="22729-130">插入</span><span class="sxs-lookup"><span data-stu-id="22729-130">INSERT</span></span>  
<span data-ttu-id="22729-131">刪除</span><span class="sxs-lookup"><span data-stu-id="22729-131">DELETE</span></span>  
<span data-ttu-id="22729-132">執行</span><span class="sxs-lookup"><span data-stu-id="22729-132">EXECUTE</span></span>  
<span data-ttu-id="22729-133">收到</span><span class="sxs-lookup"><span data-stu-id="22729-133">RECEIVE</span></span>  
<span data-ttu-id="22729-134">引用</span><span class="sxs-lookup"><span data-stu-id="22729-134">REFERENCES</span></span>  
<span data-ttu-id="22729-135">定義要稽核之動作的一般形式為：[action] ON [object] BY [principal] 請注意，上述格式的 [物件] 可參照資料表、視圖或儲存程式等物件，或是整個資料庫或架構。</span><span class="sxs-lookup"><span data-stu-id="22729-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="22729-136">在後一種情況下，會分別使用表單 DATABASE：：[dbname] 和 SCHEMA：：[schemaname]。</span><span class="sxs-lookup"><span data-stu-id="22729-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="22729-137">例如：</span><span class="sxs-lookup"><span data-stu-id="22729-137">For example:</span></span>  
<span data-ttu-id="22729-138">在 dbo.myTable 上按公用 SELECT</span><span class="sxs-lookup"><span data-stu-id="22729-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="22729-139">DATABASE 上的 SELECT：myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="22729-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="22729-140">SCHEMA 上的 SELECT：mySchema by public</span><span class="sxs-lookup"><span data-stu-id="22729-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="22729-141">詳細資訊請參閱 https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。</span><span class="sxs-lookup"><span data-stu-id="22729-141">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="22729-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="22729-142">-AuditActionGroup</span></span>
<span data-ttu-id="22729-143">建議使用的動作群組組合為下列組合：這會稽核對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="22729-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="22729-144">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="22729-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="22729-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="22729-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="22729-146">「FAILED_DATABASE_AUTHENTICATION_GROUP」</span><span class="sxs-lookup"><span data-stu-id="22729-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="22729-147">上述組合也是預設設定的組合。</span><span class="sxs-lookup"><span data-stu-id="22729-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="22729-148">這些群組涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，而且不應與其他群組搭配使用，因為這樣會導致重複的稽核記錄。</span><span class="sxs-lookup"><span data-stu-id="22729-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="22729-149">詳細資訊請參閱 https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="22729-149">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="22729-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="22729-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="22729-151">指出 Blob 儲存空間是否是稽核記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="22729-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="22729-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22729-152">-DatabaseName</span></span>
<span data-ttu-id="22729-153">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="22729-153">SQL Database name.</span></span>

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

### <span data-ttu-id="22729-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="22729-154">-DatabaseObject</span></span>
<span data-ttu-id="22729-155">要管理其稽核策略的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="22729-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="22729-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22729-156">-DefaultProfile</span></span>
<span data-ttu-id="22729-157">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="22729-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22729-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="22729-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="22729-159">事件中樞授權規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="22729-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="22729-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="22729-160">-EventHubName</span></span>
<span data-ttu-id="22729-161">事件中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="22729-161">The name of the event hub.</span></span> <span data-ttu-id="22729-162">如果在提供 EventHubAuthorizationRuleResourceId 時未指定任何專案，將會選取預設的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="22729-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="22729-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="22729-163">-EventHubTargetState</span></span>
<span data-ttu-id="22729-164">指出事件中樞是否是稽核記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="22729-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="22729-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="22729-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="22729-166">指出記錄分析是否是稽核記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="22729-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="22729-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22729-167">-PassThru</span></span>
<span data-ttu-id="22729-168">指定是否要在 Cmdlet 執行結束時輸出稽核政策</span><span class="sxs-lookup"><span data-stu-id="22729-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="22729-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="22729-169">-PredicateExpression</span></span>
<span data-ttu-id="22729-170">T-SQL 謂詞 (WHERE 子句) 用來篩選稽核記錄。</span><span class="sxs-lookup"><span data-stu-id="22729-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="22729-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22729-171">-ResourceGroupName</span></span>
<span data-ttu-id="22729-172">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22729-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="22729-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="22729-173">-RetentionInDays</span></span>
<span data-ttu-id="22729-174">稽核記錄保留天數。</span><span class="sxs-lookup"><span data-stu-id="22729-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="22729-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="22729-175">-ServerName</span></span>
<span data-ttu-id="22729-176">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="22729-176">SQL server name.</span></span>

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

### <span data-ttu-id="22729-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="22729-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="22729-178">儲存帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="22729-178">The storage account resource id</span></span>

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

### <span data-ttu-id="22729-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="22729-179">-StorageKeyType</span></span>
<span data-ttu-id="22729-180">指定要使用哪些儲存存取鍵。</span><span class="sxs-lookup"><span data-stu-id="22729-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="22729-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="22729-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="22729-182">工作區識別碼 (Log Analytics 工作區的資源識別碼) Log Analytics 工作區的資源識別碼，以傳送稽核記錄。</span><span class="sxs-lookup"><span data-stu-id="22729-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="22729-183">範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="22729-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="22729-184">-確認</span><span class="sxs-lookup"><span data-stu-id="22729-184">-Confirm</span></span>
<span data-ttu-id="22729-185">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="22729-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22729-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22729-186">-WhatIf</span></span>
<span data-ttu-id="22729-187">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22729-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22729-188">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22729-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22729-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22729-189">CommonParameters</span></span>
<span data-ttu-id="22729-190">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="22729-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22729-191">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22729-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22729-192">輸入</span><span class="sxs-lookup"><span data-stu-id="22729-192">INPUTS</span></span>

### <span data-ttu-id="22729-193">System.String</span><span class="sxs-lookup"><span data-stu-id="22729-193">System.String</span></span>

### <span data-ttu-id="22729-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="22729-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="22729-195">Microsoft.Azure.Commands.sql.Auditing.model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="22729-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="22729-196">System.String[]</span><span class="sxs-lookup"><span data-stu-id="22729-196">System.String[]</span></span>

### <span data-ttu-id="22729-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="22729-197">System.Guid</span></span>

### <span data-ttu-id="22729-198">System.Nullable'1[[System.UInt32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="22729-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="22729-199">Microsoft.Azure.Commands.sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="22729-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="22729-200">輸出</span><span class="sxs-lookup"><span data-stu-id="22729-200">OUTPUTS</span></span>

### <span data-ttu-id="22729-201">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22729-201">System.Boolean</span></span>

## <span data-ttu-id="22729-202">筆記</span><span class="sxs-lookup"><span data-stu-id="22729-202">NOTES</span></span>

## <span data-ttu-id="22729-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="22729-203">RELATED LINKS</span></span>

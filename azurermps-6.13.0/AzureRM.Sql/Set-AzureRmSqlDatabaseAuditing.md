---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446913"
---
# <span data-ttu-id="3167c-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="3167c-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="3167c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3167c-102">SYNOPSIS</span></span>
<span data-ttu-id="3167c-103">變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="3167c-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3167c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3167c-104">SYNTAX</span></span>

### <span data-ttu-id="3167c-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3167c-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3167c-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="3167c-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3167c-107">說明</span><span class="sxs-lookup"><span data-stu-id="3167c-107">DESCRIPTION</span></span>
<span data-ttu-id="3167c-108">**AzureRmSqlDatabaseAuditing** Cmdlet 會變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="3167c-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="3167c-109">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="3167c-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="3167c-110">指定 *StorageAccountName* 參數，以指定審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="3167c-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="3167c-111">使用 *State* 參數來啟用/停用原則。</span><span class="sxs-lookup"><span data-stu-id="3167c-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="3167c-112">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="3167c-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="3167c-113">成功執行 Cmdlet 之後，就會啟用資料庫審核。</span><span class="sxs-lookup"><span data-stu-id="3167c-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="3167c-114">如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了資料庫識別碼之外，它還會傳回描述目前 blob 審核原則的物件。</span><span class="sxs-lookup"><span data-stu-id="3167c-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="3167c-115">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="3167c-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="3167c-116">示例</span><span class="sxs-lookup"><span data-stu-id="3167c-116">EXAMPLES</span></span>

### <span data-ttu-id="3167c-117">範例1：啟用 Azure SQL 資料庫的審核原則</span><span class="sxs-lookup"><span data-stu-id="3167c-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="3167c-118">範例2：停用 Azure SQL 資料庫的 blob 審核原則</span><span class="sxs-lookup"><span data-stu-id="3167c-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="3167c-119">範例3：使用不同訂閱的儲存空間帳戶啟用 Azure SQL 資料庫的審核原則</span><span class="sxs-lookup"><span data-stu-id="3167c-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="3167c-120">範例4：啟用 Azure SQL 資料庫的延伸審核原則</span><span class="sxs-lookup"><span data-stu-id="3167c-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="3167c-121">範例5：移除 Azure SQL 資料庫的延伸審核原則，並設定審核原則（而非它）。</span><span class="sxs-lookup"><span data-stu-id="3167c-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="3167c-122">參數</span><span class="sxs-lookup"><span data-stu-id="3167c-122">PARAMETERS</span></span>

### <span data-ttu-id="3167c-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="3167c-123">-AuditAction</span></span>
<span data-ttu-id="3167c-124">一組審核動作。</span><span class="sxs-lookup"><span data-stu-id="3167c-124">The set of audit actions.</span></span>
<span data-ttu-id="3167c-125">受支援的審核動作為：選取 [更新插入] 執行接收參照 [一般] 表單來定義要審核的動作： [[物件] 的 [動作] 依據 [主體] 請注意，上述格式中的 [物件] 可以參照表格、視圖或儲存程式，或整個資料庫或架構等物件。</span><span class="sxs-lookup"><span data-stu-id="3167c-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="3167c-126">在後一個情況下，系統會分別使用表單資料庫：： [dbname] 和架構：： [schemaname]。</span><span class="sxs-lookup"><span data-stu-id="3167c-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="3167c-127">例如，在資料庫上選取 dbo. myTable （依公開金鑰選取）：： myDatabase 依據公用選取 [在架構：：由 public mySchema] 以取得詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。</span><span class="sxs-lookup"><span data-stu-id="3167c-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="3167c-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="3167c-128">-AuditActionGroup</span></span>
<span data-ttu-id="3167c-129">建議使用的一組動作群組是下列專案，這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：「BATCH_COMPLETED_GROUP」、「SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP」、「FAILED_DATABASE_AUTHENTICATION_GROUP」上述組合也是預設設定。</span><span class="sxs-lookup"><span data-stu-id="3167c-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="3167c-130">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="3167c-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="3167c-131">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="3167c-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3167c-132">-DatabaseName</span></span>
<span data-ttu-id="3167c-133">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3167c-133">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3167c-134">-DefaultProfile</span></span>
<span data-ttu-id="3167c-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3167c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3167c-136">-PassThru</span></span>
<span data-ttu-id="3167c-137">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="3167c-137">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-138">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="3167c-138">-PredicateExpression</span></span>
<span data-ttu-id="3167c-139">Where 子句中用來篩選審核記錄的語句。</span><span class="sxs-lookup"><span data-stu-id="3167c-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="3167c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3167c-140">-ResourceGroupName</span></span>
<span data-ttu-id="3167c-141">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3167c-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3167c-142">-RetentionInDays</span></span>
<span data-ttu-id="3167c-143">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="3167c-143">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3167c-144">-ServerName</span></span>
<span data-ttu-id="3167c-145">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3167c-145">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-146">-State</span><span class="sxs-lookup"><span data-stu-id="3167c-146">-State</span></span>
<span data-ttu-id="3167c-147">原則的狀態。</span><span class="sxs-lookup"><span data-stu-id="3167c-147">The state of the policy.</span></span>

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

### <span data-ttu-id="3167c-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3167c-148">-StorageAccountName</span></span>
<span data-ttu-id="3167c-149">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3167c-149">The name of the storage account.</span></span> <span data-ttu-id="3167c-150">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="3167c-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="3167c-151">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="3167c-151">This parameter is not required.</span></span>
<span data-ttu-id="3167c-152">如果您沒有指定此參數，則 Cmdlet 會使用先前在審核原則中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="3167c-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="3167c-153">如果這是已定義審核原則的第一次，且您不指定此參數，則 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="3167c-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3167c-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="3167c-155">指定儲存空間帳戶訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="3167c-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3167c-156">-StorageKeyType</span></span>
<span data-ttu-id="3167c-157">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3167c-157">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-158">-確認</span><span class="sxs-lookup"><span data-stu-id="3167c-158">-Confirm</span></span>
<span data-ttu-id="3167c-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3167c-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3167c-160">-WhatIf</span></span>
<span data-ttu-id="3167c-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3167c-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3167c-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3167c-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3167c-163">CommonParameters</span></span>
<span data-ttu-id="3167c-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3167c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3167c-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3167c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3167c-166">輸入</span><span class="sxs-lookup"><span data-stu-id="3167c-166">INPUTS</span></span>

## <span data-ttu-id="3167c-167">輸出</span><span class="sxs-lookup"><span data-stu-id="3167c-167">OUTPUTS</span></span>

## <span data-ttu-id="3167c-168">筆記</span><span class="sxs-lookup"><span data-stu-id="3167c-168">NOTES</span></span>

## <span data-ttu-id="3167c-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="3167c-169">RELATED LINKS</span></span>

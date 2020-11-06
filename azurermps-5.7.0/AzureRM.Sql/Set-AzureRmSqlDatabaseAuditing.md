---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447593"
---
# <span data-ttu-id="8dc58-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="8dc58-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="8dc58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8dc58-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc58-103">變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="8dc58-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dc58-104">句法</span><span class="sxs-lookup"><span data-stu-id="8dc58-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc58-105">說明</span><span class="sxs-lookup"><span data-stu-id="8dc58-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc58-106">**AzureRmSqlDatabaseAuditing** Cmdlet 會變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="8dc58-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="8dc58-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="8dc58-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="8dc58-108">指定 *StorageAccountName* 參數，以指定審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="8dc58-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="8dc58-109">使用 *State* 參數來啟用/停用原則。</span><span class="sxs-lookup"><span data-stu-id="8dc58-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="8dc58-110">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="8dc58-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="8dc58-111">成功執行 Cmdlet 之後，就會啟用資料庫審核。</span><span class="sxs-lookup"><span data-stu-id="8dc58-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="8dc58-112">如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了資料庫識別碼之外，它還會傳回描述目前 blob 審核原則的物件。</span><span class="sxs-lookup"><span data-stu-id="8dc58-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="8dc58-113">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="8dc58-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="8dc58-114">示例</span><span class="sxs-lookup"><span data-stu-id="8dc58-114">EXAMPLES</span></span>

### <span data-ttu-id="8dc58-115">範例1：啟用 Azure SQL 資料庫的審核原則</span><span class="sxs-lookup"><span data-stu-id="8dc58-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="8dc58-116">範例2：停用 Azure SQL 資料庫的 blob 審核原則</span><span class="sxs-lookup"><span data-stu-id="8dc58-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="8dc58-117">參數</span><span class="sxs-lookup"><span data-stu-id="8dc58-117">PARAMETERS</span></span>

### <span data-ttu-id="8dc58-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="8dc58-118">-AuditAction</span></span>
<span data-ttu-id="8dc58-119">一組審核動作。</span><span class="sxs-lookup"><span data-stu-id="8dc58-119">The set of audit actions.</span></span>  
<span data-ttu-id="8dc58-120">支援的審核動作包括：</span><span class="sxs-lookup"><span data-stu-id="8dc58-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="8dc58-121">SELECT</span><span class="sxs-lookup"><span data-stu-id="8dc58-121">SELECT</span></span>  
<span data-ttu-id="8dc58-122">時更新</span><span class="sxs-lookup"><span data-stu-id="8dc58-122">UPDATE</span></span>  
<span data-ttu-id="8dc58-123">插</span><span class="sxs-lookup"><span data-stu-id="8dc58-123">INSERT</span></span>  
<span data-ttu-id="8dc58-124">DELETE</span><span class="sxs-lookup"><span data-stu-id="8dc58-124">DELETE</span></span>  
<span data-ttu-id="8dc58-125">抓住</span><span class="sxs-lookup"><span data-stu-id="8dc58-125">EXECUTE</span></span>  
<span data-ttu-id="8dc58-126">接收</span><span class="sxs-lookup"><span data-stu-id="8dc58-126">RECEIVE</span></span>  
<span data-ttu-id="8dc58-127">提到</span><span class="sxs-lookup"><span data-stu-id="8dc58-127">REFERENCES</span></span>  

<span data-ttu-id="8dc58-128">定義要審核之動作的一般形式為：</span><span class="sxs-lookup"><span data-stu-id="8dc58-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="8dc58-129">執行[物件] 依據 [principal]</span><span class="sxs-lookup"><span data-stu-id="8dc58-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="8dc58-130">請注意，以上格式中的 [物件] 可以參照表格、視圖或儲存程式，或整個資料庫或架構等物件。</span><span class="sxs-lookup"><span data-stu-id="8dc58-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="8dc58-131">在後一個情況下，系統會分別使用表單資料庫：： [dbname] 和架構：： [schemaname]。</span><span class="sxs-lookup"><span data-stu-id="8dc58-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="8dc58-132">例如：</span><span class="sxs-lookup"><span data-stu-id="8dc58-132">For example:</span></span>  
<span data-ttu-id="8dc58-133">依公開選取 dbo. myTable</span><span class="sxs-lookup"><span data-stu-id="8dc58-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="8dc58-134">選取 [在資料庫：：由公用 myDatabase]</span><span class="sxs-lookup"><span data-stu-id="8dc58-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="8dc58-135">選取 [在架構：：由公用 mySchema]</span><span class="sxs-lookup"><span data-stu-id="8dc58-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="8dc58-136">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。</span><span class="sxs-lookup"><span data-stu-id="8dc58-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="8dc58-137">-AuditActionGroup</span></span>
<span data-ttu-id="8dc58-138">建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="8dc58-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="8dc58-139">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="8dc58-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="8dc58-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="8dc58-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="8dc58-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="8dc58-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="8dc58-142">上述組合也是預設設定的集合。</span><span class="sxs-lookup"><span data-stu-id="8dc58-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="8dc58-143">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="8dc58-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="8dc58-144">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="8dc58-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8dc58-145">-DatabaseName</span></span>
<span data-ttu-id="8dc58-146">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc58-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc58-147">-DefaultProfile</span></span>
<span data-ttu-id="8dc58-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8dc58-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dc58-149">-PassThru</span></span>
<span data-ttu-id="8dc58-150">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="8dc58-150">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc58-151">-ResourceGroupName</span></span>
<span data-ttu-id="8dc58-152">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc58-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8dc58-153">-RetentionInDays</span></span>
<span data-ttu-id="8dc58-154">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="8dc58-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-155">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8dc58-155">-ServerName</span></span>
<span data-ttu-id="8dc58-156">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc58-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-157">-State</span><span class="sxs-lookup"><span data-stu-id="8dc58-157">-State</span></span>
<span data-ttu-id="8dc58-158">原則的狀態。</span><span class="sxs-lookup"><span data-stu-id="8dc58-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8dc58-159">-StorageAccountName</span></span>
<span data-ttu-id="8dc58-160">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc58-160">The name of the storage account.</span></span> <span data-ttu-id="8dc58-161">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="8dc58-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="8dc58-162">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="8dc58-162">This parameter is not required.</span></span>  
<span data-ttu-id="8dc58-163">如果您沒有指定此參數，則 Cmdlet 會使用先前在審核原則中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8dc58-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="8dc58-164">如果這是已定義審核原則的第一次，且您不指定此參數，則 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="8dc58-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="8dc58-165">-StorageKeyType</span></span>
<span data-ttu-id="8dc58-166">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8dc58-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-167">-確認</span><span class="sxs-lookup"><span data-stu-id="8dc58-167">-Confirm</span></span>
<span data-ttu-id="8dc58-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8dc58-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc58-169">-WhatIf</span></span>
<span data-ttu-id="8dc58-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8dc58-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dc58-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8dc58-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc58-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc58-172">CommonParameters</span></span>
<span data-ttu-id="8dc58-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8dc58-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc58-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8dc58-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc58-175">輸入</span><span class="sxs-lookup"><span data-stu-id="8dc58-175">INPUTS</span></span>

### <span data-ttu-id="8dc58-176">所有</span><span class="sxs-lookup"><span data-stu-id="8dc58-176">None</span></span>
<span data-ttu-id="8dc58-177">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8dc58-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8dc58-178">輸出</span><span class="sxs-lookup"><span data-stu-id="8dc58-178">OUTPUTS</span></span>

### <span data-ttu-id="8dc58-179">DatabaseBlobAuditingSettingsModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="8dc58-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="8dc58-180">筆記</span><span class="sxs-lookup"><span data-stu-id="8dc58-180">NOTES</span></span>

## <span data-ttu-id="8dc58-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dc58-181">RELATED LINKS</span></span>

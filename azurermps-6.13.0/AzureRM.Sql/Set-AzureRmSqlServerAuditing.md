---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 80887d1c3cfc91c9eba23f686deac071660cf852
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452667"
---
# <span data-ttu-id="74de4-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="74de4-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="74de4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74de4-102">SYNOPSIS</span></span>
<span data-ttu-id="74de4-103">變更 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="74de4-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74de4-104">句法</span><span class="sxs-lookup"><span data-stu-id="74de4-104">SYNTAX</span></span>

### <span data-ttu-id="74de4-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74de4-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-PredicateExpression <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74de4-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="74de4-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74de4-107">說明</span><span class="sxs-lookup"><span data-stu-id="74de4-107">DESCRIPTION</span></span>
<span data-ttu-id="74de4-108">**AzureRmSqlServerAuditing** Cmdlet 會變更 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="74de4-108">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="74de4-109">若要使用 Cmdlet，請使用 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="74de4-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="74de4-110">指定 *StorageAccountName* 參數，以指定審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="74de4-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="74de4-111">使用 *State* 參數來啟用/停用原則。</span><span class="sxs-lookup"><span data-stu-id="74de4-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="74de4-112">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="74de4-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="74de4-113">成功執行 Cmdlet 之後，就會啟用在指定的 Azure SQL server 中定義的 Azure SQL 資料庫的審核。</span><span class="sxs-lookup"><span data-stu-id="74de4-113">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="74de4-114">如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了伺服器識別碼之外，它還會傳回描述目前 blob 審核原則的物件。</span><span class="sxs-lookup"><span data-stu-id="74de4-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="74de4-115">伺服器識別碼包括但不限於、 **ResourceGroupName** 和 **ServerName** 。</span><span class="sxs-lookup"><span data-stu-id="74de4-115">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="74de4-116">示例</span><span class="sxs-lookup"><span data-stu-id="74de4-116">EXAMPLES</span></span>

### <span data-ttu-id="74de4-117">範例1：啟用 Azure SQL server 的審核原則</span><span class="sxs-lookup"><span data-stu-id="74de4-117">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="74de4-118">範例2：停用 Azure SQL server 的審核原則</span><span class="sxs-lookup"><span data-stu-id="74de4-118">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="74de4-119">範例3：使用不同訂閱的儲存空間帳戶來啟用 Azure SQL server 的審核原則</span><span class="sxs-lookup"><span data-stu-id="74de4-119">Example 3: Enable the auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="74de4-120">範例4：啟用 Azure SQL 資料庫的延伸審核原則</span><span class="sxs-lookup"><span data-stu-id="74de4-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="74de4-121">範例5：移除 Azure SQL 資料庫的延伸審核原則，並設定審核原則（而非它）。</span><span class="sxs-lookup"><span data-stu-id="74de4-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="74de4-122">參數</span><span class="sxs-lookup"><span data-stu-id="74de4-122">PARAMETERS</span></span>

### <span data-ttu-id="74de4-123">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="74de4-123">-AuditActionGroup</span></span>
<span data-ttu-id="74de4-124">建議使用的一組動作群組是下列專案，這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：「BATCH_COMPLETED_GROUP」、「SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP」、「FAILED_DATABASE_AUTHENTICATION_GROUP」上述組合也是預設設定。</span><span class="sxs-lookup"><span data-stu-id="74de4-124">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="74de4-125">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="74de4-125">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="74de4-126">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="74de4-126">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="74de4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74de4-127">-DefaultProfile</span></span>
<span data-ttu-id="74de4-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74de4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74de4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74de4-129">-PassThru</span></span>
<span data-ttu-id="74de4-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="74de4-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="74de4-131">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="74de4-131">-PredicateExpression</span></span>
<span data-ttu-id="74de4-132">Where 子句中用來篩選審核記錄的語句。</span><span class="sxs-lookup"><span data-stu-id="74de4-132">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="74de4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74de4-133">-ResourceGroupName</span></span>
<span data-ttu-id="74de4-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74de4-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="74de4-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="74de4-135">-RetentionInDays</span></span>
<span data-ttu-id="74de4-136">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="74de4-136">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="74de4-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="74de4-137">-ServerName</span></span>
<span data-ttu-id="74de4-138">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="74de4-138">SQL server name.</span></span>

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

### <span data-ttu-id="74de4-139">-State</span><span class="sxs-lookup"><span data-stu-id="74de4-139">-State</span></span>
<span data-ttu-id="74de4-140">原則的狀態。</span><span class="sxs-lookup"><span data-stu-id="74de4-140">The state of the policy.</span></span>

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

### <span data-ttu-id="74de4-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="74de4-141">-StorageAccountName</span></span>
<span data-ttu-id="74de4-142">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="74de4-142">The name of the storage account.</span></span> <span data-ttu-id="74de4-143">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="74de4-143">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="74de4-144">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="74de4-144">This parameter is not required.</span></span>
<span data-ttu-id="74de4-145">如果您沒有指定此參數，則 Cmdlet 會使用先前在審核原則中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="74de4-145">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="74de4-146">如果這是已定義審核原則的第一次，且您不指定此參數，則 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="74de4-146">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="74de4-147">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74de4-147">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="74de4-148">指定儲存空間帳戶訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="74de4-148">Specifies storage account subscription id</span></span>

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

### <span data-ttu-id="74de4-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="74de4-149">-StorageKeyType</span></span>
<span data-ttu-id="74de4-150">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="74de4-150">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="74de4-151">-確認</span><span class="sxs-lookup"><span data-stu-id="74de4-151">-Confirm</span></span>
<span data-ttu-id="74de4-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74de4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74de4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74de4-153">-WhatIf</span></span>
<span data-ttu-id="74de4-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74de4-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74de4-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74de4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74de4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74de4-156">CommonParameters</span></span>
<span data-ttu-id="74de4-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74de4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74de4-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74de4-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74de4-159">輸入</span><span class="sxs-lookup"><span data-stu-id="74de4-159">INPUTS</span></span>

## <span data-ttu-id="74de4-160">輸出</span><span class="sxs-lookup"><span data-stu-id="74de4-160">OUTPUTS</span></span>

## <span data-ttu-id="74de4-161">筆記</span><span class="sxs-lookup"><span data-stu-id="74de4-161">NOTES</span></span>

## <span data-ttu-id="74de4-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="74de4-162">RELATED LINKS</span></span>

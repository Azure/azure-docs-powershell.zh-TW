---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 9f551b5b334f6151b42faebf8b60d2939a0680d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447592"
---
# <span data-ttu-id="68630-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="68630-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="68630-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68630-102">SYNOPSIS</span></span>
<span data-ttu-id="68630-103">設定資料庫的審核原則。</span><span class="sxs-lookup"><span data-stu-id="68630-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68630-104">句法</span><span class="sxs-lookup"><span data-stu-id="68630-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68630-105">說明</span><span class="sxs-lookup"><span data-stu-id="68630-105">DESCRIPTION</span></span>
<span data-ttu-id="68630-106">**AzureRmSqlDatabaseAuditingPolicy** Cmdlet 會變更 Azure SQL 資料庫的審核原則。</span><span class="sxs-lookup"><span data-stu-id="68630-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="68630-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="68630-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="68630-108">指定 *StorageAccountName* 參數，以指定審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="68630-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="68630-109">您也可以設定 *RetentionInDays* 和 *TableIdentifier* 參數的值來定義 [審核記錄] 資料表的保留，以定義審核記錄資料表名稱的期間和種子。</span><span class="sxs-lookup"><span data-stu-id="68630-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="68630-110">指定事件 *類型參數，* 以定義要審核的事件種類。</span><span class="sxs-lookup"><span data-stu-id="68630-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="68630-111">成功執行 Cmdlet 之後，就會啟用資料庫審核。</span><span class="sxs-lookup"><span data-stu-id="68630-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="68630-112">對於 [資料表審核]，如果資料庫在您執行此 Cmdlet 之前使用其伺服器的原則進行審核，則審核會停止使用該原則。</span><span class="sxs-lookup"><span data-stu-id="68630-112">For Table Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span> <span data-ttu-id="68630-113">如果是 Blob 審核，在您執行此 Cmdlet 之前，如果資料庫已使用其伺服器的原則進行審核，這兩個審核原則都將存在並排。</span><span class="sxs-lookup"><span data-stu-id="68630-113">For Blob Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, both auditing policies will exist side-by-side.</span></span>
<span data-ttu-id="68630-114">如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了資料庫識別碼之外，它還會傳回描述目前審核原則的物件。</span><span class="sxs-lookup"><span data-stu-id="68630-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="68630-115">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="68630-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="68630-116">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68630-116">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="68630-117">示例</span><span class="sxs-lookup"><span data-stu-id="68630-117">EXAMPLES</span></span>

### <span data-ttu-id="68630-118">範例1：將資料庫的審核原則設定為使用資料表審核</span><span class="sxs-lookup"><span data-stu-id="68630-118">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="68630-119">這個命令會將名為 Database01 的資料庫審核原則設定在 Server01 上，以使用名為 Storage31 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="68630-119">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="68630-120">範例2：設定資料庫現有審核原則的儲存帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="68630-120">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="68630-121">這個命令會將名為 Database01 的資料庫審核原則設定在 Server01 上，以繼續使用相同的儲存空間帳戶名稱，但現在要使用次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="68630-121">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="68630-122">範例3：將資料庫的審核原則設定為使用特定的事件種類</span><span class="sxs-lookup"><span data-stu-id="68630-122">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="68630-123">範例4：將資料庫的審核原則設定為使用 Blob 審核</span><span class="sxs-lookup"><span data-stu-id="68630-123">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="68630-124">這個命令會設定位於 Server01 的名為 Database01 的資料庫審核原則。</span><span class="sxs-lookup"><span data-stu-id="68630-124">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="68630-125">原則會記錄 Login_Failure 事件種類。</span><span class="sxs-lookup"><span data-stu-id="68630-125">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="68630-126">此命令不會變更儲存設定。</span><span class="sxs-lookup"><span data-stu-id="68630-126">The command does not change the storage settings.</span></span>

## <span data-ttu-id="68630-127">參數</span><span class="sxs-lookup"><span data-stu-id="68630-127">PARAMETERS</span></span>

### <span data-ttu-id="68630-128">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="68630-128">-AuditAction</span></span>
<span data-ttu-id="68630-129">指定一或多個審核動作。</span><span class="sxs-lookup"><span data-stu-id="68630-129">Specify one or more audit actions.</span></span>
<span data-ttu-id="68630-130">這個參數只適用于 Blob 審核。</span><span class="sxs-lookup"><span data-stu-id="68630-130">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="68630-131">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="68630-131">-AuditActionGroup</span></span>
<span data-ttu-id="68630-132">指定一個或多個審核動作群組。</span><span class="sxs-lookup"><span data-stu-id="68630-132">Specify one or more audit action groups.</span></span>
<span data-ttu-id="68630-133">這個參數只適用于 Blob 審核。</span><span class="sxs-lookup"><span data-stu-id="68630-133">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="68630-134">-AuditType</span><span class="sxs-lookup"><span data-stu-id="68630-134">-AuditType</span></span>
```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68630-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="68630-135">-DatabaseName</span></span>
<span data-ttu-id="68630-136">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="68630-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="68630-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68630-137">-DefaultProfile</span></span>
<span data-ttu-id="68630-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="68630-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68630-139">-事件</span><span class="sxs-lookup"><span data-stu-id="68630-139">-EventType</span></span>
<span data-ttu-id="68630-140">指定要審核的事件種類。</span><span class="sxs-lookup"><span data-stu-id="68630-140">Specifies the event types to audit.</span></span>
<span data-ttu-id="68630-141">這個參數只適用于資料表審核。</span><span class="sxs-lookup"><span data-stu-id="68630-141">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="68630-142">您可以指定數種事件種類。</span><span class="sxs-lookup"><span data-stu-id="68630-142">You can specify several event types.</span></span>
<span data-ttu-id="68630-143">您可以指定 All 來審核所有事件種類，或指定 None，以指定不會審核任何事件。</span><span class="sxs-lookup"><span data-stu-id="68630-143">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="68630-144">如果您同時指定 All 或 None，則無法執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68630-144">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68630-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68630-145">-PassThru</span></span>
<span data-ttu-id="68630-146">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="68630-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="68630-147">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="68630-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="68630-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68630-148">-ResourceGroupName</span></span>
<span data-ttu-id="68630-149">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68630-149">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="68630-150">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="68630-150">-RetentionInDays</span></span>
<span data-ttu-id="68630-151">指定 [審核記錄] 資料表的保留天數。</span><span class="sxs-lookup"><span data-stu-id="68630-151">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="68630-152">零的值 (0) 表示該表格未保留。</span><span class="sxs-lookup"><span data-stu-id="68630-152">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="68630-153">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="68630-153">The default value is zero.</span></span>
<span data-ttu-id="68630-154">如果您指定的值大於零，您必須指定 *TableIdentifer* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="68630-154">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="68630-155">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68630-155">-ServerName</span></span>
<span data-ttu-id="68630-156">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="68630-156">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="68630-157">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68630-157">-StorageAccountName</span></span>
<span data-ttu-id="68630-158">指定要審核資料庫的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="68630-158">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="68630-159">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="68630-159">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="68630-160">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="68630-160">This parameter is not required.</span></span>
<span data-ttu-id="68630-161">如果您沒有指定此參數，則此 Cmdlet 會使用先前在資料庫的審核原則中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="68630-161">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="68630-162">如果這是已定義資料庫審核原則的第一次，且您不指定此參數，則 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="68630-162">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="68630-163">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="68630-163">-StorageKeyType</span></span>
<span data-ttu-id="68630-164">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="68630-164">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="68630-165">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="68630-165">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68630-166">首選</span><span class="sxs-lookup"><span data-stu-id="68630-166">Primary</span></span>
- <span data-ttu-id="68630-167">備用</span><span class="sxs-lookup"><span data-stu-id="68630-167">Secondary</span></span>

<span data-ttu-id="68630-168">預設值為 [主要]。</span><span class="sxs-lookup"><span data-stu-id="68630-168">The default value is Primary.</span></span>

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

### <span data-ttu-id="68630-169">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="68630-169">-TableIdentifier</span></span>
<span data-ttu-id="68630-170">指定 [審核記錄] 資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="68630-170">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="68630-171">如果您為 *RetentionInDays* 參數指定的值大於零，請指定此值。</span><span class="sxs-lookup"><span data-stu-id="68630-171">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="68630-172">-確認</span><span class="sxs-lookup"><span data-stu-id="68630-172">-Confirm</span></span>
<span data-ttu-id="68630-173">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68630-173">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68630-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68630-174">-WhatIf</span></span>
<span data-ttu-id="68630-175">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68630-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68630-176">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68630-176">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68630-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68630-177">CommonParameters</span></span>
<span data-ttu-id="68630-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68630-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68630-179">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68630-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68630-180">輸入</span><span class="sxs-lookup"><span data-stu-id="68630-180">INPUTS</span></span>

### <span data-ttu-id="68630-181">所有</span><span class="sxs-lookup"><span data-stu-id="68630-181">None</span></span>
<span data-ttu-id="68630-182">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="68630-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68630-183">輸出</span><span class="sxs-lookup"><span data-stu-id="68630-183">OUTPUTS</span></span>

### <span data-ttu-id="68630-184">DatabaseAuditingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="68630-184">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="68630-185">筆記</span><span class="sxs-lookup"><span data-stu-id="68630-185">NOTES</span></span>

## <span data-ttu-id="68630-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="68630-186">RELATED LINKS</span></span>

[<span data-ttu-id="68630-187">AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="68630-187">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="68630-188">移除-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="68630-188">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="68630-189">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="68630-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



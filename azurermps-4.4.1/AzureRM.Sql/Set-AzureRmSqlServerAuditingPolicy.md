---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: daec1290dfa70166e532265da98bdb507b1318e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450768"
---
# <span data-ttu-id="4eb55-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4eb55-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="4eb55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4eb55-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb55-103">變更 SQL 資料庫伺服器的審核原則。</span><span class="sxs-lookup"><span data-stu-id="4eb55-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eb55-104">句法</span><span class="sxs-lookup"><span data-stu-id="4eb55-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb55-105">說明</span><span class="sxs-lookup"><span data-stu-id="4eb55-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb55-106">**AzureRmSqlServerAuditingPolicy** Cmdlet 會變更 Azure SQL 資料庫伺服器的審核原則。</span><span class="sxs-lookup"><span data-stu-id="4eb55-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="4eb55-107">指定 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器、 *StorageAccountName* 參數以指定審核記錄的儲存空間帳戶，以及用來定義要使用之儲存空間的 *StorageKeyType* 參數。</span><span class="sxs-lookup"><span data-stu-id="4eb55-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="4eb55-108">您也可以設定 *RetentionInDays* 和 *TableIdentifier* 參數的值來定義 [審核記錄] 資料表的保留，以定義審核記錄資料表名稱的期間和種子。</span><span class="sxs-lookup"><span data-stu-id="4eb55-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="4eb55-109">指定事件 *類型參數，* 以定義要審核的事件種類。</span><span class="sxs-lookup"><span data-stu-id="4eb55-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="4eb55-110">在您執行此 Cmdlet 之後，就會啟用使用此伺服器原則的資料庫審核。</span><span class="sxs-lookup"><span data-stu-id="4eb55-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="4eb55-111">如果 Cmdlet 成功且您指定 *PassThru* 參數，則 Cmdlet 會傳回描述目前審核原則和伺服器識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="4eb55-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="4eb55-112">伺服器識別碼包括 **ResourceGroupName** 和 **ServerName** 。</span><span class="sxs-lookup"><span data-stu-id="4eb55-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="4eb55-113">示例</span><span class="sxs-lookup"><span data-stu-id="4eb55-113">EXAMPLES</span></span>

### <span data-ttu-id="4eb55-114">範例1：設定 Azure SQL server 的審核原則使用資料表審核</span><span class="sxs-lookup"><span data-stu-id="4eb55-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="4eb55-115">這個命令會將名為 Server01 的伺服器的審核原則設定為使用名為 Storage22 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4eb55-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="4eb55-116">範例2：設定 Azure SQL server 現有審核原則的儲存空間帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="4eb55-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="4eb55-117">這個命令會將名為 Server01 的伺服器的審核原則設定為使用次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="4eb55-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="4eb55-118">此命令不會修改儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4eb55-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="4eb55-119">範例3：將 Azure SQL server 的審核原則設定為使用特定的事件種類</span><span class="sxs-lookup"><span data-stu-id="4eb55-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="4eb55-120">範例4：將資料庫的審核原則設定為使用 Blob 審核</span><span class="sxs-lookup"><span data-stu-id="4eb55-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="4eb55-121">這個命令會將名為 Server01 的伺服器的審核原則設定為使用 Login_Failure 事件種類。</span><span class="sxs-lookup"><span data-stu-id="4eb55-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="4eb55-122">這個命令不會修改任何其他設定。</span><span class="sxs-lookup"><span data-stu-id="4eb55-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="4eb55-123">參數</span><span class="sxs-lookup"><span data-stu-id="4eb55-123">PARAMETERS</span></span>

### <span data-ttu-id="4eb55-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="4eb55-124">-AuditActionGroup</span></span>
<span data-ttu-id="4eb55-125">指定一個或多個審核動作群組。</span><span class="sxs-lookup"><span data-stu-id="4eb55-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="4eb55-126">這個參數只適用于 Blob 審核。</span><span class="sxs-lookup"><span data-stu-id="4eb55-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="4eb55-127">-AuditType</span><span class="sxs-lookup"><span data-stu-id="4eb55-127">-AuditType</span></span>
<span data-ttu-id="4eb55-128">指定審核類型。</span><span class="sxs-lookup"><span data-stu-id="4eb55-128">Specify the audit type.</span></span> <span data-ttu-id="4eb55-129">審核記錄可以寫入資料表儲存空間或 Blob 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="4eb55-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="4eb55-130">Blob 審核可提供較高的效能並支持對象層級的審核。</span><span class="sxs-lookup"><span data-stu-id="4eb55-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb55-131">-事件</span><span class="sxs-lookup"><span data-stu-id="4eb55-131">-EventType</span></span>
<span data-ttu-id="4eb55-132">指定要審核的事件種類。</span><span class="sxs-lookup"><span data-stu-id="4eb55-132">Specifies the event types to audit.</span></span>
<span data-ttu-id="4eb55-133">這個參數只適用于資料表審核。</span><span class="sxs-lookup"><span data-stu-id="4eb55-133">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="4eb55-134">您可以指定數種事件種類。</span><span class="sxs-lookup"><span data-stu-id="4eb55-134">You can specify several event types.</span></span>
<span data-ttu-id="4eb55-135">您可以指定 All 來審核所有事件種類，或指定 None，以指定不會審核任何事件。</span><span class="sxs-lookup"><span data-stu-id="4eb55-135">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="4eb55-136">如果您同時指定 All 或 None，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="4eb55-136">If you specify All or None at the same time, the command fails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb55-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eb55-137">-PassThru</span></span>
<span data-ttu-id="4eb55-138">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="4eb55-138">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4eb55-139">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4eb55-139">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4eb55-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb55-140">-ResourceGroupName</span></span>
<span data-ttu-id="4eb55-141">指定包含資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4eb55-141">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="4eb55-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4eb55-142">-RetentionInDays</span></span>
<span data-ttu-id="4eb55-143">指定 [審核記錄] 資料表的保留天數。</span><span class="sxs-lookup"><span data-stu-id="4eb55-143">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="4eb55-144">零的值 (0) 表示該表格未保留。</span><span class="sxs-lookup"><span data-stu-id="4eb55-144">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="4eb55-145">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="4eb55-145">this is the default.</span></span>
<span data-ttu-id="4eb55-146">如果您指定的值大於零，您也必須指定 *TableIdentifer* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="4eb55-146">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="4eb55-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4eb55-147">-ServerName</span></span>
<span data-ttu-id="4eb55-148">指定包含資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4eb55-148">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb55-149">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4eb55-149">-StorageAccountName</span></span>
<span data-ttu-id="4eb55-150">指定要審核資料庫的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4eb55-150">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="4eb55-151">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="4eb55-151">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="4eb55-152">如果您沒有指定此參數，則此 Cmdlet 會使用先前在資料庫的審核原則中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4eb55-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="4eb55-153">如果這是已定義資料庫審核原則的第一次，且您不指定此參數，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="4eb55-153">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="4eb55-154">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="4eb55-154">-StorageKeyType</span></span>
<span data-ttu-id="4eb55-155">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4eb55-155">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="4eb55-156">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4eb55-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4eb55-157">首選</span><span class="sxs-lookup"><span data-stu-id="4eb55-157">Primary</span></span>
- <span data-ttu-id="4eb55-158">備用</span><span class="sxs-lookup"><span data-stu-id="4eb55-158">Secondary</span></span>

<span data-ttu-id="4eb55-159">預設值為 [主要]。</span><span class="sxs-lookup"><span data-stu-id="4eb55-159">The default value is Primary.</span></span>

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

### <span data-ttu-id="4eb55-160">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="4eb55-160">-TableIdentifier</span></span>
<span data-ttu-id="4eb55-161">指定 [審核記錄] 資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="4eb55-161">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="4eb55-162">如果您為 *RetentionInDays* 參數指定的值大於零，請指定此值。</span><span class="sxs-lookup"><span data-stu-id="4eb55-162">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="4eb55-163">-確認</span><span class="sxs-lookup"><span data-stu-id="4eb55-163">-Confirm</span></span>
<span data-ttu-id="4eb55-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4eb55-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb55-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb55-165">-WhatIf</span></span>
<span data-ttu-id="4eb55-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4eb55-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb55-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4eb55-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb55-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb55-168">-DefaultProfile</span></span>
<span data-ttu-id="4eb55-169">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4eb55-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eb55-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb55-170">CommonParameters</span></span>
<span data-ttu-id="4eb55-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4eb55-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb55-172">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4eb55-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb55-173">輸入</span><span class="sxs-lookup"><span data-stu-id="4eb55-173">INPUTS</span></span>

## <span data-ttu-id="4eb55-174">輸出</span><span class="sxs-lookup"><span data-stu-id="4eb55-174">OUTPUTS</span></span>

### <span data-ttu-id="4eb55-175">ServerAuditingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="4eb55-175">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="4eb55-176">筆記</span><span class="sxs-lookup"><span data-stu-id="4eb55-176">NOTES</span></span>

## <span data-ttu-id="4eb55-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="4eb55-177">RELATED LINKS</span></span>

[<span data-ttu-id="4eb55-178">AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4eb55-178">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="4eb55-179">使用-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4eb55-179">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="4eb55-180">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4eb55-180">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



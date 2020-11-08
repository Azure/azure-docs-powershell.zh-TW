---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: ec88d8ff9f5a514a3b1b5dcd9ecb917ee348b900
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129803"
---
# <span data-ttu-id="60ae2-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="60ae2-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="60ae2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="60ae2-103">變更 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="60ae2-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="60ae2-104">句法</span><span class="sxs-lookup"><span data-stu-id="60ae2-104">SYNTAX</span></span>

### <span data-ttu-id="60ae2-105">ServerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="60ae2-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60ae2-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60ae2-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60ae2-107">說明</span><span class="sxs-lookup"><span data-stu-id="60ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="60ae2-108">**AzSqlServerAudit** Cmdlet 會變更 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="60ae2-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="60ae2-109">若要使用 Cmdlet，請使用 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="60ae2-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="60ae2-110">當 blob 儲存為審核記錄的目的地時，請指定 *StorageAccountResourceId* 參數來判斷審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="60ae2-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="60ae2-111">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="60ae2-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="60ae2-112">示例</span><span class="sxs-lookup"><span data-stu-id="60ae2-112">EXAMPLES</span></span>

### <span data-ttu-id="60ae2-113">範例1：啟用 Azure SQL server 的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="60ae2-114">範例2：停用 Azure SQL server 的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="60ae2-115">範例3：使用 T-sql 謂詞啟用高級篩選的 Azure SQL server 的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="60ae2-116">範例4：從 Azure SQL server 的審核原則中移除 [高級篩選] 設定</span><span class="sxs-lookup"><span data-stu-id="60ae2-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="60ae2-117">範例5：啟用 Azure SQL server 的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="60ae2-118">範例6：停用 Azure SQL server 的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="60ae2-119">範例7：啟用 Azure SQL server 的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="60ae2-120">範例8：停用 Azure SQL server 的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="60ae2-121">範例9：透過管線停用 Azure SQL server 的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="60ae2-122">範例10：停用將 Azure SQL server 的審核記錄傳送到 blob 儲存空間，並允許將其傳送至記錄分析。</span><span class="sxs-lookup"><span data-stu-id="60ae2-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="60ae2-123">範例11：啟用將 Azure SQL server 的審核記錄傳送到 blob 儲存空間、事件中樞和記錄分析。</span><span class="sxs-lookup"><span data-stu-id="60ae2-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="60ae2-124">參數</span><span class="sxs-lookup"><span data-stu-id="60ae2-124">PARAMETERS</span></span>

### <span data-ttu-id="60ae2-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60ae2-125">-AsJob</span></span>
<span data-ttu-id="60ae2-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="60ae2-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60ae2-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="60ae2-127">-AuditActionGroup</span></span>
<span data-ttu-id="60ae2-128">建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="60ae2-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="60ae2-129">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="60ae2-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="60ae2-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="60ae2-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="60ae2-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="60ae2-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="60ae2-132">上述組合也是預設設定的集合。</span><span class="sxs-lookup"><span data-stu-id="60ae2-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="60ae2-133">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="60ae2-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="60ae2-134">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="60ae2-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="60ae2-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="60ae2-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="60ae2-136">指出 [blob 儲存空間] 是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="60ae2-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="60ae2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ae2-137">-DefaultProfile</span></span>
<span data-ttu-id="60ae2-138">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60ae2-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60ae2-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="60ae2-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="60ae2-140">事件中心授權規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="60ae2-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="60ae2-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="60ae2-141">-EventHubName</span></span>
<span data-ttu-id="60ae2-142">事件中心的名稱。</span><span class="sxs-lookup"><span data-stu-id="60ae2-142">The name of the event hub.</span></span> <span data-ttu-id="60ae2-143">如果在提供 EventHubAuthorizationRuleResourceId 時沒有指定，則會選取預設事件中樞。</span><span class="sxs-lookup"><span data-stu-id="60ae2-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="60ae2-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="60ae2-144">-EventHubTargetState</span></span>
<span data-ttu-id="60ae2-145">指出事件中樞是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="60ae2-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="60ae2-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="60ae2-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="60ae2-147">指出記錄分析是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="60ae2-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="60ae2-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60ae2-148">-PassThru</span></span>
<span data-ttu-id="60ae2-149">指定是否要在 Cmdlet 執行結束時輸出審核原則</span><span class="sxs-lookup"><span data-stu-id="60ae2-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="60ae2-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="60ae2-150">-PredicateExpression</span></span>
<span data-ttu-id="60ae2-151">T-sql 謂語 (WHERE 子句) 用來篩選審核記錄。</span><span class="sxs-lookup"><span data-stu-id="60ae2-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="60ae2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ae2-152">-ResourceGroupName</span></span>
<span data-ttu-id="60ae2-153">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60ae2-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ae2-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="60ae2-154">-RetentionInDays</span></span>
<span data-ttu-id="60ae2-155">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="60ae2-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="60ae2-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60ae2-156">-ServerName</span></span>
<span data-ttu-id="60ae2-157">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="60ae2-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ae2-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="60ae2-158">-ServerObject</span></span>
<span data-ttu-id="60ae2-159">伺服器物件來管理其審核原則。</span><span class="sxs-lookup"><span data-stu-id="60ae2-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ae2-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="60ae2-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="60ae2-161">儲存空間帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="60ae2-161">The storage account resource id</span></span>

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

### <span data-ttu-id="60ae2-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="60ae2-162">-StorageKeyType</span></span>
<span data-ttu-id="60ae2-163">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="60ae2-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="60ae2-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="60ae2-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="60ae2-165">您想要傳送審核記錄的 Log analytics 工作區) 的 [工作區識別碼] (資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="60ae2-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="60ae2-166">範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="60ae2-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="60ae2-167">-確認</span><span class="sxs-lookup"><span data-stu-id="60ae2-167">-Confirm</span></span>
<span data-ttu-id="60ae2-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60ae2-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60ae2-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60ae2-169">-WhatIf</span></span>
<span data-ttu-id="60ae2-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60ae2-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60ae2-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60ae2-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60ae2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ae2-172">CommonParameters</span></span>
<span data-ttu-id="60ae2-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60ae2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ae2-174">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="60ae2-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ae2-175">輸入</span><span class="sxs-lookup"><span data-stu-id="60ae2-175">INPUTS</span></span>

### <span data-ttu-id="60ae2-176">System.object</span><span class="sxs-lookup"><span data-stu-id="60ae2-176">System.String</span></span>

### <span data-ttu-id="60ae2-177">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="60ae2-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="60ae2-178">AuditActionGroups [] （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="60ae2-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="60ae2-179">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="60ae2-179">System.Guid</span></span>

### <span data-ttu-id="60ae2-180">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="60ae2-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="60ae2-181">ServerAuditModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="60ae2-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="60ae2-182">輸出</span><span class="sxs-lookup"><span data-stu-id="60ae2-182">OUTPUTS</span></span>

### <span data-ttu-id="60ae2-183">System.object</span><span class="sxs-lookup"><span data-stu-id="60ae2-183">System.Boolean</span></span>

## <span data-ttu-id="60ae2-184">筆記</span><span class="sxs-lookup"><span data-stu-id="60ae2-184">NOTES</span></span>

## <span data-ttu-id="60ae2-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="60ae2-185">RELATED LINKS</span></span>

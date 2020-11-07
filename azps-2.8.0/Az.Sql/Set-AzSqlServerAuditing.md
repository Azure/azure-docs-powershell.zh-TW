---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792632"
---
# <span data-ttu-id="346a9-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="346a9-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="346a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="346a9-102">SYNOPSIS</span></span>
<span data-ttu-id="346a9-103">**重要：此 Cmdlet 已棄用，請將它取代為 [AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) 。**</span><span class="sxs-lookup"><span data-stu-id="346a9-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="346a9-104">變更 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="346a9-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="346a9-105">句法</span><span class="sxs-lookup"><span data-stu-id="346a9-105">SYNTAX</span></span>

### <span data-ttu-id="346a9-106">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="346a9-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346a9-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="346a9-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="346a9-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="346a9-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346a9-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="346a9-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346a9-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="346a9-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346a9-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="346a9-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="346a9-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="346a9-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346a9-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="346a9-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="346a9-114">說明</span><span class="sxs-lookup"><span data-stu-id="346a9-114">DESCRIPTION</span></span>
<span data-ttu-id="346a9-115">**AzSqlServerAuditing** Cmdlet 會變更 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="346a9-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="346a9-116">若要使用 Cmdlet，請使用 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="346a9-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="346a9-117">審計記錄目的地是透過指定下列其中一個切換參數來決定： BlobStorage、LogAnalytics 或 EventHub (如果沒有指定，則預設值為 BlobStorage) 。</span><span class="sxs-lookup"><span data-stu-id="346a9-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="346a9-118">使用 *State* 參數來啟用/停用原則。</span><span class="sxs-lookup"><span data-stu-id="346a9-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="346a9-119">當審核記錄目的地為 blob 儲存時，請指定 *StorageAccountName* 參數，以判斷審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="346a9-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="346a9-120">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="346a9-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="346a9-121">如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了伺服器識別碼之外，它還會傳回描述目前審核設定的物件。</span><span class="sxs-lookup"><span data-stu-id="346a9-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="346a9-122">伺服器識別碼包括但不限於、 **ResourceGroupName** 和 **ServerName** 。</span><span class="sxs-lookup"><span data-stu-id="346a9-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="346a9-123">示例</span><span class="sxs-lookup"><span data-stu-id="346a9-123">EXAMPLES</span></span>

### <span data-ttu-id="346a9-124">範例1：啟用 Azure SQL server 的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="346a9-125">範例2：停用 Azure SQL server 的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="346a9-126">範例3：使用不同訂閱的儲存空間帳戶來啟用 Azure SQL server 的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="346a9-127">範例4：使用 T-sql 謂詞啟用高級篩選的 Azure SQL server 的 blob 儲存審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="346a9-128">範例5：從 Azure SQL server 的 blob 審核儲存原則中移除 [高級篩選] 設定</span><span class="sxs-lookup"><span data-stu-id="346a9-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="346a9-129">範例6：啟用 Azure SQL server 的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="346a9-130">範例7：停用 Azure SQL server 的事件中心審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="346a9-131">範例8：啟用 Azure SQL server 的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="346a9-132">範例9：停用 Azure SQL server 的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="346a9-133">範例10：透過管線停用 Azure SQL server 的 log analytics 審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="346a9-134">參數</span><span class="sxs-lookup"><span data-stu-id="346a9-134">PARAMETERS</span></span>

### <span data-ttu-id="346a9-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="346a9-135">-AsJob</span></span>
<span data-ttu-id="346a9-136">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="346a9-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="346a9-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="346a9-137">-AuditActionGroup</span></span>
<span data-ttu-id="346a9-138">建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="346a9-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="346a9-139">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="346a9-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="346a9-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="346a9-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="346a9-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="346a9-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="346a9-142">上述組合也是預設設定的集合。</span><span class="sxs-lookup"><span data-stu-id="346a9-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="346a9-143">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="346a9-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="346a9-144">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="346a9-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="346a9-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="346a9-145">-BlobStorage</span></span>
<span data-ttu-id="346a9-146">指定審核記錄目的地為 blob 儲存空間</span><span class="sxs-lookup"><span data-stu-id="346a9-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="346a9-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346a9-147">-DefaultProfile</span></span>
<span data-ttu-id="346a9-148">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="346a9-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="346a9-149">-EventHub</span><span class="sxs-lookup"><span data-stu-id="346a9-149">-EventHub</span></span>
<span data-ttu-id="346a9-150">指定審核記錄目的地為事件中樞</span><span class="sxs-lookup"><span data-stu-id="346a9-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="346a9-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="346a9-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="346a9-152">事件中心授權規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="346a9-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="346a9-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="346a9-153">-EventHubName</span></span>
<span data-ttu-id="346a9-154">事件中心的名稱。</span><span class="sxs-lookup"><span data-stu-id="346a9-154">The name of the event hub.</span></span> <span data-ttu-id="346a9-155">如果在提供 EventHubAuthorizationRuleResourceId 時沒有指定，則會選取預設事件中樞。</span><span class="sxs-lookup"><span data-stu-id="346a9-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="346a9-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="346a9-156">-InputObject</span></span>
<span data-ttu-id="346a9-157">伺服器物件來管理其審核原則。</span><span class="sxs-lookup"><span data-stu-id="346a9-157">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="346a9-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="346a9-158">-LogAnalytics</span></span>
<span data-ttu-id="346a9-159">指定審核記錄目的地為 log analytics</span><span class="sxs-lookup"><span data-stu-id="346a9-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="346a9-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="346a9-160">-PassThru</span></span>
<span data-ttu-id="346a9-161">指定是否要在 Cmdlet 執行結束時輸出審核原則</span><span class="sxs-lookup"><span data-stu-id="346a9-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="346a9-162">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="346a9-162">-PredicateExpression</span></span>
<span data-ttu-id="346a9-163">T-sql 謂語 (WHERE 子句) 用來篩選審核記錄。</span><span class="sxs-lookup"><span data-stu-id="346a9-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="346a9-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="346a9-164">-ResourceGroupName</span></span>
<span data-ttu-id="346a9-165">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="346a9-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="346a9-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="346a9-166">-RetentionInDays</span></span>
<span data-ttu-id="346a9-167">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="346a9-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="346a9-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="346a9-168">-ServerName</span></span>
<span data-ttu-id="346a9-169">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="346a9-169">SQL server name.</span></span>

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

### <span data-ttu-id="346a9-170">-State</span><span class="sxs-lookup"><span data-stu-id="346a9-170">-State</span></span>
<span data-ttu-id="346a9-171">原則的狀態。</span><span class="sxs-lookup"><span data-stu-id="346a9-171">The state of the policy.</span></span>

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

### <span data-ttu-id="346a9-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="346a9-172">-StorageAccountName</span></span>
<span data-ttu-id="346a9-173">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="346a9-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="346a9-174">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="346a9-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="346a9-175">儲存空間帳戶訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="346a9-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="346a9-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="346a9-176">-StorageKeyType</span></span>
<span data-ttu-id="346a9-177">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="346a9-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="346a9-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="346a9-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="346a9-179">您想要傳送審核記錄的 Log analytics 工作區) 的 [工作區識別碼] (資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="346a9-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="346a9-180">範例：/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="346a9-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="346a9-181">-確認</span><span class="sxs-lookup"><span data-stu-id="346a9-181">-Confirm</span></span>
<span data-ttu-id="346a9-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="346a9-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="346a9-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="346a9-183">-WhatIf</span></span>
<span data-ttu-id="346a9-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="346a9-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="346a9-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="346a9-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="346a9-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346a9-186">CommonParameters</span></span>
<span data-ttu-id="346a9-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="346a9-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346a9-188">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="346a9-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346a9-189">輸入</span><span class="sxs-lookup"><span data-stu-id="346a9-189">INPUTS</span></span>

### <span data-ttu-id="346a9-190">System.object</span><span class="sxs-lookup"><span data-stu-id="346a9-190">System.String</span></span>

### <span data-ttu-id="346a9-191">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="346a9-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="346a9-192">AuditActionGroups [] （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="346a9-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="346a9-193">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="346a9-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="346a9-194">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="346a9-194">System.Guid</span></span>

### <span data-ttu-id="346a9-195">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="346a9-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="346a9-196">輸出</span><span class="sxs-lookup"><span data-stu-id="346a9-196">OUTPUTS</span></span>

### <span data-ttu-id="346a9-197">ServerBlobAuditingSettingsModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="346a9-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="346a9-198">筆記</span><span class="sxs-lookup"><span data-stu-id="346a9-198">NOTES</span></span>

## <span data-ttu-id="346a9-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="346a9-199">RELATED LINKS</span></span>

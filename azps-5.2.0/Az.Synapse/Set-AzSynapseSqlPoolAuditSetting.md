---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277100"
---
# <span data-ttu-id="e014d-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="e014d-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="e014d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e014d-102">SYNOPSIS</span></span>
<span data-ttu-id="e014d-103">變更 Azure Synapse Analytics SQL pool 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="e014d-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e014d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e014d-104">SYNTAX</span></span>

### <span data-ttu-id="e014d-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e014d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e014d-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e014d-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e014d-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e014d-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e014d-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e014d-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e014d-109">說明</span><span class="sxs-lookup"><span data-stu-id="e014d-109">DESCRIPTION</span></span>
<span data-ttu-id="e014d-110">**AzSynapseSqlPoolAuditSetting** Cmdlet 會變更 Azure SYNAPSE Analytics SQL pool 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="e014d-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="e014d-111">當 blob 儲存為審核記錄的目的地時，請指定 *StorageAccountResourceId* 參數來判斷審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="e014d-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="e014d-112">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="e014d-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="e014d-113">示例</span><span class="sxs-lookup"><span data-stu-id="e014d-113">EXAMPLES</span></span>

### <span data-ttu-id="e014d-114">範例1</span><span class="sxs-lookup"><span data-stu-id="e014d-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="e014d-115">啟用名為 ContosoSqlPool 的 Azure Synapse Analytics SQL pool 的 blob 儲存審核原則。</span><span class="sxs-lookup"><span data-stu-id="e014d-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="e014d-116">範例2</span><span class="sxs-lookup"><span data-stu-id="e014d-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="e014d-117">停用名為 ContosoSqlPool 的 Azure Synapse Analytics SQL pool 的 blob 儲存審核原則。</span><span class="sxs-lookup"><span data-stu-id="e014d-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="e014d-118">範例3</span><span class="sxs-lookup"><span data-stu-id="e014d-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="e014d-119">使用 T-sql 謂詞來啟用名為 ContosoSqlPool 的 Azure Synapse Analytics SQL pool 的 blob 儲存審核原則。</span><span class="sxs-lookup"><span data-stu-id="e014d-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="e014d-120">範例4</span><span class="sxs-lookup"><span data-stu-id="e014d-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="e014d-121">從 Azure Synapse Analytics SQL pool （名為 ContosoSqlPool）的審核原則中移除 [高級篩選] 設定。</span><span class="sxs-lookup"><span data-stu-id="e014d-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="e014d-122">範例5</span><span class="sxs-lookup"><span data-stu-id="e014d-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="e014d-123">停用名為 ContosoSqlPool 的 Azure Synapse Analytics SQL pool 的 blob 儲存審核原則。</span><span class="sxs-lookup"><span data-stu-id="e014d-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="e014d-124">參數</span><span class="sxs-lookup"><span data-stu-id="e014d-124">PARAMETERS</span></span>

### <span data-ttu-id="e014d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e014d-125">-AsJob</span></span>
<span data-ttu-id="e014d-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e014d-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e014d-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="e014d-127">-AuditAction</span></span>
<span data-ttu-id="e014d-128">一組審核動作。</span><span class="sxs-lookup"><span data-stu-id="e014d-128">The set of audit actions.</span></span>

<span data-ttu-id="e014d-129">支援的審核動作包括：</span><span class="sxs-lookup"><span data-stu-id="e014d-129">The supported actions to audit are:</span></span>

<span data-ttu-id="e014d-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="e014d-130">SELECT</span></span>

<span data-ttu-id="e014d-131">時更新</span><span class="sxs-lookup"><span data-stu-id="e014d-131">UPDATE</span></span>

<span data-ttu-id="e014d-132">插</span><span class="sxs-lookup"><span data-stu-id="e014d-132">INSERT</span></span>

<span data-ttu-id="e014d-133">DELETE</span><span class="sxs-lookup"><span data-stu-id="e014d-133">DELETE</span></span>

<span data-ttu-id="e014d-134">抓住</span><span class="sxs-lookup"><span data-stu-id="e014d-134">EXECUTE</span></span>

<span data-ttu-id="e014d-135">接收</span><span class="sxs-lookup"><span data-stu-id="e014d-135">RECEIVE</span></span>

<span data-ttu-id="e014d-136">提到</span><span class="sxs-lookup"><span data-stu-id="e014d-136">REFERENCES</span></span>

<span data-ttu-id="e014d-137">定義要審核之動作的一般形式為：</span><span class="sxs-lookup"><span data-stu-id="e014d-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="e014d-138">\[\] \[ \] 依主體對物件執行的動作 \[\]</span><span class="sxs-lookup"><span data-stu-id="e014d-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="e014d-139">請注意 \[ ， \] 以上格式中的物件可以參照表格、視圖或儲存程式，或整個資料庫或架構等物件。</span><span class="sxs-lookup"><span data-stu-id="e014d-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="e014d-140">在後一個情況下，會分別使用表單資料庫：： \[ dbname \] 和 SCHEMA：： \[ schemaname \] 。</span><span class="sxs-lookup"><span data-stu-id="e014d-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="e014d-141">例如：</span><span class="sxs-lookup"><span data-stu-id="e014d-141">For example:</span></span>

<span data-ttu-id="e014d-142">依公開選取 dbo. myTable</span><span class="sxs-lookup"><span data-stu-id="e014d-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="e014d-143">選取 [在資料庫：：由公用 myDatabase]</span><span class="sxs-lookup"><span data-stu-id="e014d-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="e014d-144">選取 [在架構：：由公用 mySchema]</span><span class="sxs-lookup"><span data-stu-id="e014d-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="e014d-145">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。</span><span class="sxs-lookup"><span data-stu-id="e014d-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="e014d-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="e014d-146">-AuditActionGroup</span></span>
<span data-ttu-id="e014d-147">建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="e014d-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="e014d-148">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="e014d-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="e014d-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="e014d-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="e014d-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="e014d-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="e014d-151">上述組合也是預設設定的集合。</span><span class="sxs-lookup"><span data-stu-id="e014d-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="e014d-152">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="e014d-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="e014d-153">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="e014d-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e014d-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="e014d-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="e014d-155">指出 [blob 儲存空間] 是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="e014d-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="e014d-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e014d-156">-DefaultProfile</span></span>
<span data-ttu-id="e014d-157">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e014d-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e014d-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e014d-158">-InputObject</span></span>
<span data-ttu-id="e014d-159">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e014d-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e014d-160">-名稱</span><span class="sxs-lookup"><span data-stu-id="e014d-160">-Name</span></span>
<span data-ttu-id="e014d-161">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e014d-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e014d-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e014d-162">-PassThru</span></span>
<span data-ttu-id="e014d-163">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="e014d-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e014d-164">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e014d-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e014d-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="e014d-165">-PredicateExpression</span></span>
<span data-ttu-id="e014d-166">T-sql 謂語 (WHERE 子句) 用來篩選審核記錄。</span><span class="sxs-lookup"><span data-stu-id="e014d-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="e014d-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e014d-167">-ResourceGroupName</span></span>
<span data-ttu-id="e014d-168">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e014d-168">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e014d-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e014d-169">-ResourceId</span></span>
<span data-ttu-id="e014d-170">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e014d-170">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e014d-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e014d-171">-RetentionInDays</span></span>
<span data-ttu-id="e014d-172">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="e014d-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="e014d-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e014d-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="e014d-174">儲存空間帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e014d-174">The storage account resource id</span></span>

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

### <span data-ttu-id="e014d-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="e014d-175">-StorageKeyType</span></span>
<span data-ttu-id="e014d-176">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e014d-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="e014d-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e014d-177">-WorkspaceName</span></span>
<span data-ttu-id="e014d-178">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e014d-178">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e014d-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e014d-179">-WorkspaceObject</span></span>
<span data-ttu-id="e014d-180">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e014d-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e014d-181">-確認</span><span class="sxs-lookup"><span data-stu-id="e014d-181">-Confirm</span></span>
<span data-ttu-id="e014d-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e014d-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e014d-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e014d-183">-WhatIf</span></span>
<span data-ttu-id="e014d-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e014d-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e014d-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e014d-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e014d-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e014d-186">CommonParameters</span></span>
<span data-ttu-id="e014d-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e014d-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e014d-188">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e014d-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e014d-189">輸入</span><span class="sxs-lookup"><span data-stu-id="e014d-189">INPUTS</span></span>

### <span data-ttu-id="e014d-190">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e014d-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e014d-191">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e014d-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e014d-192">輸出</span><span class="sxs-lookup"><span data-stu-id="e014d-192">OUTPUTS</span></span>

### <span data-ttu-id="e014d-193">SqlPoolAuditModel 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e014d-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="e014d-194">筆記</span><span class="sxs-lookup"><span data-stu-id="e014d-194">NOTES</span></span>

## <span data-ttu-id="e014d-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="e014d-195">RELATED LINKS</span></span>

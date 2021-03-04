---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 102d8f9e33a90d97cadb984a671797a89d6f3833
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912226"
---
# <span data-ttu-id="29639-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="29639-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="29639-102">簡介</span><span class="sxs-lookup"><span data-stu-id="29639-102">SYNOPSIS</span></span>
<span data-ttu-id="29639-103">變更 Azure Synapse Analytics SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="29639-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="29639-104">語法</span><span class="sxs-lookup"><span data-stu-id="29639-104">SYNTAX</span></span>

### <span data-ttu-id="29639-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="29639-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29639-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29639-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29639-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29639-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29639-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29639-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29639-109">描述</span><span class="sxs-lookup"><span data-stu-id="29639-109">DESCRIPTION</span></span>
<span data-ttu-id="29639-110">**Set-AzSynapseSqlPoolAuditSetting** Cmdlet 會變更 Azure Synapse Analytics SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="29639-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="29639-111">當 Blob 儲存體是稽核記錄的目標時，請指定 *StorageAccountResourceId* 參數，以決定稽核記錄中的儲存帳戶，以及 *StorageKeyType* 參數來定義儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="29639-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="29639-112">您也可以設定 *RetentionInDays* 參數的值來定義稽核記錄期間，以定義稽核記錄保留。</span><span class="sxs-lookup"><span data-stu-id="29639-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="29639-113">例子</span><span class="sxs-lookup"><span data-stu-id="29639-113">EXAMPLES</span></span>

### <span data-ttu-id="29639-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="29639-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="29639-115">啟用名為 ContosoSqlPool 之 Azure Synapse Analytics SQL Pool 的 Blob 儲存稽核原則。</span><span class="sxs-lookup"><span data-stu-id="29639-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="29639-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="29639-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="29639-117">停用名為 ContosoSqlPool 之 Azure Synapse Analytics SQL Pool 的 Blob 儲存稽核原則。</span><span class="sxs-lookup"><span data-stu-id="29639-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="29639-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="29639-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="29639-119">啟用 Azure Synapse Analytics SQL Pool 的 Blob 儲存稽核原則，該集區名為 ContosoSqlPool，使用 T-SQL 詞詞進行進位篩選。</span><span class="sxs-lookup"><span data-stu-id="29639-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="29639-120">範例 4</span><span class="sxs-lookup"><span data-stu-id="29639-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="29639-121">從名為 ContosoSqlPool 的 Azure Synapse Analytics SQL Pool 的稽核原則移除進位篩選設定。</span><span class="sxs-lookup"><span data-stu-id="29639-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="29639-122">範例 5</span><span class="sxs-lookup"><span data-stu-id="29639-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="29639-123">停用名為 ContosoSqlPool 的 Azure Synapse Analytics SQL Pool 透過管線的 Blob 儲存稽核原則。</span><span class="sxs-lookup"><span data-stu-id="29639-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="29639-124">參數</span><span class="sxs-lookup"><span data-stu-id="29639-124">PARAMETERS</span></span>

### <span data-ttu-id="29639-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29639-125">-AsJob</span></span>
<span data-ttu-id="29639-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="29639-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29639-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="29639-127">-AuditAction</span></span>
<span data-ttu-id="29639-128">稽核動作集。</span><span class="sxs-lookup"><span data-stu-id="29639-128">The set of audit actions.</span></span>

<span data-ttu-id="29639-129">支援的稽核動作為：</span><span class="sxs-lookup"><span data-stu-id="29639-129">The supported actions to audit are:</span></span>

<span data-ttu-id="29639-130">選擇</span><span class="sxs-lookup"><span data-stu-id="29639-130">SELECT</span></span>

<span data-ttu-id="29639-131">更新</span><span class="sxs-lookup"><span data-stu-id="29639-131">UPDATE</span></span>

<span data-ttu-id="29639-132">插入</span><span class="sxs-lookup"><span data-stu-id="29639-132">INSERT</span></span>

<span data-ttu-id="29639-133">刪除</span><span class="sxs-lookup"><span data-stu-id="29639-133">DELETE</span></span>

<span data-ttu-id="29639-134">執行</span><span class="sxs-lookup"><span data-stu-id="29639-134">EXECUTE</span></span>

<span data-ttu-id="29639-135">收到</span><span class="sxs-lookup"><span data-stu-id="29639-135">RECEIVE</span></span>

<span data-ttu-id="29639-136">引用</span><span class="sxs-lookup"><span data-stu-id="29639-136">REFERENCES</span></span>

<span data-ttu-id="29639-137">定義要稽核之動作的一般表單為：</span><span class="sxs-lookup"><span data-stu-id="29639-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="29639-138">\[動作 \] ON 物件 BY \[ \] \[ 主體\]</span><span class="sxs-lookup"><span data-stu-id="29639-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="29639-139">請注意，上述格式的物件可以參照資料表、視圖或儲存程式等物件，或是 \[ \] 整個資料庫或架構。</span><span class="sxs-lookup"><span data-stu-id="29639-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="29639-140">在後一種情況下，分別使用 forms DATABASE：： \[ dbname \] 和 SCHEMA：： \[ \] schemaname。</span><span class="sxs-lookup"><span data-stu-id="29639-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="29639-141">例如：</span><span class="sxs-lookup"><span data-stu-id="29639-141">For example:</span></span>

<span data-ttu-id="29639-142">在 dbo.myTable 上按公用 SELECT</span><span class="sxs-lookup"><span data-stu-id="29639-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="29639-143">DATABASE 上的 SELECT：myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="29639-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="29639-144">SCHEMA 上的 SELECT：mySchema by public</span><span class="sxs-lookup"><span data-stu-id="29639-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="29639-145">詳細資訊請參閱 https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 。</span><span class="sxs-lookup"><span data-stu-id="29639-145">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="29639-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="29639-146">-AuditActionGroup</span></span>
<span data-ttu-id="29639-147">建議使用的動作群組組合為下列組合：這會稽核對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="29639-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="29639-148">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="29639-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="29639-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="29639-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="29639-150">「FAILED_DATABASE_AUTHENTICATION_GROUP」</span><span class="sxs-lookup"><span data-stu-id="29639-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="29639-151">上述組合也是預設設定的組合。</span><span class="sxs-lookup"><span data-stu-id="29639-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="29639-152">這些群組涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，而且不應與其他群組搭配使用，因為這樣會導致重複的稽核記錄。</span><span class="sxs-lookup"><span data-stu-id="29639-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="29639-153">詳細資訊請參閱 https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="29639-153">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="29639-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="29639-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="29639-155">指出 Blob 儲存空間是否是稽核記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="29639-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="29639-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29639-156">-DefaultProfile</span></span>
<span data-ttu-id="29639-157">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="29639-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29639-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29639-158">-InputObject</span></span>
<span data-ttu-id="29639-159">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="29639-159">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="29639-160">-名稱</span><span class="sxs-lookup"><span data-stu-id="29639-160">-Name</span></span>
<span data-ttu-id="29639-161">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="29639-161">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="29639-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29639-162">-PassThru</span></span>
<span data-ttu-id="29639-163">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="29639-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="29639-164">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="29639-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="29639-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="29639-165">-PredicateExpression</span></span>
<span data-ttu-id="29639-166">T-SQL 謂詞 (WHERE 子句) 用來篩選稽核記錄。</span><span class="sxs-lookup"><span data-stu-id="29639-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="29639-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29639-167">-ResourceGroupName</span></span>
<span data-ttu-id="29639-168">資源組名。</span><span class="sxs-lookup"><span data-stu-id="29639-168">Resource group name.</span></span>

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

### <span data-ttu-id="29639-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29639-169">-ResourceId</span></span>
<span data-ttu-id="29639-170">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="29639-170">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="29639-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="29639-171">-RetentionInDays</span></span>
<span data-ttu-id="29639-172">稽核記錄保留天數。</span><span class="sxs-lookup"><span data-stu-id="29639-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="29639-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="29639-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="29639-174">儲存帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="29639-174">The storage account resource id</span></span>

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

### <span data-ttu-id="29639-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="29639-175">-StorageKeyType</span></span>
<span data-ttu-id="29639-176">指定要使用哪些儲存存取鍵。</span><span class="sxs-lookup"><span data-stu-id="29639-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="29639-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="29639-177">-WorkspaceName</span></span>
<span data-ttu-id="29639-178">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="29639-178">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="29639-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="29639-179">-WorkspaceObject</span></span>
<span data-ttu-id="29639-180">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="29639-180">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="29639-181">-確認</span><span class="sxs-lookup"><span data-stu-id="29639-181">-Confirm</span></span>
<span data-ttu-id="29639-182">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="29639-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29639-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29639-183">-WhatIf</span></span>
<span data-ttu-id="29639-184">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29639-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29639-185">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29639-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29639-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29639-186">CommonParameters</span></span>
<span data-ttu-id="29639-187">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="29639-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29639-188">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29639-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29639-189">輸入</span><span class="sxs-lookup"><span data-stu-id="29639-189">INPUTS</span></span>

### <span data-ttu-id="29639-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="29639-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="29639-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="29639-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="29639-192">輸出</span><span class="sxs-lookup"><span data-stu-id="29639-192">OUTPUTS</span></span>

### <span data-ttu-id="29639-193">Microsoft.Azure.Commands.Synapse.models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="29639-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="29639-194">筆記</span><span class="sxs-lookup"><span data-stu-id="29639-194">NOTES</span></span>

## <span data-ttu-id="29639-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="29639-195">RELATED LINKS</span></span>

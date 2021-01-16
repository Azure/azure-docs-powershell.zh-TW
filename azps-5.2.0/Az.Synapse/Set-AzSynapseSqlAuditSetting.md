---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ae09bb11b56bd6c5fa0add402ace850fe560b293
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280568"
---
# <span data-ttu-id="dbf36-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="dbf36-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="dbf36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbf36-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf36-103">變更 Azure Synapse Analytics 工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="dbf36-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="dbf36-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbf36-104">SYNTAX</span></span>

### <span data-ttu-id="dbf36-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dbf36-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf36-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf36-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf36-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf36-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf36-108">說明</span><span class="sxs-lookup"><span data-stu-id="dbf36-108">DESCRIPTION</span></span>
<span data-ttu-id="dbf36-109">**AzSynapseSqlAuditSetting** Cmdlet 會變更 Azure Synapse Analytics 工作區的審核設定。</span><span class="sxs-lookup"><span data-stu-id="dbf36-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="dbf36-110">當 blob 儲存為審核記錄的目的地時，請指定 *StorageAccountResourceId* 參數來判斷審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="dbf36-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="dbf36-111">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="dbf36-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="dbf36-112">示例</span><span class="sxs-lookup"><span data-stu-id="dbf36-112">EXAMPLES</span></span>

### <span data-ttu-id="dbf36-113">範例1</span><span class="sxs-lookup"><span data-stu-id="dbf36-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="dbf36-114">啟用名為 ContosoWorkspace 的 Azure Synapse Analytics 工作區的 blob 儲存審核原則。</span><span class="sxs-lookup"><span data-stu-id="dbf36-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="dbf36-115">範例2</span><span class="sxs-lookup"><span data-stu-id="dbf36-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="dbf36-116">停用名為 ContosoWorkspace 的 Azure Synapse Analytics 工作區的 blob 儲存審核原則。</span><span class="sxs-lookup"><span data-stu-id="dbf36-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="dbf36-117">範例3</span><span class="sxs-lookup"><span data-stu-id="dbf36-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="dbf36-118">使用 T-sql 謂語來啟用名為 ContosoWorkspace 的 Azure Synapse Analytics 工作區的 blob 儲存審核原則。</span><span class="sxs-lookup"><span data-stu-id="dbf36-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="dbf36-119">範例4</span><span class="sxs-lookup"><span data-stu-id="dbf36-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="dbf36-120">從 Azure Synapse Analytics 工作區（名為 ContosoWorkspace）的審核原則中移除 [高級篩選] 設定。</span><span class="sxs-lookup"><span data-stu-id="dbf36-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="dbf36-121">範例5</span><span class="sxs-lookup"><span data-stu-id="dbf36-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="dbf36-122">停用名為 ContosoWorkspace 至管線的 Azure Synapse Analytics 工作區的 blob 儲存審核原則。</span><span class="sxs-lookup"><span data-stu-id="dbf36-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="dbf36-123">參數</span><span class="sxs-lookup"><span data-stu-id="dbf36-123">PARAMETERS</span></span>

### <span data-ttu-id="dbf36-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbf36-124">-AsJob</span></span>
<span data-ttu-id="dbf36-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dbf36-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbf36-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="dbf36-126">-AuditActionGroup</span></span>
<span data-ttu-id="dbf36-127">建議使用的一組動作群組是下列組合-這將會審核針對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="dbf36-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="dbf36-128">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="dbf36-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="dbf36-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="dbf36-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="dbf36-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="dbf36-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="dbf36-131">上述組合也是預設設定的集合。</span><span class="sxs-lookup"><span data-stu-id="dbf36-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="dbf36-132">這些群組會涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，因此不應與其他群組搭配使用，因為這會產生重複的審核記錄。</span><span class="sxs-lookup"><span data-stu-id="dbf36-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="dbf36-133">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="dbf36-133">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="dbf36-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="dbf36-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="dbf36-135">指出 [blob 儲存空間] 是否為審計記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="dbf36-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="dbf36-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf36-136">-DefaultProfile</span></span>
<span data-ttu-id="dbf36-137">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbf36-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf36-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbf36-138">-InputObject</span></span>
<span data-ttu-id="dbf36-139">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="dbf36-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf36-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbf36-140">-PassThru</span></span>
<span data-ttu-id="dbf36-141">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="dbf36-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="dbf36-142">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="dbf36-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="dbf36-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="dbf36-143">-PredicateExpression</span></span>
<span data-ttu-id="dbf36-144">T-sql 謂語 (WHERE 子句) 用來篩選審核記錄。</span><span class="sxs-lookup"><span data-stu-id="dbf36-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="dbf36-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf36-145">-ResourceGroupName</span></span>
<span data-ttu-id="dbf36-146">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="dbf36-146">Resource group name.</span></span>

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

### <span data-ttu-id="dbf36-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbf36-147">-ResourceId</span></span>
<span data-ttu-id="dbf36-148">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbf36-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="dbf36-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="dbf36-149">-RetentionInDays</span></span>
<span data-ttu-id="dbf36-150">審計記錄的保留天數。</span><span class="sxs-lookup"><span data-stu-id="dbf36-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="dbf36-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="dbf36-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="dbf36-152">儲存空間帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="dbf36-152">The storage account resource id</span></span>

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

### <span data-ttu-id="dbf36-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="dbf36-153">-StorageKeyType</span></span>
<span data-ttu-id="dbf36-154">指定要使用的儲存空間便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="dbf36-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="dbf36-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dbf36-155">-WorkspaceName</span></span>
<span data-ttu-id="dbf36-156">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbf36-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dbf36-157">-確認</span><span class="sxs-lookup"><span data-stu-id="dbf36-157">-Confirm</span></span>
<span data-ttu-id="dbf36-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dbf36-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf36-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf36-159">-WhatIf</span></span>
<span data-ttu-id="dbf36-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbf36-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf36-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbf36-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf36-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf36-162">CommonParameters</span></span>
<span data-ttu-id="dbf36-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbf36-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf36-164">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbf36-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf36-165">輸入</span><span class="sxs-lookup"><span data-stu-id="dbf36-165">INPUTS</span></span>

### <span data-ttu-id="dbf36-166">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="dbf36-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dbf36-167">輸出</span><span class="sxs-lookup"><span data-stu-id="dbf36-167">OUTPUTS</span></span>

### <span data-ttu-id="dbf36-168">WorkspaceAuditModel 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="dbf36-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="dbf36-169">筆記</span><span class="sxs-lookup"><span data-stu-id="dbf36-169">NOTES</span></span>

## <span data-ttu-id="dbf36-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbf36-170">RELATED LINKS</span></span>

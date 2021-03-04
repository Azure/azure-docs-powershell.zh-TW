---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 15d553800aa51bdf4752902dadd8d5b15fcdf2f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912230"
---
# <span data-ttu-id="e5f39-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="e5f39-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="e5f39-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5f39-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f39-103">變更 Azure Synapse Analytics Workspace 的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="e5f39-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="e5f39-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5f39-104">SYNTAX</span></span>

### <span data-ttu-id="e5f39-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e5f39-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f39-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f39-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f39-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f39-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f39-108">描述</span><span class="sxs-lookup"><span data-stu-id="e5f39-108">DESCRIPTION</span></span>
<span data-ttu-id="e5f39-109">**Set-AzSynapseSqlAuditSetting** Cmdlet 會變更 Azure Synapse Analytics Workspace 的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="e5f39-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="e5f39-110">當 Blob 儲存體是稽核記錄的目標時，請指定 *StorageAccountResourceId* 參數，以決定稽核記錄中的儲存帳戶，以及 *StorageKeyType* 參數來定義儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5f39-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="e5f39-111">您也可以設定 *RetentionInDays* 參數的值來定義稽核記錄期間，以定義稽核記錄保留。</span><span class="sxs-lookup"><span data-stu-id="e5f39-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="e5f39-112">例子</span><span class="sxs-lookup"><span data-stu-id="e5f39-112">EXAMPLES</span></span>

### <span data-ttu-id="e5f39-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="e5f39-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="e5f39-114">啟用名為 ContosoWorkspace 的 Azure Synapse Analytics Workspace 的 Blob 儲存稽核原則。</span><span class="sxs-lookup"><span data-stu-id="e5f39-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e5f39-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="e5f39-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="e5f39-116">停用名為 ContosoWorkspace 之 Azure Synapse Analytics Workspace 的 Blob 儲存稽核原則。</span><span class="sxs-lookup"><span data-stu-id="e5f39-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e5f39-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="e5f39-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="e5f39-118">啟用 Azure Synapse Analytics Workspace 的 Blob 儲存稽核原則，該工作區名為 ContosoWorkspace，使用 T-SQL 謂詞進行進一級的篩選。</span><span class="sxs-lookup"><span data-stu-id="e5f39-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="e5f39-119">範例 4</span><span class="sxs-lookup"><span data-stu-id="e5f39-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="e5f39-120">從名為 ContosoWorkspace 的 Azure Synapse Analytics Workspace 稽核原則移除進位篩選設定。</span><span class="sxs-lookup"><span data-stu-id="e5f39-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e5f39-121">範例 5</span><span class="sxs-lookup"><span data-stu-id="e5f39-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="e5f39-122">透過管道停用名為 ContosoWorkspace 的 Azure Synapse Analytics Workspace 的 Blob 儲存稽核原則。</span><span class="sxs-lookup"><span data-stu-id="e5f39-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e5f39-123">參數</span><span class="sxs-lookup"><span data-stu-id="e5f39-123">PARAMETERS</span></span>

### <span data-ttu-id="e5f39-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5f39-124">-AsJob</span></span>
<span data-ttu-id="e5f39-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5f39-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5f39-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="e5f39-126">-AuditActionGroup</span></span>
<span data-ttu-id="e5f39-127">建議使用的動作群組組合為下列組合：這會稽核對資料庫執行的所有查詢和儲存程式，以及成功和失敗的登入：</span><span class="sxs-lookup"><span data-stu-id="e5f39-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="e5f39-128">"BATCH_COMPLETED_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="e5f39-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="e5f39-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP"，</span><span class="sxs-lookup"><span data-stu-id="e5f39-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="e5f39-130">「FAILED_DATABASE_AUTHENTICATION_GROUP」</span><span class="sxs-lookup"><span data-stu-id="e5f39-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="e5f39-131">上述組合也是預設設定的組合。</span><span class="sxs-lookup"><span data-stu-id="e5f39-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="e5f39-132">這些群組涵蓋針對資料庫執行的所有 SQL 語句和儲存程式，而且不應與其他群組搭配使用，因為這樣會導致重複的稽核記錄。</span><span class="sxs-lookup"><span data-stu-id="e5f39-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="e5f39-133">詳細資訊請參閱 https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 。</span><span class="sxs-lookup"><span data-stu-id="e5f39-133">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="e5f39-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="e5f39-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="e5f39-135">指出 Blob 儲存空間是否是稽核記錄的目的地。</span><span class="sxs-lookup"><span data-stu-id="e5f39-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="e5f39-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f39-136">-DefaultProfile</span></span>
<span data-ttu-id="e5f39-137">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5f39-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f39-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5f39-138">-InputObject</span></span>
<span data-ttu-id="e5f39-139">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="e5f39-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e5f39-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5f39-140">-PassThru</span></span>
<span data-ttu-id="e5f39-141">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="e5f39-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e5f39-142">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="e5f39-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e5f39-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="e5f39-143">-PredicateExpression</span></span>
<span data-ttu-id="e5f39-144">T-SQL 謂詞 (WHERE 子句) 用來篩選稽核記錄。</span><span class="sxs-lookup"><span data-stu-id="e5f39-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="e5f39-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f39-145">-ResourceGroupName</span></span>
<span data-ttu-id="e5f39-146">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e5f39-146">Resource group name.</span></span>

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

### <span data-ttu-id="e5f39-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f39-147">-ResourceId</span></span>
<span data-ttu-id="e5f39-148">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5f39-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="e5f39-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e5f39-149">-RetentionInDays</span></span>
<span data-ttu-id="e5f39-150">稽核記錄保留天數。</span><span class="sxs-lookup"><span data-stu-id="e5f39-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="e5f39-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f39-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="e5f39-152">儲存帳戶資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e5f39-152">The storage account resource id</span></span>

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

### <span data-ttu-id="e5f39-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="e5f39-153">-StorageKeyType</span></span>
<span data-ttu-id="e5f39-154">指定要使用哪些儲存存取鍵。</span><span class="sxs-lookup"><span data-stu-id="e5f39-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="e5f39-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5f39-155">-WorkspaceName</span></span>
<span data-ttu-id="e5f39-156">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5f39-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e5f39-157">-確認</span><span class="sxs-lookup"><span data-stu-id="e5f39-157">-Confirm</span></span>
<span data-ttu-id="e5f39-158">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e5f39-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f39-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f39-159">-WhatIf</span></span>
<span data-ttu-id="e5f39-160">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5f39-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5f39-161">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5f39-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f39-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f39-162">CommonParameters</span></span>
<span data-ttu-id="e5f39-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5f39-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f39-164">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5f39-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f39-165">輸入</span><span class="sxs-lookup"><span data-stu-id="e5f39-165">INPUTS</span></span>

### <span data-ttu-id="e5f39-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5f39-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e5f39-167">輸出</span><span class="sxs-lookup"><span data-stu-id="e5f39-167">OUTPUTS</span></span>

### <span data-ttu-id="e5f39-168">Microsoft.Azure.Commands.Synapse.models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="e5f39-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="e5f39-169">筆記</span><span class="sxs-lookup"><span data-stu-id="e5f39-169">NOTES</span></span>

## <span data-ttu-id="e5f39-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5f39-170">RELATED LINKS</span></span>

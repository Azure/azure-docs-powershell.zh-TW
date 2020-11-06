---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448826"
---
# <span data-ttu-id="b170b-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="b170b-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="b170b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b170b-102">SYNOPSIS</span></span>
<span data-ttu-id="b170b-103">變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="b170b-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b170b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b170b-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b170b-105">說明</span><span class="sxs-lookup"><span data-stu-id="b170b-105">DESCRIPTION</span></span>
<span data-ttu-id="b170b-106">**AzureRmSqlDatabaseAuditing** Cmdlet 會變更 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="b170b-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="b170b-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="b170b-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b170b-108">指定 *StorageAccountName* 參數，以指定審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="b170b-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="b170b-109">使用 *State* 參數來啟用/停用原則。</span><span class="sxs-lookup"><span data-stu-id="b170b-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="b170b-110">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="b170b-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="b170b-111">成功執行 Cmdlet 之後，就會啟用資料庫審核。</span><span class="sxs-lookup"><span data-stu-id="b170b-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="b170b-112">如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了資料庫識別碼之外，它還會傳回描述目前 blob 審核原則的物件。</span><span class="sxs-lookup"><span data-stu-id="b170b-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="b170b-113">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="b170b-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="b170b-114">示例</span><span class="sxs-lookup"><span data-stu-id="b170b-114">EXAMPLES</span></span>

### <span data-ttu-id="b170b-115">範例1：啟用 Azure SQL 資料庫的審核原則</span><span class="sxs-lookup"><span data-stu-id="b170b-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="b170b-116">範例2：停用 Azure SQL 資料庫的 blob 審核原則</span><span class="sxs-lookup"><span data-stu-id="b170b-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="b170b-117">參數</span><span class="sxs-lookup"><span data-stu-id="b170b-117">PARAMETERS</span></span>

### <span data-ttu-id="b170b-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="b170b-118">-AuditAction</span></span>
<span data-ttu-id="b170b-119">審計動作集合</span><span class="sxs-lookup"><span data-stu-id="b170b-119">The set of the audit actions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b170b-120">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="b170b-120">-AuditActionGroup</span></span>
<span data-ttu-id="b170b-121">審計動作群組集</span><span class="sxs-lookup"><span data-stu-id="b170b-121">The set of the audit action groups</span></span>

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

### <span data-ttu-id="b170b-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b170b-122">-DatabaseName</span></span>
<span data-ttu-id="b170b-123">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b170b-123">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b170b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b170b-124">-PassThru</span></span>
<span data-ttu-id="b170b-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="b170b-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b170b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b170b-126">-ResourceGroupName</span></span>
<span data-ttu-id="b170b-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b170b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="b170b-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b170b-128">-RetentionInDays</span></span>
<span data-ttu-id="b170b-129">審計記錄的保留天數</span><span class="sxs-lookup"><span data-stu-id="b170b-129">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="b170b-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b170b-130">-ServerName</span></span>
<span data-ttu-id="b170b-131">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b170b-131">SQL Database server name.</span></span>

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

### <span data-ttu-id="b170b-132">-State</span><span class="sxs-lookup"><span data-stu-id="b170b-132">-State</span></span>
<span data-ttu-id="b170b-133">審核原則的狀態</span><span class="sxs-lookup"><span data-stu-id="b170b-133">The state of the auditing policy</span></span>

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

### <span data-ttu-id="b170b-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b170b-134">-StorageAccountName</span></span>
<span data-ttu-id="b170b-135">儲存空間帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="b170b-135">The name of the storage account</span></span>

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

### <span data-ttu-id="b170b-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="b170b-136">-StorageKeyType</span></span>
<span data-ttu-id="b170b-137">儲存金鑰類型</span><span class="sxs-lookup"><span data-stu-id="b170b-137">The type of the storage key</span></span>

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

### <span data-ttu-id="b170b-138">-確認</span><span class="sxs-lookup"><span data-stu-id="b170b-138">-Confirm</span></span>
<span data-ttu-id="b170b-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b170b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b170b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b170b-140">-WhatIf</span></span>
<span data-ttu-id="b170b-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b170b-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b170b-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b170b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b170b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b170b-143">-DefaultProfile</span></span>
<span data-ttu-id="b170b-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b170b-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b170b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b170b-145">CommonParameters</span></span>
<span data-ttu-id="b170b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b170b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b170b-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b170b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b170b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="b170b-148">INPUTS</span></span>

## <span data-ttu-id="b170b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b170b-149">OUTPUTS</span></span>

### <span data-ttu-id="b170b-150">DatabaseBlobAuditingSettingsModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="b170b-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="b170b-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b170b-151">NOTES</span></span>

## <span data-ttu-id="b170b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b170b-152">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450771"
---
# <span data-ttu-id="c2389-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="c2389-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="c2389-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2389-102">SYNOPSIS</span></span>
<span data-ttu-id="c2389-103">變更 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="c2389-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2389-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2389-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2389-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2389-105">DESCRIPTION</span></span>
<span data-ttu-id="c2389-106">**AzureRmSqlServerAuditing** Cmdlet 會變更 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="c2389-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="c2389-107">若要使用 Cmdlet，請使用 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="c2389-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="c2389-108">指定 *StorageAccountName* 參數，以指定審核記錄的儲存空間帳戶，以及 *StorageKeyType* 參數以定義儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c2389-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="c2389-109">使用 *State* 參數來啟用/停用原則。</span><span class="sxs-lookup"><span data-stu-id="c2389-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="c2389-110">您也可以設定 *RetentionInDays* 參數的值，以定義審核記錄的期間，以定義審核記錄的保留。</span><span class="sxs-lookup"><span data-stu-id="c2389-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="c2389-111">成功執行 Cmdlet 之後，就會啟用在指定的 Azure SQL server 中定義的 Azure SQL 資料庫的審核。</span><span class="sxs-lookup"><span data-stu-id="c2389-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="c2389-112">如果 Cmdlet 成功且您使用 *PassThru* 參數，則除了伺服器識別碼之外，它還會傳回描述目前 blob 審核原則的物件。</span><span class="sxs-lookup"><span data-stu-id="c2389-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="c2389-113">伺服器識別碼包括但不限於、 **ResourceGroupName** 和 **ServerName** 。</span><span class="sxs-lookup"><span data-stu-id="c2389-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="c2389-114">示例</span><span class="sxs-lookup"><span data-stu-id="c2389-114">EXAMPLES</span></span>

### <span data-ttu-id="c2389-115">範例1：啟用 Azure SQL server 的審核原則</span><span class="sxs-lookup"><span data-stu-id="c2389-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="c2389-116">範例2：停用 Azure SQL server 的審核原則</span><span class="sxs-lookup"><span data-stu-id="c2389-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="c2389-117">參數</span><span class="sxs-lookup"><span data-stu-id="c2389-117">PARAMETERS</span></span>

### <span data-ttu-id="c2389-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="c2389-118">-AuditActionGroup</span></span>
<span data-ttu-id="c2389-119">審計動作群組集</span><span class="sxs-lookup"><span data-stu-id="c2389-119">The set of the audit action groups</span></span>

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

### <span data-ttu-id="c2389-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2389-120">-PassThru</span></span>
<span data-ttu-id="c2389-121">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="c2389-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c2389-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2389-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2389-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2389-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="c2389-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c2389-124">-RetentionInDays</span></span>
<span data-ttu-id="c2389-125">審計記錄的保留天數</span><span class="sxs-lookup"><span data-stu-id="c2389-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="c2389-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c2389-126">-ServerName</span></span>
<span data-ttu-id="c2389-127">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c2389-127">SQL server name.</span></span>

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

### <span data-ttu-id="c2389-128">-State</span><span class="sxs-lookup"><span data-stu-id="c2389-128">-State</span></span>
<span data-ttu-id="c2389-129">審核原則的狀態</span><span class="sxs-lookup"><span data-stu-id="c2389-129">The state of the auditing policy</span></span>

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

### <span data-ttu-id="c2389-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2389-130">-StorageAccountName</span></span>
<span data-ttu-id="c2389-131">儲存空間帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="c2389-131">The name of the storage account</span></span>

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

### <span data-ttu-id="c2389-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="c2389-132">-StorageKeyType</span></span>
<span data-ttu-id="c2389-133">儲存金鑰類型</span><span class="sxs-lookup"><span data-stu-id="c2389-133">The type of the storage key</span></span>

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

### <span data-ttu-id="c2389-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c2389-134">-Confirm</span></span>
<span data-ttu-id="c2389-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2389-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2389-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2389-136">-WhatIf</span></span>
<span data-ttu-id="c2389-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2389-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2389-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2389-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2389-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2389-139">-DefaultProfile</span></span>
<span data-ttu-id="c2389-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2389-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2389-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2389-141">CommonParameters</span></span>
<span data-ttu-id="c2389-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2389-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2389-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2389-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2389-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c2389-144">INPUTS</span></span>

## <span data-ttu-id="c2389-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c2389-145">OUTPUTS</span></span>

### <span data-ttu-id="c2389-146">ServerBlobAuditingSettingsModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="c2389-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="c2389-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c2389-147">NOTES</span></span>

## <span data-ttu-id="c2389-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2389-148">RELATED LINKS</span></span>


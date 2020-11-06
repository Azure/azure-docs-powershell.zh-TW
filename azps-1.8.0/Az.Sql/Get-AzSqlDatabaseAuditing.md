---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: ac1057159de6f3028bd599183dc5c411155f14e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620490"
---
# <span data-ttu-id="cd683-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="cd683-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="cd683-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd683-102">SYNOPSIS</span></span>
<span data-ttu-id="cd683-103">取得 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="cd683-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="cd683-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd683-104">SYNTAX</span></span>

### <span data-ttu-id="cd683-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cd683-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd683-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="cd683-106">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd683-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="cd683-107">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd683-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="cd683-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd683-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="cd683-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd683-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="cd683-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd683-111">說明</span><span class="sxs-lookup"><span data-stu-id="cd683-111">DESCRIPTION</span></span>
<span data-ttu-id="cd683-112">**AzSqlDatabaseAuditing** Cmdlet 會取得 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="cd683-112">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="cd683-113">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="cd683-113">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="cd683-114">審計記錄目的地是透過指定下列其中一個切換參數來決定： BlobStorage、LogAnalytics 或 EventHub (如果沒有指定，則預設值為 BlobStorage) 。</span><span class="sxs-lookup"><span data-stu-id="cd683-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="cd683-115">示例</span><span class="sxs-lookup"><span data-stu-id="cd683-115">EXAMPLES</span></span>

### <span data-ttu-id="cd683-116">範例1：取得 Azure SQL 資料庫的 blob 儲存審核設定</span><span class="sxs-lookup"><span data-stu-id="cd683-116">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="cd683-117">範例2：取得 Azure SQL 資料庫的 blob 儲存審核設定</span><span class="sxs-lookup"><span data-stu-id="cd683-117">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="cd683-118">範例3：透過管線取得 Azure SQL 資料庫的 blob 儲存審核設定</span><span class="sxs-lookup"><span data-stu-id="cd683-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="cd683-119">範例4：取得 Azure SQL 資料庫的事件中心審核設定</span><span class="sxs-lookup"><span data-stu-id="cd683-119">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="cd683-120">範例5：透過管線取得 Azure SQL 資料庫的事件中心審核設定</span><span class="sxs-lookup"><span data-stu-id="cd683-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="cd683-121">範例6：取得 Azure SQL 資料庫的 log analytics 審核設定</span><span class="sxs-lookup"><span data-stu-id="cd683-121">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="cd683-122">參數</span><span class="sxs-lookup"><span data-stu-id="cd683-122">PARAMETERS</span></span>

### <span data-ttu-id="cd683-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="cd683-123">-BlobStorage</span></span>
<span data-ttu-id="cd683-124">指定審核記錄目的地為 blob 儲存空間</span><span class="sxs-lookup"><span data-stu-id="cd683-124">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd683-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd683-125">-DatabaseName</span></span>
<span data-ttu-id="cd683-126">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="cd683-126">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd683-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd683-127">-DefaultProfile</span></span>
<span data-ttu-id="cd683-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd683-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd683-129">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cd683-129">-EventHub</span></span>
<span data-ttu-id="cd683-130">指定審核記錄目的地為事件中樞</span><span class="sxs-lookup"><span data-stu-id="cd683-130">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="cd683-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd683-131">-InputObject</span></span>
<span data-ttu-id="cd683-132">要管理其審核原則的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="cd683-132">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd683-133">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="cd683-133">-LogAnalytics</span></span>
<span data-ttu-id="cd683-134">指定審核記錄目的地為 log analytics</span><span class="sxs-lookup"><span data-stu-id="cd683-134">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="cd683-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd683-135">-ResourceGroupName</span></span>
<span data-ttu-id="cd683-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd683-136">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd683-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd683-137">-ServerName</span></span>
<span data-ttu-id="cd683-138">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="cd683-138">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd683-139">-確認</span><span class="sxs-lookup"><span data-stu-id="cd683-139">-Confirm</span></span>
<span data-ttu-id="cd683-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cd683-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd683-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd683-141">-WhatIf</span></span>
<span data-ttu-id="cd683-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd683-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd683-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd683-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd683-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd683-144">CommonParameters</span></span>
<span data-ttu-id="cd683-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd683-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd683-146">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cd683-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd683-147">輸入</span><span class="sxs-lookup"><span data-stu-id="cd683-147">INPUTS</span></span>

### <span data-ttu-id="cd683-148">System.object</span><span class="sxs-lookup"><span data-stu-id="cd683-148">System.String</span></span>

### <span data-ttu-id="cd683-149">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="cd683-149">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="cd683-150">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="cd683-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cd683-151">輸出</span><span class="sxs-lookup"><span data-stu-id="cd683-151">OUTPUTS</span></span>

### <span data-ttu-id="cd683-152">DatabaseBlobAuditingSettingsModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="cd683-152">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="cd683-153">筆記</span><span class="sxs-lookup"><span data-stu-id="cd683-153">NOTES</span></span>

## <span data-ttu-id="cd683-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd683-154">RELATED LINKS</span></span>

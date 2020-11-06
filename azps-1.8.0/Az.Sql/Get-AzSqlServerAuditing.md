---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: ba225571780d4d09dfd5ecc1b47132462468b734
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620397"
---
# <span data-ttu-id="fb9eb-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="fb9eb-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="fb9eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb9eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9eb-103">取得 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="fb9eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb9eb-104">SYNTAX</span></span>

### <span data-ttu-id="fb9eb-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fb9eb-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9eb-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="fb9eb-106">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9eb-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="fb9eb-107">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9eb-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="fb9eb-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9eb-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="fb9eb-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9eb-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="fb9eb-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb9eb-111">說明</span><span class="sxs-lookup"><span data-stu-id="fb9eb-111">DESCRIPTION</span></span>
<span data-ttu-id="fb9eb-112">**AzSqlServerAuditing** Cmdlet 會取得 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-112">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="fb9eb-113">指定 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-113">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="fb9eb-114">審計記錄目的地是透過指定下列其中一個切換參數來決定： BlobStorage、LogAnalytics 或 EventHub (如果沒有指定，則預設值為 BlobStorage) 。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="fb9eb-115">示例</span><span class="sxs-lookup"><span data-stu-id="fb9eb-115">EXAMPLES</span></span>

### <span data-ttu-id="fb9eb-116">範例1：取得 Azure SQL server 的 blob 儲存審核設定</span><span class="sxs-lookup"><span data-stu-id="fb9eb-116">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="fb9eb-117">範例2：取得 Azure SQL server 的 blob 儲存審核設定</span><span class="sxs-lookup"><span data-stu-id="fb9eb-117">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
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

### <span data-ttu-id="fb9eb-118">範例3：透過管線取得 Azure SQL server 的 blob 儲存審核設定</span><span class="sxs-lookup"><span data-stu-id="fb9eb-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
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

### <span data-ttu-id="fb9eb-119">範例4：取得 Azure SQL server 的事件中心審核設定</span><span class="sxs-lookup"><span data-stu-id="fb9eb-119">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="fb9eb-120">範例5：透過管線取得 Azure SQL server 的事件中心審核設定</span><span class="sxs-lookup"><span data-stu-id="fb9eb-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="fb9eb-121">範例6：取得 Azure SQL server 的 log analytics 審核設定</span><span class="sxs-lookup"><span data-stu-id="fb9eb-121">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="fb9eb-122">參數</span><span class="sxs-lookup"><span data-stu-id="fb9eb-122">PARAMETERS</span></span>

### <span data-ttu-id="fb9eb-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="fb9eb-123">-BlobStorage</span></span>
<span data-ttu-id="fb9eb-124">指定審核記錄目的地為 blob 儲存空間</span><span class="sxs-lookup"><span data-stu-id="fb9eb-124">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="fb9eb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9eb-125">-DefaultProfile</span></span>
<span data-ttu-id="fb9eb-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb9eb-127">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fb9eb-127">-EventHub</span></span>
<span data-ttu-id="fb9eb-128">指定審核記錄目的地為事件中樞</span><span class="sxs-lookup"><span data-stu-id="fb9eb-128">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="fb9eb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb9eb-129">-InputObject</span></span>
<span data-ttu-id="fb9eb-130">伺服器物件來管理其審核原則。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-130">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9eb-131">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="fb9eb-131">-LogAnalytics</span></span>
<span data-ttu-id="fb9eb-132">指定審核記錄目的地為 log analytics</span><span class="sxs-lookup"><span data-stu-id="fb9eb-132">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="fb9eb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb9eb-133">-ResourceGroupName</span></span>
<span data-ttu-id="fb9eb-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb9eb-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb9eb-135">-ServerName</span></span>
<span data-ttu-id="fb9eb-136">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-136">SQL server name.</span></span>

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

### <span data-ttu-id="fb9eb-137">-確認</span><span class="sxs-lookup"><span data-stu-id="fb9eb-137">-Confirm</span></span>
<span data-ttu-id="fb9eb-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb9eb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb9eb-139">-WhatIf</span></span>
<span data-ttu-id="fb9eb-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb9eb-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb9eb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9eb-142">CommonParameters</span></span>
<span data-ttu-id="fb9eb-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9eb-144">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9eb-145">輸入</span><span class="sxs-lookup"><span data-stu-id="fb9eb-145">INPUTS</span></span>

### <span data-ttu-id="fb9eb-146">System.object</span><span class="sxs-lookup"><span data-stu-id="fb9eb-146">System.String</span></span>

### <span data-ttu-id="fb9eb-147">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="fb9eb-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="fb9eb-148">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="fb9eb-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb9eb-149">輸出</span><span class="sxs-lookup"><span data-stu-id="fb9eb-149">OUTPUTS</span></span>

### <span data-ttu-id="fb9eb-150">ServerBlobAuditingSettingsModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="fb9eb-150">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="fb9eb-151">筆記</span><span class="sxs-lookup"><span data-stu-id="fb9eb-151">NOTES</span></span>

## <span data-ttu-id="fb9eb-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb9eb-152">RELATED LINKS</span></span>

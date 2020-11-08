---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138140"
---
# <span data-ttu-id="de75f-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="de75f-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="de75f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de75f-102">SYNOPSIS</span></span>
<span data-ttu-id="de75f-103">取得 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="de75f-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="de75f-104">句法</span><span class="sxs-lookup"><span data-stu-id="de75f-104">SYNTAX</span></span>

### <span data-ttu-id="de75f-105">DatabaseParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="de75f-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de75f-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de75f-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de75f-107">說明</span><span class="sxs-lookup"><span data-stu-id="de75f-107">DESCRIPTION</span></span>
<span data-ttu-id="de75f-108">**AzSqlDatabaseAudit** Cmdlet 會取得 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="de75f-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="de75f-109">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="de75f-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="de75f-110">示例</span><span class="sxs-lookup"><span data-stu-id="de75f-110">EXAMPLES</span></span>

### <span data-ttu-id="de75f-111">範例1：取得 Azure SQL 資料庫的審核設定</span><span class="sxs-lookup"><span data-stu-id="de75f-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="de75f-112">範例2：透過管線取得 Azure SQL 資料庫的審核設定</span><span class="sxs-lookup"><span data-stu-id="de75f-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="de75f-113">範例3：取得 Azure SQL 資料庫的審核設定</span><span class="sxs-lookup"><span data-stu-id="de75f-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="de75f-114">參數</span><span class="sxs-lookup"><span data-stu-id="de75f-114">PARAMETERS</span></span>

### <span data-ttu-id="de75f-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de75f-115">-DatabaseName</span></span>
<span data-ttu-id="de75f-116">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="de75f-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de75f-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="de75f-117">-DatabaseObject</span></span>
<span data-ttu-id="de75f-118">要管理其審核原則的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="de75f-118">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de75f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de75f-119">-DefaultProfile</span></span>
<span data-ttu-id="de75f-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de75f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de75f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de75f-121">-ResourceGroupName</span></span>
<span data-ttu-id="de75f-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de75f-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de75f-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="de75f-123">-ServerName</span></span>
<span data-ttu-id="de75f-124">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="de75f-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de75f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de75f-125">CommonParameters</span></span>
<span data-ttu-id="de75f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de75f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de75f-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="de75f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de75f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="de75f-128">INPUTS</span></span>

### <span data-ttu-id="de75f-129">System.object</span><span class="sxs-lookup"><span data-stu-id="de75f-129">System.String</span></span>

### <span data-ttu-id="de75f-130">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="de75f-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="de75f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="de75f-131">OUTPUTS</span></span>

### <span data-ttu-id="de75f-132">DatabaseAuditModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="de75f-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="de75f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="de75f-133">NOTES</span></span>

## <span data-ttu-id="de75f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="de75f-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 6b07ba5e31ab8e301d94b50170aca3869f9dea65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283376"
---
# <span data-ttu-id="e86c2-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e86c2-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="e86c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e86c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e86c2-103">取得 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="e86c2-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="e86c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="e86c2-104">SYNTAX</span></span>

### <span data-ttu-id="e86c2-105">ServerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e86c2-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e86c2-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e86c2-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e86c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="e86c2-107">DESCRIPTION</span></span>
<span data-ttu-id="e86c2-108">**AzSqlServerAudit** Cmdlet 會取得 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="e86c2-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="e86c2-109">指定 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="e86c2-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="e86c2-110">示例</span><span class="sxs-lookup"><span data-stu-id="e86c2-110">EXAMPLES</span></span>

### <span data-ttu-id="e86c2-111">範例1：取得 Azure SQL server 的審核設定</span><span class="sxs-lookup"><span data-stu-id="e86c2-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

### <span data-ttu-id="e86c2-112">範例2：透過管線取得 Azure SQL server 的審核設定</span><span class="sxs-lookup"><span data-stu-id="e86c2-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAudit
ServerName                          : server01
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

### <span data-ttu-id="e86c2-113">範例3：取得 Azure SQL server 的審核設定</span><span class="sxs-lookup"><span data-stu-id="e86c2-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

## <span data-ttu-id="e86c2-114">參數</span><span class="sxs-lookup"><span data-stu-id="e86c2-114">PARAMETERS</span></span>

### <span data-ttu-id="e86c2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e86c2-115">-AsJob</span></span>
<span data-ttu-id="e86c2-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e86c2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e86c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e86c2-117">-DefaultProfile</span></span>
<span data-ttu-id="e86c2-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e86c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e86c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e86c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="e86c2-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e86c2-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86c2-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e86c2-121">-ServerName</span></span>
<span data-ttu-id="e86c2-122">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="e86c2-122">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86c2-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="e86c2-123">-ServerObject</span></span>
<span data-ttu-id="e86c2-124">伺服器物件來管理其審核原則。</span><span class="sxs-lookup"><span data-stu-id="e86c2-124">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e86c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e86c2-125">CommonParameters</span></span>
<span data-ttu-id="e86c2-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e86c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e86c2-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e86c2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e86c2-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e86c2-128">INPUTS</span></span>

### <span data-ttu-id="e86c2-129">System.object</span><span class="sxs-lookup"><span data-stu-id="e86c2-129">System.String</span></span>

### <span data-ttu-id="e86c2-130">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="e86c2-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="e86c2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e86c2-131">OUTPUTS</span></span>

### <span data-ttu-id="e86c2-132">ServerAuditModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="e86c2-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="e86c2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e86c2-133">NOTES</span></span>

## <span data-ttu-id="e86c2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e86c2-134">RELATED LINKS</span></span>

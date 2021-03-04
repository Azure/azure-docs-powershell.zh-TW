---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 4c9311bfba05862b1c073be5ec5b07106d8b19a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909453"
---
# <span data-ttu-id="da813-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="da813-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="da813-102">簡介</span><span class="sxs-lookup"><span data-stu-id="da813-102">SYNOPSIS</span></span>
<span data-ttu-id="da813-103">獲得 Azure SQL 伺服器的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="da813-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="da813-104">語法</span><span class="sxs-lookup"><span data-stu-id="da813-104">SYNTAX</span></span>

### <span data-ttu-id="da813-105">ServerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="da813-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da813-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da813-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da813-107">描述</span><span class="sxs-lookup"><span data-stu-id="da813-107">DESCRIPTION</span></span>
<span data-ttu-id="da813-108">**Get-AzSqlServerAudit** Cmdlet 會取得 Azure SQL 伺服器的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="da813-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="da813-109">指定 *ResourceGroupName* 和 *ServerName* 參數以識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="da813-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="da813-110">例子</span><span class="sxs-lookup"><span data-stu-id="da813-110">EXAMPLES</span></span>

### <span data-ttu-id="da813-111">範例 1：取得 Azure SQL 伺服器的稽核設定</span><span class="sxs-lookup"><span data-stu-id="da813-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="da813-112">範例 2：透過管道取得 Azure SQL 伺服器的稽核設定</span><span class="sxs-lookup"><span data-stu-id="da813-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="da813-113">範例 3：取得 Azure SQL 伺服器的稽核設定</span><span class="sxs-lookup"><span data-stu-id="da813-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="da813-114">參數</span><span class="sxs-lookup"><span data-stu-id="da813-114">PARAMETERS</span></span>

### <span data-ttu-id="da813-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da813-115">-AsJob</span></span>
<span data-ttu-id="da813-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="da813-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da813-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da813-117">-DefaultProfile</span></span>
<span data-ttu-id="da813-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="da813-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da813-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da813-119">-ResourceGroupName</span></span>
<span data-ttu-id="da813-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="da813-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="da813-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da813-121">-ServerName</span></span>
<span data-ttu-id="da813-122">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="da813-122">SQL server name.</span></span>

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

### <span data-ttu-id="da813-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="da813-123">-ServerObject</span></span>
<span data-ttu-id="da813-124">管理其稽核策略的伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="da813-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="da813-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da813-125">CommonParameters</span></span>
<span data-ttu-id="da813-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="da813-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da813-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da813-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da813-128">輸入</span><span class="sxs-lookup"><span data-stu-id="da813-128">INPUTS</span></span>

### <span data-ttu-id="da813-129">System.String</span><span class="sxs-lookup"><span data-stu-id="da813-129">System.String</span></span>

### <span data-ttu-id="da813-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="da813-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="da813-131">輸出</span><span class="sxs-lookup"><span data-stu-id="da813-131">OUTPUTS</span></span>

### <span data-ttu-id="da813-132">Microsoft.Azure.Commands.sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="da813-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="da813-133">筆記</span><span class="sxs-lookup"><span data-stu-id="da813-133">NOTES</span></span>

## <span data-ttu-id="da813-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="da813-134">RELATED LINKS</span></span>

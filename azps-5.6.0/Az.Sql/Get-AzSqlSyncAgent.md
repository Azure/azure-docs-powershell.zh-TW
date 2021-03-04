---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 08248056ec98d79e00f2c606870e21af495310f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903761"
---
# <span data-ttu-id="f1d7d-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f1d7d-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="f1d7d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d7d-103">會返回有關 Azure SQL 同步處理代理程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="f1d7d-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1d7d-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1d7d-105">描述</span><span class="sxs-lookup"><span data-stu-id="f1d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="f1d7d-106">**Get-AzSqlSyncAgent Cmdlet** 會返回一或多個 Azure SQL 同步處理代理程式相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="f1d7d-107">指定同步代理程式的名稱，只查看該同步代理程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="f1d7d-108">例子</span><span class="sxs-lookup"><span data-stu-id="f1d7d-108">EXAMPLES</span></span>

### <span data-ttu-id="f1d7d-109">範例 1：取得指派給 Azure SQL Server 的 Azure SQL 同步處理代理程式的所有實例</span><span class="sxs-lookup"><span data-stu-id="f1d7d-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="f1d7d-110">此命令會獲得所有指派給 Azure SQL Server 的 Azure SQL 同步處理代理程式相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="f1d7d-111">範例 2：取得 Azure SQL 同步代理程式相關資訊</span><span class="sxs-lookup"><span data-stu-id="f1d7d-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="f1d7d-112">此命令會獲得名稱為「SyncAgent01」的 Azure SQL 資料庫同步處理代理程式相關資訊</span><span class="sxs-lookup"><span data-stu-id="f1d7d-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="f1d7d-113">範例 3：使用篩選將 Azure SQL 同步處理代理程式的所有實例指派給 Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f1d7d-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="f1d7d-114">此命令會獲得指派給以「SyncAgent」為開始之 Azure SQL Server 之所有 Azure SQL 同步處理代理程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="f1d7d-115">參數</span><span class="sxs-lookup"><span data-stu-id="f1d7d-115">PARAMETERS</span></span>

### <span data-ttu-id="f1d7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d7d-116">-DefaultProfile</span></span>
<span data-ttu-id="f1d7d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f1d7d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1d7d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1d7d-118">-Name</span></span>
<span data-ttu-id="f1d7d-119">同步代理程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d7d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d7d-120">-ResourceGroupName</span></span>
<span data-ttu-id="f1d7d-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1d7d-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1d7d-122">-ServerName</span></span>
<span data-ttu-id="f1d7d-123">同步處理代理程式位於 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f1d7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d7d-124">CommonParameters</span></span>
<span data-ttu-id="f1d7d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1d7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d7d-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1d7d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d7d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f1d7d-127">INPUTS</span></span>

### <span data-ttu-id="f1d7d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f1d7d-128">System.String</span></span>

## <span data-ttu-id="f1d7d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f1d7d-129">OUTPUTS</span></span>

### <span data-ttu-id="f1d7d-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="f1d7d-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="f1d7d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f1d7d-131">NOTES</span></span>

## <span data-ttu-id="f1d7d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1d7d-132">RELATED LINKS</span></span>

[<span data-ttu-id="f1d7d-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f1d7d-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="f1d7d-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f1d7d-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)


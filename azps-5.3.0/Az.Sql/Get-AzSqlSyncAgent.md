---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285667"
---
# <span data-ttu-id="a4d3e-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a4d3e-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="a4d3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d3e-103">傳回有關 Azure SQL 同步處理代理程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="a4d3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4d3e-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4d3e-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d3e-106">**AzSqlSyncAgent** Cmdlet 會傳回一或多個 Azure SQL 同步處理代理程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="a4d3e-107">指定同步處理常式的名稱，只查看該同步處理常式的資訊。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="a4d3e-108">示例</span><span class="sxs-lookup"><span data-stu-id="a4d3e-108">EXAMPLES</span></span>

### <span data-ttu-id="a4d3e-109">範例1：取得指派給 Azure SQL Server 的 Azure SQL 同步處理代理程式的所有實例</span><span class="sxs-lookup"><span data-stu-id="a4d3e-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="a4d3e-110">這個命令會取得指派給 Azure SQL Server 的所有 Azure SQL 同步處理代理程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="a4d3e-111">範例2：取得 Azure SQL 同步處理代理程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="a4d3e-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="a4d3e-112">這個命令會取得名為 "SyncAgent01" 的 Azure SQL 資料庫同步處理代理程式資訊</span><span class="sxs-lookup"><span data-stu-id="a4d3e-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="a4d3e-113">範例3：使用篩選來取得指派給 Azure SQL Server 的 Azure SQL 同步處理代理程式的所有實例</span><span class="sxs-lookup"><span data-stu-id="a4d3e-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="a4d3e-114">這個命令會取得指派給以 "SyncAgent" 開頭的 Azure SQL Server 的所有 Azure SQL 同步處理代理程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="a4d3e-115">參數</span><span class="sxs-lookup"><span data-stu-id="a4d3e-115">PARAMETERS</span></span>

### <span data-ttu-id="a4d3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d3e-116">-DefaultProfile</span></span>
<span data-ttu-id="a4d3e-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a4d3e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4d3e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4d3e-118">-Name</span></span>
<span data-ttu-id="a4d3e-119">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-119">The sync agent name.</span></span>

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

### <span data-ttu-id="a4d3e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d3e-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4d3e-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4d3e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4d3e-122">-ServerName</span></span>
<span data-ttu-id="a4d3e-123">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="a4d3e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d3e-124">CommonParameters</span></span>
<span data-ttu-id="a4d3e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d3e-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4d3e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d3e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a4d3e-127">INPUTS</span></span>

### <span data-ttu-id="a4d3e-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a4d3e-128">System.String</span></span>

## <span data-ttu-id="a4d3e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a4d3e-129">OUTPUTS</span></span>

### <span data-ttu-id="a4d3e-130">AzureSqlSyncAgentModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="a4d3e-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="a4d3e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a4d3e-131">NOTES</span></span>

## <span data-ttu-id="a4d3e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4d3e-132">RELATED LINKS</span></span>

[<span data-ttu-id="a4d3e-133">移除-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a4d3e-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="a4d3e-134">新-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a4d3e-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)


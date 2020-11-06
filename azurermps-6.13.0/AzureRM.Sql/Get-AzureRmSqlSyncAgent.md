---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 8b590e6ba8329ba6e0c45d30f7163c637d90f79e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448878"
---
# <span data-ttu-id="aca62-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="aca62-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="aca62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aca62-102">SYNOPSIS</span></span>
<span data-ttu-id="aca62-103">傳回有關 Azure SQL 同步處理代理程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="aca62-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aca62-104">句法</span><span class="sxs-lookup"><span data-stu-id="aca62-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aca62-105">說明</span><span class="sxs-lookup"><span data-stu-id="aca62-105">DESCRIPTION</span></span>
<span data-ttu-id="aca62-106">**AzureRmSqlSyncAgent** Cmdlet 會傳回一或多個 Azure SQL 同步處理代理程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aca62-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="aca62-107">指定同步處理常式的名稱，只查看該同步處理常式的資訊。</span><span class="sxs-lookup"><span data-stu-id="aca62-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="aca62-108">示例</span><span class="sxs-lookup"><span data-stu-id="aca62-108">EXAMPLES</span></span>

### <span data-ttu-id="aca62-109">範例1：取得指派給 Azure SQL Server 的 Azure SQL 同步處理代理程式的所有實例</span><span class="sxs-lookup"><span data-stu-id="aca62-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="aca62-110">這個命令會取得指派給 Azure SQL Server 的所有 Azure SQL 同步處理代理程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aca62-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="aca62-111">範例2：取得 Azure SQL 同步處理代理程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="aca62-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="aca62-112">這個命令會取得名為 "SyncAgent01" 的 Azure SQL 資料庫同步處理代理程式資訊</span><span class="sxs-lookup"><span data-stu-id="aca62-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="aca62-113">參數</span><span class="sxs-lookup"><span data-stu-id="aca62-113">PARAMETERS</span></span>

### <span data-ttu-id="aca62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca62-114">-DefaultProfile</span></span>
<span data-ttu-id="aca62-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="aca62-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aca62-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="aca62-116">-Name</span></span>
<span data-ttu-id="aca62-117">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="aca62-117">The sync agent name.</span></span>

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

### <span data-ttu-id="aca62-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca62-118">-ResourceGroupName</span></span>
<span data-ttu-id="aca62-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aca62-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="aca62-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aca62-120">-ServerName</span></span>
<span data-ttu-id="aca62-121">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="aca62-121">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="aca62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca62-122">CommonParameters</span></span>
<span data-ttu-id="aca62-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aca62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca62-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aca62-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca62-125">輸入</span><span class="sxs-lookup"><span data-stu-id="aca62-125">INPUTS</span></span>

### <span data-ttu-id="aca62-126">System.object</span><span class="sxs-lookup"><span data-stu-id="aca62-126">System.String</span></span>

## <span data-ttu-id="aca62-127">輸出</span><span class="sxs-lookup"><span data-stu-id="aca62-127">OUTPUTS</span></span>

### <span data-ttu-id="aca62-128">AzureSqlSyncAgentModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="aca62-128">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="aca62-129">筆記</span><span class="sxs-lookup"><span data-stu-id="aca62-129">NOTES</span></span>

## <span data-ttu-id="aca62-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="aca62-130">RELATED LINKS</span></span>

[<span data-ttu-id="aca62-131">移除-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="aca62-131">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="aca62-132">新-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="aca62-132">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)


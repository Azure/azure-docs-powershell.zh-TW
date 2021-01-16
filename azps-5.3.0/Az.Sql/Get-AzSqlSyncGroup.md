---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285647"
---
# <span data-ttu-id="4ecce-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4ecce-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="4ecce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ecce-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecce-103">傳回有關 Azure SQL 資料庫同步處理群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="4ecce-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="4ecce-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ecce-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ecce-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ecce-105">DESCRIPTION</span></span>
<span data-ttu-id="4ecce-106">**AzSqlSyncGroup** Cmdlet 會傳回一或多個 Azure SQL 資料庫同步處理群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4ecce-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="4ecce-107">指定同步群組的名稱，只查看該同步群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="4ecce-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="4ecce-108">示例</span><span class="sxs-lookup"><span data-stu-id="4ecce-108">EXAMPLES</span></span>

### <span data-ttu-id="4ecce-109">範例1：取得指派給 Azure SQL 資料庫之 Azure SQL 同步處理群組的所有實例</span><span class="sxs-lookup"><span data-stu-id="4ecce-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="4ecce-110">這個命令會取得指派給 Azure SQL 資料庫的所有 Azure SQL 資料庫同步處理群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4ecce-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="4ecce-111">範例2：取得 Azure SQL 資料庫同步處理群組的相關資訊</span><span class="sxs-lookup"><span data-stu-id="4ecce-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="4ecce-112">此命令會取得名為 "SyncGroup01" 的 Azure SQL 資料庫同步處理群組的相關資訊</span><span class="sxs-lookup"><span data-stu-id="4ecce-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="4ecce-113">範例3：使用篩選來取得指派給 Azure SQL Database 之 Azure SQL 同步處理群組的所有實例</span><span class="sxs-lookup"><span data-stu-id="4ecce-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="4ecce-114">此命令會取得指派給以 "SyncGroup" 開頭的 Azure SQL 資料庫的所有 Azure SQL 資料庫同步處理群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4ecce-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="4ecce-115">參數</span><span class="sxs-lookup"><span data-stu-id="4ecce-115">PARAMETERS</span></span>

### <span data-ttu-id="4ecce-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ecce-116">-DatabaseName</span></span>
<span data-ttu-id="4ecce-117">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ecce-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4ecce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecce-118">-DefaultProfile</span></span>
<span data-ttu-id="4ecce-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4ecce-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ecce-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ecce-120">-Name</span></span>
<span data-ttu-id="4ecce-121">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="4ecce-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ecce-122">-ResourceGroupName</span></span>
<span data-ttu-id="4ecce-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ecce-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ecce-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4ecce-124">-ServerName</span></span>
<span data-ttu-id="4ecce-125">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ecce-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4ecce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecce-126">CommonParameters</span></span>
<span data-ttu-id="4ecce-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ecce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecce-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ecce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecce-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4ecce-129">INPUTS</span></span>

### <span data-ttu-id="4ecce-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4ecce-130">System.String</span></span>

## <span data-ttu-id="4ecce-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4ecce-131">OUTPUTS</span></span>

### <span data-ttu-id="4ecce-132">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="4ecce-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4ecce-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4ecce-133">NOTES</span></span>

## <span data-ttu-id="4ecce-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ecce-134">RELATED LINKS</span></span>

[<span data-ttu-id="4ecce-135">新-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4ecce-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="4ecce-136">更新-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4ecce-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="4ecce-137">移除-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4ecce-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)


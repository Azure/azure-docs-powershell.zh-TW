---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: 3ce7abdb2feb053fe2731484fda0f301225c0b6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915778"
---
# <span data-ttu-id="740d3-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="740d3-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="740d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="740d3-102">SYNOPSIS</span></span>
<span data-ttu-id="740d3-103">會返回有關 Azure SQL 資料庫同步群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="740d3-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="740d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="740d3-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="740d3-105">描述</span><span class="sxs-lookup"><span data-stu-id="740d3-105">DESCRIPTION</span></span>
<span data-ttu-id="740d3-106">**Get-AzSqlSyncGroup** Cmdlet 會返回有關一或多個 Azure SQL 資料庫同步群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="740d3-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="740d3-107">指定同步組的名稱，只查看該同步組的資訊。</span><span class="sxs-lookup"><span data-stu-id="740d3-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="740d3-108">例子</span><span class="sxs-lookup"><span data-stu-id="740d3-108">EXAMPLES</span></span>

### <span data-ttu-id="740d3-109">範例 1：取得指派給 Azure SQL Database 的 Azure SQL 同步處理群組的所有實例</span><span class="sxs-lookup"><span data-stu-id="740d3-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="740d3-110">此命令會獲得所有指派給 Azure SQL Database 的 Azure SQL 資料庫同步群組相關資訊。</span><span class="sxs-lookup"><span data-stu-id="740d3-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="740d3-111">範例 2：取得 Azure SQL 資料庫同步組相關資訊</span><span class="sxs-lookup"><span data-stu-id="740d3-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="740d3-112">此命令會獲得名稱為「SyncGroup01」的 Azure SQL 資料庫同步處理群組相關資訊</span><span class="sxs-lookup"><span data-stu-id="740d3-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="740d3-113">範例 3：使用篩選將 Azure SQL 同步處理群組的所有實例指派給 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="740d3-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
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

<span data-ttu-id="740d3-114">此命令會獲得指派給以「同步處理群組」為開始之 Azure SQL 資料庫之所有 Azure SQL 資料庫同步處理群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="740d3-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="740d3-115">參數</span><span class="sxs-lookup"><span data-stu-id="740d3-115">PARAMETERS</span></span>

### <span data-ttu-id="740d3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="740d3-116">-DatabaseName</span></span>
<span data-ttu-id="740d3-117">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="740d3-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="740d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="740d3-118">-DefaultProfile</span></span>
<span data-ttu-id="740d3-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="740d3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="740d3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="740d3-120">-Name</span></span>
<span data-ttu-id="740d3-121">同步組名。</span><span class="sxs-lookup"><span data-stu-id="740d3-121">The sync group name.</span></span>

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

### <span data-ttu-id="740d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="740d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="740d3-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="740d3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="740d3-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="740d3-124">-ServerName</span></span>
<span data-ttu-id="740d3-125">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="740d3-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="740d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="740d3-126">CommonParameters</span></span>
<span data-ttu-id="740d3-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="740d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="740d3-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="740d3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="740d3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="740d3-129">INPUTS</span></span>

### <span data-ttu-id="740d3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="740d3-130">System.String</span></span>

## <span data-ttu-id="740d3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="740d3-131">OUTPUTS</span></span>

### <span data-ttu-id="740d3-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="740d3-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="740d3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="740d3-133">NOTES</span></span>

## <span data-ttu-id="740d3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="740d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="740d3-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="740d3-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="740d3-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="740d3-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="740d3-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="740d3-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)


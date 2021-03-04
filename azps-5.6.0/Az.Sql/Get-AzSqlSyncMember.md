---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: c9c3aff7d449c12cd3514518fc68d8ca50dbec0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914253"
---
# <span data-ttu-id="67098-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="67098-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="67098-102">簡介</span><span class="sxs-lookup"><span data-stu-id="67098-102">SYNOPSIS</span></span>
<span data-ttu-id="67098-103">會返回有關 Azure SQL 資料庫同步成員的資訊。</span><span class="sxs-lookup"><span data-stu-id="67098-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="67098-104">語法</span><span class="sxs-lookup"><span data-stu-id="67098-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67098-105">描述</span><span class="sxs-lookup"><span data-stu-id="67098-105">DESCRIPTION</span></span>
<span data-ttu-id="67098-106">**Get-AzSqlSyncMember Cmdlet** 會返回有關一或多個 Azure SQL 資料庫同步成員的資訊。</span><span class="sxs-lookup"><span data-stu-id="67098-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="67098-107">指定同步成員的名稱，只查看該同步成員的資訊。</span><span class="sxs-lookup"><span data-stu-id="67098-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="67098-108">例子</span><span class="sxs-lookup"><span data-stu-id="67098-108">EXAMPLES</span></span>

### <span data-ttu-id="67098-109">範例 1：取得指派給同步處理群組之 Azure SQL 同步處理成員的所有實例</span><span class="sxs-lookup"><span data-stu-id="67098-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="67098-110">此命令會獲得所有指派給同步群組 SyncGroup01 的 Azure SQL 資料庫同步成員相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67098-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="67098-111">範例 2：取得 Azure SQL 資料庫同步成員相關資訊</span><span class="sxs-lookup"><span data-stu-id="67098-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="67098-112">此命令會獲得名稱為「SyncMember01」的 Azure SQL 資料庫同步處理成員相關資訊</span><span class="sxs-lookup"><span data-stu-id="67098-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="67098-113">範例 3：使用篩選將 Azure SQL 同步處理成員的所有實例指派給同步處理群組</span><span class="sxs-lookup"><span data-stu-id="67098-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="67098-114">此命令會獲得所有指派給同步處理群組 SyncGroup01 的 Azure SQL 資料庫同步處理成員相關資訊，該群組以「SyncMember」為開始。</span><span class="sxs-lookup"><span data-stu-id="67098-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="67098-115">參數</span><span class="sxs-lookup"><span data-stu-id="67098-115">PARAMETERS</span></span>

### <span data-ttu-id="67098-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67098-116">-DatabaseName</span></span>
<span data-ttu-id="67098-117">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="67098-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="67098-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67098-118">-DefaultProfile</span></span>
<span data-ttu-id="67098-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="67098-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67098-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="67098-120">-Name</span></span>
<span data-ttu-id="67098-121">同步成員名稱。</span><span class="sxs-lookup"><span data-stu-id="67098-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67098-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67098-122">-ResourceGroupName</span></span>
<span data-ttu-id="67098-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67098-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="67098-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67098-124">-ServerName</span></span>
<span data-ttu-id="67098-125">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="67098-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="67098-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="67098-126">-SyncGroupName</span></span>
<span data-ttu-id="67098-127">同步組名。</span><span class="sxs-lookup"><span data-stu-id="67098-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67098-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67098-128">CommonParameters</span></span>
<span data-ttu-id="67098-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="67098-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67098-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67098-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67098-131">輸入</span><span class="sxs-lookup"><span data-stu-id="67098-131">INPUTS</span></span>

### <span data-ttu-id="67098-132">System.String</span><span class="sxs-lookup"><span data-stu-id="67098-132">System.String</span></span>

## <span data-ttu-id="67098-133">輸出</span><span class="sxs-lookup"><span data-stu-id="67098-133">OUTPUTS</span></span>

### <span data-ttu-id="67098-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="67098-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="67098-135">筆記</span><span class="sxs-lookup"><span data-stu-id="67098-135">NOTES</span></span>

## <span data-ttu-id="67098-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="67098-136">RELATED LINKS</span></span>

[<span data-ttu-id="67098-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="67098-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="67098-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="67098-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="67098-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="67098-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)


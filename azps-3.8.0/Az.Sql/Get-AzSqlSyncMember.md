---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956707"
---
# <span data-ttu-id="31d95-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="31d95-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="31d95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31d95-102">SYNOPSIS</span></span>
<span data-ttu-id="31d95-103">傳回有關 Azure SQL 資料庫同步處理成員的資訊。</span><span class="sxs-lookup"><span data-stu-id="31d95-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="31d95-104">句法</span><span class="sxs-lookup"><span data-stu-id="31d95-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31d95-105">說明</span><span class="sxs-lookup"><span data-stu-id="31d95-105">DESCRIPTION</span></span>
<span data-ttu-id="31d95-106">**AzSqlSyncMember** Cmdlet 會傳回一或多個 Azure SQL 資料庫同步處理成員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31d95-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="31d95-107">指定同步處理成員的名稱，只查看該同步處理成員的資訊。</span><span class="sxs-lookup"><span data-stu-id="31d95-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="31d95-108">示例</span><span class="sxs-lookup"><span data-stu-id="31d95-108">EXAMPLES</span></span>

### <span data-ttu-id="31d95-109">範例1：取得指派給同步處理群組之 Azure SQL 同步處理成員的所有實例</span><span class="sxs-lookup"><span data-stu-id="31d95-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="31d95-110">這個命令會取得指派給同步處理群組 SyncGroup01 的所有 Azure SQL 資料庫同步處理成員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31d95-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="31d95-111">範例2：取得 Azure SQL 資料庫同步處理成員的相關資訊</span><span class="sxs-lookup"><span data-stu-id="31d95-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="31d95-112">此命令會取得名為 "SyncMember01" 的 Azure SQL 資料庫同步處理成員相關資訊</span><span class="sxs-lookup"><span data-stu-id="31d95-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="31d95-113">範例3：使用篩選取得指派給同步群組的所有 Azure SQL 同步處理成員實例</span><span class="sxs-lookup"><span data-stu-id="31d95-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="31d95-114">這個命令會取得指派給以「SyncMember」開頭的同步處理群組 SyncGroup01 的所有 Azure SQL 資料庫同步處理成員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31d95-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="31d95-115">參數</span><span class="sxs-lookup"><span data-stu-id="31d95-115">PARAMETERS</span></span>

### <span data-ttu-id="31d95-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31d95-116">-DatabaseName</span></span>
<span data-ttu-id="31d95-117">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="31d95-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="31d95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d95-118">-DefaultProfile</span></span>
<span data-ttu-id="31d95-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="31d95-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31d95-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="31d95-120">-Name</span></span>
<span data-ttu-id="31d95-121">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="31d95-121">The sync member name.</span></span>

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

### <span data-ttu-id="31d95-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31d95-122">-ResourceGroupName</span></span>
<span data-ttu-id="31d95-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31d95-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="31d95-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31d95-124">-ServerName</span></span>
<span data-ttu-id="31d95-125">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="31d95-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="31d95-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="31d95-126">-SyncGroupName</span></span>
<span data-ttu-id="31d95-127">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="31d95-127">The sync group name.</span></span>

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

### <span data-ttu-id="31d95-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d95-128">CommonParameters</span></span>
<span data-ttu-id="31d95-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31d95-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d95-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="31d95-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d95-131">輸入</span><span class="sxs-lookup"><span data-stu-id="31d95-131">INPUTS</span></span>

### <span data-ttu-id="31d95-132">System.object</span><span class="sxs-lookup"><span data-stu-id="31d95-132">System.String</span></span>

## <span data-ttu-id="31d95-133">輸出</span><span class="sxs-lookup"><span data-stu-id="31d95-133">OUTPUTS</span></span>

### <span data-ttu-id="31d95-134">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="31d95-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="31d95-135">筆記</span><span class="sxs-lookup"><span data-stu-id="31d95-135">NOTES</span></span>

## <span data-ttu-id="31d95-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="31d95-136">RELATED LINKS</span></span>

[<span data-ttu-id="31d95-137">新-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="31d95-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="31d95-138">更新-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="31d95-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="31d95-139">移除-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="31d95-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)


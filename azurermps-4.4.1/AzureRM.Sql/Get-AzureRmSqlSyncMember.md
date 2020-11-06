---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: bd828a88b870174b870d3acb963cdcb3b3c58ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446635"
---
# <span data-ttu-id="490a9-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="490a9-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="490a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="490a9-102">SYNOPSIS</span></span>
<span data-ttu-id="490a9-103">傳回有關 Azure SQL 資料庫同步處理成員的資訊。</span><span class="sxs-lookup"><span data-stu-id="490a9-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="490a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="490a9-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="490a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="490a9-105">DESCRIPTION</span></span>
<span data-ttu-id="490a9-106">**AzureRmSqlSyncMember** Cmdlet 會傳回一或多個 Azure SQL 資料庫同步處理成員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="490a9-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="490a9-107">指定同步處理成員的名稱，只查看該同步處理成員的資訊。</span><span class="sxs-lookup"><span data-stu-id="490a9-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="490a9-108">示例</span><span class="sxs-lookup"><span data-stu-id="490a9-108">EXAMPLES</span></span>

### <span data-ttu-id="490a9-109">範例1：取得指派給同步處理群組之 Azure SQL 同步處理成員的所有實例</span><span class="sxs-lookup"><span data-stu-id="490a9-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="490a9-110">這個命令會取得指派給同步處理群組 SyncGroup01 的所有 Azure SQL 資料庫同步處理成員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="490a9-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="490a9-111">範例2：取得 Azure SQL 資料庫同步處理成員的相關資訊</span><span class="sxs-lookup"><span data-stu-id="490a9-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="490a9-112">此命令會取得名為 "SyncMember01" 的 Azure SQL 資料庫同步處理成員相關資訊</span><span class="sxs-lookup"><span data-stu-id="490a9-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="490a9-113">參數</span><span class="sxs-lookup"><span data-stu-id="490a9-113">PARAMETERS</span></span>

### <span data-ttu-id="490a9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="490a9-114">-DatabaseName</span></span>
<span data-ttu-id="490a9-115">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="490a9-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="490a9-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="490a9-116">-Name</span></span>
<span data-ttu-id="490a9-117">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="490a9-117">The sync member name.</span></span>

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

### <span data-ttu-id="490a9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="490a9-118">-ResourceGroupName</span></span>
<span data-ttu-id="490a9-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="490a9-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="490a9-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="490a9-120">-ServerName</span></span>
<span data-ttu-id="490a9-121">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="490a9-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="490a9-122">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="490a9-122">-SyncGroupName</span></span>
<span data-ttu-id="490a9-123">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="490a9-123">The sync group name.</span></span>

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

### <span data-ttu-id="490a9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490a9-124">-DefaultProfile</span></span>
<span data-ttu-id="490a9-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="490a9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="490a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490a9-126">CommonParameters</span></span>
<span data-ttu-id="490a9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="490a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490a9-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="490a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490a9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="490a9-129">INPUTS</span></span>

## <span data-ttu-id="490a9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="490a9-130">OUTPUTS</span></span>

### <span data-ttu-id="490a9-131">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="490a9-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="490a9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="490a9-132">NOTES</span></span>

## <span data-ttu-id="490a9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="490a9-133">RELATED LINKS</span></span>

[<span data-ttu-id="490a9-134">新-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="490a9-134">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="490a9-135">更新-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="490a9-135">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="490a9-136">移除-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="490a9-136">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)


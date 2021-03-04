---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 3c4b50a4d4f4c01365d853e64cb3a53ea9c05d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912269"
---
# <span data-ttu-id="e3351-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e3351-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="e3351-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3351-102">SYNOPSIS</span></span>
<span data-ttu-id="e3351-103">更新 Azure SQL 資料庫同步成員。</span><span class="sxs-lookup"><span data-stu-id="e3351-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e3351-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3351-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3351-105">描述</span><span class="sxs-lookup"><span data-stu-id="e3351-105">DESCRIPTION</span></span>
<span data-ttu-id="e3351-106">**Update-AzSqlSyncGroup** Cmdlet 會修改 Azure SQL 資料庫同步成員的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3351-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e3351-107">例子</span><span class="sxs-lookup"><span data-stu-id="e3351-107">EXAMPLES</span></span>

### <span data-ttu-id="e3351-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e3351-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
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
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="e3351-109">此命令會重設成員資料庫的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="e3351-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="e3351-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3351-110">PARAMETERS</span></span>

### <span data-ttu-id="e3351-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3351-111">-DatabaseName</span></span>
<span data-ttu-id="e3351-112">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3351-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e3351-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3351-113">-DefaultProfile</span></span>
<span data-ttu-id="e3351-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e3351-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3351-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="e3351-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="e3351-116">Azure SQL database (使用者) 密碼的認證。</span><span class="sxs-lookup"><span data-stu-id="e3351-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3351-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3351-117">-Name</span></span>
<span data-ttu-id="e3351-118">同步成員名稱。</span><span class="sxs-lookup"><span data-stu-id="e3351-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3351-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3351-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3351-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3351-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3351-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e3351-121">-ServerName</span></span>
<span data-ttu-id="e3351-122">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3351-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e3351-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e3351-123">-SyncGroupName</span></span>
<span data-ttu-id="e3351-124">同步組名。</span><span class="sxs-lookup"><span data-stu-id="e3351-124">The sync group name.</span></span>

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

### <span data-ttu-id="e3351-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="e3351-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="e3351-126">同步處理成員資料庫的資源識別碼，用於 UsePrivateLinkConnection 設為 True 時。</span><span class="sxs-lookup"><span data-stu-id="e3351-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3351-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e3351-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="e3351-128">是否要在連結至此同步成員時使用私人連結。</span><span class="sxs-lookup"><span data-stu-id="e3351-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3351-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e3351-129">-Confirm</span></span>
<span data-ttu-id="e3351-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e3351-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3351-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3351-131">-WhatIf</span></span>
<span data-ttu-id="e3351-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3351-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3351-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3351-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3351-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3351-134">CommonParameters</span></span>
<span data-ttu-id="e3351-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3351-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3351-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3351-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3351-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e3351-137">INPUTS</span></span>

### <span data-ttu-id="e3351-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e3351-138">System.String</span></span>

## <span data-ttu-id="e3351-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e3351-139">OUTPUTS</span></span>

### <span data-ttu-id="e3351-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="e3351-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="e3351-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e3351-141">NOTES</span></span>

## <span data-ttu-id="e3351-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3351-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3351-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e3351-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="e3351-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e3351-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="e3351-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e3351-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)


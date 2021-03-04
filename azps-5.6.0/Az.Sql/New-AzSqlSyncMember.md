---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: c26cb74f1d9f9c30e63bb39ec7668216a5f3a297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904278"
---
# <span data-ttu-id="c37e1-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c37e1-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="c37e1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c37e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c37e1-103">建立 Azure SQL 資料庫同步成員。</span><span class="sxs-lookup"><span data-stu-id="c37e1-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c37e1-104">語法</span><span class="sxs-lookup"><span data-stu-id="c37e1-104">SYNTAX</span></span>

### <span data-ttu-id="c37e1-105">AzureSqlDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="c37e1-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c37e1-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="c37e1-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c37e1-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="c37e1-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c37e1-108">描述</span><span class="sxs-lookup"><span data-stu-id="c37e1-108">DESCRIPTION</span></span>
<span data-ttu-id="c37e1-109">**New-AzSqlSyncMember** Cmdlet 會建立 Azure SQL 資料庫同步成員。</span><span class="sxs-lookup"><span data-stu-id="c37e1-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c37e1-110">例子</span><span class="sxs-lookup"><span data-stu-id="c37e1-110">EXAMPLES</span></span>

### <span data-ttu-id="c37e1-111">範例 1：建立 Azure SQL 資料庫的同步成員。</span><span class="sxs-lookup"><span data-stu-id="c37e1-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
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
SyncState                   : UnProvisioned
```

<span data-ttu-id="c37e1-112">此命令會為 Azure SQL 資料庫建立同步成員。</span><span class="sxs-lookup"><span data-stu-id="c37e1-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="c37e1-113">範例 2：為內部部署 SQL Server 資料庫建立同步處理成員</span><span class="sxs-lookup"><span data-stu-id="c37e1-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="c37e1-114">此命令會為內部部署 SQL 資料庫建立同步成員。</span><span class="sxs-lookup"><span data-stu-id="c37e1-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="c37e1-115">參數</span><span class="sxs-lookup"><span data-stu-id="c37e1-115">PARAMETERS</span></span>

### <span data-ttu-id="c37e1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c37e1-116">-DatabaseName</span></span>
<span data-ttu-id="c37e1-117">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c37e1-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="c37e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37e1-118">-DefaultProfile</span></span>
<span data-ttu-id="c37e1-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c37e1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c37e1-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="c37e1-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="c37e1-121">Azure SQL database (使用者) 密碼的認證。</span><span class="sxs-lookup"><span data-stu-id="c37e1-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c37e1-122">-MemberDatabaseName</span></span>
<span data-ttu-id="c37e1-123">成員資料庫的 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c37e1-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="c37e1-124">-MemberDatabaseType</span></span>
<span data-ttu-id="c37e1-125">成員資料庫的資料庫類型。</span><span class="sxs-lookup"><span data-stu-id="c37e1-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="c37e1-126">-MemberServerName</span></span>
<span data-ttu-id="c37e1-127">成員資料庫的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c37e1-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="c37e1-128">-Name</span></span>
<span data-ttu-id="c37e1-129">同步成員名稱。</span><span class="sxs-lookup"><span data-stu-id="c37e1-129">The sync member name.</span></span>

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

### <span data-ttu-id="c37e1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c37e1-130">-ResourceGroupName</span></span>
<span data-ttu-id="c37e1-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c37e1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="c37e1-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c37e1-132">-ServerName</span></span>
<span data-ttu-id="c37e1-133">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c37e1-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c37e1-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="c37e1-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="c37e1-135">同步處理代理程式所連接的 SQL 伺服器資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="c37e1-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="c37e1-136">-SyncAgentName</span></span>
<span data-ttu-id="c37e1-137">同步代理程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="c37e1-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c37e1-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="c37e1-139">同步代理程式位於下的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c37e1-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="c37e1-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="c37e1-141">同步代理程式的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c37e1-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="c37e1-142">-SyncAgentServerName</span></span>
<span data-ttu-id="c37e1-143">同步處理代理程式位於下的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c37e1-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-144">-同步目錄</span><span class="sxs-lookup"><span data-stu-id="c37e1-144">-SyncDirection</span></span>
<span data-ttu-id="c37e1-145">此同步成員之同步方向。</span><span class="sxs-lookup"><span data-stu-id="c37e1-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37e1-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c37e1-146">-SyncGroupName</span></span>
<span data-ttu-id="c37e1-147">同步組名。</span><span class="sxs-lookup"><span data-stu-id="c37e1-147">The sync group name.</span></span>

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

### <span data-ttu-id="c37e1-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="c37e1-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="c37e1-149">同步處理成員資料庫的資源識別碼，用於 UsePrivateLinkConnection 設為 True 時。</span><span class="sxs-lookup"><span data-stu-id="c37e1-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="c37e1-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c37e1-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="c37e1-151">當您連接到此同步成員時，請使用私人連結連接。</span><span class="sxs-lookup"><span data-stu-id="c37e1-151">Use a private link connection when connecting to this sync member.</span></span>

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

### <span data-ttu-id="c37e1-152">-確認</span><span class="sxs-lookup"><span data-stu-id="c37e1-152">-Confirm</span></span>
<span data-ttu-id="c37e1-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c37e1-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c37e1-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c37e1-154">-WhatIf</span></span>
<span data-ttu-id="c37e1-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c37e1-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c37e1-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c37e1-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c37e1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37e1-157">CommonParameters</span></span>
<span data-ttu-id="c37e1-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c37e1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37e1-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c37e1-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37e1-160">輸入</span><span class="sxs-lookup"><span data-stu-id="c37e1-160">INPUTS</span></span>

### <span data-ttu-id="c37e1-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c37e1-161">System.String</span></span>

## <span data-ttu-id="c37e1-162">輸出</span><span class="sxs-lookup"><span data-stu-id="c37e1-162">OUTPUTS</span></span>

### <span data-ttu-id="c37e1-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="c37e1-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="c37e1-164">筆記</span><span class="sxs-lookup"><span data-stu-id="c37e1-164">NOTES</span></span>

## <span data-ttu-id="c37e1-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="c37e1-165">RELATED LINKS</span></span>

[<span data-ttu-id="c37e1-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c37e1-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="c37e1-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c37e1-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="c37e1-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c37e1-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)


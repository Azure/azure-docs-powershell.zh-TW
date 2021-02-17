---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 793962db73fd053764a794b64bea8e68edadd73b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413246"
---
# <span data-ttu-id="d1808-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1808-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="d1808-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1808-102">SYNOPSIS</span></span>
<span data-ttu-id="d1808-103">建立 Azure SQL 資料庫同步成員。</span><span class="sxs-lookup"><span data-stu-id="d1808-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d1808-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1808-104">SYNTAX</span></span>

### <span data-ttu-id="d1808-105">AzureSqlDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="d1808-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1808-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="d1808-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1808-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="d1808-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1808-108">描述</span><span class="sxs-lookup"><span data-stu-id="d1808-108">DESCRIPTION</span></span>
<span data-ttu-id="d1808-109">**New-AzSqlSyncMember** Cmdlet 會建立 Azure SQL 資料庫同步成員。</span><span class="sxs-lookup"><span data-stu-id="d1808-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d1808-110">例子</span><span class="sxs-lookup"><span data-stu-id="d1808-110">EXAMPLES</span></span>

### <span data-ttu-id="d1808-111">範例 1：建立 Azure SQL 資料庫的同步成員。</span><span class="sxs-lookup"><span data-stu-id="d1808-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="d1808-112">此命令會為 Azure SQL 資料庫建立同步成員。</span><span class="sxs-lookup"><span data-stu-id="d1808-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="d1808-113">範例 2：為內部部署 SQL Server 資料庫建立同步處理成員</span><span class="sxs-lookup"><span data-stu-id="d1808-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="d1808-114">此命令會為內部部署 SQL 資料庫建立同步成員。</span><span class="sxs-lookup"><span data-stu-id="d1808-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="d1808-115">參數</span><span class="sxs-lookup"><span data-stu-id="d1808-115">PARAMETERS</span></span>

### <span data-ttu-id="d1808-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1808-116">-DatabaseName</span></span>
<span data-ttu-id="d1808-117">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1808-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d1808-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1808-118">-DefaultProfile</span></span>
<span data-ttu-id="d1808-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d1808-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1808-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="d1808-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="d1808-121">Azure SQL database (使用者) 密碼的認證。</span><span class="sxs-lookup"><span data-stu-id="d1808-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d1808-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1808-122">-MemberDatabaseName</span></span>
<span data-ttu-id="d1808-123">成員資料庫的 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d1808-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="d1808-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="d1808-124">-MemberDatabaseType</span></span>
<span data-ttu-id="d1808-125">成員資料庫的資料庫類型。</span><span class="sxs-lookup"><span data-stu-id="d1808-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="d1808-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="d1808-126">-MemberServerName</span></span>
<span data-ttu-id="d1808-127">成員資料庫的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="d1808-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="d1808-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1808-128">-Name</span></span>
<span data-ttu-id="d1808-129">同步成員名稱。</span><span class="sxs-lookup"><span data-stu-id="d1808-129">The sync member name.</span></span>

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

### <span data-ttu-id="d1808-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1808-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1808-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1808-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1808-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1808-132">-ServerName</span></span>
<span data-ttu-id="d1808-133">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1808-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d1808-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="d1808-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="d1808-135">由同步處理代理程式連接的 SQL 伺服器資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1808-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="d1808-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="d1808-136">-SyncAgentName</span></span>
<span data-ttu-id="d1808-137">同步代理程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1808-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="d1808-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1808-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="d1808-139">同步代理程式位於下的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d1808-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="d1808-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="d1808-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="d1808-141">同步代理程式的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1808-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="d1808-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="d1808-142">-SyncAgentServerName</span></span>
<span data-ttu-id="d1808-143">同步處理代理程式位於下的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="d1808-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="d1808-144">-同步目錄</span><span class="sxs-lookup"><span data-stu-id="d1808-144">-SyncDirection</span></span>
<span data-ttu-id="d1808-145">此同步成員之同步方向。</span><span class="sxs-lookup"><span data-stu-id="d1808-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="d1808-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d1808-146">-SyncGroupName</span></span>
<span data-ttu-id="d1808-147">同步組名。</span><span class="sxs-lookup"><span data-stu-id="d1808-147">The sync group name.</span></span>

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

### <span data-ttu-id="d1808-148">-確認</span><span class="sxs-lookup"><span data-stu-id="d1808-148">-Confirm</span></span>
<span data-ttu-id="d1808-149">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1808-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1808-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1808-150">-WhatIf</span></span>
<span data-ttu-id="d1808-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1808-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1808-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1808-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1808-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1808-153">CommonParameters</span></span>
<span data-ttu-id="d1808-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1808-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1808-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1808-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1808-156">輸入</span><span class="sxs-lookup"><span data-stu-id="d1808-156">INPUTS</span></span>

### <span data-ttu-id="d1808-157">System.String</span><span class="sxs-lookup"><span data-stu-id="d1808-157">System.String</span></span>

## <span data-ttu-id="d1808-158">輸出</span><span class="sxs-lookup"><span data-stu-id="d1808-158">OUTPUTS</span></span>

### <span data-ttu-id="d1808-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="d1808-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d1808-160">筆記</span><span class="sxs-lookup"><span data-stu-id="d1808-160">NOTES</span></span>

## <span data-ttu-id="d1808-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1808-161">RELATED LINKS</span></span>

[<span data-ttu-id="d1808-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1808-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


[<span data-ttu-id="d1808-163">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1808-163">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)


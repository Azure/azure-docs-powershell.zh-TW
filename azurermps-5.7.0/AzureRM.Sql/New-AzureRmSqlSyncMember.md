---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: d2df78cc4cbf7bea7918653e310193bf013d7495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450434"
---
# <span data-ttu-id="d9ea0-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9ea0-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="d9ea0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ea0-103">建立 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9ea0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9ea0-104">SYNTAX</span></span>

### <span data-ttu-id="d9ea0-105">AzureSqlDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="d9ea0-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ea0-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="d9ea0-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ea0-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="d9ea0-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ea0-108">說明</span><span class="sxs-lookup"><span data-stu-id="d9ea0-108">DESCRIPTION</span></span>
<span data-ttu-id="d9ea0-109">**新的-AzureRmSqlSyncMember** Cmdlet 會建立 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d9ea0-110">示例</span><span class="sxs-lookup"><span data-stu-id="d9ea0-110">EXAMPLES</span></span>

### <span data-ttu-id="d9ea0-111">範例1：建立 Azure SQL 資料庫的同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="d9ea0-112">這個命令會建立 Azure SQL 資料庫的同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="d9ea0-113">範例2：建立內部部署 SQL Server 資料庫的同步成員</span><span class="sxs-lookup"><span data-stu-id="d9ea0-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="d9ea0-114">這個命令會建立內部部署 SQL 資料庫的同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="d9ea0-115">參數</span><span class="sxs-lookup"><span data-stu-id="d9ea0-115">PARAMETERS</span></span>

### <span data-ttu-id="d9ea0-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-116">-DatabaseName</span></span>
<span data-ttu-id="d9ea0-117">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ea0-118">-DefaultProfile</span></span>
<span data-ttu-id="d9ea0-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d9ea0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="d9ea0-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="d9ea0-121">認證 (Azure SQL 資料庫的使用者名稱和密碼) 。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-122">-MemberDatabaseName</span></span>
<span data-ttu-id="d9ea0-123">成員資料庫的 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="d9ea0-124">-MemberDatabaseType</span></span>
<span data-ttu-id="d9ea0-125">成員資料庫的資料庫類型。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-125">The database type of the member database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-126">-MemberServerName</span></span>
<span data-ttu-id="d9ea0-127">成員資料庫的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9ea0-128">-Name</span></span>
<span data-ttu-id="d9ea0-129">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-129">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-130">-ResourceGroupName</span></span>
<span data-ttu-id="d9ea0-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-132">-ServerName</span></span>
<span data-ttu-id="d9ea0-133">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="d9ea0-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="d9ea0-135">同步處理代理程式所連線之 SQL server 資料庫的 id。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-136">-SyncAgentName</span></span>
<span data-ttu-id="d9ea0-137">同步處理常式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-137">The name of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="d9ea0-139">同步處理代理程式所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="d9ea0-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="d9ea0-141">同步處理常式的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-141">The resource ID of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-142">-SyncAgentServerName</span></span>
<span data-ttu-id="d9ea0-143">同步處理代理程式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="d9ea0-144">-SyncDirection</span></span>
<span data-ttu-id="d9ea0-145">此同步處理成員的同步處理方向。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-145">The sync direction of this sync member.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ea0-146">-SyncGroupName</span></span>
<span data-ttu-id="d9ea0-147">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-147">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-148">-確認</span><span class="sxs-lookup"><span data-stu-id="d9ea0-148">-Confirm</span></span>
<span data-ttu-id="d9ea0-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ea0-150">-WhatIf</span></span>
<span data-ttu-id="d9ea0-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ea0-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ea0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ea0-153">CommonParameters</span></span>
<span data-ttu-id="d9ea0-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ea0-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ea0-156">輸入</span><span class="sxs-lookup"><span data-stu-id="d9ea0-156">INPUTS</span></span>

### <span data-ttu-id="d9ea0-157">所有</span><span class="sxs-lookup"><span data-stu-id="d9ea0-157">None</span></span>
<span data-ttu-id="d9ea0-158">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d9ea0-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9ea0-159">輸出</span><span class="sxs-lookup"><span data-stu-id="d9ea0-159">OUTPUTS</span></span>

### <span data-ttu-id="d9ea0-160">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="d9ea0-160">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d9ea0-161">筆記</span><span class="sxs-lookup"><span data-stu-id="d9ea0-161">NOTES</span></span>

## <span data-ttu-id="d9ea0-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9ea0-162">RELATED LINKS</span></span>

[<span data-ttu-id="d9ea0-163">AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9ea0-163">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="d9ea0-164">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9ea0-164">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="d9ea0-165">移除-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9ea0-165">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)


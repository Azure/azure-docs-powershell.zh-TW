---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 76b7366dabc648dc7f5812aedcc7fef18437b68e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614655"
---
# <span data-ttu-id="8d9a0-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8d9a0-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="8d9a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9a0-103">更新 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="8d9a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d9a0-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d9a0-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d9a0-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9a0-106">**AzSqlSyncGroup** Cmdlet 會修改 Azure SQL Database 同步處理成員的屬性。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="8d9a0-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d9a0-107">EXAMPLES</span></span>

### <span data-ttu-id="8d9a0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8d9a0-108">Example 1</span></span>
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

<span data-ttu-id="8d9a0-109">這個命令會針對成員資料庫重設系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="8d9a0-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d9a0-110">PARAMETERS</span></span>

### <span data-ttu-id="8d9a0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d9a0-111">-DatabaseName</span></span>
<span data-ttu-id="8d9a0-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8d9a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9a0-113">-DefaultProfile</span></span>
<span data-ttu-id="8d9a0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8d9a0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d9a0-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="8d9a0-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="8d9a0-116">認證 (Azure SQL 資料庫的使用者名稱和密碼) 。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9a0-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d9a0-117">-Name</span></span>
<span data-ttu-id="8d9a0-118">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-118">The sync member name.</span></span>

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

### <span data-ttu-id="8d9a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d9a0-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d9a0-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8d9a0-121">-ServerName</span></span>
<span data-ttu-id="8d9a0-122">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="8d9a0-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9a0-123">-SyncGroupName</span></span>
<span data-ttu-id="8d9a0-124">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-124">The sync group name.</span></span>

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

### <span data-ttu-id="8d9a0-125">-確認</span><span class="sxs-lookup"><span data-stu-id="8d9a0-125">-Confirm</span></span>
<span data-ttu-id="8d9a0-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9a0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9a0-127">-WhatIf</span></span>
<span data-ttu-id="8d9a0-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d9a0-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9a0-130">CommonParameters</span></span>
<span data-ttu-id="8d9a0-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9a0-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d9a0-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9a0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8d9a0-133">INPUTS</span></span>

### <span data-ttu-id="8d9a0-134">System.object</span><span class="sxs-lookup"><span data-stu-id="8d9a0-134">System.String</span></span>

## <span data-ttu-id="8d9a0-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8d9a0-135">OUTPUTS</span></span>

### <span data-ttu-id="8d9a0-136">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="8d9a0-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="8d9a0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8d9a0-137">NOTES</span></span>

## <span data-ttu-id="8d9a0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d9a0-138">RELATED LINKS</span></span>

[<span data-ttu-id="8d9a0-139">新-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8d9a0-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="8d9a0-140">AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8d9a0-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="8d9a0-141">移除-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8d9a0-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)


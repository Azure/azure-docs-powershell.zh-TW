---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: 7737baa8459cc9acae86cbd3e632dd73f9433056
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454475"
---
# <span data-ttu-id="592a5-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="592a5-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="592a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="592a5-102">SYNOPSIS</span></span>
<span data-ttu-id="592a5-103">更新 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="592a5-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="592a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="592a5-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="592a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="592a5-105">DESCRIPTION</span></span>
<span data-ttu-id="592a5-106">**AzureRmSqlSyncGroup** Cmdlet 會修改 Azure SQL Database 同步處理成員的屬性。</span><span class="sxs-lookup"><span data-stu-id="592a5-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="592a5-107">示例</span><span class="sxs-lookup"><span data-stu-id="592a5-107">EXAMPLES</span></span>

### <span data-ttu-id="592a5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="592a5-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
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

<span data-ttu-id="592a5-109">這個命令會針對成員資料庫重設系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="592a5-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="592a5-110">參數</span><span class="sxs-lookup"><span data-stu-id="592a5-110">PARAMETERS</span></span>

### <span data-ttu-id="592a5-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="592a5-111">-DatabaseName</span></span>
<span data-ttu-id="592a5-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="592a5-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="592a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592a5-113">-DefaultProfile</span></span>
<span data-ttu-id="592a5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="592a5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="592a5-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="592a5-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="592a5-116">認證 (Azure SQL 資料庫的使用者名稱和密碼) 。</span><span class="sxs-lookup"><span data-stu-id="592a5-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="592a5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="592a5-117">-Name</span></span>
<span data-ttu-id="592a5-118">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="592a5-118">The sync member name.</span></span>

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

### <span data-ttu-id="592a5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592a5-119">-ResourceGroupName</span></span>
<span data-ttu-id="592a5-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="592a5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="592a5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="592a5-121">-ServerName</span></span>
<span data-ttu-id="592a5-122">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="592a5-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="592a5-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="592a5-123">-SyncGroupName</span></span>
<span data-ttu-id="592a5-124">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="592a5-124">The sync group name.</span></span>

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

### <span data-ttu-id="592a5-125">-確認</span><span class="sxs-lookup"><span data-stu-id="592a5-125">-Confirm</span></span>
<span data-ttu-id="592a5-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="592a5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="592a5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="592a5-127">-WhatIf</span></span>
<span data-ttu-id="592a5-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="592a5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="592a5-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="592a5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="592a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592a5-130">CommonParameters</span></span>
<span data-ttu-id="592a5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="592a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592a5-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="592a5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592a5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="592a5-133">INPUTS</span></span>

### <span data-ttu-id="592a5-134">System.object</span><span class="sxs-lookup"><span data-stu-id="592a5-134">System.String</span></span>

## <span data-ttu-id="592a5-135">輸出</span><span class="sxs-lookup"><span data-stu-id="592a5-135">OUTPUTS</span></span>

### <span data-ttu-id="592a5-136">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="592a5-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="592a5-137">筆記</span><span class="sxs-lookup"><span data-stu-id="592a5-137">NOTES</span></span>

## <span data-ttu-id="592a5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="592a5-138">RELATED LINKS</span></span>

[<span data-ttu-id="592a5-139">新-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="592a5-139">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="592a5-140">AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="592a5-140">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="592a5-141">移除-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="592a5-141">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)


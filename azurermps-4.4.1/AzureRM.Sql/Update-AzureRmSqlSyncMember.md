---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: f72091d142b57cc7ef3897eceda2219634376daf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624539"
---
# <span data-ttu-id="6f8ab-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6f8ab-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="6f8ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8ab-103">更新 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f8ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f8ab-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f8ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f8ab-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8ab-106">**AzureRmSqlSyncGroup** Cmdlet 會修改 Azure SQL Database 同步處理成員的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6f8ab-107">示例</span><span class="sxs-lookup"><span data-stu-id="6f8ab-107">EXAMPLES</span></span>

### <span data-ttu-id="6f8ab-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6f8ab-108">Example 1</span></span>
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

<span data-ttu-id="6f8ab-109">這個命令會針對成員資料庫重設系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="6f8ab-110">參數</span><span class="sxs-lookup"><span data-stu-id="6f8ab-110">PARAMETERS</span></span>

### <span data-ttu-id="6f8ab-111">-確認</span><span class="sxs-lookup"><span data-stu-id="6f8ab-111">-Confirm</span></span>
<span data-ttu-id="6f8ab-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8ab-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f8ab-113">-DatabaseName</span></span>
<span data-ttu-id="6f8ab-114">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6f8ab-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="6f8ab-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="6f8ab-116">認證 (Azure SQL 資料庫的使用者名稱和密碼) 。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6f8ab-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f8ab-117">-Name</span></span>
<span data-ttu-id="6f8ab-118">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-118">The sync member name.</span></span>

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

### <span data-ttu-id="6f8ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f8ab-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6f8ab-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f8ab-121">-ServerName</span></span>
<span data-ttu-id="6f8ab-122">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6f8ab-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8ab-123">-SyncGroupName</span></span>
<span data-ttu-id="6f8ab-124">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-124">The sync group name.</span></span>

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

### <span data-ttu-id="6f8ab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8ab-125">-WhatIf</span></span>
<span data-ttu-id="6f8ab-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f8ab-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f8ab-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8ab-128">-DefaultProfile</span></span>
<span data-ttu-id="6f8ab-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8ab-130">CommonParameters</span></span>
<span data-ttu-id="6f8ab-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8ab-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f8ab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8ab-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6f8ab-133">INPUTS</span></span>

## <span data-ttu-id="6f8ab-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6f8ab-134">OUTPUTS</span></span>

### <span data-ttu-id="6f8ab-135">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="6f8ab-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="6f8ab-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6f8ab-136">NOTES</span></span>

## <span data-ttu-id="6f8ab-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f8ab-137">RELATED LINKS</span></span>

[<span data-ttu-id="6f8ab-138">新-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6f8ab-138">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="6f8ab-139">AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6f8ab-139">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="6f8ab-140">移除-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6f8ab-140">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)


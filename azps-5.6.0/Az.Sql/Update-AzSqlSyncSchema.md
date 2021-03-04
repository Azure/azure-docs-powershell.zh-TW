---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 394ae4d82437795f62e19b4d0f7a536cdd893da9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912265"
---
# <span data-ttu-id="bf9ea-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="bf9ea-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="bf9ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bf9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9ea-103">更新同步成員資料庫或同步中樞資料庫的同步架構。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="bf9ea-104">它會從實際資料庫取得最新的資料庫架構，然後使用它重新組織同步中繼資料資料庫所快回的架構。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="bf9ea-105">如果指定 「SyncMemberName」，它會重新組織成員資料庫架構;如果沒有，它會重新組織中樞資料庫架構。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="bf9ea-106">語法</span><span class="sxs-lookup"><span data-stu-id="bf9ea-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf9ea-107">描述</span><span class="sxs-lookup"><span data-stu-id="bf9ea-107">DESCRIPTION</span></span>
<span data-ttu-id="bf9ea-108">**Update-AzSqlSyncSchema** Cmdlet 會更新同步成員資料庫或同步中樞資料庫的同步架構。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="bf9ea-109">例子</span><span class="sxs-lookup"><span data-stu-id="bf9ea-109">EXAMPLES</span></span>

### <span data-ttu-id="bf9ea-110">範例 1：更新中樞資料庫的同步架構</span><span class="sxs-lookup"><span data-stu-id="bf9ea-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="bf9ea-111">此命令會更新同步群組 SyncGroup01 中中樞資料庫的同步架構</span><span class="sxs-lookup"><span data-stu-id="bf9ea-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="bf9ea-112">範例 2：更新成員資料庫的同步架構</span><span class="sxs-lookup"><span data-stu-id="bf9ea-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="bf9ea-113">此命令會更新同步成員 SyncMember01 中成員資料庫的同步架構</span><span class="sxs-lookup"><span data-stu-id="bf9ea-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="bf9ea-114">參數</span><span class="sxs-lookup"><span data-stu-id="bf9ea-114">PARAMETERS</span></span>

### <span data-ttu-id="bf9ea-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf9ea-115">-DatabaseName</span></span>
<span data-ttu-id="bf9ea-116">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="bf9ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ea-117">-DefaultProfile</span></span>
<span data-ttu-id="bf9ea-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bf9ea-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf9ea-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf9ea-119">-PassThru</span></span>
<span data-ttu-id="bf9ea-120">定義此 Cmdlet 是否返回同步組</span><span class="sxs-lookup"><span data-stu-id="bf9ea-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="bf9ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="bf9ea-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="bf9ea-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bf9ea-123">-ServerName</span></span>
<span data-ttu-id="bf9ea-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="bf9ea-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9ea-125">-SyncGroupName</span></span>
<span data-ttu-id="bf9ea-126">同步組名。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-126">The sync group name.</span></span>

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

### <span data-ttu-id="bf9ea-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="bf9ea-127">-SyncMemberName</span></span>
<span data-ttu-id="bf9ea-128">同步成員名稱。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ea-129">-確認</span><span class="sxs-lookup"><span data-stu-id="bf9ea-129">-Confirm</span></span>
<span data-ttu-id="bf9ea-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf9ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9ea-131">-WhatIf</span></span>
<span data-ttu-id="bf9ea-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf9ea-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf9ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9ea-134">CommonParameters</span></span>
<span data-ttu-id="bf9ea-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bf9ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9ea-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf9ea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9ea-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bf9ea-137">INPUTS</span></span>

### <span data-ttu-id="bf9ea-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bf9ea-138">System.String</span></span>

## <span data-ttu-id="bf9ea-139">輸出</span><span class="sxs-lookup"><span data-stu-id="bf9ea-139">OUTPUTS</span></span>

### <span data-ttu-id="bf9ea-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="bf9ea-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="bf9ea-141">筆記</span><span class="sxs-lookup"><span data-stu-id="bf9ea-141">NOTES</span></span>

## <span data-ttu-id="bf9ea-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf9ea-142">RELATED LINKS</span></span>

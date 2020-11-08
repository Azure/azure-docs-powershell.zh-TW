---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126744"
---
# <span data-ttu-id="655d9-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="655d9-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="655d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="655d9-102">SYNOPSIS</span></span>
<span data-ttu-id="655d9-103">更新同步處理成員資料庫或同步處理中樞資料庫的同步處理架構。</span><span class="sxs-lookup"><span data-stu-id="655d9-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="655d9-104">它會從真實資料庫取得最新的資料庫架構，然後使用它來重新整理同步處理中繼資料資料庫所緩存的架構。</span><span class="sxs-lookup"><span data-stu-id="655d9-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="655d9-105">如果指定了 "SyncMemberName"，則會重新整理成員資料庫架構;如果不是，它會重新整理中心資料庫架構。</span><span class="sxs-lookup"><span data-stu-id="655d9-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="655d9-106">句法</span><span class="sxs-lookup"><span data-stu-id="655d9-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="655d9-107">說明</span><span class="sxs-lookup"><span data-stu-id="655d9-107">DESCRIPTION</span></span>
<span data-ttu-id="655d9-108">**更新-AzSqlSyncSchema** Cmdlet 會更新同步處理成員資料庫或同步處理中樞資料庫的同步架構。</span><span class="sxs-lookup"><span data-stu-id="655d9-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="655d9-109">示例</span><span class="sxs-lookup"><span data-stu-id="655d9-109">EXAMPLES</span></span>

### <span data-ttu-id="655d9-110">範例1：更新中心資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="655d9-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="655d9-111">這個命令會在同步處理群組 syncGroup01 中更新中心資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="655d9-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="655d9-112">範例2：更新成員資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="655d9-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="655d9-113">這個命令會在同步處理成員 syncMember01 中更新成員資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="655d9-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="655d9-114">參數</span><span class="sxs-lookup"><span data-stu-id="655d9-114">PARAMETERS</span></span>

### <span data-ttu-id="655d9-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="655d9-115">-DatabaseName</span></span>
<span data-ttu-id="655d9-116">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="655d9-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="655d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="655d9-117">-DefaultProfile</span></span>
<span data-ttu-id="655d9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="655d9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="655d9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="655d9-119">-PassThru</span></span>
<span data-ttu-id="655d9-120">定義是否傳回這個 Cmdlet 適用的同步群組</span><span class="sxs-lookup"><span data-stu-id="655d9-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="655d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="655d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="655d9-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="655d9-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="655d9-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="655d9-123">-ServerName</span></span>
<span data-ttu-id="655d9-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="655d9-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="655d9-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="655d9-125">-SyncGroupName</span></span>
<span data-ttu-id="655d9-126">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="655d9-126">The sync group name.</span></span>

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

### <span data-ttu-id="655d9-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="655d9-127">-SyncMemberName</span></span>
<span data-ttu-id="655d9-128">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="655d9-128">The sync member name.</span></span>

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

### <span data-ttu-id="655d9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="655d9-129">-Confirm</span></span>
<span data-ttu-id="655d9-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="655d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="655d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="655d9-131">-WhatIf</span></span>
<span data-ttu-id="655d9-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="655d9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="655d9-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="655d9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="655d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655d9-134">CommonParameters</span></span>
<span data-ttu-id="655d9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="655d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655d9-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="655d9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655d9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="655d9-137">INPUTS</span></span>

### <span data-ttu-id="655d9-138">System.object</span><span class="sxs-lookup"><span data-stu-id="655d9-138">System.String</span></span>

## <span data-ttu-id="655d9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="655d9-139">OUTPUTS</span></span>

### <span data-ttu-id="655d9-140">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="655d9-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="655d9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="655d9-141">NOTES</span></span>

## <span data-ttu-id="655d9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="655d9-142">RELATED LINKS</span></span>

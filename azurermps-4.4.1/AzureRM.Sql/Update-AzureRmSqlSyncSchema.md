---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 34aec11e5f4bd2ee0aef37a4287544081bb9a87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451584"
---
# <span data-ttu-id="b85e3-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="b85e3-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="b85e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b85e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b85e3-103">更新同步處理成員資料庫或同步處理中樞資料庫的同步處理架構。</span><span class="sxs-lookup"><span data-stu-id="b85e3-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="b85e3-104">它會從真實資料庫取得最新的資料庫架構，然後使用它來重新整理同步處理中繼資料資料庫所緩存的架構。</span><span class="sxs-lookup"><span data-stu-id="b85e3-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="b85e3-105">如果指定了 "SyncMemberName"，則會重新整理成員資料庫架構;如果不是，它會重新整理中心資料庫架構。</span><span class="sxs-lookup"><span data-stu-id="b85e3-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b85e3-106">句法</span><span class="sxs-lookup"><span data-stu-id="b85e3-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b85e3-107">說明</span><span class="sxs-lookup"><span data-stu-id="b85e3-107">DESCRIPTION</span></span>
<span data-ttu-id="b85e3-108">**更新-AzureRmSqlSyncSchema** Cmdlet 會更新同步處理成員資料庫或同步處理中樞資料庫的同步架構。</span><span class="sxs-lookup"><span data-stu-id="b85e3-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="b85e3-109">示例</span><span class="sxs-lookup"><span data-stu-id="b85e3-109">EXAMPLES</span></span>

### <span data-ttu-id="b85e3-110">範例1：更新中心資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="b85e3-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="b85e3-111">這個命令會在同步處理群組 syncGroup01 中更新中心資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="b85e3-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="b85e3-112">範例2：更新成員資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="b85e3-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="b85e3-113">這個命令會在同步處理成員 syncMember01 中更新成員資料庫的同步處理架構</span><span class="sxs-lookup"><span data-stu-id="b85e3-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="b85e3-114">參數</span><span class="sxs-lookup"><span data-stu-id="b85e3-114">PARAMETERS</span></span>

### <span data-ttu-id="b85e3-115">-確認</span><span class="sxs-lookup"><span data-stu-id="b85e3-115">-Confirm</span></span>
<span data-ttu-id="b85e3-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b85e3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85e3-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b85e3-117">-DatabaseName</span></span>
<span data-ttu-id="b85e3-118">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85e3-118">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b85e3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b85e3-119">-PassThru</span></span>
<span data-ttu-id="b85e3-120">定義是否傳回這個 Cmdlet 適用的同步群組</span><span class="sxs-lookup"><span data-stu-id="b85e3-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="b85e3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85e3-121">-ResourceGroupName</span></span>
<span data-ttu-id="b85e3-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85e3-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b85e3-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b85e3-123">-ServerName</span></span>
<span data-ttu-id="b85e3-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85e3-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b85e3-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b85e3-125">-SyncGroupName</span></span>
<span data-ttu-id="b85e3-126">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="b85e3-126">The sync group name.</span></span>

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

### <span data-ttu-id="b85e3-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="b85e3-127">-SyncMemberName</span></span>
<span data-ttu-id="b85e3-128">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="b85e3-128">The sync member name.</span></span>

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

### <span data-ttu-id="b85e3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85e3-129">-WhatIf</span></span>
<span data-ttu-id="b85e3-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b85e3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b85e3-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b85e3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85e3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85e3-132">-DefaultProfile</span></span>
<span data-ttu-id="b85e3-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b85e3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b85e3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85e3-134">CommonParameters</span></span>
<span data-ttu-id="b85e3-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b85e3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85e3-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b85e3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85e3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b85e3-137">INPUTS</span></span>

## <span data-ttu-id="b85e3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b85e3-138">OUTPUTS</span></span>

### <span data-ttu-id="b85e3-139">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="b85e3-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="b85e3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b85e3-140">NOTES</span></span>

## <span data-ttu-id="b85e3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b85e3-141">RELATED LINKS</span></span>


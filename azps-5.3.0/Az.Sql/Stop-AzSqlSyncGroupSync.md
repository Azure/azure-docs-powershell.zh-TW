---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436654"
---
# <span data-ttu-id="b6065-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="b6065-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="b6065-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6065-102">SYNOPSIS</span></span>
<span data-ttu-id="b6065-103">停止同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="b6065-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="b6065-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6065-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6065-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6065-105">DESCRIPTION</span></span>
<span data-ttu-id="b6065-106">**AzSqlSyncGroupSync** Cmdlet 會停止同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="b6065-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="b6065-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6065-107">EXAMPLES</span></span>

### <span data-ttu-id="b6065-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b6065-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="b6065-109">這個命令會停止對同步處理群組 mysg 進行的同步處理。</span><span class="sxs-lookup"><span data-stu-id="b6065-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="b6065-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6065-110">PARAMETERS</span></span>

### <span data-ttu-id="b6065-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b6065-111">-DatabaseName</span></span>
<span data-ttu-id="b6065-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6065-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b6065-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6065-113">-DefaultProfile</span></span>
<span data-ttu-id="b6065-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b6065-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6065-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6065-115">-PassThru</span></span>
<span data-ttu-id="b6065-116">定義是否要傳回同步處理群組</span><span class="sxs-lookup"><span data-stu-id="b6065-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="b6065-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6065-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6065-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6065-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b6065-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6065-119">-ServerName</span></span>
<span data-ttu-id="b6065-120">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6065-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b6065-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b6065-121">-SyncGroupName</span></span>
<span data-ttu-id="b6065-122">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="b6065-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6065-123">-確認</span><span class="sxs-lookup"><span data-stu-id="b6065-123">-Confirm</span></span>
<span data-ttu-id="b6065-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6065-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6065-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6065-125">-WhatIf</span></span>
<span data-ttu-id="b6065-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6065-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6065-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6065-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6065-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6065-128">CommonParameters</span></span>
<span data-ttu-id="b6065-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6065-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6065-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6065-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6065-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b6065-131">INPUTS</span></span>

### <span data-ttu-id="b6065-132">System.object</span><span class="sxs-lookup"><span data-stu-id="b6065-132">System.String</span></span>

## <span data-ttu-id="b6065-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b6065-133">OUTPUTS</span></span>

### <span data-ttu-id="b6065-134">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="b6065-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="b6065-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b6065-135">NOTES</span></span>

## <span data-ttu-id="b6065-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6065-136">RELATED LINKS</span></span>

[<span data-ttu-id="b6065-137">開始-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="b6065-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)


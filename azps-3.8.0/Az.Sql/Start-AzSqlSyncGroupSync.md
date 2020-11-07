---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798170"
---
# <span data-ttu-id="e6668-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="e6668-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="e6668-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6668-102">SYNOPSIS</span></span>
<span data-ttu-id="e6668-103">啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="e6668-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="e6668-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6668-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6668-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6668-105">DESCRIPTION</span></span>
<span data-ttu-id="e6668-106">**Start-AzSqlSyncGroupSync** Cmdlet 會啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="e6668-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="e6668-107">示例</span><span class="sxs-lookup"><span data-stu-id="e6668-107">EXAMPLES</span></span>

### <span data-ttu-id="e6668-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e6668-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="e6668-109">這個命令會針對同步處理群組 mysg 啟動一輪同步處理。</span><span class="sxs-lookup"><span data-stu-id="e6668-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="e6668-110">參數</span><span class="sxs-lookup"><span data-stu-id="e6668-110">PARAMETERS</span></span>

### <span data-ttu-id="e6668-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6668-111">-DatabaseName</span></span>
<span data-ttu-id="e6668-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6668-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e6668-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6668-113">-DefaultProfile</span></span>
<span data-ttu-id="e6668-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e6668-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6668-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6668-115">-PassThru</span></span>
<span data-ttu-id="e6668-116">定義是否要傳回同步處理群組</span><span class="sxs-lookup"><span data-stu-id="e6668-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="e6668-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6668-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6668-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6668-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6668-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6668-119">-ServerName</span></span>
<span data-ttu-id="e6668-120">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6668-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e6668-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e6668-121">-SyncGroupName</span></span>
<span data-ttu-id="e6668-122">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="e6668-122">The sync group name.</span></span>

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

### <span data-ttu-id="e6668-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e6668-123">-Confirm</span></span>
<span data-ttu-id="e6668-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6668-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6668-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6668-125">-WhatIf</span></span>
<span data-ttu-id="e6668-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6668-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6668-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6668-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6668-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6668-128">CommonParameters</span></span>
<span data-ttu-id="e6668-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6668-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6668-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e6668-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6668-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e6668-131">INPUTS</span></span>

### <span data-ttu-id="e6668-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e6668-132">System.String</span></span>

## <span data-ttu-id="e6668-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e6668-133">OUTPUTS</span></span>

### <span data-ttu-id="e6668-134">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="e6668-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e6668-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e6668-135">NOTES</span></span>

## <span data-ttu-id="e6668-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6668-136">RELATED LINKS</span></span>

[<span data-ttu-id="e6668-137">停止 AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="e6668-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)


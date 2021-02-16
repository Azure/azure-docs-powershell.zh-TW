---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128182"
---
# <span data-ttu-id="a65cc-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a65cc-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="a65cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a65cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a65cc-103">啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="a65cc-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="a65cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="a65cc-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a65cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="a65cc-105">DESCRIPTION</span></span>
<span data-ttu-id="a65cc-106">**Start-AzSqlSyncGroupSync** Cmdlet 會啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="a65cc-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="a65cc-107">示例</span><span class="sxs-lookup"><span data-stu-id="a65cc-107">EXAMPLES</span></span>

### <span data-ttu-id="a65cc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a65cc-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="a65cc-109">這個命令會針對同步處理群組 mysg 啟動一輪同步處理。</span><span class="sxs-lookup"><span data-stu-id="a65cc-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="a65cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="a65cc-110">PARAMETERS</span></span>

### <span data-ttu-id="a65cc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a65cc-111">-DatabaseName</span></span>
<span data-ttu-id="a65cc-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a65cc-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a65cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65cc-113">-DefaultProfile</span></span>
<span data-ttu-id="a65cc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a65cc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a65cc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a65cc-115">-PassThru</span></span>
<span data-ttu-id="a65cc-116">定義是否要傳回同步處理群組</span><span class="sxs-lookup"><span data-stu-id="a65cc-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="a65cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a65cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="a65cc-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a65cc-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a65cc-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a65cc-119">-ServerName</span></span>
<span data-ttu-id="a65cc-120">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a65cc-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a65cc-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a65cc-121">-SyncGroupName</span></span>
<span data-ttu-id="a65cc-122">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="a65cc-122">The sync group name.</span></span>

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

### <span data-ttu-id="a65cc-123">-確認</span><span class="sxs-lookup"><span data-stu-id="a65cc-123">-Confirm</span></span>
<span data-ttu-id="a65cc-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a65cc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a65cc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a65cc-125">-WhatIf</span></span>
<span data-ttu-id="a65cc-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a65cc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a65cc-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a65cc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a65cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65cc-128">CommonParameters</span></span>
<span data-ttu-id="a65cc-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a65cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65cc-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a65cc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65cc-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a65cc-131">INPUTS</span></span>

### <span data-ttu-id="a65cc-132">System.object</span><span class="sxs-lookup"><span data-stu-id="a65cc-132">System.String</span></span>

## <span data-ttu-id="a65cc-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a65cc-133">OUTPUTS</span></span>

### <span data-ttu-id="a65cc-134">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="a65cc-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a65cc-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a65cc-135">NOTES</span></span>

## <span data-ttu-id="a65cc-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a65cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="a65cc-137">停止 AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a65cc-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: 13f58f454fb84a4bcd003afd84761197d41c16ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916487"
---
# <span data-ttu-id="db975-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="db975-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="db975-102">簡介</span><span class="sxs-lookup"><span data-stu-id="db975-102">SYNOPSIS</span></span>
<span data-ttu-id="db975-103">開始同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="db975-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="db975-104">語法</span><span class="sxs-lookup"><span data-stu-id="db975-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db975-105">描述</span><span class="sxs-lookup"><span data-stu-id="db975-105">DESCRIPTION</span></span>
<span data-ttu-id="db975-106">**Start-AzSqlSyncGroupSync** Cmdlet 會啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="db975-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="db975-107">例子</span><span class="sxs-lookup"><span data-stu-id="db975-107">EXAMPLES</span></span>

### <span data-ttu-id="db975-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="db975-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="db975-109">此命令會針對同步處理群組 mysg 開始一輪同步處理。</span><span class="sxs-lookup"><span data-stu-id="db975-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="db975-110">參數</span><span class="sxs-lookup"><span data-stu-id="db975-110">PARAMETERS</span></span>

### <span data-ttu-id="db975-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db975-111">-DatabaseName</span></span>
<span data-ttu-id="db975-112">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="db975-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="db975-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db975-113">-DefaultProfile</span></span>
<span data-ttu-id="db975-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="db975-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db975-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db975-115">-PassThru</span></span>
<span data-ttu-id="db975-116">定義是否返回同步組</span><span class="sxs-lookup"><span data-stu-id="db975-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="db975-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db975-117">-ResourceGroupName</span></span>
<span data-ttu-id="db975-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db975-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="db975-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db975-119">-ServerName</span></span>
<span data-ttu-id="db975-120">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="db975-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="db975-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="db975-121">-SyncGroupName</span></span>
<span data-ttu-id="db975-122">同步組名。</span><span class="sxs-lookup"><span data-stu-id="db975-122">The sync group name.</span></span>

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

### <span data-ttu-id="db975-123">-確認</span><span class="sxs-lookup"><span data-stu-id="db975-123">-Confirm</span></span>
<span data-ttu-id="db975-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="db975-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db975-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db975-125">-WhatIf</span></span>
<span data-ttu-id="db975-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="db975-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db975-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db975-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db975-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db975-128">CommonParameters</span></span>
<span data-ttu-id="db975-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="db975-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db975-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db975-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db975-131">輸入</span><span class="sxs-lookup"><span data-stu-id="db975-131">INPUTS</span></span>

### <span data-ttu-id="db975-132">System.String</span><span class="sxs-lookup"><span data-stu-id="db975-132">System.String</span></span>

## <span data-ttu-id="db975-133">輸出</span><span class="sxs-lookup"><span data-stu-id="db975-133">OUTPUTS</span></span>

### <span data-ttu-id="db975-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="db975-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="db975-135">筆記</span><span class="sxs-lookup"><span data-stu-id="db975-135">NOTES</span></span>

## <span data-ttu-id="db975-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="db975-136">RELATED LINKS</span></span>

[<span data-ttu-id="db975-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="db975-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)


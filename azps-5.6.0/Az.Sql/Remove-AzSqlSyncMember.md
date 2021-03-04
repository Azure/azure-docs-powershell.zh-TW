---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 58a6ee3d51af355c0824025f856ed1646fa23cf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913070"
---
# <span data-ttu-id="edea5-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="edea5-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="edea5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="edea5-102">SYNOPSIS</span></span>
<span data-ttu-id="edea5-103">移除 Azure SQL 資料庫同步成員。</span><span class="sxs-lookup"><span data-stu-id="edea5-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="edea5-104">語法</span><span class="sxs-lookup"><span data-stu-id="edea5-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edea5-105">描述</span><span class="sxs-lookup"><span data-stu-id="edea5-105">DESCRIPTION</span></span>
<span data-ttu-id="edea5-106">**Remove-AzSqlSyncMember Cmdlet** 會移除 Azure SQL 資料庫同步成員。</span><span class="sxs-lookup"><span data-stu-id="edea5-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="edea5-107">例子</span><span class="sxs-lookup"><span data-stu-id="edea5-107">EXAMPLES</span></span>

### <span data-ttu-id="edea5-108">範例 1：移除同步成員</span><span class="sxs-lookup"><span data-stu-id="edea5-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="edea5-109">此命令會移除名為 syncMember01 的 Azure SQL 資料庫同步成員。</span><span class="sxs-lookup"><span data-stu-id="edea5-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="edea5-110">參數</span><span class="sxs-lookup"><span data-stu-id="edea5-110">PARAMETERS</span></span>

### <span data-ttu-id="edea5-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="edea5-111">-DatabaseName</span></span>
<span data-ttu-id="edea5-112">Azure SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="edea5-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="edea5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edea5-113">-DefaultProfile</span></span>
<span data-ttu-id="edea5-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="edea5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edea5-115">-強制</span><span class="sxs-lookup"><span data-stu-id="edea5-115">-Force</span></span>
<span data-ttu-id="edea5-116">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="edea5-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="edea5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="edea5-117">-Name</span></span>
<span data-ttu-id="edea5-118">同步成員名稱。</span><span class="sxs-lookup"><span data-stu-id="edea5-118">The sync member name.</span></span>

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

### <span data-ttu-id="edea5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edea5-119">-PassThru</span></span>
<span data-ttu-id="edea5-120">定義是否返回已移除的同步成員</span><span class="sxs-lookup"><span data-stu-id="edea5-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="edea5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edea5-121">-ResourceGroupName</span></span>
<span data-ttu-id="edea5-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="edea5-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="edea5-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="edea5-123">-ServerName</span></span>
<span data-ttu-id="edea5-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="edea5-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="edea5-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="edea5-125">-SyncGroupName</span></span>
<span data-ttu-id="edea5-126">同步組名。</span><span class="sxs-lookup"><span data-stu-id="edea5-126">The sync group name.</span></span>

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

### <span data-ttu-id="edea5-127">-確認</span><span class="sxs-lookup"><span data-stu-id="edea5-127">-Confirm</span></span>
<span data-ttu-id="edea5-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="edea5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edea5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edea5-129">-WhatIf</span></span>
<span data-ttu-id="edea5-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edea5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edea5-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edea5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edea5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edea5-132">CommonParameters</span></span>
<span data-ttu-id="edea5-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="edea5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edea5-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edea5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edea5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="edea5-135">INPUTS</span></span>

### <span data-ttu-id="edea5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="edea5-136">System.String</span></span>

## <span data-ttu-id="edea5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="edea5-137">OUTPUTS</span></span>

### <span data-ttu-id="edea5-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="edea5-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="edea5-139">筆記</span><span class="sxs-lookup"><span data-stu-id="edea5-139">NOTES</span></span>

## <span data-ttu-id="edea5-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="edea5-140">RELATED LINKS</span></span>

[<span data-ttu-id="edea5-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="edea5-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="edea5-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="edea5-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="edea5-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="edea5-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


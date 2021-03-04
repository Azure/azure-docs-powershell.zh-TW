---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a8ad9a3925ccf1c0f56ce9be6a962d667f122307
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912282"
---
# <span data-ttu-id="77f54-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="77f54-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="77f54-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77f54-102">SYNOPSIS</span></span>
<span data-ttu-id="77f54-103">執行 Azure SQL Database 容錯移轉群組的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="77f54-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="77f54-104">語法</span><span class="sxs-lookup"><span data-stu-id="77f54-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77f54-105">描述</span><span class="sxs-lookup"><span data-stu-id="77f54-105">DESCRIPTION</span></span>
<span data-ttu-id="77f54-106">此命令會交換容錯移轉群組中的伺服器角色，並切換所有次要資料庫至主要角色。</span><span class="sxs-lookup"><span data-stu-id="77f54-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="77f54-107">重新更新 DNS 用戶端緩存後，所有新的 TDS 會話都會自動重新路由至次要伺服器。</span><span class="sxs-lookup"><span data-stu-id="77f54-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="77f54-108">當原始主伺服器恢復連線時，其中所有之前的主要資料庫都會切換至次要角色。</span><span class="sxs-lookup"><span data-stu-id="77f54-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="77f54-109">容錯移轉群組的次要伺服器必須用來執行此命令。</span><span class="sxs-lookup"><span data-stu-id="77f54-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="77f54-110">如果未指定 AllowDataLoss 參數，此命令會等候兩個角色切換完成。</span><span class="sxs-lookup"><span data-stu-id="77f54-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="77f54-111">如果指定 AllowDataLoss 參數，則命令只會等到新主命令承擔其角色後才會執行。</span><span class="sxs-lookup"><span data-stu-id="77f54-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="77f54-112">例子</span><span class="sxs-lookup"><span data-stu-id="77f54-112">EXAMPLES</span></span>

### <span data-ttu-id="77f54-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="77f54-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="77f54-114">在容錯移轉群組中發出允許資料遺失的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="77f54-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="77f54-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="77f54-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="77f54-116">發出最佳嘗試容錯移轉作業，該作業可能會成功而不會失去資料，或失敗並回復。</span><span class="sxs-lookup"><span data-stu-id="77f54-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="77f54-117">參數</span><span class="sxs-lookup"><span data-stu-id="77f54-117">PARAMETERS</span></span>

### <span data-ttu-id="77f54-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="77f54-118">-AllowDataLoss</span></span>
<span data-ttu-id="77f54-119">即使執行此操作可能會導致資料遺失，也請完成容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="77f54-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="77f54-120">這樣即使主資料庫無法使用，也允許容錯移轉繼續進行。</span><span class="sxs-lookup"><span data-stu-id="77f54-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f54-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77f54-121">-AsJob</span></span>
<span data-ttu-id="77f54-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="77f54-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77f54-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f54-123">-DefaultProfile</span></span>
<span data-ttu-id="77f54-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="77f54-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77f54-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="77f54-125">-FailoverGroupName</span></span>
<span data-ttu-id="77f54-126">Azure SQL 資料庫容錯移轉組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77f54-126">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f54-127">-ResourceGroupName</span></span>
<span data-ttu-id="77f54-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77f54-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="77f54-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="77f54-129">-ServerName</span></span>
<span data-ttu-id="77f54-130">容錯移轉群組的次要 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="77f54-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="77f54-131">-確認</span><span class="sxs-lookup"><span data-stu-id="77f54-131">-Confirm</span></span>
<span data-ttu-id="77f54-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="77f54-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f54-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f54-133">-WhatIf</span></span>
<span data-ttu-id="77f54-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77f54-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77f54-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77f54-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f54-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f54-136">CommonParameters</span></span>
<span data-ttu-id="77f54-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77f54-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f54-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77f54-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f54-139">輸入</span><span class="sxs-lookup"><span data-stu-id="77f54-139">INPUTS</span></span>

### <span data-ttu-id="77f54-140">System.String</span><span class="sxs-lookup"><span data-stu-id="77f54-140">System.String</span></span>

## <span data-ttu-id="77f54-141">輸出</span><span class="sxs-lookup"><span data-stu-id="77f54-141">OUTPUTS</span></span>

### <span data-ttu-id="77f54-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="77f54-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="77f54-143">筆記</span><span class="sxs-lookup"><span data-stu-id="77f54-143">NOTES</span></span>

## <span data-ttu-id="77f54-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="77f54-144">RELATED LINKS</span></span>

[<span data-ttu-id="77f54-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="77f54-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="77f54-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="77f54-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="77f54-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="77f54-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="77f54-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="77f54-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="77f54-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="77f54-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="77f54-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="77f54-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="77f54-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="77f54-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

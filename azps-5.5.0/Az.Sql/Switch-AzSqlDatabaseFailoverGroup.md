---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136962"
---
# <span data-ttu-id="48ac6-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="48ac6-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="48ac6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="48ac6-103">執行 Azure SQL Database 容錯移轉群組的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="48ac6-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="48ac6-104">句法</span><span class="sxs-lookup"><span data-stu-id="48ac6-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48ac6-105">說明</span><span class="sxs-lookup"><span data-stu-id="48ac6-105">DESCRIPTION</span></span>
<span data-ttu-id="48ac6-106">這個命令會交換容錯移轉群組中伺服器的角色，並將所有次要資料庫切換為主要角色。</span><span class="sxs-lookup"><span data-stu-id="48ac6-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="48ac6-107">在重新整理 DNS 用戶端快取之後，所有新的 TDS 會話都會自動重新路由到從屬伺服器。</span><span class="sxs-lookup"><span data-stu-id="48ac6-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="48ac6-108">當原始主要伺服器回到線上時，所有先前的主資料庫都會切換到副角色。</span><span class="sxs-lookup"><span data-stu-id="48ac6-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="48ac6-109">容錯移轉群組的次要伺服器必須用來執行這個命令。</span><span class="sxs-lookup"><span data-stu-id="48ac6-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="48ac6-110">如果未指定 AllowDataLoss 參數，這個命令會等到兩個角色都切換為止。</span><span class="sxs-lookup"><span data-stu-id="48ac6-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="48ac6-111">如果指定了 AllowDataLoss 參數，則命令只會等到新主要的主要假設角色。</span><span class="sxs-lookup"><span data-stu-id="48ac6-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="48ac6-112">示例</span><span class="sxs-lookup"><span data-stu-id="48ac6-112">EXAMPLES</span></span>

### <span data-ttu-id="48ac6-113">範例1</span><span class="sxs-lookup"><span data-stu-id="48ac6-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="48ac6-114">在容錯移轉群組中，以管道方式發出容錯移轉作業，以使資料遺失。</span><span class="sxs-lookup"><span data-stu-id="48ac6-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="48ac6-115">範例2</span><span class="sxs-lookup"><span data-stu-id="48ac6-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="48ac6-116">在不遺失資料或失敗與回滾的情況下，發出最佳的成功容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="48ac6-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="48ac6-117">參數</span><span class="sxs-lookup"><span data-stu-id="48ac6-117">PARAMETERS</span></span>

### <span data-ttu-id="48ac6-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="48ac6-118">-AllowDataLoss</span></span>
<span data-ttu-id="48ac6-119">完成容錯移轉，即使這樣做可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="48ac6-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="48ac6-120">這可讓容錯移轉即使在主要資料庫無法使用時仍能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="48ac6-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="48ac6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48ac6-121">-AsJob</span></span>
<span data-ttu-id="48ac6-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="48ac6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48ac6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ac6-123">-DefaultProfile</span></span>
<span data-ttu-id="48ac6-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="48ac6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48ac6-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="48ac6-125">-FailoverGroupName</span></span>
<span data-ttu-id="48ac6-126">Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48ac6-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="48ac6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ac6-127">-ResourceGroupName</span></span>
<span data-ttu-id="48ac6-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48ac6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="48ac6-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48ac6-129">-ServerName</span></span>
<span data-ttu-id="48ac6-130">容錯移轉群組之副 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="48ac6-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="48ac6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="48ac6-131">-Confirm</span></span>
<span data-ttu-id="48ac6-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48ac6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48ac6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ac6-133">-WhatIf</span></span>
<span data-ttu-id="48ac6-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48ac6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48ac6-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48ac6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48ac6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ac6-136">CommonParameters</span></span>
<span data-ttu-id="48ac6-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48ac6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ac6-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48ac6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ac6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="48ac6-139">INPUTS</span></span>

### <span data-ttu-id="48ac6-140">System.object</span><span class="sxs-lookup"><span data-stu-id="48ac6-140">System.String</span></span>

## <span data-ttu-id="48ac6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="48ac6-141">OUTPUTS</span></span>

### <span data-ttu-id="48ac6-142">AzureSqlFailoverGroupModel 中的 [FailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="48ac6-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="48ac6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="48ac6-143">NOTES</span></span>

## <span data-ttu-id="48ac6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="48ac6-144">RELATED LINKS</span></span>

[<span data-ttu-id="48ac6-145">新-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="48ac6-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="48ac6-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="48ac6-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="48ac6-147">AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="48ac6-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="48ac6-148">附加 AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="48ac6-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="48ac6-149">移除-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="48ac6-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="48ac6-150">移除-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="48ac6-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="48ac6-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="48ac6-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

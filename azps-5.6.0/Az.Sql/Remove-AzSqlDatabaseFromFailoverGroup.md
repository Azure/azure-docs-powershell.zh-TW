---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 556cece1b4fb22067918fb84dd1474c39d8c5aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904266"
---
# <span data-ttu-id="98c63-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c63-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="98c63-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98c63-102">SYNOPSIS</span></span>
<span data-ttu-id="98c63-103">從 Azure SQL Database 容錯移轉群組移除一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="98c63-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="98c63-104">語法</span><span class="sxs-lookup"><span data-stu-id="98c63-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98c63-105">描述</span><span class="sxs-lookup"><span data-stu-id="98c63-105">DESCRIPTION</span></span>
<span data-ttu-id="98c63-106">從指定的 Azure SQL Database 容錯移轉群組移除一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="98c63-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="98c63-107">資料庫和複製關係會保持不變，但無法再透過容錯移轉群組端點來便於使用。</span><span class="sxs-lookup"><span data-stu-id="98c63-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="98c63-108">若要取得要填入 '-Database' 參數的資料庫物件，請使用 (例如，) Cmdlet Get-AzSqlDatabase物件。</span><span class="sxs-lookup"><span data-stu-id="98c63-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="98c63-109">容錯移轉群組的主伺服器必須用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="98c63-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="98c63-110">例子</span><span class="sxs-lookup"><span data-stu-id="98c63-110">EXAMPLES</span></span>

### <span data-ttu-id="98c63-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="98c63-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="98c63-112">此命令會從容錯移轉群組移除其中一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="98c63-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="98c63-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="98c63-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="98c63-114">此命令會從容錯移轉群組移除所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="98c63-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="98c63-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="98c63-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="98c63-116">此命令會從容錯移轉群組移除一個集中資料庫的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="98c63-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="98c63-117">參數</span><span class="sxs-lookup"><span data-stu-id="98c63-117">PARAMETERS</span></span>

### <span data-ttu-id="98c63-118">-資料庫</span><span class="sxs-lookup"><span data-stu-id="98c63-118">-Database</span></span>
<span data-ttu-id="98c63-119">從容錯移轉群組中移除容錯移轉群組主伺服器的一或多個 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="98c63-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98c63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c63-120">-DefaultProfile</span></span>
<span data-ttu-id="98c63-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="98c63-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98c63-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="98c63-122">-FailoverGroupName</span></span>
<span data-ttu-id="98c63-123">Azure SQL 資料庫容錯移轉組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98c63-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="98c63-124">-強制</span><span class="sxs-lookup"><span data-stu-id="98c63-124">-Force</span></span>
<span data-ttu-id="98c63-125">跳過執行動作的確認訊息。</span><span class="sxs-lookup"><span data-stu-id="98c63-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="98c63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c63-126">-ResourceGroupName</span></span>
<span data-ttu-id="98c63-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98c63-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="98c63-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98c63-128">-ServerName</span></span>
<span data-ttu-id="98c63-129">容錯移轉群組的主要 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="98c63-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="98c63-130">-確認</span><span class="sxs-lookup"><span data-stu-id="98c63-130">-Confirm</span></span>
<span data-ttu-id="98c63-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="98c63-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c63-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c63-132">-WhatIf</span></span>
<span data-ttu-id="98c63-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98c63-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98c63-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98c63-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c63-135">CommonParameters</span></span>
<span data-ttu-id="98c63-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98c63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c63-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98c63-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c63-138">輸入</span><span class="sxs-lookup"><span data-stu-id="98c63-138">INPUTS</span></span>

### <span data-ttu-id="98c63-139">System.String</span><span class="sxs-lookup"><span data-stu-id="98c63-139">System.String</span></span>

### <span data-ttu-id="98c63-140">System.Collections.generic.List'1[[Microsoft.Azure.Commands.sql.database.Model.AzureSqlDatabaseModel，Microsoft.Azure.PowerShell.Cmdlets.Sql，Version=1.3.0.0，Culture=neutral，PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="98c63-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="98c63-141">輸出</span><span class="sxs-lookup"><span data-stu-id="98c63-141">OUTPUTS</span></span>

### <span data-ttu-id="98c63-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="98c63-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="98c63-143">筆記</span><span class="sxs-lookup"><span data-stu-id="98c63-143">NOTES</span></span>

## <span data-ttu-id="98c63-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="98c63-144">RELATED LINKS</span></span>

[<span data-ttu-id="98c63-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c63-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c63-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c63-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c63-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c63-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c63-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c63-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="98c63-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c63-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c63-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c63-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c63-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="98c63-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

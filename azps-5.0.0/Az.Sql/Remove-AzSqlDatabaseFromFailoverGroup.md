---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138083"
---
# <span data-ttu-id="b30f7-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b30f7-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="b30f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b30f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b30f7-103">從 Azure SQL Database 容錯移轉群組中移除一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="b30f7-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="b30f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b30f7-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b30f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="b30f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b30f7-106">從指定的 Azure SQL Database 容錯移轉群組中移除一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="b30f7-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="b30f7-107">資料庫與複製關聯保持不變，但無法再透過容錯移轉群組端點存取它們。</span><span class="sxs-lookup"><span data-stu-id="b30f7-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="b30f7-108">若要取得用以填入 "-Database" 參數的資料庫物件，請在 Get-AzSqlDatabase Cmdlet) 使用 (範例。</span><span class="sxs-lookup"><span data-stu-id="b30f7-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="b30f7-109">必須使用容錯移轉群組的主要伺服器來執行命令。</span><span class="sxs-lookup"><span data-stu-id="b30f7-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="b30f7-110">示例</span><span class="sxs-lookup"><span data-stu-id="b30f7-110">EXAMPLES</span></span>

### <span data-ttu-id="b30f7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b30f7-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="b30f7-112">這個命令會將一個資料庫從容錯移轉群組中移除，只要將它作為管道。</span><span class="sxs-lookup"><span data-stu-id="b30f7-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="b30f7-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b30f7-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="b30f7-114">這個命令會從容錯移轉群組中移除所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="b30f7-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="b30f7-115">範例3</span><span class="sxs-lookup"><span data-stu-id="b30f7-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="b30f7-116">這個命令會從容錯移轉群組中移除彈性池中的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="b30f7-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="b30f7-117">參數</span><span class="sxs-lookup"><span data-stu-id="b30f7-117">PARAMETERS</span></span>

### <span data-ttu-id="b30f7-118">-資料庫</span><span class="sxs-lookup"><span data-stu-id="b30f7-118">-Database</span></span>
<span data-ttu-id="b30f7-119">要從容錯移轉群組中移除之容錯移轉群組主要伺服器上的一個或多個 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b30f7-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="b30f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30f7-120">-DefaultProfile</span></span>
<span data-ttu-id="b30f7-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b30f7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b30f7-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="b30f7-122">-FailoverGroupName</span></span>
<span data-ttu-id="b30f7-123">Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b30f7-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="b30f7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b30f7-124">-Force</span></span>
<span data-ttu-id="b30f7-125">跳過確認訊息以執行動作。</span><span class="sxs-lookup"><span data-stu-id="b30f7-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="b30f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="b30f7-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b30f7-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="b30f7-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b30f7-128">-ServerName</span></span>
<span data-ttu-id="b30f7-129">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b30f7-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="b30f7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b30f7-130">-Confirm</span></span>
<span data-ttu-id="b30f7-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b30f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b30f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b30f7-132">-WhatIf</span></span>
<span data-ttu-id="b30f7-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b30f7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b30f7-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b30f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b30f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30f7-135">CommonParameters</span></span>
<span data-ttu-id="b30f7-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b30f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30f7-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b30f7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30f7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b30f7-138">INPUTS</span></span>

### <span data-ttu-id="b30f7-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b30f7-139">System.String</span></span>

### <span data-ttu-id="b30f7-140">[System.object]。清單 ' 1 [AzureSqlDatabaseModel，1.3.0.0，.sql. 2]。Sql. .Sql，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="b30f7-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b30f7-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b30f7-141">OUTPUTS</span></span>

### <span data-ttu-id="b30f7-142">AzureSqlFailoverGroupModel 中的 [FailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="b30f7-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="b30f7-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b30f7-143">NOTES</span></span>

## <span data-ttu-id="b30f7-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b30f7-144">RELATED LINKS</span></span>

[<span data-ttu-id="b30f7-145">新-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b30f7-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b30f7-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b30f7-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b30f7-147">AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b30f7-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b30f7-148">附加 AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b30f7-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="b30f7-149">切換 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b30f7-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b30f7-150">移除-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b30f7-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b30f7-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b30f7-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276043"
---
# <span data-ttu-id="9e7c3-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e7c3-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="9e7c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e7c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7c3-103">將一或多個資料庫新增至 Azure SQL Database [容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="9e7c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e7c3-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e7c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e7c3-105">DESCRIPTION</span></span>
<span data-ttu-id="9e7c3-106">在 Azure SQL Database 容錯移轉群組的主要伺服器上新增一個或多個資料庫至該容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="9e7c3-107">資料庫不得是現有複製關聯中的次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="9e7c3-108">該命令會將任何已新增資料庫的異地複製，啟動至容錯移轉群組的次要伺服器。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="9e7c3-109">若要取得用以填入 "-Database" 參數的資料庫物件，請在 Get-AzSqlDatabase Cmdlet) 使用 (範例。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="9e7c3-110">必須使用容錯移轉群組的主要伺服器來執行命令。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="9e7c3-111">示例</span><span class="sxs-lookup"><span data-stu-id="9e7c3-111">EXAMPLES</span></span>

### <span data-ttu-id="9e7c3-112">範例1</span><span class="sxs-lookup"><span data-stu-id="9e7c3-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="9e7c3-113">這個命令會將一個資料庫新增至容錯移轉群組，方法是將它輸送。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="9e7c3-114">範例2</span><span class="sxs-lookup"><span data-stu-id="9e7c3-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="9e7c3-115">這個命令會將伺服器中的所有資料庫新增至 [容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="9e7c3-116">範例3</span><span class="sxs-lookup"><span data-stu-id="9e7c3-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="9e7c3-117">這個命令會將彈性池中的所有資料庫新增至容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="9e7c3-118">參數</span><span class="sxs-lookup"><span data-stu-id="9e7c3-118">PARAMETERS</span></span>

### <span data-ttu-id="9e7c3-119">-資料庫</span><span class="sxs-lookup"><span data-stu-id="9e7c3-119">-Database</span></span>
<span data-ttu-id="9e7c3-120">要新增至容錯移轉群組之 [容錯移轉] 群組主要伺服器上的一個或多個 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="9e7c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7c3-121">-DefaultProfile</span></span>
<span data-ttu-id="9e7c3-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9e7c3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e7c3-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7c3-123">-FailoverGroupName</span></span>
<span data-ttu-id="9e7c3-124">Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="9e7c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e7c3-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e7c3-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e7c3-127">-ServerName</span></span>
<span data-ttu-id="9e7c3-128">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="9e7c3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7c3-129">CommonParameters</span></span>
<span data-ttu-id="9e7c3-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7c3-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e7c3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7c3-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9e7c3-132">INPUTS</span></span>

### <span data-ttu-id="9e7c3-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9e7c3-133">System.String</span></span>

### <span data-ttu-id="9e7c3-134">[System.object]。清單 ' 1 [AzureSqlDatabaseModel，1.3.0.0，.sql. 2]。Sql. .Sql，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="9e7c3-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9e7c3-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9e7c3-135">OUTPUTS</span></span>

### <span data-ttu-id="9e7c3-136">AzureSqlFailoverGroupModel 中的 [FailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="9e7c3-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="9e7c3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9e7c3-137">NOTES</span></span>

## <span data-ttu-id="9e7c3-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e7c3-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e7c3-139">新-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e7c3-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e7c3-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e7c3-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e7c3-141">AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e7c3-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e7c3-142">移除-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e7c3-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9e7c3-143">切換 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e7c3-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e7c3-144">移除-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e7c3-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e7c3-145">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="9e7c3-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

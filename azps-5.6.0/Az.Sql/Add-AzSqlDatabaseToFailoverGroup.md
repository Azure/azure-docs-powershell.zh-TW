---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 5c06c8e95d85e6a2b9f7c8449859edd94d9568b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904309"
---
# <span data-ttu-id="0e8ad-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0e8ad-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="0e8ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8ad-103">新增一或多個資料庫至 Azure SQL Database 容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="0e8ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e8ad-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e8ad-105">描述</span><span class="sxs-lookup"><span data-stu-id="0e8ad-105">DESCRIPTION</span></span>
<span data-ttu-id="0e8ad-106">在 Azure SQL Database 容錯移轉群組的主伺服器上新增一或多個資料庫至該容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="0e8ad-107">資料庫不能是現有複製關係中的次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="0e8ad-108">該命令會開始對新增的資料庫進行異地複製，以至容錯移轉群組的次要伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="0e8ad-109">若要取得要填入 '-Database' 參數的資料庫物件，請使用 (例如，) Cmdlet Get-AzSqlDatabase物件。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="0e8ad-110">容錯移轉群組的主伺服器必須用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="0e8ad-111">例子</span><span class="sxs-lookup"><span data-stu-id="0e8ad-111">EXAMPLES</span></span>

### <span data-ttu-id="0e8ad-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0e8ad-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="0e8ad-113">此命令會以管道將一個資料庫新增到容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="0e8ad-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="0e8ad-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="0e8ad-115">此命令會將伺服器內的所有資料庫新增到容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="0e8ad-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="0e8ad-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="0e8ad-117">此命令會將一個集中資料庫的所有資料庫新增到容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="0e8ad-118">參數</span><span class="sxs-lookup"><span data-stu-id="0e8ad-118">PARAMETERS</span></span>

### <span data-ttu-id="0e8ad-119">-資料庫</span><span class="sxs-lookup"><span data-stu-id="0e8ad-119">-Database</span></span>
<span data-ttu-id="0e8ad-120">要新增到容錯移轉群組之容錯移轉群組之容錯移轉群組上，容錯移轉群組上的一或多個 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="0e8ad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8ad-121">-DefaultProfile</span></span>
<span data-ttu-id="0e8ad-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0e8ad-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e8ad-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8ad-123">-FailoverGroupName</span></span>
<span data-ttu-id="0e8ad-124">Azure SQL 資料庫容錯移轉組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="0e8ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="0e8ad-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="0e8ad-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e8ad-127">-ServerName</span></span>
<span data-ttu-id="0e8ad-128">容錯移轉群組的主要 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="0e8ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8ad-129">CommonParameters</span></span>
<span data-ttu-id="0e8ad-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e8ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8ad-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e8ad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8ad-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0e8ad-132">INPUTS</span></span>

### <span data-ttu-id="0e8ad-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0e8ad-133">System.String</span></span>

### <span data-ttu-id="0e8ad-134">System.Collections.generic.List'1[[Microsoft.Azure.Commands.sql.database.Model.AzureSqlDatabaseModel，Microsoft.Azure.PowerShell.Cmdlets.Sql，Version=1.3.0.0，Culture=neutral，PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0e8ad-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0e8ad-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0e8ad-135">OUTPUTS</span></span>

### <span data-ttu-id="0e8ad-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="0e8ad-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="0e8ad-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0e8ad-137">NOTES</span></span>

## <span data-ttu-id="0e8ad-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e8ad-138">RELATED LINKS</span></span>

[<span data-ttu-id="0e8ad-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0e8ad-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0e8ad-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0e8ad-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0e8ad-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0e8ad-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0e8ad-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0e8ad-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="0e8ad-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0e8ad-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0e8ad-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0e8ad-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0e8ad-145">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="0e8ad-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

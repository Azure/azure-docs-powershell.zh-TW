---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: c195215bb38152287e1aa65457a5a0ff4b5452cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449711"
---
# <span data-ttu-id="df73b-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="df73b-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="df73b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df73b-102">SYNOPSIS</span></span>
<span data-ttu-id="df73b-103">將一或多個資料庫新增至 Azure SQL Database [容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="df73b-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df73b-104">句法</span><span class="sxs-lookup"><span data-stu-id="df73b-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df73b-105">說明</span><span class="sxs-lookup"><span data-stu-id="df73b-105">DESCRIPTION</span></span>
<span data-ttu-id="df73b-106">在 Azure SQL Database 容錯移轉群組的主要伺服器上新增一個或多個資料庫至該容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="df73b-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="df73b-107">資料庫不得是現有複製關聯中的次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="df73b-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="df73b-108">該命令會將任何已新增資料庫的異地複製，啟動至容錯移轉群組的次要伺服器。</span><span class="sxs-lookup"><span data-stu-id="df73b-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="df73b-109">若要取得用以填入 "-Database" 參數的資料庫物件，請在 Get-AzureRmSqlDatabase Cmdlet) 使用 (範例。</span><span class="sxs-lookup"><span data-stu-id="df73b-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>
<span data-ttu-id="df73b-110">必須使用容錯移轉群組的主要伺服器來執行命令。</span><span class="sxs-lookup"><span data-stu-id="df73b-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="df73b-111">示例</span><span class="sxs-lookup"><span data-stu-id="df73b-111">EXAMPLES</span></span>

### <span data-ttu-id="df73b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="df73b-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="df73b-113">這個命令會將一個資料庫新增至容錯移轉群組，方法是將它輸送。</span><span class="sxs-lookup"><span data-stu-id="df73b-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="df73b-114">範例2</span><span class="sxs-lookup"><span data-stu-id="df73b-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="df73b-115">這個命令會將伺服器中的所有資料庫新增至 [容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="df73b-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="df73b-116">範例3</span><span class="sxs-lookup"><span data-stu-id="df73b-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="df73b-117">這個命令會將彈性池中的所有資料庫新增至容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="df73b-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="df73b-118">參數</span><span class="sxs-lookup"><span data-stu-id="df73b-118">PARAMETERS</span></span>

### <span data-ttu-id="df73b-119">-資料庫</span><span class="sxs-lookup"><span data-stu-id="df73b-119">-Database</span></span>
<span data-ttu-id="df73b-120">要新增至容錯移轉群組之 [容錯移轉] 群組主要伺服器上的一個或多個 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="df73b-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="df73b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df73b-121">-DefaultProfile</span></span>
<span data-ttu-id="df73b-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="df73b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df73b-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="df73b-123">-FailoverGroupName</span></span>
<span data-ttu-id="df73b-124">Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df73b-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="df73b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df73b-125">-ResourceGroupName</span></span>
<span data-ttu-id="df73b-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df73b-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="df73b-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df73b-127">-ServerName</span></span>
<span data-ttu-id="df73b-128">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="df73b-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="df73b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df73b-129">CommonParameters</span></span>
<span data-ttu-id="df73b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df73b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df73b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df73b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df73b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="df73b-132">INPUTS</span></span>

### <span data-ttu-id="df73b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="df73b-133">System.String</span></span>

### <span data-ttu-id="df73b-134">[System.object]。清單 ' 1 [AzureSqlDatabaseModel，4.11.0.0，.Sql. .sql，版本 =，Culture = 中性，PublicKeyToken = null]]。））。</span><span class="sxs-lookup"><span data-stu-id="df73b-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=4.11.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="df73b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="df73b-135">OUTPUTS</span></span>

### <span data-ttu-id="df73b-136">AzureSqlFailoverGroupModel 中的 [FailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="df73b-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="df73b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="df73b-137">NOTES</span></span>

## <span data-ttu-id="df73b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="df73b-138">RELATED LINKS</span></span>

[<span data-ttu-id="df73b-139">新-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="df73b-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="df73b-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="df73b-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="df73b-141">AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="df73b-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="df73b-142">移除-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="df73b-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="df73b-143">切換 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="df73b-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="df73b-144">移除-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="df73b-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="df73b-145">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="df73b-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

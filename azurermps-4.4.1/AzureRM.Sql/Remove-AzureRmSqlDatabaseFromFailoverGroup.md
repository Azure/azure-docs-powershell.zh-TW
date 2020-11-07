---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: b796d1247d1f8a49316431ca944ac6cd1fb77d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626496"
---
# <span data-ttu-id="4bdd6-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4bdd6-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="4bdd6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bdd6-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdd6-103">從 Azure SQL Database 容錯移轉群組中移除一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bdd6-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bdd6-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bdd6-105">說明</span><span class="sxs-lookup"><span data-stu-id="4bdd6-105">DESCRIPTION</span></span>
<span data-ttu-id="4bdd6-106">從指定的 Azure SQL Database 容錯移轉群組中移除一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="4bdd6-107">資料庫與複製關聯保持不變，但無法再透過容錯移轉群組端點存取它們。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>

<span data-ttu-id="4bdd6-108">若要取得用以填入 "-Database" 參數的資料庫物件，請在 Get-AzureRmSqlDatabase Cmdlet) 使用 (範例。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="4bdd6-109">必須使用容錯移轉群組的主要伺服器來執行命令。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="4bdd6-110">示例</span><span class="sxs-lookup"><span data-stu-id="4bdd6-110">EXAMPLES</span></span>

### <span data-ttu-id="4bdd6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4bdd6-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="4bdd6-112">這個命令會將一個資料庫從容錯移轉群組中移除，只要將它作為管道。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="4bdd6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4bdd6-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="4bdd6-114">這個命令會從容錯移轉群組中移除所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="4bdd6-115">範例3</span><span class="sxs-lookup"><span data-stu-id="4bdd6-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="4bdd6-116">這個命令會從容錯移轉群組中移除彈性池中的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="4bdd6-117">參數</span><span class="sxs-lookup"><span data-stu-id="4bdd6-117">PARAMETERS</span></span>

### <span data-ttu-id="4bdd6-118">-資料庫</span><span class="sxs-lookup"><span data-stu-id="4bdd6-118">-Database</span></span>
<span data-ttu-id="4bdd6-119">要從容錯移轉群組中移除之容錯移轉群組主要伺服器上的一個或多個 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="4bdd6-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdd6-120">-FailoverGroupName</span></span>
<span data-ttu-id="4bdd6-121">Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4bdd6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4bdd6-122">-Force</span></span>
<span data-ttu-id="4bdd6-123">跳過確認訊息以執行動作。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-123">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="4bdd6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdd6-124">-ResourceGroupName</span></span>
<span data-ttu-id="4bdd6-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="4bdd6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4bdd6-126">-ServerName</span></span>
<span data-ttu-id="4bdd6-127">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-127">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4bdd6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="4bdd6-128">-Confirm</span></span>
<span data-ttu-id="4bdd6-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bdd6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdd6-130">-WhatIf</span></span>
<span data-ttu-id="4bdd6-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bdd6-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bdd6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdd6-133">-DefaultProfile</span></span>
<span data-ttu-id="4bdd6-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bdd6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdd6-135">CommonParameters</span></span>
<span data-ttu-id="4bdd6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdd6-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdd6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4bdd6-138">INPUTS</span></span>

### <span data-ttu-id="4bdd6-139">System.object</span><span class="sxs-lookup"><span data-stu-id="4bdd6-139">System.String</span></span>
<span data-ttu-id="4bdd6-140">[System.object]。清單 ' 1 [AzureSqlDatabaseModel，2.5.0.0，.Sql. .sql，版本 =，Culture = 中性，PublicKeyToken = null]]。））。</span><span class="sxs-lookup"><span data-stu-id="4bdd6-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4bdd6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4bdd6-141">OUTPUTS</span></span>

### <span data-ttu-id="4bdd6-142">System.object</span><span class="sxs-lookup"><span data-stu-id="4bdd6-142">System.Object</span></span>

## <span data-ttu-id="4bdd6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4bdd6-143">NOTES</span></span>

## <span data-ttu-id="4bdd6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bdd6-144">RELATED LINKS</span></span>

[<span data-ttu-id="4bdd6-145">新-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4bdd6-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4bdd6-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4bdd6-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4bdd6-147">AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4bdd6-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4bdd6-148">附加 AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4bdd6-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4bdd6-149">切換 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4bdd6-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4bdd6-150">移除-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4bdd6-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4bdd6-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4bdd6-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

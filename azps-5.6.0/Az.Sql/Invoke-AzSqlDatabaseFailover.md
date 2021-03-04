---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 23df8f00c91cfabf4ad01b5dd641069f159eb064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910921"
---
# <span data-ttu-id="d0275-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="d0275-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="d0275-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d0275-102">SYNOPSIS</span></span>
<span data-ttu-id="d0275-103">容錯移轉資料庫。</span><span class="sxs-lookup"><span data-stu-id="d0275-103">Failovers a database.</span></span>

## <span data-ttu-id="d0275-104">語法</span><span class="sxs-lookup"><span data-stu-id="d0275-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0275-105">描述</span><span class="sxs-lookup"><span data-stu-id="d0275-105">DESCRIPTION</span></span>
<span data-ttu-id="d0275-106">Cmdlet Invoke-AzSqlDatabaseFailover容錯移轉 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="d0275-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="d0275-107">如果資料庫位於資料庫的集中資料庫，此命令將會容錯移轉到給定資料庫，而不會影響同一個資料庫集中的其他資料庫。</span><span class="sxs-lookup"><span data-stu-id="d0275-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="d0275-108">例子</span><span class="sxs-lookup"><span data-stu-id="d0275-108">EXAMPLES</span></span>

### <span data-ttu-id="d0275-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="d0275-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d0275-110">此命令將容錯移轉名為「Server01」之伺服器上名為「資料庫01」之資料庫的主要複本</span><span class="sxs-lookup"><span data-stu-id="d0275-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="d0275-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="d0275-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="d0275-112">此命令將容錯移轉名為「Server01」之伺服器上名為「資料庫01」之資料庫的可讀取次要複本</span><span class="sxs-lookup"><span data-stu-id="d0275-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="d0275-113">參數</span><span class="sxs-lookup"><span data-stu-id="d0275-113">PARAMETERS</span></span>

### <span data-ttu-id="d0275-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0275-114">-AsJob</span></span>
<span data-ttu-id="d0275-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d0275-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0275-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0275-116">-DatabaseName</span></span>
<span data-ttu-id="d0275-117">要容錯移轉的 Azure SQL Database 名稱。</span><span class="sxs-lookup"><span data-stu-id="d0275-117">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0275-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0275-118">-DefaultProfile</span></span>
<span data-ttu-id="d0275-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0275-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0275-120">-強制</span><span class="sxs-lookup"><span data-stu-id="d0275-120">-Force</span></span>
<span data-ttu-id="d0275-121">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="d0275-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d0275-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0275-122">-PassThru</span></span>
<span data-ttu-id="d0275-123">成功執行時，會返回 True。</span><span class="sxs-lookup"><span data-stu-id="d0275-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="d0275-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d0275-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0275-125">-可讀取的秒</span><span class="sxs-lookup"><span data-stu-id="d0275-125">-ReadableSecondary</span></span>
<span data-ttu-id="d0275-126">容錯移轉可讀取的次要複本，而非預設的主複本</span><span class="sxs-lookup"><span data-stu-id="d0275-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="d0275-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0275-127">-ResourceGroupName</span></span>
<span data-ttu-id="d0275-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0275-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0275-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0275-129">-ServerName</span></span>
<span data-ttu-id="d0275-130">資料庫位於 Azure SQL Database Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0275-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="d0275-131">-確認</span><span class="sxs-lookup"><span data-stu-id="d0275-131">-Confirm</span></span>
<span data-ttu-id="d0275-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d0275-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0275-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0275-133">-WhatIf</span></span>
<span data-ttu-id="d0275-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0275-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0275-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0275-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0275-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0275-136">CommonParameters</span></span>
<span data-ttu-id="d0275-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d0275-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0275-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0275-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0275-139">輸入</span><span class="sxs-lookup"><span data-stu-id="d0275-139">INPUTS</span></span>

### <span data-ttu-id="d0275-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d0275-140">System.String</span></span>

## <span data-ttu-id="d0275-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d0275-141">OUTPUTS</span></span>

## <span data-ttu-id="d0275-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d0275-142">NOTES</span></span>

## <span data-ttu-id="d0275-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0275-143">RELATED LINKS</span></span>

[<span data-ttu-id="d0275-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d0275-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="d0275-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="d0275-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="d0275-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d0275-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="d0275-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d0275-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="d0275-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d0275-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="d0275-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d0275-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="d0275-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d0275-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="d0275-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d0275-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285635"
---
# <span data-ttu-id="49b47-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="49b47-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="49b47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49b47-102">SYNOPSIS</span></span>
<span data-ttu-id="49b47-103">針對資料庫進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="49b47-103">Failovers a database.</span></span>

## <span data-ttu-id="49b47-104">句法</span><span class="sxs-lookup"><span data-stu-id="49b47-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b47-105">說明</span><span class="sxs-lookup"><span data-stu-id="49b47-105">DESCRIPTION</span></span>
<span data-ttu-id="49b47-106">Invoke-AzSqlDatabaseFailover Cmdlet 會針對 Azure SQL 資料庫進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="49b47-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="49b47-107">如果資料庫位於彈性池中，此命令會將指定的資料庫容錯移轉，而不會影響相同彈性池中的其他資料庫。</span><span class="sxs-lookup"><span data-stu-id="49b47-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="49b47-108">示例</span><span class="sxs-lookup"><span data-stu-id="49b47-108">EXAMPLES</span></span>

### <span data-ttu-id="49b47-109">範例1</span><span class="sxs-lookup"><span data-stu-id="49b47-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="49b47-110">這個命令會將名為 "Server01" 的伺服器上名為 "Database01" 的主要複本容錯移轉</span><span class="sxs-lookup"><span data-stu-id="49b47-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="49b47-111">範例2</span><span class="sxs-lookup"><span data-stu-id="49b47-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="49b47-112">這個命令會將名為 "Server01" 的伺服器上名為 "Database01" 的可讀取輔助副本容錯移轉</span><span class="sxs-lookup"><span data-stu-id="49b47-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="49b47-113">參數</span><span class="sxs-lookup"><span data-stu-id="49b47-113">PARAMETERS</span></span>

### <span data-ttu-id="49b47-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49b47-114">-AsJob</span></span>
<span data-ttu-id="49b47-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="49b47-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49b47-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49b47-116">-DatabaseName</span></span>
<span data-ttu-id="49b47-117">要進行容錯移轉的 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="49b47-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="49b47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b47-118">-DefaultProfile</span></span>
<span data-ttu-id="49b47-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49b47-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b47-120">-Force</span><span class="sxs-lookup"><span data-stu-id="49b47-120">-Force</span></span>
<span data-ttu-id="49b47-121">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="49b47-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="49b47-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49b47-122">-PassThru</span></span>
<span data-ttu-id="49b47-123">成功執行時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="49b47-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="49b47-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="49b47-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49b47-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="49b47-125">-ReadableSecondary</span></span>
<span data-ttu-id="49b47-126">容錯移轉可讀取的次要複本，而不是預設的主要複本</span><span class="sxs-lookup"><span data-stu-id="49b47-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="49b47-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b47-127">-ResourceGroupName</span></span>
<span data-ttu-id="49b47-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49b47-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="49b47-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49b47-129">-ServerName</span></span>
<span data-ttu-id="49b47-130">資料庫所在之 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="49b47-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="49b47-131">-確認</span><span class="sxs-lookup"><span data-stu-id="49b47-131">-Confirm</span></span>
<span data-ttu-id="49b47-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49b47-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b47-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b47-133">-WhatIf</span></span>
<span data-ttu-id="49b47-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49b47-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49b47-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49b47-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b47-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b47-136">CommonParameters</span></span>
<span data-ttu-id="49b47-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49b47-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b47-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="49b47-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b47-139">輸入</span><span class="sxs-lookup"><span data-stu-id="49b47-139">INPUTS</span></span>

### <span data-ttu-id="49b47-140">System.object</span><span class="sxs-lookup"><span data-stu-id="49b47-140">System.String</span></span>

## <span data-ttu-id="49b47-141">輸出</span><span class="sxs-lookup"><span data-stu-id="49b47-141">OUTPUTS</span></span>

## <span data-ttu-id="49b47-142">筆記</span><span class="sxs-lookup"><span data-stu-id="49b47-142">NOTES</span></span>

## <span data-ttu-id="49b47-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="49b47-143">RELATED LINKS</span></span>

[<span data-ttu-id="49b47-144">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49b47-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="49b47-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="49b47-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="49b47-146">新-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49b47-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="49b47-147">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49b47-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="49b47-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49b47-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="49b47-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49b47-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="49b47-150">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49b47-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="49b47-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="49b47-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

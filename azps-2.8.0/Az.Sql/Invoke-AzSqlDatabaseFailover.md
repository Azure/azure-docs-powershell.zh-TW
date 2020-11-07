---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792735"
---
# <span data-ttu-id="3a6ea-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="3a6ea-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="3a6ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6ea-103">針對資料庫進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-103">Failovers a database.</span></span>

## <span data-ttu-id="3a6ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a6ea-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a6ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a6ea-105">DESCRIPTION</span></span>
<span data-ttu-id="3a6ea-106">Invoke-AzSqlDatabaseFailover Cmdlet 會針對 Azure SQL 資料庫進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="3a6ea-107">如果資料庫位於彈性池中，此命令會將指定的資料庫容錯移轉，而不會影響相同彈性池中的其他資料庫。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="3a6ea-108">示例</span><span class="sxs-lookup"><span data-stu-id="3a6ea-108">EXAMPLES</span></span>

### <span data-ttu-id="3a6ea-109">範例1</span><span class="sxs-lookup"><span data-stu-id="3a6ea-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="3a6ea-110">這個命令會將名為 "Server01" 的伺服器上名為 "Database01" 的資料庫容錯移轉</span><span class="sxs-lookup"><span data-stu-id="3a6ea-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="3a6ea-111">參數</span><span class="sxs-lookup"><span data-stu-id="3a6ea-111">PARAMETERS</span></span>

### <span data-ttu-id="3a6ea-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a6ea-112">-AsJob</span></span>
<span data-ttu-id="3a6ea-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3a6ea-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a6ea-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a6ea-114">-DatabaseName</span></span>
<span data-ttu-id="3a6ea-115">要進行容錯移轉的 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-115">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="3a6ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6ea-116">-DefaultProfile</span></span>
<span data-ttu-id="3a6ea-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a6ea-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3a6ea-118">-Force</span></span>
<span data-ttu-id="3a6ea-119">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="3a6ea-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3a6ea-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a6ea-120">-PassThru</span></span>
<span data-ttu-id="3a6ea-121">成功執行時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="3a6ea-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a6ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a6ea-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a6ea-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3a6ea-125">-ServerName</span></span>
<span data-ttu-id="3a6ea-126">資料庫所在之 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="3a6ea-127">-確認</span><span class="sxs-lookup"><span data-stu-id="3a6ea-127">-Confirm</span></span>
<span data-ttu-id="3a6ea-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a6ea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a6ea-129">-WhatIf</span></span>
<span data-ttu-id="3a6ea-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a6ea-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a6ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6ea-132">CommonParameters</span></span>
<span data-ttu-id="3a6ea-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6ea-134">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3a6ea-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6ea-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3a6ea-135">INPUTS</span></span>

### <span data-ttu-id="3a6ea-136">System.object</span><span class="sxs-lookup"><span data-stu-id="3a6ea-136">System.String</span></span>

## <span data-ttu-id="3a6ea-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3a6ea-137">OUTPUTS</span></span>

## <span data-ttu-id="3a6ea-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3a6ea-138">NOTES</span></span>

## <span data-ttu-id="3a6ea-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a6ea-139">RELATED LINKS</span></span>

[<span data-ttu-id="3a6ea-140">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a6ea-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="3a6ea-141">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="3a6ea-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="3a6ea-142">新-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a6ea-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="3a6ea-143">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a6ea-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="3a6ea-144">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a6ea-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="3a6ea-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a6ea-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="3a6ea-146">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a6ea-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="3a6ea-147">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="3a6ea-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

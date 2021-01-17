---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434968"
---
# <span data-ttu-id="4a258-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a258-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="4a258-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a258-102">SYNOPSIS</span></span>
<span data-ttu-id="4a258-103">暫停 SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a258-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="4a258-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a258-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a258-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a258-105">DESCRIPTION</span></span>
<span data-ttu-id="4a258-106">**AzSqlDatabase** Cmdlet 會暫停 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a258-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="4a258-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a258-107">EXAMPLES</span></span>

### <span data-ttu-id="4a258-108">範例1：暫停 Azure SQL 資料倉儲資料庫</span><span class="sxs-lookup"><span data-stu-id="4a258-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4a258-109">這個命令會暫停使用中的 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a258-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="4a258-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a258-110">PARAMETERS</span></span>

### <span data-ttu-id="4a258-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a258-111">-AsJob</span></span>
<span data-ttu-id="4a258-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4a258-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a258-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a258-113">-DatabaseName</span></span>
<span data-ttu-id="4a258-114">指定此 Cmdlet 暫停的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4a258-114">Specifies the name of the database that this cmdlet suspends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a258-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a258-115">-DefaultProfile</span></span>
<span data-ttu-id="4a258-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4a258-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a258-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a258-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a258-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a258-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4a258-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a258-119">-ServerName</span></span>
<span data-ttu-id="4a258-120">指定主機資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4a258-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="4a258-121">-確認</span><span class="sxs-lookup"><span data-stu-id="4a258-121">-Confirm</span></span>
<span data-ttu-id="4a258-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4a258-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a258-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a258-123">-WhatIf</span></span>
<span data-ttu-id="4a258-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a258-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a258-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a258-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a258-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a258-126">CommonParameters</span></span>
<span data-ttu-id="4a258-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a258-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a258-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4a258-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a258-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4a258-129">INPUTS</span></span>

### <span data-ttu-id="4a258-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4a258-130">System.String</span></span>

## <span data-ttu-id="4a258-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4a258-131">OUTPUTS</span></span>

### <span data-ttu-id="4a258-132">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="4a258-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4a258-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4a258-133">NOTES</span></span>
* <span data-ttu-id="4a258-134">**AzSqlDatabase** Cmdlet 只適用于 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a258-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="4a258-135">Azure SQL Database Basic、Standard 和 Premium 版本不支援此操作。</span><span class="sxs-lookup"><span data-stu-id="4a258-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="4a258-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a258-136">RELATED LINKS</span></span>

[<span data-ttu-id="4a258-137">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a258-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="4a258-138">新-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a258-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="4a258-139">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a258-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="4a258-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a258-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="4a258-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a258-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="4a258-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4a258-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



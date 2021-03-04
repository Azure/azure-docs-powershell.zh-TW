---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: 43284eb2f3d0cc39e5fcf5869ad26ebf0e52bd5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912289"
---
# <span data-ttu-id="0a61a-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a61a-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="0a61a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a61a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a61a-103">暫停 SQL Data Warehouse 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0a61a-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="0a61a-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a61a-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a61a-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a61a-105">DESCRIPTION</span></span>
<span data-ttu-id="0a61a-106">**Suspend-AzSqlDatabase** Cmdlet 會暫停 Azure SQL Data Warehouse 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0a61a-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="0a61a-107">例子</span><span class="sxs-lookup"><span data-stu-id="0a61a-107">EXAMPLES</span></span>

### <span data-ttu-id="0a61a-108">範例 1：暫停 Azure SQL Data Warehouse 資料庫</span><span class="sxs-lookup"><span data-stu-id="0a61a-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="0a61a-109">此命令會暫停使用中的 Azure SQL Data Warehouse 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0a61a-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="0a61a-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a61a-110">PARAMETERS</span></span>

### <span data-ttu-id="0a61a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a61a-111">-AsJob</span></span>
<span data-ttu-id="0a61a-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a61a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a61a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a61a-113">-DatabaseName</span></span>
<span data-ttu-id="0a61a-114">指定此 Cmdlet 暫停的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0a61a-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="0a61a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a61a-115">-DefaultProfile</span></span>
<span data-ttu-id="0a61a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0a61a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a61a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a61a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a61a-118">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0a61a-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0a61a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a61a-119">-ServerName</span></span>
<span data-ttu-id="0a61a-120">指定主託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0a61a-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="0a61a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="0a61a-121">-Confirm</span></span>
<span data-ttu-id="0a61a-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a61a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a61a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a61a-123">-WhatIf</span></span>
<span data-ttu-id="0a61a-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a61a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a61a-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a61a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a61a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a61a-126">CommonParameters</span></span>
<span data-ttu-id="0a61a-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a61a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a61a-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a61a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a61a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0a61a-129">INPUTS</span></span>

### <span data-ttu-id="0a61a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0a61a-130">System.String</span></span>

## <span data-ttu-id="0a61a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0a61a-131">OUTPUTS</span></span>

### <span data-ttu-id="0a61a-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0a61a-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0a61a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0a61a-133">NOTES</span></span>
* <span data-ttu-id="0a61a-134">**Suspend-AzSqlDatabase** Cmdlet 僅適用于 Azure SQL Data Warehouse 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0a61a-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="0a61a-135">Azure SQL Database Basic、Standard 和 Premium 版本不支援此作業。</span><span class="sxs-lookup"><span data-stu-id="0a61a-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="0a61a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a61a-136">RELATED LINKS</span></span>

[<span data-ttu-id="0a61a-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a61a-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0a61a-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a61a-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="0a61a-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a61a-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="0a61a-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a61a-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="0a61a-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a61a-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="0a61a-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="0a61a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



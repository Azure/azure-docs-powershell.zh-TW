---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797450"
---
# <span data-ttu-id="6c203-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c203-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="6c203-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c203-102">SYNOPSIS</span></span>
<span data-ttu-id="6c203-103">移除 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6c203-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="6c203-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c203-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c203-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c203-105">DESCRIPTION</span></span>
<span data-ttu-id="6c203-106">**AzSqlDatabase** Cmdlet 會移除 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6c203-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="6c203-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c203-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6c203-108">示例</span><span class="sxs-lookup"><span data-stu-id="6c203-108">EXAMPLES</span></span>

### <span data-ttu-id="6c203-109">範例1：從 Azure SQL server 移除資料庫</span><span class="sxs-lookup"><span data-stu-id="6c203-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="6c203-110">這個命令會從伺服器 Server01 中移除名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6c203-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="6c203-111">參數</span><span class="sxs-lookup"><span data-stu-id="6c203-111">PARAMETERS</span></span>

### <span data-ttu-id="6c203-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6c203-112">-DatabaseName</span></span>
<span data-ttu-id="6c203-113">指定此 Cmdlet 移除之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c203-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6c203-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c203-114">-DefaultProfile</span></span>
<span data-ttu-id="6c203-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6c203-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c203-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6c203-116">-Force</span></span>
<span data-ttu-id="6c203-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6c203-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6c203-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c203-118">-ResourceGroupName</span></span>
<span data-ttu-id="6c203-119">指定指派給資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c203-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="6c203-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6c203-120">-ServerName</span></span>
<span data-ttu-id="6c203-121">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6c203-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="6c203-122">-確認</span><span class="sxs-lookup"><span data-stu-id="6c203-122">-Confirm</span></span>
<span data-ttu-id="6c203-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c203-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c203-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c203-124">-WhatIf</span></span>
<span data-ttu-id="6c203-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c203-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c203-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c203-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c203-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c203-127">CommonParameters</span></span>
<span data-ttu-id="6c203-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c203-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c203-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c203-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c203-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6c203-130">INPUTS</span></span>

### <span data-ttu-id="6c203-131">System.object</span><span class="sxs-lookup"><span data-stu-id="6c203-131">System.String</span></span>

## <span data-ttu-id="6c203-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6c203-132">OUTPUTS</span></span>

### <span data-ttu-id="6c203-133">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="6c203-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="6c203-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6c203-134">NOTES</span></span>

## <span data-ttu-id="6c203-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c203-135">RELATED LINKS</span></span>

[<span data-ttu-id="6c203-136">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c203-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="6c203-137">新-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c203-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="6c203-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c203-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="6c203-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c203-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="6c203-140">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c203-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="6c203-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="6c203-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 2a4142c7d8bb0f48bf75613b214dccd1876c5264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903410"
---
# <span data-ttu-id="864ab-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="864ab-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="864ab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="864ab-102">SYNOPSIS</span></span>
<span data-ttu-id="864ab-103">移除 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="864ab-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="864ab-104">語法</span><span class="sxs-lookup"><span data-stu-id="864ab-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="864ab-105">描述</span><span class="sxs-lookup"><span data-stu-id="864ab-105">DESCRIPTION</span></span>
<span data-ttu-id="864ab-106">**Remove-AzSqlDatabase** Cmdlet 會移除 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="864ab-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="864ab-107">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="864ab-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="864ab-108">例子</span><span class="sxs-lookup"><span data-stu-id="864ab-108">EXAMPLES</span></span>

### <span data-ttu-id="864ab-109">範例 1：從 Azure SQL 伺服器移除資料庫</span><span class="sxs-lookup"><span data-stu-id="864ab-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="864ab-110">此命令會從伺服器 Server01 移除名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="864ab-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="864ab-111">參數</span><span class="sxs-lookup"><span data-stu-id="864ab-111">PARAMETERS</span></span>

### <span data-ttu-id="864ab-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="864ab-112">-DatabaseName</span></span>
<span data-ttu-id="864ab-113">指定此 Cmdlet 移除的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="864ab-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="864ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864ab-114">-DefaultProfile</span></span>
<span data-ttu-id="864ab-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="864ab-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="864ab-116">-強制</span><span class="sxs-lookup"><span data-stu-id="864ab-116">-Force</span></span>
<span data-ttu-id="864ab-117">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="864ab-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="864ab-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="864ab-118">-ResourceGroupName</span></span>
<span data-ttu-id="864ab-119">指定指派資料庫的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="864ab-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="864ab-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="864ab-120">-ServerName</span></span>
<span data-ttu-id="864ab-121">指定主資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="864ab-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="864ab-122">-確認</span><span class="sxs-lookup"><span data-stu-id="864ab-122">-Confirm</span></span>
<span data-ttu-id="864ab-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="864ab-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="864ab-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="864ab-124">-WhatIf</span></span>
<span data-ttu-id="864ab-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="864ab-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="864ab-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="864ab-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="864ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864ab-127">CommonParameters</span></span>
<span data-ttu-id="864ab-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="864ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864ab-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="864ab-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864ab-130">輸入</span><span class="sxs-lookup"><span data-stu-id="864ab-130">INPUTS</span></span>

### <span data-ttu-id="864ab-131">System.String</span><span class="sxs-lookup"><span data-stu-id="864ab-131">System.String</span></span>

## <span data-ttu-id="864ab-132">輸出</span><span class="sxs-lookup"><span data-stu-id="864ab-132">OUTPUTS</span></span>

### <span data-ttu-id="864ab-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="864ab-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="864ab-134">筆記</span><span class="sxs-lookup"><span data-stu-id="864ab-134">NOTES</span></span>

## <span data-ttu-id="864ab-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="864ab-135">RELATED LINKS</span></span>

[<span data-ttu-id="864ab-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="864ab-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="864ab-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="864ab-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="864ab-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="864ab-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="864ab-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="864ab-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="864ab-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="864ab-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="864ab-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="864ab-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



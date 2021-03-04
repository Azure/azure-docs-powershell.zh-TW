---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: 3ba3703882371975ee9b0d2f87bd03b75b58e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913062"
---
# <span data-ttu-id="42b7b-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42b7b-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="42b7b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="42b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="42b7b-103">繼續 SQL Data Warehouse 資料庫。</span><span class="sxs-lookup"><span data-stu-id="42b7b-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="42b7b-104">語法</span><span class="sxs-lookup"><span data-stu-id="42b7b-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42b7b-105">描述</span><span class="sxs-lookup"><span data-stu-id="42b7b-105">DESCRIPTION</span></span>
<span data-ttu-id="42b7b-106">**Resume-AzSqlDatabase** Cmdlet 會繼續 Azure SQL Data Warehouse 資料庫。</span><span class="sxs-lookup"><span data-stu-id="42b7b-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="42b7b-107">例子</span><span class="sxs-lookup"><span data-stu-id="42b7b-107">EXAMPLES</span></span>

### <span data-ttu-id="42b7b-108">範例 1：繼續 Azure SQL Data Warehouse 資料庫</span><span class="sxs-lookup"><span data-stu-id="42b7b-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="42b7b-109">此命令會繼續暫停的 Azure SQL Data Warehouse 資料庫。</span><span class="sxs-lookup"><span data-stu-id="42b7b-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="42b7b-110">參數</span><span class="sxs-lookup"><span data-stu-id="42b7b-110">PARAMETERS</span></span>

### <span data-ttu-id="42b7b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42b7b-111">-AsJob</span></span>
<span data-ttu-id="42b7b-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42b7b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42b7b-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42b7b-113">-DatabaseName</span></span>
<span data-ttu-id="42b7b-114">指定此 Cmdlet 繼續執行的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7b-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="42b7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b7b-115">-DefaultProfile</span></span>
<span data-ttu-id="42b7b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="42b7b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42b7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="42b7b-118">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="42b7b-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="42b7b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42b7b-119">-ServerName</span></span>
<span data-ttu-id="42b7b-120">指定主管此 Cmdlet 繼續之資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7b-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="42b7b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="42b7b-121">-Confirm</span></span>
<span data-ttu-id="42b7b-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="42b7b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42b7b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42b7b-123">-WhatIf</span></span>
<span data-ttu-id="42b7b-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42b7b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42b7b-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42b7b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42b7b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b7b-126">CommonParameters</span></span>
<span data-ttu-id="42b7b-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="42b7b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b7b-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42b7b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b7b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="42b7b-129">INPUTS</span></span>

### <span data-ttu-id="42b7b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="42b7b-130">System.String</span></span>

## <span data-ttu-id="42b7b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="42b7b-131">OUTPUTS</span></span>

### <span data-ttu-id="42b7b-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="42b7b-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="42b7b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="42b7b-133">NOTES</span></span>
* <span data-ttu-id="42b7b-134">**Resume-AzSqlDatabase** Cmdlet 僅適用于 Azure SQL Data Warehouse 資料庫。</span><span class="sxs-lookup"><span data-stu-id="42b7b-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="42b7b-135">Azure SQL Database Basic、Standard 和 Premium 版本不支援此作業。</span><span class="sxs-lookup"><span data-stu-id="42b7b-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="42b7b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="42b7b-136">RELATED LINKS</span></span>

[<span data-ttu-id="42b7b-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42b7b-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="42b7b-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42b7b-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="42b7b-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42b7b-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="42b7b-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42b7b-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="42b7b-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42b7b-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="42b7b-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="42b7b-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



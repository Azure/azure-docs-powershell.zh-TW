---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: c5f30388e1e3cb804aa0ef8d45e0afe34a1d2cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792395"
---
# <span data-ttu-id="b401f-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b401f-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="b401f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b401f-102">SYNOPSIS</span></span>
<span data-ttu-id="b401f-103">繼續 SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="b401f-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="b401f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b401f-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b401f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b401f-105">DESCRIPTION</span></span>
<span data-ttu-id="b401f-106">**Resume AzSqlDatabase** Cmdlet 會繼續執行 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="b401f-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="b401f-107">示例</span><span class="sxs-lookup"><span data-stu-id="b401f-107">EXAMPLES</span></span>

### <span data-ttu-id="b401f-108">範例1：繼續執行 Azure SQL 資料倉儲資料庫</span><span class="sxs-lookup"><span data-stu-id="b401f-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b401f-109">這個命令會繼續執行暫停的 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="b401f-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="b401f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b401f-110">PARAMETERS</span></span>

### <span data-ttu-id="b401f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b401f-111">-AsJob</span></span>
<span data-ttu-id="b401f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b401f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b401f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b401f-113">-DatabaseName</span></span>
<span data-ttu-id="b401f-114">指定此 Cmdlet 繼續的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b401f-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="b401f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b401f-115">-DefaultProfile</span></span>
<span data-ttu-id="b401f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b401f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b401f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b401f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b401f-118">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b401f-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b401f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b401f-119">-ServerName</span></span>
<span data-ttu-id="b401f-120">指定此 Cmdlet 繼續的宿主資料庫所在伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b401f-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="b401f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b401f-121">-Confirm</span></span>
<span data-ttu-id="b401f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b401f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b401f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b401f-123">-WhatIf</span></span>
<span data-ttu-id="b401f-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b401f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b401f-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b401f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b401f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b401f-126">CommonParameters</span></span>
<span data-ttu-id="b401f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b401f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b401f-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b401f-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b401f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b401f-129">INPUTS</span></span>

### <span data-ttu-id="b401f-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b401f-130">System.String</span></span>

## <span data-ttu-id="b401f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b401f-131">OUTPUTS</span></span>

### <span data-ttu-id="b401f-132">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="b401f-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b401f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b401f-133">NOTES</span></span>
* <span data-ttu-id="b401f-134">**Resume AzSqlDatabase** Cmdlet 只適用于 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="b401f-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="b401f-135">Azure SQL Database Basic、Standard 和 Premium 版本不支援此操作。</span><span class="sxs-lookup"><span data-stu-id="b401f-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="b401f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b401f-136">RELATED LINKS</span></span>

[<span data-ttu-id="b401f-137">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b401f-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b401f-138">新-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b401f-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="b401f-139">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b401f-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="b401f-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b401f-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="b401f-141">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b401f-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="b401f-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b401f-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



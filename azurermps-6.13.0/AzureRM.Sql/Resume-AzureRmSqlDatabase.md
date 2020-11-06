---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/resume-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: 5681b046afb6682809d9b2dc744784514c2aefa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449702"
---
# <span data-ttu-id="a22ab-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a22ab-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="a22ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a22ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a22ab-103">繼續 SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="a22ab-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a22ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="a22ab-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a22ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="a22ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a22ab-106">**Resume AzureRmSqlDatabase** Cmdlet 會繼續執行 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="a22ab-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a22ab-107">示例</span><span class="sxs-lookup"><span data-stu-id="a22ab-107">EXAMPLES</span></span>

### <span data-ttu-id="a22ab-108">範例1：繼續執行 Azure SQL 資料倉儲資料庫</span><span class="sxs-lookup"><span data-stu-id="a22ab-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a22ab-109">這個命令會繼續執行暫停的 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="a22ab-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a22ab-110">參數</span><span class="sxs-lookup"><span data-stu-id="a22ab-110">PARAMETERS</span></span>

### <span data-ttu-id="a22ab-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a22ab-111">-AsJob</span></span>
<span data-ttu-id="a22ab-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a22ab-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a22ab-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a22ab-113">-DatabaseName</span></span>
<span data-ttu-id="a22ab-114">指定此 Cmdlet 繼續的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a22ab-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="a22ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a22ab-115">-DefaultProfile</span></span>
<span data-ttu-id="a22ab-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a22ab-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a22ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a22ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="a22ab-118">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a22ab-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a22ab-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a22ab-119">-ServerName</span></span>
<span data-ttu-id="a22ab-120">指定此 Cmdlet 繼續的宿主資料庫所在伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a22ab-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="a22ab-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a22ab-121">-Confirm</span></span>
<span data-ttu-id="a22ab-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a22ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a22ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a22ab-123">-WhatIf</span></span>
<span data-ttu-id="a22ab-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a22ab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a22ab-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a22ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a22ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22ab-126">CommonParameters</span></span>
<span data-ttu-id="a22ab-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a22ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22ab-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a22ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22ab-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a22ab-129">INPUTS</span></span>

### <span data-ttu-id="a22ab-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a22ab-130">System.String</span></span>

## <span data-ttu-id="a22ab-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a22ab-131">OUTPUTS</span></span>

### <span data-ttu-id="a22ab-132">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="a22ab-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a22ab-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a22ab-133">NOTES</span></span>
* <span data-ttu-id="a22ab-134">**Resume AzureRmSqlDatabase** Cmdlet 只適用于 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="a22ab-134">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="a22ab-135">Azure SQL Database Basic、Standard 和 Premium 版本不支援此操作。</span><span class="sxs-lookup"><span data-stu-id="a22ab-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="a22ab-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a22ab-136">RELATED LINKS</span></span>

[<span data-ttu-id="a22ab-137">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a22ab-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a22ab-138">新-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a22ab-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="a22ab-139">移除-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a22ab-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="a22ab-140">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a22ab-140">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="a22ab-141">暫停-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a22ab-141">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="a22ab-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a22ab-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



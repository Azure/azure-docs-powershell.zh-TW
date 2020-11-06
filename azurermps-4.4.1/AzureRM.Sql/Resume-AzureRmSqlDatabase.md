---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: f3554aa2e7f4970b3fa1752077a25e02d631abbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457224"
---
# <span data-ttu-id="37fbe-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37fbe-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="37fbe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="37fbe-103">繼續 SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="37fbe-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37fbe-104">句法</span><span class="sxs-lookup"><span data-stu-id="37fbe-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37fbe-105">說明</span><span class="sxs-lookup"><span data-stu-id="37fbe-105">DESCRIPTION</span></span>
<span data-ttu-id="37fbe-106">**Resume AzureRmSqlDatabase** Cmdlet 會繼續執行 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="37fbe-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="37fbe-107">示例</span><span class="sxs-lookup"><span data-stu-id="37fbe-107">EXAMPLES</span></span>

### <span data-ttu-id="37fbe-108">範例1：繼續執行 Azure SQL 資料倉儲資料庫</span><span class="sxs-lookup"><span data-stu-id="37fbe-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="37fbe-109">這個命令會繼續執行暫停的 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="37fbe-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="37fbe-110">參數</span><span class="sxs-lookup"><span data-stu-id="37fbe-110">PARAMETERS</span></span>

### <span data-ttu-id="37fbe-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="37fbe-111">-DatabaseName</span></span>
<span data-ttu-id="37fbe-112">指定此 Cmdlet 繼續的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="37fbe-112">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="37fbe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37fbe-113">-ResourceGroupName</span></span>
<span data-ttu-id="37fbe-114">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37fbe-114">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="37fbe-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37fbe-115">-ServerName</span></span>
<span data-ttu-id="37fbe-116">指定此 Cmdlet 繼續的宿主資料庫所在伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="37fbe-116">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="37fbe-117">-確認</span><span class="sxs-lookup"><span data-stu-id="37fbe-117">-Confirm</span></span>
<span data-ttu-id="37fbe-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37fbe-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37fbe-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37fbe-119">-WhatIf</span></span>
<span data-ttu-id="37fbe-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37fbe-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37fbe-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37fbe-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37fbe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fbe-122">-DefaultProfile</span></span>
<span data-ttu-id="37fbe-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37fbe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37fbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fbe-124">CommonParameters</span></span>
<span data-ttu-id="37fbe-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37fbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37fbe-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37fbe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fbe-127">輸入</span><span class="sxs-lookup"><span data-stu-id="37fbe-127">INPUTS</span></span>

### <span data-ttu-id="37fbe-128">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="37fbe-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="37fbe-129">輸出</span><span class="sxs-lookup"><span data-stu-id="37fbe-129">OUTPUTS</span></span>

### <span data-ttu-id="37fbe-130">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="37fbe-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="37fbe-131">筆記</span><span class="sxs-lookup"><span data-stu-id="37fbe-131">NOTES</span></span>
* <span data-ttu-id="37fbe-132">**Resume AzureRmSqlDatabase** Cmdlet 只適用于 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="37fbe-132">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="37fbe-133">Azure SQL Database Basic、Standard 和 Premium 版本不支援此操作。</span><span class="sxs-lookup"><span data-stu-id="37fbe-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="37fbe-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="37fbe-134">RELATED LINKS</span></span>

[<span data-ttu-id="37fbe-135">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37fbe-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="37fbe-136">新-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37fbe-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="37fbe-137">移除-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37fbe-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="37fbe-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37fbe-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="37fbe-139">暫停-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37fbe-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="37fbe-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="37fbe-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



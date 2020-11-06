---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454807"
---
# <span data-ttu-id="9fe93-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe93-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="9fe93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9fe93-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe93-103">暫停 SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="9fe93-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fe93-104">句法</span><span class="sxs-lookup"><span data-stu-id="9fe93-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe93-105">說明</span><span class="sxs-lookup"><span data-stu-id="9fe93-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe93-106">**AzureRmSqlDatabase** Cmdlet 會暫停 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="9fe93-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="9fe93-107">示例</span><span class="sxs-lookup"><span data-stu-id="9fe93-107">EXAMPLES</span></span>

### <span data-ttu-id="9fe93-108">範例1：暫停 Azure SQL 資料倉儲資料庫</span><span class="sxs-lookup"><span data-stu-id="9fe93-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="9fe93-109">這個命令會暫停使用中的 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="9fe93-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="9fe93-110">參數</span><span class="sxs-lookup"><span data-stu-id="9fe93-110">PARAMETERS</span></span>

### <span data-ttu-id="9fe93-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9fe93-111">-DatabaseName</span></span>
<span data-ttu-id="9fe93-112">指定此 Cmdlet 暫停的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe93-112">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="9fe93-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe93-113">-ResourceGroupName</span></span>
<span data-ttu-id="9fe93-114">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe93-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9fe93-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9fe93-115">-ServerName</span></span>
<span data-ttu-id="9fe93-116">指定主機資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="9fe93-116">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="9fe93-117">-確認</span><span class="sxs-lookup"><span data-stu-id="9fe93-117">-Confirm</span></span>
<span data-ttu-id="9fe93-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9fe93-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe93-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe93-119">-WhatIf</span></span>
<span data-ttu-id="9fe93-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9fe93-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe93-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9fe93-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe93-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe93-122">-DefaultProfile</span></span>
<span data-ttu-id="9fe93-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fe93-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fe93-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe93-124">CommonParameters</span></span>
<span data-ttu-id="9fe93-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9fe93-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe93-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9fe93-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe93-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9fe93-127">INPUTS</span></span>

### <span data-ttu-id="9fe93-128">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="9fe93-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9fe93-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9fe93-129">OUTPUTS</span></span>

### <span data-ttu-id="9fe93-130">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="9fe93-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9fe93-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9fe93-131">NOTES</span></span>
* <span data-ttu-id="9fe93-132">**AzureRmSqlDatabase** Cmdlet 只適用于 Azure SQL 資料倉儲資料庫。</span><span class="sxs-lookup"><span data-stu-id="9fe93-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="9fe93-133">Azure SQL Database Basic、Standard 和 Premium 版本不支援此操作。</span><span class="sxs-lookup"><span data-stu-id="9fe93-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="9fe93-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fe93-134">RELATED LINKS</span></span>

[<span data-ttu-id="9fe93-135">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe93-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="9fe93-136">新-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe93-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="9fe93-137">移除-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe93-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="9fe93-138">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe93-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="9fe93-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe93-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="9fe93-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="9fe93-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



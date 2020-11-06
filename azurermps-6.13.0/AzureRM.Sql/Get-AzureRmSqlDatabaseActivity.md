---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 08c5778002a80bb4fb2effdd977f134079f3aa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451040"
---
# <span data-ttu-id="41cb2-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="41cb2-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="41cb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="41cb2-103">取得資料庫操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="41cb2-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41cb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="41cb2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41cb2-105">說明</span><span class="sxs-lookup"><span data-stu-id="41cb2-105">DESCRIPTION</span></span>
<span data-ttu-id="41cb2-106">**AzureRmSqlDatabaseActivity** Cmdlet 會取得 Azure SQL 資料庫中資料庫作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="41cb2-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="41cb2-107">示例</span><span class="sxs-lookup"><span data-stu-id="41cb2-107">EXAMPLES</span></span>

### <span data-ttu-id="41cb2-108">範例1：取得所有 SQL 資料庫實例的狀態</span><span class="sxs-lookup"><span data-stu-id="41cb2-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="41cb2-109">這個命令會傳回一個名為 ElasticPool01 的彈性池中所有 SQL 資料庫實例的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="41cb2-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="41cb2-110">範例2：取得所有 SQL 資料庫作業的狀態</span><span class="sxs-lookup"><span data-stu-id="41cb2-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="41cb2-111">這個命令會傳回資料庫中所有 SQL 資料庫操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="41cb2-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="41cb2-112">參數</span><span class="sxs-lookup"><span data-stu-id="41cb2-112">PARAMETERS</span></span>

### <span data-ttu-id="41cb2-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41cb2-113">-DatabaseName</span></span>
<span data-ttu-id="41cb2-114">指定此 Cmdlet 取得狀態之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="41cb2-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="41cb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cb2-115">-DefaultProfile</span></span>
<span data-ttu-id="41cb2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41cb2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41cb2-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="41cb2-117">-ElasticPoolName</span></span>
<span data-ttu-id="41cb2-118">指定此 Cmdlet 取得狀態的彈性資料庫池的名稱。</span><span class="sxs-lookup"><span data-stu-id="41cb2-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41cb2-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="41cb2-119">-OperationId</span></span>
<span data-ttu-id="41cb2-120">指定此 Cmdlet 取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="41cb2-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41cb2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cb2-121">-ResourceGroupName</span></span>
<span data-ttu-id="41cb2-122">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="41cb2-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="41cb2-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="41cb2-123">-ServerName</span></span>
<span data-ttu-id="41cb2-124">指定裝載資料庫之 Microsoft SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="41cb2-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="41cb2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="41cb2-125">-Confirm</span></span>
<span data-ttu-id="41cb2-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41cb2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41cb2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cb2-127">-WhatIf</span></span>
<span data-ttu-id="41cb2-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41cb2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41cb2-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41cb2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41cb2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cb2-130">CommonParameters</span></span>
<span data-ttu-id="41cb2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41cb2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cb2-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41cb2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cb2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="41cb2-133">INPUTS</span></span>

### <span data-ttu-id="41cb2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="41cb2-134">System.String</span></span>

### <span data-ttu-id="41cb2-135">系統. Nullable "1 [[System. Guid，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="41cb2-135">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="41cb2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="41cb2-136">OUTPUTS</span></span>

### <span data-ttu-id="41cb2-137">AzureSqlDatabaseActivityModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="41cb2-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="41cb2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="41cb2-138">NOTES</span></span>

## <span data-ttu-id="41cb2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="41cb2-139">RELATED LINKS</span></span>
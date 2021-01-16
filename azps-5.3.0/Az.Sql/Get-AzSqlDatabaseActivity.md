---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285771"
---
# <span data-ttu-id="e0fb3-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="e0fb3-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="e0fb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="e0fb3-103">取得資料庫操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="e0fb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0fb3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0fb3-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="e0fb3-106">**AzSqlDatabaseActivity** Cmdlet 會取得 Azure SQL 資料庫中資料庫作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="e0fb3-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0fb3-107">EXAMPLES</span></span>

### <span data-ttu-id="e0fb3-108">範例1：取得所有 SQL 資料庫實例的狀態</span><span class="sxs-lookup"><span data-stu-id="e0fb3-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="e0fb3-109">這個命令會傳回一個名為 ElasticPool01 的彈性池中所有 SQL 資料庫實例的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="e0fb3-110">範例2：取得所有 SQL 資料庫作業的狀態</span><span class="sxs-lookup"><span data-stu-id="e0fb3-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="e0fb3-111">這個命令會傳回資料庫中所有 SQL 資料庫操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="e0fb3-112">參數</span><span class="sxs-lookup"><span data-stu-id="e0fb3-112">PARAMETERS</span></span>

### <span data-ttu-id="e0fb3-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e0fb3-113">-DatabaseName</span></span>
<span data-ttu-id="e0fb3-114">指定此 Cmdlet 取得狀態之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="e0fb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0fb3-115">-DefaultProfile</span></span>
<span data-ttu-id="e0fb3-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0fb3-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e0fb3-117">-ElasticPoolName</span></span>
<span data-ttu-id="e0fb3-118">指定此 Cmdlet 取得狀態的彈性資料庫池的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="e0fb3-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e0fb3-119">-OperationId</span></span>
<span data-ttu-id="e0fb3-120">指定此 Cmdlet 取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e0fb3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0fb3-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0fb3-122">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e0fb3-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0fb3-123">-ServerName</span></span>
<span data-ttu-id="e0fb3-124">指定裝載資料庫之 Microsoft SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="e0fb3-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e0fb3-125">-Confirm</span></span>
<span data-ttu-id="e0fb3-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0fb3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0fb3-127">-WhatIf</span></span>
<span data-ttu-id="e0fb3-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0fb3-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0fb3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0fb3-130">CommonParameters</span></span>
<span data-ttu-id="e0fb3-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0fb3-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0fb3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e0fb3-133">INPUTS</span></span>

### <span data-ttu-id="e0fb3-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e0fb3-134">System.String</span></span>

### <span data-ttu-id="e0fb3-135">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e0fb3-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e0fb3-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e0fb3-136">OUTPUTS</span></span>

### <span data-ttu-id="e0fb3-137">AzureSqlDatabaseActivityModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="e0fb3-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="e0fb3-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e0fb3-138">NOTES</span></span>

## <span data-ttu-id="e0fb3-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0fb3-139">RELATED LINKS</span></span>

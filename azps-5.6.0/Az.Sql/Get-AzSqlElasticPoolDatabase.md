---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 4a9e128fb8c67c44329dd2b99da8ce4722835323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914337"
---
# <span data-ttu-id="919eb-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="919eb-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="919eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="919eb-102">SYNOPSIS</span></span>
<span data-ttu-id="919eb-103">在彈性資料庫及其屬性值中，獲得彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="919eb-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="919eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="919eb-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="919eb-105">描述</span><span class="sxs-lookup"><span data-stu-id="919eb-105">DESCRIPTION</span></span>
<span data-ttu-id="919eb-106">**Get-AzSqlElasticPoolDatabase** Cmdlet 會取得一個壓縮資料庫及其屬性值中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="919eb-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="919eb-107">您可以在 Azure SQL Database 中指定彈性資料庫的名稱，只查看該資料庫的屬性值。</span><span class="sxs-lookup"><span data-stu-id="919eb-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="919eb-108">例子</span><span class="sxs-lookup"><span data-stu-id="919eb-108">EXAMPLES</span></span>

### <span data-ttu-id="919eb-109">範例 1：取得資料庫集中的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="919eb-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="919eb-110">此命令會獲得位於一個名為Pool01 的集中資料庫。</span><span class="sxs-lookup"><span data-stu-id="919eb-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="919eb-111">範例 2：使用篩選取得資料庫集中的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="919eb-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="919eb-112">此命令會獲得名稱為「資料庫」之一個名為「Pool01」的集中資料庫。</span><span class="sxs-lookup"><span data-stu-id="919eb-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="919eb-113">參數</span><span class="sxs-lookup"><span data-stu-id="919eb-113">PARAMETERS</span></span>

### <span data-ttu-id="919eb-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="919eb-114">-DatabaseName</span></span>
<span data-ttu-id="919eb-115">指定此 Cmdlet 所獲取的 SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="919eb-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="919eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919eb-116">-DefaultProfile</span></span>
<span data-ttu-id="919eb-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="919eb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="919eb-118">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="919eb-118">-ElasticPoolName</span></span>
<span data-ttu-id="919eb-119">指定泳層資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="919eb-119">Specifies the name of an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="919eb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="919eb-120">-ResourceGroupName</span></span>
<span data-ttu-id="919eb-121">指定指派了壓縮資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="919eb-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="919eb-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="919eb-122">-ServerName</span></span>
<span data-ttu-id="919eb-123">指定包含集區集區的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="919eb-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="919eb-124">-確認</span><span class="sxs-lookup"><span data-stu-id="919eb-124">-Confirm</span></span>
<span data-ttu-id="919eb-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="919eb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="919eb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="919eb-126">-WhatIf</span></span>
<span data-ttu-id="919eb-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="919eb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="919eb-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="919eb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="919eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919eb-129">CommonParameters</span></span>
<span data-ttu-id="919eb-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="919eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919eb-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="919eb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919eb-132">輸入</span><span class="sxs-lookup"><span data-stu-id="919eb-132">INPUTS</span></span>

### <span data-ttu-id="919eb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="919eb-133">System.String</span></span>

## <span data-ttu-id="919eb-134">輸出</span><span class="sxs-lookup"><span data-stu-id="919eb-134">OUTPUTS</span></span>

### <span data-ttu-id="919eb-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="919eb-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="919eb-136">筆記</span><span class="sxs-lookup"><span data-stu-id="919eb-136">NOTES</span></span>

## <span data-ttu-id="919eb-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="919eb-137">RELATED LINKS</span></span>

[<span data-ttu-id="919eb-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="919eb-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="919eb-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="919eb-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="919eb-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="919eb-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="919eb-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="919eb-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="919eb-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="919eb-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


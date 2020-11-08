---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970128"
---
# <span data-ttu-id="cc331-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="cc331-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="cc331-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc331-102">SYNOPSIS</span></span>
<span data-ttu-id="cc331-103">在彈性池中取得彈性資料庫及其屬性值。</span><span class="sxs-lookup"><span data-stu-id="cc331-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="cc331-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc331-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc331-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc331-105">DESCRIPTION</span></span>
<span data-ttu-id="cc331-106">**AzSqlElasticPoolDatabase** Cmdlet 會在彈性池中取得彈性資料庫及其屬性值。</span><span class="sxs-lookup"><span data-stu-id="cc331-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="cc331-107">您可以在 Azure SQL Database 中指定彈性資料庫的名稱，只查看該資料庫的屬性值。</span><span class="sxs-lookup"><span data-stu-id="cc331-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="cc331-108">示例</span><span class="sxs-lookup"><span data-stu-id="cc331-108">EXAMPLES</span></span>

### <span data-ttu-id="cc331-109">範例1：取得彈性池中的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="cc331-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="cc331-110">這個命令會取得一個名為 ElasticPool01 的彈性池中的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="cc331-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="cc331-111">範例2：使用篩選在彈性池中取得所有資料庫</span><span class="sxs-lookup"><span data-stu-id="cc331-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="cc331-112">這個命令會取得名為 ElasticPool01 且名為「Database」的彈性池中的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="cc331-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="cc331-113">參數</span><span class="sxs-lookup"><span data-stu-id="cc331-113">PARAMETERS</span></span>

### <span data-ttu-id="cc331-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc331-114">-DatabaseName</span></span>
<span data-ttu-id="cc331-115">指定此 Cmdlet 所取得之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc331-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cc331-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc331-116">-DefaultProfile</span></span>
<span data-ttu-id="cc331-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cc331-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc331-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="cc331-118">-ElasticPoolName</span></span>
<span data-ttu-id="cc331-119">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc331-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="cc331-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc331-120">-ResourceGroupName</span></span>
<span data-ttu-id="cc331-121">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc331-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="cc331-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc331-122">-ServerName</span></span>
<span data-ttu-id="cc331-123">指定包含彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cc331-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="cc331-124">-確認</span><span class="sxs-lookup"><span data-stu-id="cc331-124">-Confirm</span></span>
<span data-ttu-id="cc331-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc331-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc331-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc331-126">-WhatIf</span></span>
<span data-ttu-id="cc331-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc331-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc331-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc331-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc331-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc331-129">CommonParameters</span></span>
<span data-ttu-id="cc331-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc331-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc331-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc331-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc331-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cc331-132">INPUTS</span></span>

### <span data-ttu-id="cc331-133">System.object</span><span class="sxs-lookup"><span data-stu-id="cc331-133">System.String</span></span>

## <span data-ttu-id="cc331-134">輸出</span><span class="sxs-lookup"><span data-stu-id="cc331-134">OUTPUTS</span></span>

### <span data-ttu-id="cc331-135">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="cc331-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cc331-136">筆記</span><span class="sxs-lookup"><span data-stu-id="cc331-136">NOTES</span></span>

## <span data-ttu-id="cc331-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc331-137">RELATED LINKS</span></span>

[<span data-ttu-id="cc331-138">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cc331-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="cc331-139">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="cc331-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="cc331-140">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cc331-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="cc331-141">移除-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cc331-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="cc331-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cc331-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

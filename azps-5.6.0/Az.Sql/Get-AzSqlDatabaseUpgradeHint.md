---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917590"
---
# <span data-ttu-id="a94a7-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="a94a7-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="a94a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a94a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a94a7-103">獲得資料庫的定價層級提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="a94a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="a94a7-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a94a7-105">描述</span><span class="sxs-lookup"><span data-stu-id="a94a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a94a7-106">**Get-AzSqlDatabaseUpgradeHint** Cmdlet 會取得升級 Azure SQL Database 的定價層級提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="a94a7-107">仍在 Web 和商務定價層級的資料庫會獲得升級至新基本、標準或進一版定價層級的提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="a94a7-108">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a94a7-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a94a7-109">例子</span><span class="sxs-lookup"><span data-stu-id="a94a7-109">EXAMPLES</span></span>

### <span data-ttu-id="a94a7-110">範例 1：取得伺服器上所有資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="a94a7-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a94a7-111">此命令會針對伺服器名稱為 Server01 的所有資料庫，會返回升級提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="a94a7-112">範例 2：取得特定資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="a94a7-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a94a7-113">此命令會針對特定資料庫返回升級提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="a94a7-114">範例 3：取得所有不在彈性資料庫資料庫中之資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="a94a7-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="a94a7-115">此命令會針對不位於彈性資料庫資料庫資料庫中的所有資料庫，會針對這些資料庫，會返回升級提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="a94a7-116">範例 4：使用篩選取得伺服器上所有資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="a94a7-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="a94a7-117">此命令會針對伺服器名稱為 「資料庫」的所有資料庫，會針對該伺服器的所有資料庫，會返回升級提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="a94a7-118">參數</span><span class="sxs-lookup"><span data-stu-id="a94a7-118">PARAMETERS</span></span>

### <span data-ttu-id="a94a7-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a94a7-119">-DatabaseName</span></span>
<span data-ttu-id="a94a7-120">指定此 Cmdlet 會獲得升級提示的 SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a94a7-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="a94a7-121">如果您未指定資料庫，此 Cmdlet 會針對邏輯伺服器上的所有資料庫獲得提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="a94a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94a7-122">-DefaultProfile</span></span>
<span data-ttu-id="a94a7-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a94a7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a94a7-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="a94a7-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="a94a7-125">指出系統管理資料庫資料庫中的資料庫是否排除在所退回的建議中。</span><span class="sxs-lookup"><span data-stu-id="a94a7-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94a7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a94a7-126">-ResourceGroupName</span></span>
<span data-ttu-id="a94a7-127">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a94a7-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a94a7-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a94a7-128">-ServerName</span></span>
<span data-ttu-id="a94a7-129">指定主管此 Cmdlet 之資料庫的伺服器名稱，此 Cmdlet 會獲得升級提示。</span><span class="sxs-lookup"><span data-stu-id="a94a7-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="a94a7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a94a7-130">-Confirm</span></span>
<span data-ttu-id="a94a7-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a94a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a94a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a94a7-132">-WhatIf</span></span>
<span data-ttu-id="a94a7-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a94a7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a94a7-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a94a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a94a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94a7-135">CommonParameters</span></span>
<span data-ttu-id="a94a7-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a94a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94a7-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a94a7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94a7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a94a7-138">INPUTS</span></span>

### <span data-ttu-id="a94a7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a94a7-139">System.String</span></span>

### <span data-ttu-id="a94a7-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a94a7-140">System.Boolean</span></span>

## <span data-ttu-id="a94a7-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a94a7-141">OUTPUTS</span></span>

### <span data-ttu-id="a94a7-142">Microsoft.Azure.management.sql.LegacySdk.models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="a94a7-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="a94a7-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a94a7-143">NOTES</span></span>

## <span data-ttu-id="a94a7-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a94a7-144">RELATED LINKS</span></span>

[<span data-ttu-id="a94a7-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="a94a7-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="a94a7-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="a94a7-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)



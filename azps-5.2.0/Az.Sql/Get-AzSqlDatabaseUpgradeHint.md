---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284855"
---
# <span data-ttu-id="d68cc-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="d68cc-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="d68cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d68cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d68cc-103">取得資料庫的定價層提示。</span><span class="sxs-lookup"><span data-stu-id="d68cc-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="d68cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="d68cc-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d68cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="d68cc-105">DESCRIPTION</span></span>
<span data-ttu-id="d68cc-106">**AzSqlDatabaseUpgradeHint** Cmdlet 會取得升級 Azure SQL 資料庫的定價層提示。</span><span class="sxs-lookup"><span data-stu-id="d68cc-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="d68cc-107">仍在網頁和商務定價層級的資料庫會取得升級至新的基本、標準或 Premium 定價層級的提示。</span><span class="sxs-lookup"><span data-stu-id="d68cc-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="d68cc-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d68cc-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d68cc-109">示例</span><span class="sxs-lookup"><span data-stu-id="d68cc-109">EXAMPLES</span></span>

### <span data-ttu-id="d68cc-110">範例1：取得伺服器上所有資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="d68cc-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="d68cc-111">這個命令會傳回伺服器上名為 Server01 的所有資料庫的升級提示。</span><span class="sxs-lookup"><span data-stu-id="d68cc-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="d68cc-112">範例2：取得特定資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="d68cc-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d68cc-113">這個命令會傳回特定資料庫的升級提示。</span><span class="sxs-lookup"><span data-stu-id="d68cc-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="d68cc-114">範例3：針對不在彈性資料庫池中的所有資料庫取得建議</span><span class="sxs-lookup"><span data-stu-id="d68cc-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="d68cc-115">這個命令會針對不在彈性資料庫池中的所有資料庫傳回升級提示。</span><span class="sxs-lookup"><span data-stu-id="d68cc-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="d68cc-116">範例4：使用篩選在伺服器上取得所有資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="d68cc-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="d68cc-117">這個命令會傳回伺服器上名為「Database」開頭的所有資料庫的升級提示。</span><span class="sxs-lookup"><span data-stu-id="d68cc-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="d68cc-118">參數</span><span class="sxs-lookup"><span data-stu-id="d68cc-118">PARAMETERS</span></span>

### <span data-ttu-id="d68cc-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d68cc-119">-DatabaseName</span></span>
<span data-ttu-id="d68cc-120">指定此 Cmdlet 取得升級提示之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d68cc-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="d68cc-121">如果您不指定資料庫，此 Cmdlet 會取得邏輯伺服器上所有資料庫的提示。</span><span class="sxs-lookup"><span data-stu-id="d68cc-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="d68cc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68cc-122">-DefaultProfile</span></span>
<span data-ttu-id="d68cc-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d68cc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d68cc-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="d68cc-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="d68cc-125">指出是否已從傳回的建議中排除彈性資料庫池中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="d68cc-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="d68cc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68cc-126">-ResourceGroupName</span></span>
<span data-ttu-id="d68cc-127">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d68cc-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d68cc-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d68cc-128">-ServerName</span></span>
<span data-ttu-id="d68cc-129">指定主持此 Cmdlet 取得升級提示之資料庫之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d68cc-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="d68cc-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d68cc-130">-Confirm</span></span>
<span data-ttu-id="d68cc-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d68cc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d68cc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d68cc-132">-WhatIf</span></span>
<span data-ttu-id="d68cc-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d68cc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d68cc-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d68cc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d68cc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68cc-135">CommonParameters</span></span>
<span data-ttu-id="d68cc-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d68cc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68cc-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d68cc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68cc-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d68cc-138">INPUTS</span></span>

### <span data-ttu-id="d68cc-139">System.object</span><span class="sxs-lookup"><span data-stu-id="d68cc-139">System.String</span></span>

### <span data-ttu-id="d68cc-140">System.object</span><span class="sxs-lookup"><span data-stu-id="d68cc-140">System.Boolean</span></span>

## <span data-ttu-id="d68cc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d68cc-141">OUTPUTS</span></span>

### <span data-ttu-id="d68cc-142">RecommendedDatabaseProperties 中的 [LegacySdk]</span><span class="sxs-lookup"><span data-stu-id="d68cc-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="d68cc-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d68cc-143">NOTES</span></span>

## <span data-ttu-id="d68cc-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d68cc-144">RELATED LINKS</span></span>

[<span data-ttu-id="d68cc-145">AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="d68cc-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="d68cc-146">AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="d68cc-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)



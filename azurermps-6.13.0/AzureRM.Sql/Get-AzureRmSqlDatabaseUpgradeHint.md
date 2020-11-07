---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b289dc637b3d75321120f06eb9ddf604ebcdabba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624875"
---
# <span data-ttu-id="c0e0e-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="c0e0e-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="c0e0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e0e-103">取得資料庫的定價層提示。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0e0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0e0e-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e0e-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0e0e-105">DESCRIPTION</span></span>
<span data-ttu-id="c0e0e-106">**AzureRmSqlDatabaseUpgradeHint** Cmdlet 會取得升級 Azure SQL 資料庫的定價層提示。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="c0e0e-107">仍在網頁和商務定價層級的資料庫會取得升級至新的基本、標準或 Premium 定價層級的提示。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="c0e0e-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c0e0e-109">示例</span><span class="sxs-lookup"><span data-stu-id="c0e0e-109">EXAMPLES</span></span>

### <span data-ttu-id="c0e0e-110">範例1：取得伺服器上所有資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="c0e0e-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c0e0e-111">這個命令會傳回伺服器上名為 Server01 的所有資料庫的升級提示。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="c0e0e-112">範例2：取得特定資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="c0e0e-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="c0e0e-113">這個命令會傳回特定資料庫的升級提示。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="c0e0e-114">範例3：針對不在彈性資料庫池中的所有資料庫取得建議</span><span class="sxs-lookup"><span data-stu-id="c0e0e-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="c0e0e-115">這個命令會針對不在彈性資料庫池中的所有資料庫傳回升級提示。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="c0e0e-116">參數</span><span class="sxs-lookup"><span data-stu-id="c0e0e-116">PARAMETERS</span></span>

### <span data-ttu-id="c0e0e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0e0e-117">-DatabaseName</span></span>
<span data-ttu-id="c0e0e-118">指定此 Cmdlet 取得升級提示之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="c0e0e-119">如果您不指定資料庫，此 Cmdlet 會取得邏輯伺服器上所有資料庫的提示。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="c0e0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e0e-120">-DefaultProfile</span></span>
<span data-ttu-id="c0e0e-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c0e0e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0e0e-122">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="c0e0e-122">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="c0e0e-123">指出是否已從傳回的建議中排除彈性資料庫池中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-123">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="c0e0e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e0e-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0e0e-125">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-125">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c0e0e-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c0e0e-126">-ServerName</span></span>
<span data-ttu-id="c0e0e-127">指定主持此 Cmdlet 取得升級提示之資料庫之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-127">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="c0e0e-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c0e0e-128">-Confirm</span></span>
<span data-ttu-id="c0e0e-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e0e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e0e-130">-WhatIf</span></span>
<span data-ttu-id="c0e0e-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e0e-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e0e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e0e-133">CommonParameters</span></span>
<span data-ttu-id="c0e0e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e0e-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0e0e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e0e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c0e0e-136">INPUTS</span></span>

### <span data-ttu-id="c0e0e-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c0e0e-137">System.String</span></span>

### <span data-ttu-id="c0e0e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="c0e0e-138">System.Boolean</span></span>

## <span data-ttu-id="c0e0e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c0e0e-139">OUTPUTS</span></span>

### <span data-ttu-id="c0e0e-140">RecommendedDatabaseProperties 中的 [LegacySdk]</span><span class="sxs-lookup"><span data-stu-id="c0e0e-140">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="c0e0e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c0e0e-141">NOTES</span></span>

## <span data-ttu-id="c0e0e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0e0e-142">RELATED LINKS</span></span>

[<span data-ttu-id="c0e0e-143">AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="c0e0e-143">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="c0e0e-144">AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="c0e0e-144">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)



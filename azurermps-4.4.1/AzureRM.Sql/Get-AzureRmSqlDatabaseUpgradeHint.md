---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: c0a917d2f5e10bb499ecf6fc698bee9a84d64363
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625058"
---
# <span data-ttu-id="4ec72-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="4ec72-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="4ec72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ec72-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec72-103">取得資料庫的定價層提示。</span><span class="sxs-lookup"><span data-stu-id="4ec72-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec72-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ec72-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec72-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ec72-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec72-106">**AzureRmSqlDatabaseUpgradeHint** Cmdlet 會取得升級 Azure SQL 資料庫的定價層提示。</span><span class="sxs-lookup"><span data-stu-id="4ec72-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="4ec72-107">仍在網頁和商務定價層級的資料庫會取得升級至新的基本、標準或 Premium 定價層級的提示。</span><span class="sxs-lookup"><span data-stu-id="4ec72-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>

<span data-ttu-id="4ec72-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ec72-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4ec72-109">示例</span><span class="sxs-lookup"><span data-stu-id="4ec72-109">EXAMPLES</span></span>

### <span data-ttu-id="4ec72-110">範例1：取得伺服器上所有資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="4ec72-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="4ec72-111">這個命令會傳回伺服器上名為 Server01 的所有資料庫的升級提示。</span><span class="sxs-lookup"><span data-stu-id="4ec72-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="4ec72-112">範例2：取得特定資料庫的建議</span><span class="sxs-lookup"><span data-stu-id="4ec72-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4ec72-113">這個命令會傳回特定資料庫的升級提示。</span><span class="sxs-lookup"><span data-stu-id="4ec72-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="4ec72-114">範例3：針對不在彈性資料庫池中的所有資料庫取得建議</span><span class="sxs-lookup"><span data-stu-id="4ec72-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="4ec72-115">這個命令會針對不在彈性資料庫池中的所有資料庫傳回升級提示。</span><span class="sxs-lookup"><span data-stu-id="4ec72-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="4ec72-116">參數</span><span class="sxs-lookup"><span data-stu-id="4ec72-116">PARAMETERS</span></span>

### <span data-ttu-id="4ec72-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ec72-117">-DatabaseName</span></span>
<span data-ttu-id="4ec72-118">指定此 Cmdlet 取得升級提示之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ec72-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="4ec72-119">如果您不指定資料庫，此 Cmdlet 會取得邏輯伺服器上所有資料庫的提示。</span><span class="sxs-lookup"><span data-stu-id="4ec72-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="4ec72-120">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="4ec72-120">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="4ec72-121">指出是否已從傳回的建議中排除彈性資料庫池中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ec72-121">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="4ec72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec72-122">-ResourceGroupName</span></span>
<span data-ttu-id="4ec72-123">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ec72-123">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4ec72-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4ec72-124">-ServerName</span></span>
<span data-ttu-id="4ec72-125">指定主持此 Cmdlet 取得升級提示之資料庫之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ec72-125">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="4ec72-126">-確認</span><span class="sxs-lookup"><span data-stu-id="4ec72-126">-Confirm</span></span>
<span data-ttu-id="4ec72-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ec72-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec72-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec72-128">-WhatIf</span></span>
<span data-ttu-id="4ec72-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ec72-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec72-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ec72-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec72-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec72-131">-DefaultProfile</span></span>
<span data-ttu-id="4ec72-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ec72-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ec72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec72-133">CommonParameters</span></span>
<span data-ttu-id="4ec72-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ec72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec72-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ec72-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec72-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4ec72-136">INPUTS</span></span>

## <span data-ttu-id="4ec72-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4ec72-137">OUTPUTS</span></span>

## <span data-ttu-id="4ec72-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4ec72-138">NOTES</span></span>

## <span data-ttu-id="4ec72-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ec72-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ec72-140">AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="4ec72-140">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="4ec72-141">AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="4ec72-141">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)



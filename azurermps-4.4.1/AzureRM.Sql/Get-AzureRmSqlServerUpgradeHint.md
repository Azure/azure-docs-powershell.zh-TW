---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 18dcc69746e46ba75c01cb3aeb935bdd6b25d3bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446645"
---
# <span data-ttu-id="b4576-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="b4576-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="b4576-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4576-102">SYNOPSIS</span></span>
<span data-ttu-id="b4576-103">取得升級 Azure SQL 資料庫伺服器的定價層提示。</span><span class="sxs-lookup"><span data-stu-id="b4576-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4576-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4576-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4576-105">說明</span><span class="sxs-lookup"><span data-stu-id="b4576-105">DESCRIPTION</span></span>
<span data-ttu-id="b4576-106">**AzureRmSqlServerUpgradeHint** Cmdlet 會取得升級 Azure SQL 資料庫伺服器的定價層提示。</span><span class="sxs-lookup"><span data-stu-id="b4576-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="b4576-107">提示可能包含彈性資料庫池和獨立的資料庫提示。</span><span class="sxs-lookup"><span data-stu-id="b4576-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="b4576-108">仍在網頁和商務定價層級的資料庫會收到升級至新的基本、標準或 Premium 定價層級的提示，或進入彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="b4576-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="b4576-109">這個 Cmdlet 會傳回位於指定伺服器上的所有資料庫的提示。</span><span class="sxs-lookup"><span data-stu-id="b4576-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="b4576-110">示例</span><span class="sxs-lookup"><span data-stu-id="b4576-110">EXAMPLES</span></span>

### <span data-ttu-id="b4576-111">範例1：取得結合的建議</span><span class="sxs-lookup"><span data-stu-id="b4576-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="b4576-112">這個命令會針對名為 Server01 的伺服器上的所有資料庫，取得合併的建議。</span><span class="sxs-lookup"><span data-stu-id="b4576-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="b4576-113">參數</span><span class="sxs-lookup"><span data-stu-id="b4576-113">PARAMETERS</span></span>

### <span data-ttu-id="b4576-114">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="b4576-114">-ExcludeElasticPools</span></span>
<span data-ttu-id="b4576-115">指出是否應傳回彈性資料庫池中包含的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b4576-115">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="b4576-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4576-116">-ResourceGroupName</span></span>
<span data-ttu-id="b4576-117">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4576-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b4576-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4576-118">-ServerName</span></span>
<span data-ttu-id="b4576-119">指定此 Cmdlet 取得升級提示的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b4576-119">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="b4576-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b4576-120">-Confirm</span></span>
<span data-ttu-id="b4576-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b4576-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4576-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4576-122">-WhatIf</span></span>
<span data-ttu-id="b4576-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4576-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4576-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4576-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4576-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4576-125">-DefaultProfile</span></span>
<span data-ttu-id="b4576-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4576-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4576-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4576-127">CommonParameters</span></span>
<span data-ttu-id="b4576-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4576-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4576-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b4576-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4576-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b4576-130">INPUTS</span></span>

## <span data-ttu-id="b4576-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b4576-131">OUTPUTS</span></span>

## <span data-ttu-id="b4576-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b4576-132">NOTES</span></span>

## <span data-ttu-id="b4576-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4576-133">RELATED LINKS</span></span>

[<span data-ttu-id="b4576-134">AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="b4576-134">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="b4576-135">AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="b4576-135">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="b4576-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b4576-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


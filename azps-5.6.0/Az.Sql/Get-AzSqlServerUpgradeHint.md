---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: fc75aa4f838d19044514d3e6c343e04cdbf1d9be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902746"
---
# <span data-ttu-id="6b661-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="6b661-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="6b661-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6b661-102">SYNOPSIS</span></span>
<span data-ttu-id="6b661-103">獲得升級 Azure SQL Database 伺服器的價格層級提示。</span><span class="sxs-lookup"><span data-stu-id="6b661-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="6b661-104">語法</span><span class="sxs-lookup"><span data-stu-id="6b661-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b661-105">描述</span><span class="sxs-lookup"><span data-stu-id="6b661-105">DESCRIPTION</span></span>
<span data-ttu-id="6b661-106">**Get-AzSqlServerUpgradeHint** Cmdlet 會取得升級 Azure SQL Database 伺服器的價格層級提示。</span><span class="sxs-lookup"><span data-stu-id="6b661-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="6b661-107">提示可能包含彈性資料庫和獨立資料庫提示。</span><span class="sxs-lookup"><span data-stu-id="6b661-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="6b661-108">仍在 Web 和商務定價層級的資料庫會獲得升級至新基本、標準或進一步定價層級的提示，或進入彈性資料庫資料庫。</span><span class="sxs-lookup"><span data-stu-id="6b661-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="6b661-109">此 Cmdlet 會針對特定伺服器上託管的所有資料庫，會返回提示。</span><span class="sxs-lookup"><span data-stu-id="6b661-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="6b661-110">例子</span><span class="sxs-lookup"><span data-stu-id="6b661-110">EXAMPLES</span></span>

### <span data-ttu-id="6b661-111">範例 1：取得合併建議</span><span class="sxs-lookup"><span data-stu-id="6b661-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="6b661-112">此命令會針對伺服器名稱為 Server01 的所有資料庫提供合併建議。</span><span class="sxs-lookup"><span data-stu-id="6b661-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="6b661-113">參數</span><span class="sxs-lookup"><span data-stu-id="6b661-113">PARAMETERS</span></span>

### <span data-ttu-id="6b661-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b661-114">-DefaultProfile</span></span>
<span data-ttu-id="6b661-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6b661-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b661-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="6b661-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="6b661-117">指出是否應會退回應會包含在彈性資料庫資料庫資料庫中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6b661-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="6b661-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b661-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b661-119">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6b661-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6b661-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b661-120">-ServerName</span></span>
<span data-ttu-id="6b661-121">指定此 Cmdlet 會獲得升級提示的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6b661-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="6b661-122">-確認</span><span class="sxs-lookup"><span data-stu-id="6b661-122">-Confirm</span></span>
<span data-ttu-id="6b661-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6b661-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b661-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b661-124">-WhatIf</span></span>
<span data-ttu-id="6b661-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b661-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b661-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b661-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b661-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b661-127">CommonParameters</span></span>
<span data-ttu-id="6b661-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6b661-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b661-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b661-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b661-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6b661-130">INPUTS</span></span>

### <span data-ttu-id="6b661-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6b661-131">System.String</span></span>

### <span data-ttu-id="6b661-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b661-132">System.Boolean</span></span>

## <span data-ttu-id="6b661-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6b661-133">OUTPUTS</span></span>

### <span data-ttu-id="6b661-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="6b661-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="6b661-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6b661-135">NOTES</span></span>

## <span data-ttu-id="6b661-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b661-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b661-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6b661-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="6b661-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="6b661-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="6b661-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="6b661-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 03f2d7b9ae97282d0144ca19b493081fd2d8d774
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914333"
---
# <span data-ttu-id="a182a-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="a182a-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="a182a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a182a-102">SYNOPSIS</span></span>
<span data-ttu-id="a182a-103">獲得進位區建議。</span><span class="sxs-lookup"><span data-stu-id="a182a-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="a182a-104">語法</span><span class="sxs-lookup"><span data-stu-id="a182a-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a182a-105">描述</span><span class="sxs-lookup"><span data-stu-id="a182a-105">DESCRIPTION</span></span>
<span data-ttu-id="a182a-106">**Get-AzSqlElasticPoolRecommendation** Cmdlet 會取得伺服器的資料格建議。</span><span class="sxs-lookup"><span data-stu-id="a182a-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="a182a-107">這些建議包含下列值：</span><span class="sxs-lookup"><span data-stu-id="a182a-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="a182a-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="a182a-108">DatabaseCollection.</span></span> <span data-ttu-id="a182a-109">屬於集區的資料庫名稱集合。</span><span class="sxs-lookup"><span data-stu-id="a182a-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="a182a-110">DatabaseDtuMin。</span><span class="sxs-lookup"><span data-stu-id="a182a-110">DatabaseDtuMin.</span></span> <span data-ttu-id="a182a-111">資料傳輸單位 (DTU) 資料庫的保證。</span><span class="sxs-lookup"><span data-stu-id="a182a-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="a182a-112">-- DatabaseDtuMax。</span><span class="sxs-lookup"><span data-stu-id="a182a-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="a182a-113">資料庫在資料庫的 DTU 上限。</span><span class="sxs-lookup"><span data-stu-id="a182a-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="a182a-114">Dtu。</span><span class="sxs-lookup"><span data-stu-id="a182a-114">Dtu.</span></span> <span data-ttu-id="a182a-115">DTU 保證使用資料庫。</span><span class="sxs-lookup"><span data-stu-id="a182a-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="a182a-116">StorageMb。</span><span class="sxs-lookup"><span data-stu-id="a182a-116">StorageMb.</span></span> <span data-ttu-id="a182a-117">儲存空間 ，以 MB 為單位，用於存放資料庫。</span><span class="sxs-lookup"><span data-stu-id="a182a-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="a182a-118">版。</span><span class="sxs-lookup"><span data-stu-id="a182a-118">Edition.</span></span> <span data-ttu-id="a182a-119">適用于泳層資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="a182a-119">Edition for the elastic pool.</span></span> <span data-ttu-id="a182a-120">此參數可接受的值為：基本、標準及進一步。</span><span class="sxs-lookup"><span data-stu-id="a182a-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="a182a-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="a182a-121">IncludeAllDatabases.</span></span> <span data-ttu-id="a182a-122">指出是否要將資料庫壓縮資料庫的所有資料庫都退回。</span><span class="sxs-lookup"><span data-stu-id="a182a-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="a182a-123">名字。</span><span class="sxs-lookup"><span data-stu-id="a182a-123">Name.</span></span> <span data-ttu-id="a182a-124">泳層資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a182a-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="a182a-125">例子</span><span class="sxs-lookup"><span data-stu-id="a182a-125">EXAMPLES</span></span>

### <span data-ttu-id="a182a-126">範例 1：取得伺服器的建議</span><span class="sxs-lookup"><span data-stu-id="a182a-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a182a-127">此命令會針對伺服器名稱為 Server01 的伺服器，提供資料庫建議。</span><span class="sxs-lookup"><span data-stu-id="a182a-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="a182a-128">參數</span><span class="sxs-lookup"><span data-stu-id="a182a-128">PARAMETERS</span></span>

### <span data-ttu-id="a182a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a182a-129">-DefaultProfile</span></span>
<span data-ttu-id="a182a-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a182a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a182a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a182a-131">-ResourceGroupName</span></span>
<span data-ttu-id="a182a-132">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a182a-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a182a-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a182a-133">-ServerName</span></span>
<span data-ttu-id="a182a-134">指定此 Cmdlet 會提供建議的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a182a-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="a182a-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a182a-135">-Confirm</span></span>
<span data-ttu-id="a182a-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a182a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a182a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a182a-137">-WhatIf</span></span>
<span data-ttu-id="a182a-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a182a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a182a-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a182a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a182a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a182a-140">CommonParameters</span></span>
<span data-ttu-id="a182a-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a182a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a182a-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a182a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a182a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a182a-143">INPUTS</span></span>

### <span data-ttu-id="a182a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a182a-144">System.String</span></span>

## <span data-ttu-id="a182a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a182a-145">OUTPUTS</span></span>

### <span data-ttu-id="a182a-146">Microsoft.Azure.management.sql.LegacySdk.Models.UpgradeRecom一體式公司Properties</span><span class="sxs-lookup"><span data-stu-id="a182a-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="a182a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a182a-147">NOTES</span></span>

## <span data-ttu-id="a182a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a182a-148">RELATED LINKS</span></span>

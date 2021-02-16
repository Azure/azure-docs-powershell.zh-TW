---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133063"
---
# <span data-ttu-id="18a96-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="18a96-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="18a96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18a96-102">SYNOPSIS</span></span>
<span data-ttu-id="18a96-103">取得彈性池建議。</span><span class="sxs-lookup"><span data-stu-id="18a96-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="18a96-104">句法</span><span class="sxs-lookup"><span data-stu-id="18a96-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18a96-105">說明</span><span class="sxs-lookup"><span data-stu-id="18a96-105">DESCRIPTION</span></span>
<span data-ttu-id="18a96-106">**AzSqlElasticPoolRecommendation** Cmdlet 會取得伺服器的彈性池建議。</span><span class="sxs-lookup"><span data-stu-id="18a96-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="18a96-107">這些建議包括下列值：</span><span class="sxs-lookup"><span data-stu-id="18a96-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="18a96-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="18a96-108">DatabaseCollection.</span></span> <span data-ttu-id="18a96-109">屬於該池的資料庫名稱集合。</span><span class="sxs-lookup"><span data-stu-id="18a96-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="18a96-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="18a96-110">DatabaseDtuMin.</span></span> <span data-ttu-id="18a96-111">資料傳輸單元 (DTU) 保證彈性池中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="18a96-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="18a96-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="18a96-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="18a96-113">彈性池中資料庫的 DTU 上限。</span><span class="sxs-lookup"><span data-stu-id="18a96-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="18a96-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="18a96-114">Dtu.</span></span> <span data-ttu-id="18a96-115">彈性池的 DTU 保證。</span><span class="sxs-lookup"><span data-stu-id="18a96-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="18a96-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="18a96-116">StorageMb.</span></span> <span data-ttu-id="18a96-117">彈性池的儲存空間（mb）。</span><span class="sxs-lookup"><span data-stu-id="18a96-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="18a96-118">相比.</span><span class="sxs-lookup"><span data-stu-id="18a96-118">Edition.</span></span> <span data-ttu-id="18a96-119">彈性池的版本。</span><span class="sxs-lookup"><span data-stu-id="18a96-119">Edition for the elastic pool.</span></span> <span data-ttu-id="18a96-120">此參數可接受的值為： [基本]、[標準] 和 [特優]。</span><span class="sxs-lookup"><span data-stu-id="18a96-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="18a96-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="18a96-121">IncludeAllDatabases.</span></span> <span data-ttu-id="18a96-122">指出是否傳回彈性池中的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="18a96-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="18a96-123">列名.</span><span class="sxs-lookup"><span data-stu-id="18a96-123">Name.</span></span> <span data-ttu-id="18a96-124">彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="18a96-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="18a96-125">示例</span><span class="sxs-lookup"><span data-stu-id="18a96-125">EXAMPLES</span></span>

### <span data-ttu-id="18a96-126">範例1：取得伺服器的建議</span><span class="sxs-lookup"><span data-stu-id="18a96-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="18a96-127">這個命令會取得名為 Server01 之伺服器的彈性池建議。</span><span class="sxs-lookup"><span data-stu-id="18a96-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="18a96-128">參數</span><span class="sxs-lookup"><span data-stu-id="18a96-128">PARAMETERS</span></span>

### <span data-ttu-id="18a96-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a96-129">-DefaultProfile</span></span>
<span data-ttu-id="18a96-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="18a96-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18a96-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a96-131">-ResourceGroupName</span></span>
<span data-ttu-id="18a96-132">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18a96-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="18a96-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="18a96-133">-ServerName</span></span>
<span data-ttu-id="18a96-134">指定此 Cmdlet 取得建議的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="18a96-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="18a96-135">-確認</span><span class="sxs-lookup"><span data-stu-id="18a96-135">-Confirm</span></span>
<span data-ttu-id="18a96-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18a96-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a96-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a96-137">-WhatIf</span></span>
<span data-ttu-id="18a96-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18a96-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18a96-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18a96-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a96-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a96-140">CommonParameters</span></span>
<span data-ttu-id="18a96-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18a96-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a96-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="18a96-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a96-143">輸入</span><span class="sxs-lookup"><span data-stu-id="18a96-143">INPUTS</span></span>

### <span data-ttu-id="18a96-144">System.object</span><span class="sxs-lookup"><span data-stu-id="18a96-144">System.String</span></span>

## <span data-ttu-id="18a96-145">輸出</span><span class="sxs-lookup"><span data-stu-id="18a96-145">OUTPUTS</span></span>

### <span data-ttu-id="18a96-146">UpgradeRecommendedElasticPoolProperties 中的 [LegacySdk]</span><span class="sxs-lookup"><span data-stu-id="18a96-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="18a96-147">筆記</span><span class="sxs-lookup"><span data-stu-id="18a96-147">NOTES</span></span>

## <span data-ttu-id="18a96-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="18a96-148">RELATED LINKS</span></span>

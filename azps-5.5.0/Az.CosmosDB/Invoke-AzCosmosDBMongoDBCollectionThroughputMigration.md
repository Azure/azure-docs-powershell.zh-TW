---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 79dcea6f66d01e9bfa2dd53b990a8f38ec5b0f2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141170"
---
# <span data-ttu-id="18468-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="18468-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="18468-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18468-102">SYNOPSIS</span></span>
<span data-ttu-id="18468-103">使用此操作可將自動縮放輸送量遷移成手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="18468-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="18468-104">句法</span><span class="sxs-lookup"><span data-stu-id="18468-104">SYNTAX</span></span>

### <span data-ttu-id="18468-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="18468-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18468-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18468-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18468-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18468-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18468-108">說明</span><span class="sxs-lookup"><span data-stu-id="18468-108">DESCRIPTION</span></span>
<span data-ttu-id="18468-109">ThroughpyteType 參數定義您想要將哪些輸送量遷移至。</span><span class="sxs-lookup"><span data-stu-id="18468-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="18468-110">示例</span><span class="sxs-lookup"><span data-stu-id="18468-110">EXAMPLES</span></span>

### <span data-ttu-id="18468-111">範例1</span><span class="sxs-lookup"><span data-stu-id="18468-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="18468-112">參數</span><span class="sxs-lookup"><span data-stu-id="18468-112">PARAMETERS</span></span>

### <span data-ttu-id="18468-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18468-113">-AccountName</span></span>
<span data-ttu-id="18468-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="18468-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18468-115">-確認</span><span class="sxs-lookup"><span data-stu-id="18468-115">-Confirm</span></span>
<span data-ttu-id="18468-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18468-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18468-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="18468-117">-DatabaseName</span></span>
<span data-ttu-id="18468-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="18468-118">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18468-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18468-119">-DefaultProfile</span></span>
<span data-ttu-id="18468-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18468-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18468-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18468-121">-InputObject</span></span>
<span data-ttu-id="18468-122">Mongo 集合物件。</span><span class="sxs-lookup"><span data-stu-id="18468-122">Mongo Collection object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18468-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="18468-123">-Name</span></span>
<span data-ttu-id="18468-124">集合名稱。</span><span class="sxs-lookup"><span data-stu-id="18468-124">Collection name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18468-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="18468-125">-ParentObject</span></span>
<span data-ttu-id="18468-126">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="18468-126">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18468-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18468-127">-ResourceGroupName</span></span>
<span data-ttu-id="18468-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18468-128">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18468-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="18468-129">-ThroughputType</span></span>
<span data-ttu-id="18468-130">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="18468-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="18468-131">可能的值為：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="18468-131">Possible values are: Autoscale, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18468-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18468-132">-WhatIf</span></span>
<span data-ttu-id="18468-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18468-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18468-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18468-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18468-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18468-135">CommonParameters</span></span>
<span data-ttu-id="18468-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18468-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18468-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="18468-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18468-138">輸入</span><span class="sxs-lookup"><span data-stu-id="18468-138">INPUTS</span></span>

### <span data-ttu-id="18468-139">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="18468-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="18468-140">PSMongoDBCollectionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="18468-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="18468-141">輸出</span><span class="sxs-lookup"><span data-stu-id="18468-141">OUTPUTS</span></span>

### <span data-ttu-id="18468-142">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="18468-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="18468-143">筆記</span><span class="sxs-lookup"><span data-stu-id="18468-143">NOTES</span></span>

## <span data-ttu-id="18468-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="18468-144">RELATED LINKS</span></span>

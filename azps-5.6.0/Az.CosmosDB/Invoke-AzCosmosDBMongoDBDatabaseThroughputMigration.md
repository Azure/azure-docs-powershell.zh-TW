---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: c1ae582bcbf5fb2a19ee3c1904635dd886cbf8fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908286"
---
# <span data-ttu-id="b85d0-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="b85d0-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="b85d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b85d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b85d0-103">請使用此功能將自動縮放輸送量遷移到手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="b85d0-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="b85d0-104">語法</span><span class="sxs-lookup"><span data-stu-id="b85d0-104">SYNTAX</span></span>

### <span data-ttu-id="b85d0-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b85d0-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b85d0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85d0-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85d0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85d0-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b85d0-108">描述</span><span class="sxs-lookup"><span data-stu-id="b85d0-108">DESCRIPTION</span></span>
<span data-ttu-id="b85d0-109">ThroughpyteType 參數會定義要遷移到的輸送量。</span><span class="sxs-lookup"><span data-stu-id="b85d0-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="b85d0-110">例子</span><span class="sxs-lookup"><span data-stu-id="b85d0-110">EXAMPLES</span></span>

### <span data-ttu-id="b85d0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b85d0-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="b85d0-112">參數</span><span class="sxs-lookup"><span data-stu-id="b85d0-112">PARAMETERS</span></span>

### <span data-ttu-id="b85d0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b85d0-113">-AccountName</span></span>
<span data-ttu-id="b85d0-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85d0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b85d0-115">-確認</span><span class="sxs-lookup"><span data-stu-id="b85d0-115">-Confirm</span></span>
<span data-ttu-id="b85d0-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b85d0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85d0-117">-DefaultProfile</span></span>
<span data-ttu-id="b85d0-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b85d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b85d0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b85d0-119">-InputObject</span></span>
<span data-ttu-id="b85d0-120">Mongo Database 物件。</span><span class="sxs-lookup"><span data-stu-id="b85d0-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b85d0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b85d0-121">-Name</span></span>
<span data-ttu-id="b85d0-122">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b85d0-122">Database name.</span></span>

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

### <span data-ttu-id="b85d0-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b85d0-123">-ParentObject</span></span>
<span data-ttu-id="b85d0-124">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="b85d0-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="b85d0-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85d0-126">Name of resource group.</span></span>

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

### <span data-ttu-id="b85d0-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="b85d0-127">-ThroughputType</span></span>
<span data-ttu-id="b85d0-128">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="b85d0-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="b85d0-129">可能的值有：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="b85d0-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="b85d0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85d0-130">-WhatIf</span></span>
<span data-ttu-id="b85d0-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b85d0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b85d0-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b85d0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85d0-133">CommonParameters</span></span>
<span data-ttu-id="b85d0-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b85d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85d0-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b85d0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85d0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b85d0-136">INPUTS</span></span>

### <span data-ttu-id="b85d0-137">Microsoft.Azure.Commands.AzsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b85d0-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="b85d0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b85d0-138">OUTPUTS</span></span>

### <span data-ttu-id="b85d0-139">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b85d0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b85d0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b85d0-140">NOTES</span></span>

## <span data-ttu-id="b85d0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b85d0-141">RELATED LINKS</span></span>

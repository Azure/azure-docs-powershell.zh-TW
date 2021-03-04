---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 2511ddc7174d4b76ec6d5df5bcbcd334f423a882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913581"
---
# <span data-ttu-id="d190e-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="d190e-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="d190e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d190e-102">SYNOPSIS</span></span>
<span data-ttu-id="d190e-103">請使用此功能將自動縮放輸送量遷移到手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="d190e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="d190e-104">語法</span><span class="sxs-lookup"><span data-stu-id="d190e-104">SYNTAX</span></span>

### <span data-ttu-id="d190e-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d190e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d190e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d190e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d190e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d190e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d190e-108">描述</span><span class="sxs-lookup"><span data-stu-id="d190e-108">DESCRIPTION</span></span>
<span data-ttu-id="d190e-109">ThroughpyteType 參數會定義要遷移到的輸送量。</span><span class="sxs-lookup"><span data-stu-id="d190e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="d190e-110">例子</span><span class="sxs-lookup"><span data-stu-id="d190e-110">EXAMPLES</span></span>

### <span data-ttu-id="d190e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d190e-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="d190e-112">參數</span><span class="sxs-lookup"><span data-stu-id="d190e-112">PARAMETERS</span></span>

### <span data-ttu-id="d190e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d190e-113">-AccountName</span></span>
<span data-ttu-id="d190e-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d190e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d190e-115">-確認</span><span class="sxs-lookup"><span data-stu-id="d190e-115">-Confirm</span></span>
<span data-ttu-id="d190e-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d190e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d190e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d190e-117">-DefaultProfile</span></span>
<span data-ttu-id="d190e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d190e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d190e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d190e-119">-InputObject</span></span>
<span data-ttu-id="d190e-120">資料表物件。</span><span class="sxs-lookup"><span data-stu-id="d190e-120">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d190e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d190e-121">-Name</span></span>
<span data-ttu-id="d190e-122">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="d190e-122">Name of the Table.</span></span>

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

### <span data-ttu-id="d190e-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d190e-123">-ParentObject</span></span>
<span data-ttu-id="d190e-124">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="d190e-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d190e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d190e-125">-ResourceGroupName</span></span>
<span data-ttu-id="d190e-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d190e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d190e-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="d190e-127">-ThroughputType</span></span>
<span data-ttu-id="d190e-128">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="d190e-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="d190e-129">可能的值有：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="d190e-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="d190e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d190e-130">-WhatIf</span></span>
<span data-ttu-id="d190e-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d190e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d190e-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d190e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d190e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d190e-133">CommonParameters</span></span>
<span data-ttu-id="d190e-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d190e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d190e-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d190e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d190e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d190e-136">INPUTS</span></span>

### <span data-ttu-id="d190e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="d190e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="d190e-138">Microsoft.Azure.Commands.AzsDB.models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d190e-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="d190e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d190e-139">OUTPUTS</span></span>

### <span data-ttu-id="d190e-140">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d190e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d190e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d190e-141">NOTES</span></span>

## <span data-ttu-id="d190e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d190e-142">RELATED LINKS</span></span>

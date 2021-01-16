---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 009048c5f37936d469fe88c5e75cab8270efa81c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281945"
---
# <span data-ttu-id="5fd4c-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="5fd4c-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="5fd4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5fd4c-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd4c-103">使用此操作可將自動縮放輸送量遷移成手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="5fd4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5fd4c-104">SYNTAX</span></span>

### <span data-ttu-id="5fd4c-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5fd4c-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd4c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd4c-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd4c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd4c-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd4c-108">說明</span><span class="sxs-lookup"><span data-stu-id="5fd4c-108">DESCRIPTION</span></span>
<span data-ttu-id="5fd4c-109">ThroughpyteType 參數定義您想要將哪些輸送量遷移至。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="5fd4c-110">示例</span><span class="sxs-lookup"><span data-stu-id="5fd4c-110">EXAMPLES</span></span>

### <span data-ttu-id="5fd4c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5fd4c-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="5fd4c-112">參數</span><span class="sxs-lookup"><span data-stu-id="5fd4c-112">PARAMETERS</span></span>

### <span data-ttu-id="5fd4c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5fd4c-113">-AccountName</span></span>
<span data-ttu-id="5fd4c-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5fd4c-115">-確認</span><span class="sxs-lookup"><span data-stu-id="5fd4c-115">-Confirm</span></span>
<span data-ttu-id="5fd4c-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd4c-117">-DefaultProfile</span></span>
<span data-ttu-id="5fd4c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fd4c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fd4c-119">-InputObject</span></span>
<span data-ttu-id="5fd4c-120">Table 物件。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-120">Table Object.</span></span>

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

### <span data-ttu-id="5fd4c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5fd4c-121">-Name</span></span>
<span data-ttu-id="5fd4c-122">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-122">Name of the Table.</span></span>

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

### <span data-ttu-id="5fd4c-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5fd4c-123">-ParentObject</span></span>
<span data-ttu-id="5fd4c-124">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="5fd4c-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5fd4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="5fd4c-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5fd4c-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="5fd4c-127">-ThroughputType</span></span>
<span data-ttu-id="5fd4c-128">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="5fd4c-129">可能的值為：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="5fd4c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd4c-130">-WhatIf</span></span>
<span data-ttu-id="5fd4c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd4c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd4c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd4c-133">CommonParameters</span></span>
<span data-ttu-id="5fd4c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd4c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd4c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="5fd4c-136">INPUTS</span></span>

### <span data-ttu-id="5fd4c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="5fd4c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="5fd4c-138">PSTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="5fd4c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5fd4c-139">OUTPUTS</span></span>

### <span data-ttu-id="5fd4c-140">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5fd4c-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5fd4c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5fd4c-141">NOTES</span></span>

## <span data-ttu-id="5fd4c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fd4c-142">RELATED LINKS</span></span>

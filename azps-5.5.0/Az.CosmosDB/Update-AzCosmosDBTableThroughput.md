---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137379"
---
# <span data-ttu-id="275c1-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="275c1-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="275c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="275c1-102">SYNOPSIS</span></span>
<span data-ttu-id="275c1-103">更新 CosmosDB 資料表的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="275c1-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="275c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="275c1-104">SYNTAX</span></span>

### <span data-ttu-id="275c1-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="275c1-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275c1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="275c1-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275c1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="275c1-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="275c1-108">說明</span><span class="sxs-lookup"><span data-stu-id="275c1-108">DESCRIPTION</span></span>
<span data-ttu-id="275c1-109">更新 CosmosDB 資料表的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="275c1-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="275c1-110">示例</span><span class="sxs-lookup"><span data-stu-id="275c1-110">EXAMPLES</span></span>

### <span data-ttu-id="275c1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="275c1-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="275c1-112">參數</span><span class="sxs-lookup"><span data-stu-id="275c1-112">PARAMETERS</span></span>

### <span data-ttu-id="275c1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="275c1-113">-AccountName</span></span>
<span data-ttu-id="275c1-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="275c1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="275c1-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="275c1-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="275c1-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="275c1-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275c1-117">-確認</span><span class="sxs-lookup"><span data-stu-id="275c1-117">-Confirm</span></span>
<span data-ttu-id="275c1-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="275c1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275c1-119">-DefaultProfile</span></span>
<span data-ttu-id="275c1-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="275c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275c1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="275c1-121">-InputObject</span></span>
<span data-ttu-id="275c1-122">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="275c1-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="275c1-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="275c1-123">-Name</span></span>
<span data-ttu-id="275c1-124">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="275c1-124">Name of the Table.</span></span>

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

### <span data-ttu-id="275c1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="275c1-125">-ParentObject</span></span>
<span data-ttu-id="275c1-126">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="275c1-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="275c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="275c1-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="275c1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="275c1-129">-輸送量</span><span class="sxs-lookup"><span data-stu-id="275c1-129">-Throughput</span></span>
<span data-ttu-id="275c1-130">資料表 (RU/s) 的輸送量。</span><span class="sxs-lookup"><span data-stu-id="275c1-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="275c1-131">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="275c1-131">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275c1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275c1-132">-WhatIf</span></span>
<span data-ttu-id="275c1-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="275c1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275c1-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="275c1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275c1-135">CommonParameters</span></span>
<span data-ttu-id="275c1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="275c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275c1-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="275c1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275c1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="275c1-138">INPUTS</span></span>

### <span data-ttu-id="275c1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="275c1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="275c1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="275c1-140">OUTPUTS</span></span>

### <span data-ttu-id="275c1-141">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="275c1-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="275c1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="275c1-142">NOTES</span></span>

## <span data-ttu-id="275c1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="275c1-143">RELATED LINKS</span></span>

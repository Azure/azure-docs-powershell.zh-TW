---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 78cae2438b941e479d1f1ab26fbf2275bcff7b3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913577"
---
# <span data-ttu-id="4fc5d-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="4fc5d-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="4fc5d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4fc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc5d-103">更新一個更新一個一流表格的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="4fc5d-104">語法</span><span class="sxs-lookup"><span data-stu-id="4fc5d-104">SYNTAX</span></span>

### <span data-ttu-id="4fc5d-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4fc5d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fc5d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc5d-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fc5d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc5d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fc5d-108">描述</span><span class="sxs-lookup"><span data-stu-id="4fc5d-108">DESCRIPTION</span></span>
<span data-ttu-id="4fc5d-109">更新一個更新一個一流表格的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="4fc5d-110">例子</span><span class="sxs-lookup"><span data-stu-id="4fc5d-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc5d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4fc5d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="4fc5d-112">參數</span><span class="sxs-lookup"><span data-stu-id="4fc5d-112">PARAMETERS</span></span>

### <span data-ttu-id="4fc5d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4fc5d-113">-AccountName</span></span>
<span data-ttu-id="4fc5d-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4fc5d-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4fc5d-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4fc5d-116">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="4fc5d-117">-確認</span><span class="sxs-lookup"><span data-stu-id="4fc5d-117">-Confirm</span></span>
<span data-ttu-id="4fc5d-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc5d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc5d-119">-DefaultProfile</span></span>
<span data-ttu-id="4fc5d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fc5d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fc5d-121">-InputObject</span></span>
<span data-ttu-id="4fc5d-122">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="4fc5d-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4fc5d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4fc5d-123">-Name</span></span>
<span data-ttu-id="4fc5d-124">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-124">Name of the Table.</span></span>

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

### <span data-ttu-id="4fc5d-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4fc5d-125">-ParentObject</span></span>
<span data-ttu-id="4fc5d-126">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="4fc5d-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4fc5d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc5d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4fc5d-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-128">Name of resource group.</span></span>

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

### <span data-ttu-id="4fc5d-129">-輸送量</span><span class="sxs-lookup"><span data-stu-id="4fc5d-129">-Throughput</span></span>
<span data-ttu-id="4fc5d-130">Table (RU/s) 。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="4fc5d-131">預設值為 400。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-131">Default value is 400.</span></span>

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

### <span data-ttu-id="4fc5d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc5d-132">-WhatIf</span></span>
<span data-ttu-id="4fc5d-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc5d-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc5d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc5d-135">CommonParameters</span></span>
<span data-ttu-id="4fc5d-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4fc5d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc5d-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fc5d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc5d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4fc5d-138">INPUTS</span></span>

### <span data-ttu-id="4fc5d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4fc5d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4fc5d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4fc5d-140">OUTPUTS</span></span>

### <span data-ttu-id="4fc5d-141">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4fc5d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4fc5d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4fc5d-142">NOTES</span></span>

## <span data-ttu-id="4fc5d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fc5d-143">RELATED LINKS</span></span>

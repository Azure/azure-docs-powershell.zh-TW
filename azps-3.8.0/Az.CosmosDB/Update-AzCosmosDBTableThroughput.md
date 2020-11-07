---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 56c99a1e3cf21f38544e97ee84ba10efb51bc983
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958117"
---
# <span data-ttu-id="6b83a-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="6b83a-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="6b83a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b83a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b83a-103">更新 CosmosDB 資料表的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="6b83a-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="6b83a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b83a-104">SYNTAX</span></span>

### <span data-ttu-id="6b83a-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6b83a-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b83a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b83a-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -ParentObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b83a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b83a-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -InputObject <PSTableGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b83a-108">示例</span><span class="sxs-lookup"><span data-stu-id="6b83a-108">EXAMPLES</span></span>

### <span data-ttu-id="6b83a-109">範例1</span><span class="sxs-lookup"><span data-stu-id="6b83a-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="6b83a-110">參數</span><span class="sxs-lookup"><span data-stu-id="6b83a-110">PARAMETERS</span></span>

### <span data-ttu-id="6b83a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6b83a-111">-AccountName</span></span>
<span data-ttu-id="6b83a-112">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b83a-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6b83a-113">-確認</span><span class="sxs-lookup"><span data-stu-id="6b83a-113">-Confirm</span></span>
<span data-ttu-id="6b83a-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b83a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b83a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b83a-115">-DefaultProfile</span></span>
<span data-ttu-id="6b83a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b83a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b83a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b83a-117">-InputObject</span></span>
<span data-ttu-id="6b83a-118">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="6b83a-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6b83a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b83a-119">-Name</span></span>
<span data-ttu-id="6b83a-120">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b83a-120">Name of the Table.</span></span>

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

### <span data-ttu-id="6b83a-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6b83a-121">-ParentObject</span></span>
<span data-ttu-id="6b83a-122">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="6b83a-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b83a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b83a-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b83a-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b83a-124">Name of resource group.</span></span>

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

### <span data-ttu-id="6b83a-125">-輸送量</span><span class="sxs-lookup"><span data-stu-id="6b83a-125">-Throughput</span></span>
<span data-ttu-id="6b83a-126">資料表 (RU/s) 的輸送量。</span><span class="sxs-lookup"><span data-stu-id="6b83a-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="6b83a-127">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="6b83a-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b83a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b83a-128">-WhatIf</span></span>
<span data-ttu-id="6b83a-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b83a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b83a-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b83a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b83a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b83a-131">CommonParameters</span></span>
<span data-ttu-id="6b83a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b83a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b83a-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6b83a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b83a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6b83a-134">INPUTS</span></span>

### <span data-ttu-id="6b83a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="6b83a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="6b83a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6b83a-136">OUTPUTS</span></span>

### <span data-ttu-id="6b83a-137">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6b83a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6b83a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6b83a-138">NOTES</span></span>

## <span data-ttu-id="6b83a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b83a-139">RELATED LINKS</span></span>

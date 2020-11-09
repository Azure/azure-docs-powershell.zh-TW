---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285427"
---
# <span data-ttu-id="08385-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="08385-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="08385-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08385-102">SYNOPSIS</span></span>
<span data-ttu-id="08385-103">更新 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="08385-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="08385-104">透過讀取現有的資料庫來執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="08385-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="08385-105">句法</span><span class="sxs-lookup"><span data-stu-id="08385-105">SYNTAX</span></span>

### <span data-ttu-id="08385-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="08385-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08385-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08385-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08385-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08385-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08385-109">說明</span><span class="sxs-lookup"><span data-stu-id="08385-109">DESCRIPTION</span></span>
<span data-ttu-id="08385-110">更新 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="08385-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="08385-111">透過讀取現有的資料庫來執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="08385-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="08385-112">示例</span><span class="sxs-lookup"><span data-stu-id="08385-112">EXAMPLES</span></span>

### <span data-ttu-id="08385-113">範例1</span><span class="sxs-lookup"><span data-stu-id="08385-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="08385-114">參數</span><span class="sxs-lookup"><span data-stu-id="08385-114">PARAMETERS</span></span>

### <span data-ttu-id="08385-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08385-115">-AccountName</span></span>
<span data-ttu-id="08385-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="08385-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="08385-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="08385-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="08385-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="08385-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="08385-119">-確認</span><span class="sxs-lookup"><span data-stu-id="08385-119">-Confirm</span></span>
<span data-ttu-id="08385-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08385-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08385-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08385-121">-DefaultProfile</span></span>
<span data-ttu-id="08385-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08385-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08385-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08385-123">-InputObject</span></span>
<span data-ttu-id="08385-124">Gremlin 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="08385-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08385-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="08385-125">-Name</span></span>
<span data-ttu-id="08385-126">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="08385-126">Database name.</span></span>

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

### <span data-ttu-id="08385-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="08385-127">-ParentObject</span></span>
<span data-ttu-id="08385-128">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="08385-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="08385-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08385-129">-ResourceGroupName</span></span>
<span data-ttu-id="08385-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08385-130">Name of resource group.</span></span>

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

### <span data-ttu-id="08385-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="08385-131">-Throughput</span></span>
<span data-ttu-id="08385-132">Gremlin 資料庫的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="08385-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="08385-133">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="08385-133">Default value is 400.</span></span>

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

### <span data-ttu-id="08385-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08385-134">-WhatIf</span></span>
<span data-ttu-id="08385-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08385-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08385-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08385-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08385-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08385-137">CommonParameters</span></span>
<span data-ttu-id="08385-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08385-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08385-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="08385-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08385-140">輸入</span><span class="sxs-lookup"><span data-stu-id="08385-140">INPUTS</span></span>

### <span data-ttu-id="08385-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="08385-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="08385-142">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="08385-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="08385-143">輸出</span><span class="sxs-lookup"><span data-stu-id="08385-143">OUTPUTS</span></span>

### <span data-ttu-id="08385-144">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="08385-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="08385-145">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="08385-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="08385-146">筆記</span><span class="sxs-lookup"><span data-stu-id="08385-146">NOTES</span></span>

## <span data-ttu-id="08385-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="08385-147">RELATED LINKS</span></span>

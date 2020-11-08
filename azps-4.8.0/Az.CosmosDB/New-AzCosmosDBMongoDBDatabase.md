---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136074"
---
# <span data-ttu-id="e3c0a-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="e3c0a-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="e3c0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c0a-103">建立新的 CosmosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="e3c0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3c0a-104">SYNTAX</span></span>

### <span data-ttu-id="e3c0a-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e3c0a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3c0a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3c0a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3c0a-107">說明</span><span class="sxs-lookup"><span data-stu-id="e3c0a-107">DESCRIPTION</span></span>
<span data-ttu-id="e3c0a-108">建立新的 CosmosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="e3c0a-109">示例</span><span class="sxs-lookup"><span data-stu-id="e3c0a-109">EXAMPLES</span></span>

### <span data-ttu-id="e3c0a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e3c0a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="e3c0a-111">參數</span><span class="sxs-lookup"><span data-stu-id="e3c0a-111">PARAMETERS</span></span>

### <span data-ttu-id="e3c0a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3c0a-112">-AccountName</span></span>
<span data-ttu-id="e3c0a-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e3c0a-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e3c0a-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e3c0a-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e3c0a-116">-確認</span><span class="sxs-lookup"><span data-stu-id="e3c0a-116">-Confirm</span></span>
<span data-ttu-id="e3c0a-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c0a-118">-DefaultProfile</span></span>
<span data-ttu-id="e3c0a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3c0a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3c0a-120">-Name</span></span>
<span data-ttu-id="e3c0a-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-121">Database name.</span></span>

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

### <span data-ttu-id="e3c0a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e3c0a-122">-ParentObject</span></span>
<span data-ttu-id="e3c0a-123">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="e3c0a-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e3c0a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c0a-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3c0a-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e3c0a-126">-輸送量</span><span class="sxs-lookup"><span data-stu-id="e3c0a-126">-Throughput</span></span>
<span data-ttu-id="e3c0a-127">Mongo 資料庫的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="e3c0a-128">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-128">Default value is 400.</span></span>

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

### <span data-ttu-id="e3c0a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c0a-129">-WhatIf</span></span>
<span data-ttu-id="e3c0a-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c0a-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c0a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c0a-132">CommonParameters</span></span>
<span data-ttu-id="e3c0a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c0a-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c0a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e3c0a-135">INPUTS</span></span>

### <span data-ttu-id="e3c0a-136">所有</span><span class="sxs-lookup"><span data-stu-id="e3c0a-136">None</span></span>

## <span data-ttu-id="e3c0a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e3c0a-137">OUTPUTS</span></span>

### <span data-ttu-id="e3c0a-138">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="e3c0a-139">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e3c0a-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e3c0a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e3c0a-140">NOTES</span></span>

## <span data-ttu-id="e3c0a-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3c0a-141">RELATED LINKS</span></span>

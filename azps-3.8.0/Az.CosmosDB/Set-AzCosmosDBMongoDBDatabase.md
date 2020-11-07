---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 2ee1f932e1829e6c1d9d35ccd2cf67473a851414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965881"
---
# <span data-ttu-id="7559e-101">Set-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="7559e-101">Set-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="7559e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7559e-102">SYNOPSIS</span></span>
<span data-ttu-id="7559e-103">設定 CosmosDB MongoDB 資料庫</span><span class="sxs-lookup"><span data-stu-id="7559e-103">Sets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="7559e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7559e-104">SYNTAX</span></span>

### <span data-ttu-id="7559e-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7559e-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7559e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7559e-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7559e-107">說明</span><span class="sxs-lookup"><span data-stu-id="7559e-107">DESCRIPTION</span></span>
<span data-ttu-id="7559e-108">**AzCosmosDBMongoDBDatabase** Cmdlet 會取得 CosmosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7559e-108">The **Set-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="7559e-109">示例</span><span class="sxs-lookup"><span data-stu-id="7559e-109">EXAMPLES</span></span>

### <span data-ttu-id="7559e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7559e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="7559e-111">資源物件包含 _rid、_ts _etag 屬性。</span><span class="sxs-lookup"><span data-stu-id="7559e-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="7559e-112">參數</span><span class="sxs-lookup"><span data-stu-id="7559e-112">PARAMETERS</span></span>

### <span data-ttu-id="7559e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7559e-113">-AccountName</span></span>
<span data-ttu-id="7559e-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7559e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7559e-115">-確認</span><span class="sxs-lookup"><span data-stu-id="7559e-115">-Confirm</span></span>
<span data-ttu-id="7559e-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7559e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7559e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7559e-117">-DefaultProfile</span></span>
<span data-ttu-id="7559e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7559e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7559e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7559e-119">-InputObject</span></span>
<span data-ttu-id="7559e-120">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="7559e-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7559e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7559e-121">-Name</span></span>
<span data-ttu-id="7559e-122">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7559e-122">Database name.</span></span>

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

### <span data-ttu-id="7559e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7559e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7559e-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7559e-124">Name of resource group.</span></span>

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

### <span data-ttu-id="7559e-125">-輸送量</span><span class="sxs-lookup"><span data-stu-id="7559e-125">-Throughput</span></span>
<span data-ttu-id="7559e-126">Mongo 資料庫的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="7559e-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="7559e-127">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="7559e-127">Default value is 400.</span></span>

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

### <span data-ttu-id="7559e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7559e-128">-WhatIf</span></span>
<span data-ttu-id="7559e-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7559e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7559e-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7559e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7559e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7559e-131">CommonParameters</span></span>
<span data-ttu-id="7559e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7559e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7559e-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7559e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7559e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="7559e-134">INPUTS</span></span>

### <span data-ttu-id="7559e-135">所有</span><span class="sxs-lookup"><span data-stu-id="7559e-135">None</span></span>

## <span data-ttu-id="7559e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7559e-136">OUTPUTS</span></span>

### <span data-ttu-id="7559e-137">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7559e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="7559e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7559e-138">NOTES</span></span>

## <span data-ttu-id="7559e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7559e-139">RELATED LINKS</span></span>

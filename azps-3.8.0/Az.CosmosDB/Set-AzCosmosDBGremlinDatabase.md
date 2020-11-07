---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965882"
---
# <span data-ttu-id="26356-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="26356-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="26356-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26356-102">SYNOPSIS</span></span>
<span data-ttu-id="26356-103">設定 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="26356-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="26356-104">句法</span><span class="sxs-lookup"><span data-stu-id="26356-104">SYNTAX</span></span>

### <span data-ttu-id="26356-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="26356-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26356-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26356-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26356-107">說明</span><span class="sxs-lookup"><span data-stu-id="26356-107">DESCRIPTION</span></span>
<span data-ttu-id="26356-108">**AzCosmosDBGremlinDatabase** Cmdlet 會設定 CosmosDB Gremlin 資料庫。</span><span class="sxs-lookup"><span data-stu-id="26356-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="26356-109">示例</span><span class="sxs-lookup"><span data-stu-id="26356-109">EXAMPLES</span></span>

### <span data-ttu-id="26356-110">範例1</span><span class="sxs-lookup"><span data-stu-id="26356-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="26356-111">資源物件包含 _rid、_ts _etag。</span><span class="sxs-lookup"><span data-stu-id="26356-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="26356-112">參數</span><span class="sxs-lookup"><span data-stu-id="26356-112">PARAMETERS</span></span>

### <span data-ttu-id="26356-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26356-113">-AccountName</span></span>
<span data-ttu-id="26356-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="26356-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26356-115">-確認</span><span class="sxs-lookup"><span data-stu-id="26356-115">-Confirm</span></span>
<span data-ttu-id="26356-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26356-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26356-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26356-117">-DefaultProfile</span></span>
<span data-ttu-id="26356-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26356-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26356-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26356-119">-InputObject</span></span>
<span data-ttu-id="26356-120">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="26356-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="26356-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="26356-121">-Name</span></span>
<span data-ttu-id="26356-122">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="26356-122">Database name.</span></span>

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

### <span data-ttu-id="26356-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26356-123">-ResourceGroupName</span></span>
<span data-ttu-id="26356-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26356-124">Name of resource group.</span></span>

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

### <span data-ttu-id="26356-125">-輸送量</span><span class="sxs-lookup"><span data-stu-id="26356-125">-Throughput</span></span>
<span data-ttu-id="26356-126">Gremlin 資料庫的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="26356-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="26356-127">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="26356-127">Default value is 400.</span></span>

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

### <span data-ttu-id="26356-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26356-128">-WhatIf</span></span>
<span data-ttu-id="26356-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26356-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26356-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26356-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26356-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26356-131">CommonParameters</span></span>
<span data-ttu-id="26356-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26356-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26356-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="26356-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26356-134">輸入</span><span class="sxs-lookup"><span data-stu-id="26356-134">INPUTS</span></span>

### <span data-ttu-id="26356-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="26356-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="26356-136">輸出</span><span class="sxs-lookup"><span data-stu-id="26356-136">OUTPUTS</span></span>

### <span data-ttu-id="26356-137">PSGremlinDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="26356-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="26356-138">筆記</span><span class="sxs-lookup"><span data-stu-id="26356-138">NOTES</span></span>

## <span data-ttu-id="26356-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="26356-139">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 961ba3375c25098de32bf93b4559d9bfa6b8944d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965570"
---
# <span data-ttu-id="59c91-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="59c91-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="59c91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59c91-102">SYNOPSIS</span></span>
<span data-ttu-id="59c91-103">取得 CosmosDB Gremlin 資料庫的輸送量。</span><span class="sxs-lookup"><span data-stu-id="59c91-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="59c91-104">句法</span><span class="sxs-lookup"><span data-stu-id="59c91-104">SYNTAX</span></span>

### <span data-ttu-id="59c91-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="59c91-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59c91-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59c91-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59c91-107">說明</span><span class="sxs-lookup"><span data-stu-id="59c91-107">DESCRIPTION</span></span>
<span data-ttu-id="59c91-108">**AzCosmosDBGremlinDatabaseThroughput** Cmdlet 會取得 CosmosDB Gremlin 資料庫的輸送量。</span><span class="sxs-lookup"><span data-stu-id="59c91-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="59c91-109">示例</span><span class="sxs-lookup"><span data-stu-id="59c91-109">EXAMPLES</span></span>

### <span data-ttu-id="59c91-110">範例1</span><span class="sxs-lookup"><span data-stu-id="59c91-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="59c91-111">參數</span><span class="sxs-lookup"><span data-stu-id="59c91-111">PARAMETERS</span></span>

### <span data-ttu-id="59c91-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="59c91-112">-AccountName</span></span>
<span data-ttu-id="59c91-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="59c91-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="59c91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c91-114">-DefaultProfile</span></span>
<span data-ttu-id="59c91-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59c91-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c91-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59c91-116">-InputObject</span></span>
<span data-ttu-id="59c91-117">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="59c91-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="59c91-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="59c91-118">-Name</span></span>
<span data-ttu-id="59c91-119">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="59c91-119">Database name.</span></span>

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

### <span data-ttu-id="59c91-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c91-120">-ResourceGroupName</span></span>
<span data-ttu-id="59c91-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="59c91-121">Name of resource group.</span></span>

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

### <span data-ttu-id="59c91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c91-122">CommonParameters</span></span>
<span data-ttu-id="59c91-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59c91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c91-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="59c91-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c91-125">輸入</span><span class="sxs-lookup"><span data-stu-id="59c91-125">INPUTS</span></span>

### <span data-ttu-id="59c91-126">所有</span><span class="sxs-lookup"><span data-stu-id="59c91-126">None</span></span>

## <span data-ttu-id="59c91-127">輸出</span><span class="sxs-lookup"><span data-stu-id="59c91-127">OUTPUTS</span></span>

### <span data-ttu-id="59c91-128">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="59c91-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="59c91-129">筆記</span><span class="sxs-lookup"><span data-stu-id="59c91-129">NOTES</span></span>

## <span data-ttu-id="59c91-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="59c91-130">RELATED LINKS</span></span>

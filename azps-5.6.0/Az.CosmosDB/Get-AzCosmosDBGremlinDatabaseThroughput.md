---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 4dbfea5106b46bd8d0f1efc1926841dd964b0299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909833"
---
# <span data-ttu-id="1dbfc-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="1dbfc-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="1dbfc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbfc-103">獲得一個一流資料庫的輸送量。</span><span class="sxs-lookup"><span data-stu-id="1dbfc-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="1dbfc-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dbfc-104">SYNTAX</span></span>

### <span data-ttu-id="1dbfc-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1dbfc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbfc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dbfc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dbfc-107">描述</span><span class="sxs-lookup"><span data-stu-id="1dbfc-107">DESCRIPTION</span></span>
<span data-ttu-id="1dbfc-108">**Get-AzCosmosDBGremlinDatabaseThroughput** Cmdlet 會取得一個以一個 ThroughputsDB 的墨林資料庫。</span><span class="sxs-lookup"><span data-stu-id="1dbfc-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="1dbfc-109">例子</span><span class="sxs-lookup"><span data-stu-id="1dbfc-109">EXAMPLES</span></span>

### <span data-ttu-id="1dbfc-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1dbfc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="1dbfc-111">參數</span><span class="sxs-lookup"><span data-stu-id="1dbfc-111">PARAMETERS</span></span>

### <span data-ttu-id="1dbfc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1dbfc-112">-AccountName</span></span>
<span data-ttu-id="1dbfc-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dbfc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1dbfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbfc-114">-DefaultProfile</span></span>
<span data-ttu-id="1dbfc-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dbfc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbfc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dbfc-116">-InputObject</span></span>
<span data-ttu-id="1dbfc-117">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="1dbfc-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1dbfc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dbfc-118">-Name</span></span>
<span data-ttu-id="1dbfc-119">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1dbfc-119">Database name.</span></span>

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

### <span data-ttu-id="1dbfc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbfc-120">-ResourceGroupName</span></span>
<span data-ttu-id="1dbfc-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dbfc-121">Name of resource group.</span></span>

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

### <span data-ttu-id="1dbfc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbfc-122">CommonParameters</span></span>
<span data-ttu-id="1dbfc-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dbfc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbfc-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dbfc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbfc-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1dbfc-125">INPUTS</span></span>

### <span data-ttu-id="1dbfc-126">沒有</span><span class="sxs-lookup"><span data-stu-id="1dbfc-126">None</span></span>

## <span data-ttu-id="1dbfc-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1dbfc-127">OUTPUTS</span></span>

### <span data-ttu-id="1dbfc-128">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1dbfc-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1dbfc-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1dbfc-129">NOTES</span></span>

## <span data-ttu-id="1dbfc-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dbfc-130">RELATED LINKS</span></span>

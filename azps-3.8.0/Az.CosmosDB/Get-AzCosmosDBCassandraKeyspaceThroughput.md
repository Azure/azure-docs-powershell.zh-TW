---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 21a32bc2c3251d0069dcdb05d9eea29c52207ae8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965576"
---
# <span data-ttu-id="81ba1-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="81ba1-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="81ba1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="81ba1-103">取得 Cassandra Keyspace 的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="81ba1-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="81ba1-104">句法</span><span class="sxs-lookup"><span data-stu-id="81ba1-104">SYNTAX</span></span>

### <span data-ttu-id="81ba1-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="81ba1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81ba1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81ba1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81ba1-107">說明</span><span class="sxs-lookup"><span data-stu-id="81ba1-107">DESCRIPTION</span></span>
<span data-ttu-id="81ba1-108">**AzCosmosDBCassandraKeyspaceThroughput** Cmdlet 會取得對應至指定 Keyspace 的輸送量物件。</span><span class="sxs-lookup"><span data-stu-id="81ba1-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="81ba1-109">示例</span><span class="sxs-lookup"><span data-stu-id="81ba1-109">EXAMPLES</span></span>

### <span data-ttu-id="81ba1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="81ba1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="81ba1-111">參數</span><span class="sxs-lookup"><span data-stu-id="81ba1-111">PARAMETERS</span></span>

### <span data-ttu-id="81ba1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="81ba1-112">-AccountName</span></span>
<span data-ttu-id="81ba1-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="81ba1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="81ba1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ba1-114">-DefaultProfile</span></span>
<span data-ttu-id="81ba1-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81ba1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81ba1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81ba1-116">-InputObject</span></span>
<span data-ttu-id="81ba1-117">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="81ba1-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="81ba1-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="81ba1-118">-Name</span></span>
<span data-ttu-id="81ba1-119">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="81ba1-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="81ba1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81ba1-120">-ResourceGroupName</span></span>
<span data-ttu-id="81ba1-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81ba1-121">Name of resource group.</span></span>

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

### <span data-ttu-id="81ba1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ba1-122">CommonParameters</span></span>
<span data-ttu-id="81ba1-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81ba1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ba1-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="81ba1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ba1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="81ba1-125">INPUTS</span></span>

### <span data-ttu-id="81ba1-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="81ba1-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="81ba1-127">輸出</span><span class="sxs-lookup"><span data-stu-id="81ba1-127">OUTPUTS</span></span>

### <span data-ttu-id="81ba1-128">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="81ba1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="81ba1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="81ba1-129">NOTES</span></span>

## <span data-ttu-id="81ba1-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="81ba1-130">RELATED LINKS</span></span>
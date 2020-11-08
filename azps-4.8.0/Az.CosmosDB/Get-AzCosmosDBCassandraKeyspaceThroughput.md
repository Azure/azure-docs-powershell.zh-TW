---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128336"
---
# <span data-ttu-id="1177b-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="1177b-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="1177b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1177b-102">SYNOPSIS</span></span>
<span data-ttu-id="1177b-103">取得 Cassandra Keyspace 的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="1177b-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="1177b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1177b-104">SYNTAX</span></span>

### <span data-ttu-id="1177b-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1177b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1177b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1177b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1177b-107">說明</span><span class="sxs-lookup"><span data-stu-id="1177b-107">DESCRIPTION</span></span>
<span data-ttu-id="1177b-108">**AzCosmosDBCassandraKeyspaceThroughput** Cmdlet 會取得對應至指定 Keyspace 的輸送量物件。</span><span class="sxs-lookup"><span data-stu-id="1177b-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="1177b-109">示例</span><span class="sxs-lookup"><span data-stu-id="1177b-109">EXAMPLES</span></span>

### <span data-ttu-id="1177b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1177b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="1177b-111">參數</span><span class="sxs-lookup"><span data-stu-id="1177b-111">PARAMETERS</span></span>

### <span data-ttu-id="1177b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1177b-112">-AccountName</span></span>
<span data-ttu-id="1177b-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1177b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1177b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1177b-114">-DefaultProfile</span></span>
<span data-ttu-id="1177b-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1177b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1177b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1177b-116">-InputObject</span></span>
<span data-ttu-id="1177b-117">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="1177b-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1177b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1177b-118">-Name</span></span>
<span data-ttu-id="1177b-119">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="1177b-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1177b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1177b-120">-ResourceGroupName</span></span>
<span data-ttu-id="1177b-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1177b-121">Name of resource group.</span></span>

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

### <span data-ttu-id="1177b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1177b-122">CommonParameters</span></span>
<span data-ttu-id="1177b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1177b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1177b-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1177b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1177b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1177b-125">INPUTS</span></span>

### <span data-ttu-id="1177b-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1177b-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1177b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1177b-127">OUTPUTS</span></span>

### <span data-ttu-id="1177b-128">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="1177b-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1177b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1177b-129">NOTES</span></span>

## <span data-ttu-id="1177b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1177b-130">RELATED LINKS</span></span>
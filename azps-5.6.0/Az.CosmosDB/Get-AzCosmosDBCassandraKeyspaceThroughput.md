---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 965e7b3d1f0775f3842e423e47c1a4cc60021408
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909853"
---
# <span data-ttu-id="22892-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="22892-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="22892-102">簡介</span><span class="sxs-lookup"><span data-stu-id="22892-102">SYNOPSIS</span></span>
<span data-ttu-id="22892-103">獲得 Cassandra Keyspace 的輸送量值。</span><span class="sxs-lookup"><span data-stu-id="22892-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="22892-104">語法</span><span class="sxs-lookup"><span data-stu-id="22892-104">SYNTAX</span></span>

### <span data-ttu-id="22892-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="22892-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22892-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22892-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22892-107">描述</span><span class="sxs-lookup"><span data-stu-id="22892-107">DESCRIPTION</span></span>
<span data-ttu-id="22892-108">**Get-AzCosmosDBCassandraKeyspaceThroughput** Cmdlet 會取得對應至給定 Keyspace 的輸送量物件。</span><span class="sxs-lookup"><span data-stu-id="22892-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="22892-109">例子</span><span class="sxs-lookup"><span data-stu-id="22892-109">EXAMPLES</span></span>

### <span data-ttu-id="22892-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="22892-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="22892-111">參數</span><span class="sxs-lookup"><span data-stu-id="22892-111">PARAMETERS</span></span>

### <span data-ttu-id="22892-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22892-112">-AccountName</span></span>
<span data-ttu-id="22892-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="22892-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="22892-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22892-114">-DefaultProfile</span></span>
<span data-ttu-id="22892-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="22892-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22892-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22892-116">-InputObject</span></span>
<span data-ttu-id="22892-117">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="22892-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="22892-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="22892-118">-Name</span></span>
<span data-ttu-id="22892-119">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="22892-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="22892-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22892-120">-ResourceGroupName</span></span>
<span data-ttu-id="22892-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22892-121">Name of resource group.</span></span>

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

### <span data-ttu-id="22892-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22892-122">CommonParameters</span></span>
<span data-ttu-id="22892-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="22892-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22892-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22892-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22892-125">輸入</span><span class="sxs-lookup"><span data-stu-id="22892-125">INPUTS</span></span>

### <span data-ttu-id="22892-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="22892-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="22892-127">輸出</span><span class="sxs-lookup"><span data-stu-id="22892-127">OUTPUTS</span></span>

### <span data-ttu-id="22892-128">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="22892-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="22892-129">筆記</span><span class="sxs-lookup"><span data-stu-id="22892-129">NOTES</span></span>

## <span data-ttu-id="22892-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="22892-130">RELATED LINKS</span></span>

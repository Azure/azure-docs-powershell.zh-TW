---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1d470870d27001a07302240dba1abd7e56153d0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965553"
---
# <span data-ttu-id="dae2c-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="dae2c-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="dae2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dae2c-102">SYNOPSIS</span></span>
<span data-ttu-id="dae2c-103">取得 MongoDB 資料庫的 CosmosDB 輸送量屬性。</span><span class="sxs-lookup"><span data-stu-id="dae2c-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="dae2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="dae2c-104">SYNTAX</span></span>

### <span data-ttu-id="dae2c-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dae2c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dae2c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dae2c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dae2c-107">說明</span><span class="sxs-lookup"><span data-stu-id="dae2c-107">DESCRIPTION</span></span>
<span data-ttu-id="dae2c-108">**AzCosmosDBMongoDBDatabaseThroughput** Cmdlet 會取得 MongoDB 資料庫的輸送量屬性。</span><span class="sxs-lookup"><span data-stu-id="dae2c-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="dae2c-109">示例</span><span class="sxs-lookup"><span data-stu-id="dae2c-109">EXAMPLES</span></span>

### <span data-ttu-id="dae2c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="dae2c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="dae2c-111">參數</span><span class="sxs-lookup"><span data-stu-id="dae2c-111">PARAMETERS</span></span>

### <span data-ttu-id="dae2c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dae2c-112">-AccountName</span></span>
<span data-ttu-id="dae2c-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dae2c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dae2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae2c-114">-DefaultProfile</span></span>
<span data-ttu-id="dae2c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dae2c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dae2c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dae2c-116">-InputObject</span></span>
<span data-ttu-id="dae2c-117">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="dae2c-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="dae2c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="dae2c-118">-Name</span></span>
<span data-ttu-id="dae2c-119">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="dae2c-119">Database name.</span></span>

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

### <span data-ttu-id="dae2c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae2c-120">-ResourceGroupName</span></span>
<span data-ttu-id="dae2c-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dae2c-121">Name of resource group.</span></span>

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

### <span data-ttu-id="dae2c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae2c-122">CommonParameters</span></span>
<span data-ttu-id="dae2c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dae2c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae2c-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dae2c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae2c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="dae2c-125">INPUTS</span></span>

### <span data-ttu-id="dae2c-126">所有</span><span class="sxs-lookup"><span data-stu-id="dae2c-126">None</span></span>

## <span data-ttu-id="dae2c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="dae2c-127">OUTPUTS</span></span>

### <span data-ttu-id="dae2c-128">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dae2c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dae2c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="dae2c-129">NOTES</span></span>

## <span data-ttu-id="dae2c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="dae2c-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129711"
---
# <span data-ttu-id="fcbef-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="fcbef-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="fcbef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fcbef-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbef-103">取得 CosmosDB MongoDB 資料庫</span><span class="sxs-lookup"><span data-stu-id="fcbef-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="fcbef-104">句法</span><span class="sxs-lookup"><span data-stu-id="fcbef-104">SYNTAX</span></span>

### <span data-ttu-id="fcbef-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fcbef-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcbef-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcbef-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcbef-107">說明</span><span class="sxs-lookup"><span data-stu-id="fcbef-107">DESCRIPTION</span></span>
<span data-ttu-id="fcbef-108">**AzCosmosDBMongoDBDatabase** Cmdlet 會取得 CosmosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="fcbef-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="fcbef-109">示例</span><span class="sxs-lookup"><span data-stu-id="fcbef-109">EXAMPLES</span></span>

### <span data-ttu-id="fcbef-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fcbef-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="fcbef-111">資源物件包含 _rid、_ts _etag 屬性。</span><span class="sxs-lookup"><span data-stu-id="fcbef-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="fcbef-112">參數</span><span class="sxs-lookup"><span data-stu-id="fcbef-112">PARAMETERS</span></span>

### <span data-ttu-id="fcbef-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fcbef-113">-AccountName</span></span>
<span data-ttu-id="fcbef-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcbef-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fcbef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbef-115">-DefaultProfile</span></span>
<span data-ttu-id="fcbef-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fcbef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcbef-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fcbef-117">-Name</span></span>
<span data-ttu-id="fcbef-118">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="fcbef-118">Database name.</span></span>

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

### <span data-ttu-id="fcbef-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fcbef-119">-ParentObject</span></span>
<span data-ttu-id="fcbef-120">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="fcbef-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcbef-121">-ResourceGroupName</span></span>
<span data-ttu-id="fcbef-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcbef-122">Name of resource group.</span></span>

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

### <span data-ttu-id="fcbef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbef-123">CommonParameters</span></span>
<span data-ttu-id="fcbef-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fcbef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbef-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fcbef-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbef-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fcbef-126">INPUTS</span></span>

### <span data-ttu-id="fcbef-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fcbef-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fcbef-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fcbef-128">OUTPUTS</span></span>

### <span data-ttu-id="fcbef-129">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="fcbef-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="fcbef-130">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="fcbef-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fcbef-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fcbef-131">NOTES</span></span>

## <span data-ttu-id="fcbef-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcbef-132">RELATED LINKS</span></span>

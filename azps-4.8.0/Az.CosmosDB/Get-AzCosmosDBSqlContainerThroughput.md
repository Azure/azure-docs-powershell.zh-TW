---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135646"
---
# <span data-ttu-id="a980b-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="a980b-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="a980b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a980b-102">SYNOPSIS</span></span>
<span data-ttu-id="a980b-103">取得與 CosmosDB Sql 容器相對應的輸送量設定。</span><span class="sxs-lookup"><span data-stu-id="a980b-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="a980b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a980b-104">SYNTAX</span></span>

### <span data-ttu-id="a980b-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a980b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a980b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a980b-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a980b-107">說明</span><span class="sxs-lookup"><span data-stu-id="a980b-107">DESCRIPTION</span></span>
<span data-ttu-id="a980b-108">**AzCosmosDBSqlContainerThroughput** Cmdlet 會取得與 CosmosDB Sql 容器相對應的輸送量設定。</span><span class="sxs-lookup"><span data-stu-id="a980b-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="a980b-109">示例</span><span class="sxs-lookup"><span data-stu-id="a980b-109">EXAMPLES</span></span>

### <span data-ttu-id="a980b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a980b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="a980b-111">參數</span><span class="sxs-lookup"><span data-stu-id="a980b-111">PARAMETERS</span></span>

### <span data-ttu-id="a980b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a980b-112">-AccountName</span></span>
<span data-ttu-id="a980b-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a980b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a980b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a980b-114">-DatabaseName</span></span>
<span data-ttu-id="a980b-115">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a980b-115">Database name.</span></span>

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

### <span data-ttu-id="a980b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a980b-116">-DefaultProfile</span></span>
<span data-ttu-id="a980b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a980b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a980b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a980b-118">-InputObject</span></span>
<span data-ttu-id="a980b-119">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="a980b-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a980b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a980b-120">-Name</span></span>
<span data-ttu-id="a980b-121">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="a980b-121">Container name.</span></span>

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

### <span data-ttu-id="a980b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a980b-122">-ResourceGroupName</span></span>
<span data-ttu-id="a980b-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a980b-123">Name of resource group.</span></span>

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

### <span data-ttu-id="a980b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a980b-124">CommonParameters</span></span>
<span data-ttu-id="a980b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a980b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a980b-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a980b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a980b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a980b-127">INPUTS</span></span>

### <span data-ttu-id="a980b-128">所有</span><span class="sxs-lookup"><span data-stu-id="a980b-128">None</span></span>

## <span data-ttu-id="a980b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a980b-129">OUTPUTS</span></span>

### <span data-ttu-id="a980b-130">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="a980b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a980b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a980b-131">NOTES</span></span>

## <span data-ttu-id="a980b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a980b-132">RELATED LINKS</span></span>

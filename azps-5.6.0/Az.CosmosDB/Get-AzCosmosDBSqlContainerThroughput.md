---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 3ceb7ccbb789c21fc0fdb51244260e6a54b3e900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914157"
---
# <span data-ttu-id="80933-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="80933-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="80933-102">簡介</span><span class="sxs-lookup"><span data-stu-id="80933-102">SYNOPSIS</span></span>
<span data-ttu-id="80933-103">獲得對應至一個更新 Sql Container 的輸送量設定。</span><span class="sxs-lookup"><span data-stu-id="80933-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="80933-104">語法</span><span class="sxs-lookup"><span data-stu-id="80933-104">SYNTAX</span></span>

### <span data-ttu-id="80933-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="80933-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80933-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80933-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80933-107">描述</span><span class="sxs-lookup"><span data-stu-id="80933-107">DESCRIPTION</span></span>
<span data-ttu-id="80933-108">**Get-AzCosmosDBSqlContainerThroughput** Cmdlet 會取得對應至一個因應至一個因應的輸送量設定。</span><span class="sxs-lookup"><span data-stu-id="80933-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="80933-109">例子</span><span class="sxs-lookup"><span data-stu-id="80933-109">EXAMPLES</span></span>

### <span data-ttu-id="80933-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="80933-110">Example 1</span></span>
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

## <span data-ttu-id="80933-111">參數</span><span class="sxs-lookup"><span data-stu-id="80933-111">PARAMETERS</span></span>

### <span data-ttu-id="80933-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80933-112">-AccountName</span></span>
<span data-ttu-id="80933-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="80933-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="80933-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80933-114">-DatabaseName</span></span>
<span data-ttu-id="80933-115">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="80933-115">Database name.</span></span>

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

### <span data-ttu-id="80933-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80933-116">-DefaultProfile</span></span>
<span data-ttu-id="80933-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="80933-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80933-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80933-118">-InputObject</span></span>
<span data-ttu-id="80933-119">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="80933-119">Sql Container object.</span></span>

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

### <span data-ttu-id="80933-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="80933-120">-Name</span></span>
<span data-ttu-id="80933-121">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="80933-121">Container name.</span></span>

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

### <span data-ttu-id="80933-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80933-122">-ResourceGroupName</span></span>
<span data-ttu-id="80933-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80933-123">Name of resource group.</span></span>

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

### <span data-ttu-id="80933-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80933-124">CommonParameters</span></span>
<span data-ttu-id="80933-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="80933-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80933-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80933-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80933-127">輸入</span><span class="sxs-lookup"><span data-stu-id="80933-127">INPUTS</span></span>

### <span data-ttu-id="80933-128">沒有</span><span class="sxs-lookup"><span data-stu-id="80933-128">None</span></span>

## <span data-ttu-id="80933-129">輸出</span><span class="sxs-lookup"><span data-stu-id="80933-129">OUTPUTS</span></span>

### <span data-ttu-id="80933-130">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="80933-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="80933-131">筆記</span><span class="sxs-lookup"><span data-stu-id="80933-131">NOTES</span></span>

## <span data-ttu-id="80933-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="80933-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128338"
---
# <span data-ttu-id="2b9a2-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="2b9a2-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="2b9a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9a2-103">取得 CosmosDB 表格的輸送量。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="2b9a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b9a2-104">SYNTAX</span></span>

### <span data-ttu-id="2b9a2-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2b9a2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b9a2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b9a2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b9a2-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b9a2-107">DESCRIPTION</span></span>
<span data-ttu-id="2b9a2-108">**AzCosmosDBTableThroughput** Cmdlet 會取得 CosmosDB 資料表的輸送量。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="2b9a2-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b9a2-109">EXAMPLES</span></span>

### <span data-ttu-id="2b9a2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2b9a2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="2b9a2-111">參數</span><span class="sxs-lookup"><span data-stu-id="2b9a2-111">PARAMETERS</span></span>

### <span data-ttu-id="2b9a2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b9a2-112">-AccountName</span></span>
<span data-ttu-id="2b9a2-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2b9a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9a2-114">-DefaultProfile</span></span>
<span data-ttu-id="2b9a2-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b9a2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b9a2-116">-InputObject</span></span>
<span data-ttu-id="2b9a2-117">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="2b9a2-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2b9a2-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b9a2-118">-Name</span></span>
<span data-ttu-id="2b9a2-119">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-119">Name of the Table.</span></span>

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

### <span data-ttu-id="2b9a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="2b9a2-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-121">Name of resource group.</span></span>

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

### <span data-ttu-id="2b9a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9a2-122">CommonParameters</span></span>
<span data-ttu-id="2b9a2-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9a2-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9a2-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2b9a2-125">INPUTS</span></span>

### <span data-ttu-id="2b9a2-126">所有</span><span class="sxs-lookup"><span data-stu-id="2b9a2-126">None</span></span>

## <span data-ttu-id="2b9a2-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2b9a2-127">OUTPUTS</span></span>

### <span data-ttu-id="2b9a2-128">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2b9a2-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2b9a2-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2b9a2-129">NOTES</span></span>

## <span data-ttu-id="2b9a2-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b9a2-130">RELATED LINKS</span></span>

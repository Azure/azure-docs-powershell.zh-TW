---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129687"
---
# <span data-ttu-id="822a3-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="822a3-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="822a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="822a3-102">SYNOPSIS</span></span>
<span data-ttu-id="822a3-103">取得 CosmosDB 表格的輸送量。</span><span class="sxs-lookup"><span data-stu-id="822a3-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="822a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="822a3-104">SYNTAX</span></span>

### <span data-ttu-id="822a3-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="822a3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="822a3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="822a3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="822a3-107">說明</span><span class="sxs-lookup"><span data-stu-id="822a3-107">DESCRIPTION</span></span>
<span data-ttu-id="822a3-108">**AzCosmosDBTableThroughput** Cmdlet 會取得 CosmosDB 資料表的輸送量。</span><span class="sxs-lookup"><span data-stu-id="822a3-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="822a3-109">示例</span><span class="sxs-lookup"><span data-stu-id="822a3-109">EXAMPLES</span></span>

### <span data-ttu-id="822a3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="822a3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="822a3-111">參數</span><span class="sxs-lookup"><span data-stu-id="822a3-111">PARAMETERS</span></span>

### <span data-ttu-id="822a3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="822a3-112">-AccountName</span></span>
<span data-ttu-id="822a3-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="822a3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="822a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822a3-114">-DefaultProfile</span></span>
<span data-ttu-id="822a3-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="822a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="822a3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="822a3-116">-InputObject</span></span>
<span data-ttu-id="822a3-117">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="822a3-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="822a3-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="822a3-118">-Name</span></span>
<span data-ttu-id="822a3-119">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="822a3-119">Name of the Table.</span></span>

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

### <span data-ttu-id="822a3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822a3-120">-ResourceGroupName</span></span>
<span data-ttu-id="822a3-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="822a3-121">Name of resource group.</span></span>

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

### <span data-ttu-id="822a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822a3-122">CommonParameters</span></span>
<span data-ttu-id="822a3-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="822a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822a3-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="822a3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822a3-125">輸入</span><span class="sxs-lookup"><span data-stu-id="822a3-125">INPUTS</span></span>

### <span data-ttu-id="822a3-126">所有</span><span class="sxs-lookup"><span data-stu-id="822a3-126">None</span></span>

## <span data-ttu-id="822a3-127">輸出</span><span class="sxs-lookup"><span data-stu-id="822a3-127">OUTPUTS</span></span>

### <span data-ttu-id="822a3-128">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="822a3-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="822a3-129">筆記</span><span class="sxs-lookup"><span data-stu-id="822a3-129">NOTES</span></span>

## <span data-ttu-id="822a3-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="822a3-130">RELATED LINKS</span></span>

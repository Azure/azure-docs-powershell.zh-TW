---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966328"
---
# <span data-ttu-id="3ac25-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="3ac25-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="3ac25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ac25-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac25-103">取得 CosmosDB 資料表。</span><span class="sxs-lookup"><span data-stu-id="3ac25-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="3ac25-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ac25-104">SYNTAX</span></span>

### <span data-ttu-id="3ac25-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3ac25-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ac25-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ac25-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ac25-107">說明</span><span class="sxs-lookup"><span data-stu-id="3ac25-107">DESCRIPTION</span></span>
<span data-ttu-id="3ac25-108">**AzCosmosDBTable** Cmdlet 會取得現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="3ac25-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="3ac25-109">示例</span><span class="sxs-lookup"><span data-stu-id="3ac25-109">EXAMPLES</span></span>

### <span data-ttu-id="3ac25-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3ac25-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="3ac25-111">資源物件包含資料表的 _rid、_ts、# etag 屬性。</span><span class="sxs-lookup"><span data-stu-id="3ac25-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="3ac25-112">參數</span><span class="sxs-lookup"><span data-stu-id="3ac25-112">PARAMETERS</span></span>

### <span data-ttu-id="3ac25-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3ac25-113">-AccountName</span></span>
<span data-ttu-id="3ac25-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac25-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3ac25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac25-115">-DefaultProfile</span></span>
<span data-ttu-id="3ac25-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ac25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac25-117">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="3ac25-117">-Detailed</span></span>
<span data-ttu-id="3ac25-118">如果提供，則 Cmdlet 會傳回具有對應的輸送量值的資料表。</span><span class="sxs-lookup"><span data-stu-id="3ac25-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac25-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ac25-119">-InputObject</span></span>
<span data-ttu-id="3ac25-120">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="3ac25-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac25-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ac25-121">-Name</span></span>
<span data-ttu-id="3ac25-122">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac25-122">Name of the Table.</span></span>

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

### <span data-ttu-id="3ac25-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac25-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ac25-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac25-124">Name of resource group.</span></span>

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

### <span data-ttu-id="3ac25-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac25-125">CommonParameters</span></span>
<span data-ttu-id="3ac25-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ac25-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac25-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ac25-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac25-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3ac25-128">INPUTS</span></span>

### <span data-ttu-id="3ac25-129">所有</span><span class="sxs-lookup"><span data-stu-id="3ac25-129">None</span></span>

## <span data-ttu-id="3ac25-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3ac25-130">OUTPUTS</span></span>

### <span data-ttu-id="3ac25-131">PSTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3ac25-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="3ac25-132">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3ac25-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3ac25-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3ac25-133">NOTES</span></span>

## <span data-ttu-id="3ac25-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ac25-134">RELATED LINKS</span></span>

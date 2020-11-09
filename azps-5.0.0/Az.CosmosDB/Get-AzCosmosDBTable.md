---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285561"
---
# <span data-ttu-id="a6553-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="a6553-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="a6553-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6553-102">SYNOPSIS</span></span>
<span data-ttu-id="a6553-103">取得 CosmosDB 資料表。</span><span class="sxs-lookup"><span data-stu-id="a6553-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="a6553-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6553-104">SYNTAX</span></span>

### <span data-ttu-id="a6553-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a6553-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6553-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6553-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6553-107">說明</span><span class="sxs-lookup"><span data-stu-id="a6553-107">DESCRIPTION</span></span>
<span data-ttu-id="a6553-108">**AzCosmosDBTable** Cmdlet 會取得現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="a6553-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="a6553-109">示例</span><span class="sxs-lookup"><span data-stu-id="a6553-109">EXAMPLES</span></span>

### <span data-ttu-id="a6553-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a6553-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="a6553-111">資源物件包含資料表的 _rid、_ts、# etag 屬性。</span><span class="sxs-lookup"><span data-stu-id="a6553-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="a6553-112">參數</span><span class="sxs-lookup"><span data-stu-id="a6553-112">PARAMETERS</span></span>

### <span data-ttu-id="a6553-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6553-113">-AccountName</span></span>
<span data-ttu-id="a6553-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6553-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a6553-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6553-115">-DefaultProfile</span></span>
<span data-ttu-id="a6553-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6553-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6553-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6553-117">-Name</span></span>
<span data-ttu-id="a6553-118">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6553-118">Name of the Table.</span></span>

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

### <span data-ttu-id="a6553-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a6553-119">-ParentObject</span></span>
<span data-ttu-id="a6553-120">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="a6553-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a6553-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6553-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6553-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6553-122">Name of resource group.</span></span>

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

### <span data-ttu-id="a6553-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6553-123">CommonParameters</span></span>
<span data-ttu-id="a6553-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6553-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6553-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a6553-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6553-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a6553-126">INPUTS</span></span>

### <span data-ttu-id="a6553-127">所有</span><span class="sxs-lookup"><span data-stu-id="a6553-127">None</span></span>

## <span data-ttu-id="a6553-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a6553-128">OUTPUTS</span></span>

### <span data-ttu-id="a6553-129">PSTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="a6553-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="a6553-130">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="a6553-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a6553-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a6553-131">NOTES</span></span>

## <span data-ttu-id="a6553-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6553-132">RELATED LINKS</span></span>

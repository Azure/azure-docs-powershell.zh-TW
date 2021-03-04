---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: c83e1d2edba5f34a4d8478ae97cee09b57f823ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910734"
---
# <span data-ttu-id="7a7f8-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="7a7f8-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="7a7f8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7a7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7f8-103">獲得一個科克斯DB 表格。</span><span class="sxs-lookup"><span data-stu-id="7a7f8-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="7a7f8-104">語法</span><span class="sxs-lookup"><span data-stu-id="7a7f8-104">SYNTAX</span></span>

### <span data-ttu-id="7a7f8-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7a7f8-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a7f8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a7f8-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7f8-107">描述</span><span class="sxs-lookup"><span data-stu-id="7a7f8-107">DESCRIPTION</span></span>
<span data-ttu-id="7a7f8-108">**Get-AzCosmosDBTable** Cmdlet 會取得現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="7a7f8-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="7a7f8-109">例子</span><span class="sxs-lookup"><span data-stu-id="7a7f8-109">EXAMPLES</span></span>

### <span data-ttu-id="7a7f8-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="7a7f8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="7a7f8-111">資源物件包含_rid、_ts、 _ etag 屬性的表格。</span><span class="sxs-lookup"><span data-stu-id="7a7f8-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="7a7f8-112">參數</span><span class="sxs-lookup"><span data-stu-id="7a7f8-112">PARAMETERS</span></span>

### <span data-ttu-id="7a7f8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a7f8-113">-AccountName</span></span>
<span data-ttu-id="7a7f8-114">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a7f8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7a7f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7f8-115">-DefaultProfile</span></span>
<span data-ttu-id="7a7f8-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a7f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a7f8-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a7f8-117">-Name</span></span>
<span data-ttu-id="7a7f8-118">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a7f8-118">Name of the Table.</span></span>

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

### <span data-ttu-id="7a7f8-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7a7f8-119">-ParentObject</span></span>
<span data-ttu-id="7a7f8-120">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="7a7f8-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7a7f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="7a7f8-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a7f8-122">Name of resource group.</span></span>

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

### <span data-ttu-id="7a7f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7f8-123">CommonParameters</span></span>
<span data-ttu-id="7a7f8-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7a7f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7f8-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a7f8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7f8-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7a7f8-126">INPUTS</span></span>

### <span data-ttu-id="7a7f8-127">沒有</span><span class="sxs-lookup"><span data-stu-id="7a7f8-127">None</span></span>

## <span data-ttu-id="7a7f8-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7a7f8-128">OUTPUTS</span></span>

### <span data-ttu-id="7a7f8-129">Microsoft.Azure.Commands.AzsDB.models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="7a7f8-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="7a7f8-130">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7a7f8-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7a7f8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7a7f8-131">NOTES</span></span>

## <span data-ttu-id="7a7f8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a7f8-132">RELATED LINKS</span></span>

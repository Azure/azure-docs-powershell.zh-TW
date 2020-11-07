---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958135"
---
# <span data-ttu-id="e9813-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="e9813-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="e9813-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9813-102">SYNOPSIS</span></span>
<span data-ttu-id="e9813-103">設定 CosmosDB 資料表。</span><span class="sxs-lookup"><span data-stu-id="e9813-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="e9813-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9813-104">SYNTAX</span></span>

### <span data-ttu-id="e9813-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e9813-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9813-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9813-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9813-107">說明</span><span class="sxs-lookup"><span data-stu-id="e9813-107">DESCRIPTION</span></span>
<span data-ttu-id="e9813-108">**AzCosmosDBTable** Cmdlet 會建立新的資料表，或更新現有的資料表，完全取代現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="e9813-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="e9813-109">示例</span><span class="sxs-lookup"><span data-stu-id="e9813-109">EXAMPLES</span></span>

### <span data-ttu-id="e9813-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e9813-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="e9813-111">資源物件包含資料表的 _rid、_ts、# etag 屬性。</span><span class="sxs-lookup"><span data-stu-id="e9813-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="e9813-112">參數</span><span class="sxs-lookup"><span data-stu-id="e9813-112">PARAMETERS</span></span>

### <span data-ttu-id="e9813-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e9813-113">-AccountName</span></span>
<span data-ttu-id="e9813-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9813-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e9813-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e9813-115">-Confirm</span></span>
<span data-ttu-id="e9813-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9813-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9813-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9813-117">-DefaultProfile</span></span>
<span data-ttu-id="e9813-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9813-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9813-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9813-119">-InputObject</span></span>
<span data-ttu-id="e9813-120">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="e9813-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9813-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9813-121">-Name</span></span>
<span data-ttu-id="e9813-122">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9813-122">Name of the Table.</span></span>

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

### <span data-ttu-id="e9813-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9813-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9813-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9813-124">Name of resource group.</span></span>

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

### <span data-ttu-id="e9813-125">-輸送量</span><span class="sxs-lookup"><span data-stu-id="e9813-125">-Throughput</span></span>
<span data-ttu-id="e9813-126">資料表 (RU/s) 的輸送量。</span><span class="sxs-lookup"><span data-stu-id="e9813-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="e9813-127">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="e9813-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9813-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9813-128">-WhatIf</span></span>
<span data-ttu-id="e9813-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9813-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9813-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9813-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9813-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9813-131">CommonParameters</span></span>
<span data-ttu-id="e9813-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9813-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9813-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9813-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9813-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e9813-134">INPUTS</span></span>

### <span data-ttu-id="e9813-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e9813-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e9813-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e9813-136">OUTPUTS</span></span>

### <span data-ttu-id="e9813-137">PSTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="e9813-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="e9813-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e9813-138">NOTES</span></span>

## <span data-ttu-id="e9813-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9813-139">RELATED LINKS</span></span>

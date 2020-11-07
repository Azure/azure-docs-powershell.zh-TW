---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956496"
---
# <span data-ttu-id="1848a-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1848a-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="1848a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1848a-102">SYNOPSIS</span></span>
<span data-ttu-id="1848a-103">建立新的 CosmosDB Sql 資料庫或更新現有的 Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1848a-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="1848a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1848a-104">SYNTAX</span></span>

### <span data-ttu-id="1848a-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1848a-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1848a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1848a-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1848a-107">說明</span><span class="sxs-lookup"><span data-stu-id="1848a-107">DESCRIPTION</span></span>
<span data-ttu-id="1848a-108">**AzCosmosDBSqlDatabase** Cmdlet 會建立新的或更新現有的 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1848a-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="1848a-109">示例</span><span class="sxs-lookup"><span data-stu-id="1848a-109">EXAMPLES</span></span>

### <span data-ttu-id="1848a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1848a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="1848a-111">參數</span><span class="sxs-lookup"><span data-stu-id="1848a-111">PARAMETERS</span></span>

### <span data-ttu-id="1848a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1848a-112">-AccountName</span></span>
<span data-ttu-id="1848a-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1848a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1848a-114">-確認</span><span class="sxs-lookup"><span data-stu-id="1848a-114">-Confirm</span></span>
<span data-ttu-id="1848a-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1848a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1848a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1848a-116">-DefaultProfile</span></span>
<span data-ttu-id="1848a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1848a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1848a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1848a-118">-InputObject</span></span>
<span data-ttu-id="1848a-119">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="1848a-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1848a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1848a-120">-Name</span></span>
<span data-ttu-id="1848a-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1848a-121">Database name.</span></span>

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

### <span data-ttu-id="1848a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1848a-122">-ResourceGroupName</span></span>
<span data-ttu-id="1848a-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1848a-123">Name of resource group.</span></span>

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

### <span data-ttu-id="1848a-124">-輸送量</span><span class="sxs-lookup"><span data-stu-id="1848a-124">-Throughput</span></span>
<span data-ttu-id="1848a-125">SQL database 的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="1848a-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="1848a-126">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="1848a-126">Default value is 400.</span></span>

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

### <span data-ttu-id="1848a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1848a-127">-WhatIf</span></span>
<span data-ttu-id="1848a-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1848a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1848a-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1848a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1848a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1848a-130">CommonParameters</span></span>
<span data-ttu-id="1848a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1848a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1848a-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1848a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1848a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1848a-133">INPUTS</span></span>

### <span data-ttu-id="1848a-134">所有</span><span class="sxs-lookup"><span data-stu-id="1848a-134">None</span></span>

## <span data-ttu-id="1848a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1848a-135">OUTPUTS</span></span>

### <span data-ttu-id="1848a-136">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="1848a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="1848a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1848a-137">NOTES</span></span>

## <span data-ttu-id="1848a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1848a-138">RELATED LINKS</span></span>

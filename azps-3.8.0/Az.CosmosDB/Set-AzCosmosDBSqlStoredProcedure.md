---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 2914284849fa9a00e3cb2d0b1c96c1efd905e9e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956493"
---
# <span data-ttu-id="fce7c-101">Set-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="fce7c-101">Set-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="fce7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fce7c-102">SYNOPSIS</span></span>
<span data-ttu-id="fce7c-103">建立新的或更新現有的 CosmosDB Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="fce7c-103">Creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="fce7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="fce7c-104">SYNTAX</span></span>

### <span data-ttu-id="fce7c-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fce7c-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fce7c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fce7c-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fce7c-107">說明</span><span class="sxs-lookup"><span data-stu-id="fce7c-107">DESCRIPTION</span></span>
<span data-ttu-id="fce7c-108">**AzCosmosDBSqlStoredProcedure** Cmdlet 會建立新的或更新現有的 CosmosDB Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="fce7c-108">The **Set-AzCosmosDBSqlStoredProcedure** cmdlet creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="fce7c-109">示例</span><span class="sxs-lookup"><span data-stu-id="fce7c-109">EXAMPLES</span></span>

### <span data-ttu-id="fce7c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fce7c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName} -Body {sampleBody}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
SqlStoredProcedureGetResultsId :
Body                           :
_rid                           :
_ts                            :
_etag                          :
```

## <span data-ttu-id="fce7c-111">參數</span><span class="sxs-lookup"><span data-stu-id="fce7c-111">PARAMETERS</span></span>

### <span data-ttu-id="fce7c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fce7c-112">-AccountName</span></span>
<span data-ttu-id="fce7c-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="fce7c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fce7c-114">-Body</span><span class="sxs-lookup"><span data-stu-id="fce7c-114">-Body</span></span>
<span data-ttu-id="fce7c-115">已儲存程式的內文。</span><span class="sxs-lookup"><span data-stu-id="fce7c-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="fce7c-116">-確認</span><span class="sxs-lookup"><span data-stu-id="fce7c-116">-Confirm</span></span>
<span data-ttu-id="fce7c-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fce7c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fce7c-118">-容器</span><span class="sxs-lookup"><span data-stu-id="fce7c-118">-ContainerName</span></span>
<span data-ttu-id="fce7c-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="fce7c-119">Container name.</span></span>

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

### <span data-ttu-id="fce7c-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fce7c-120">-DatabaseName</span></span>
<span data-ttu-id="fce7c-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="fce7c-121">Database name.</span></span>

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

### <span data-ttu-id="fce7c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce7c-122">-DefaultProfile</span></span>
<span data-ttu-id="fce7c-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fce7c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fce7c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fce7c-124">-InputObject</span></span>
<span data-ttu-id="fce7c-125">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="fce7c-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fce7c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="fce7c-126">-Name</span></span>
<span data-ttu-id="fce7c-127">儲存的 Prcodecure 名稱。</span><span class="sxs-lookup"><span data-stu-id="fce7c-127">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="fce7c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce7c-128">-ResourceGroupName</span></span>
<span data-ttu-id="fce7c-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fce7c-129">Name of resource group.</span></span>

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

### <span data-ttu-id="fce7c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce7c-130">-WhatIf</span></span>
<span data-ttu-id="fce7c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fce7c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fce7c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fce7c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fce7c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce7c-133">CommonParameters</span></span>
<span data-ttu-id="fce7c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fce7c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce7c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fce7c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce7c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fce7c-136">INPUTS</span></span>

### <span data-ttu-id="fce7c-137">所有</span><span class="sxs-lookup"><span data-stu-id="fce7c-137">None</span></span>

## <span data-ttu-id="fce7c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fce7c-138">OUTPUTS</span></span>

### <span data-ttu-id="fce7c-139">PSSqlStoredProcedureGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="fce7c-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="fce7c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="fce7c-140">NOTES</span></span>

## <span data-ttu-id="fce7c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fce7c-141">RELATED LINKS</span></span>

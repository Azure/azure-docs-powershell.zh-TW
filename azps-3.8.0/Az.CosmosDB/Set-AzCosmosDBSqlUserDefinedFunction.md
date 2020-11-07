---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 27363873996505a15e8eccd3dcb3620a2f88c1a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796797"
---
# <span data-ttu-id="26f72-101">Set-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="26f72-101">Set-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="26f72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26f72-102">SYNOPSIS</span></span>
<span data-ttu-id="26f72-103">建立新的或更新現有的 CosmosDB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="26f72-103">Creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="26f72-104">句法</span><span class="sxs-lookup"><span data-stu-id="26f72-104">SYNTAX</span></span>

### <span data-ttu-id="26f72-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="26f72-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f72-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f72-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26f72-107">說明</span><span class="sxs-lookup"><span data-stu-id="26f72-107">DESCRIPTION</span></span>
<span data-ttu-id="26f72-108">**AzCosmosDBSqlUserDefinedFunction** Cmdlet 會建立新的或更新現有的 CosmosDB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="26f72-108">The **Set-AzCosmosDBSqlUserDefinedFunction** cmdlet creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="26f72-109">示例</span><span class="sxs-lookup"><span data-stu-id="26f72-109">EXAMPLES</span></span>

### <span data-ttu-id="26f72-110">範例1</span><span class="sxs-lookup"><span data-stu-id="26f72-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {udfName} -ContainerName {containerName} -Body {sampleBody}

Name                               : {udfName}
Id                                 : {udfId}
SqlUserDefinedFunctionGetResultsId :
Body                               :
_rid                               :
_ts                                :
_etag                              :
```

## <span data-ttu-id="26f72-111">參數</span><span class="sxs-lookup"><span data-stu-id="26f72-111">PARAMETERS</span></span>

### <span data-ttu-id="26f72-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26f72-112">-AccountName</span></span>
<span data-ttu-id="26f72-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="26f72-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26f72-114">-Body</span><span class="sxs-lookup"><span data-stu-id="26f72-114">-Body</span></span>
<span data-ttu-id="26f72-115">使用者定義函數的主體。</span><span class="sxs-lookup"><span data-stu-id="26f72-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="26f72-116">-確認</span><span class="sxs-lookup"><span data-stu-id="26f72-116">-Confirm</span></span>
<span data-ttu-id="26f72-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26f72-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f72-118">-容器</span><span class="sxs-lookup"><span data-stu-id="26f72-118">-ContainerName</span></span>
<span data-ttu-id="26f72-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="26f72-119">Container name.</span></span>

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

### <span data-ttu-id="26f72-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26f72-120">-DatabaseName</span></span>
<span data-ttu-id="26f72-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="26f72-121">Database name.</span></span>

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

### <span data-ttu-id="26f72-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f72-122">-DefaultProfile</span></span>
<span data-ttu-id="26f72-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26f72-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f72-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26f72-124">-InputObject</span></span>
<span data-ttu-id="26f72-125">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="26f72-125">Sql Container object.</span></span>

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

### <span data-ttu-id="26f72-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="26f72-126">-Name</span></span>
<span data-ttu-id="26f72-127">使用者定義的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="26f72-127">User Defined Function Name.</span></span>

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

### <span data-ttu-id="26f72-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f72-128">-ResourceGroupName</span></span>
<span data-ttu-id="26f72-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26f72-129">Name of resource group.</span></span>

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

### <span data-ttu-id="26f72-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f72-130">-WhatIf</span></span>
<span data-ttu-id="26f72-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26f72-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26f72-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f72-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f72-133">CommonParameters</span></span>
<span data-ttu-id="26f72-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26f72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f72-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="26f72-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f72-136">輸入</span><span class="sxs-lookup"><span data-stu-id="26f72-136">INPUTS</span></span>

### <span data-ttu-id="26f72-137">所有</span><span class="sxs-lookup"><span data-stu-id="26f72-137">None</span></span>

## <span data-ttu-id="26f72-138">輸出</span><span class="sxs-lookup"><span data-stu-id="26f72-138">OUTPUTS</span></span>

### <span data-ttu-id="26f72-139">PSSqlUserDefinedFunctionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="26f72-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="26f72-140">筆記</span><span class="sxs-lookup"><span data-stu-id="26f72-140">NOTES</span></span>

## <span data-ttu-id="26f72-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f72-141">RELATED LINKS</span></span>

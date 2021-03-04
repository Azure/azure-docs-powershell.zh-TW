---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: ab64359e8db417c3c87a49a773fe56c3dcc5334b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903281"
---
# <span data-ttu-id="32b56-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="32b56-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="32b56-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32b56-102">SYNOPSIS</span></span>
<span data-ttu-id="32b56-103">刪除集區DB Sql Container。</span><span class="sxs-lookup"><span data-stu-id="32b56-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="32b56-104">語法</span><span class="sxs-lookup"><span data-stu-id="32b56-104">SYNTAX</span></span>

### <span data-ttu-id="32b56-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="32b56-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32b56-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32b56-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32b56-107">描述</span><span class="sxs-lookup"><span data-stu-id="32b56-107">DESCRIPTION</span></span>
<span data-ttu-id="32b56-108">**Remove-AzCosmosDBSqlContainer Cmdlet** 會刪除對應到給定 ResourceGroupName、AccountName、DatabaseName 和 ContainerName 的一個一切 Sql Container。</span><span class="sxs-lookup"><span data-stu-id="32b56-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="32b56-109">例子</span><span class="sxs-lookup"><span data-stu-id="32b56-109">EXAMPLES</span></span>

### <span data-ttu-id="32b56-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="32b56-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="32b56-111">參數</span><span class="sxs-lookup"><span data-stu-id="32b56-111">PARAMETERS</span></span>

### <span data-ttu-id="32b56-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="32b56-112">-AccountName</span></span>
<span data-ttu-id="32b56-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="32b56-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="32b56-114">-確認</span><span class="sxs-lookup"><span data-stu-id="32b56-114">-Confirm</span></span>
<span data-ttu-id="32b56-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="32b56-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b56-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32b56-116">-DatabaseName</span></span>
<span data-ttu-id="32b56-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="32b56-117">Database name.</span></span>

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

### <span data-ttu-id="32b56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b56-118">-DefaultProfile</span></span>
<span data-ttu-id="32b56-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="32b56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b56-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32b56-120">-InputObject</span></span>
<span data-ttu-id="32b56-121">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="32b56-121">Sql Container object.</span></span>

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

### <span data-ttu-id="32b56-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="32b56-122">-Name</span></span>
<span data-ttu-id="32b56-123">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="32b56-123">Container name.</span></span>

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

### <span data-ttu-id="32b56-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32b56-124">-PassThru</span></span>
<span data-ttu-id="32b56-125">如果使用者想要接收輸出，則設為 True。</span><span class="sxs-lookup"><span data-stu-id="32b56-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="32b56-126">如果作業成功，則輸出為 True，若未成功，則系統即會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="32b56-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="32b56-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b56-127">-ResourceGroupName</span></span>
<span data-ttu-id="32b56-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="32b56-128">Name of resource group.</span></span>

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

### <span data-ttu-id="32b56-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b56-129">-WhatIf</span></span>
<span data-ttu-id="32b56-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32b56-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b56-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32b56-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b56-132">CommonParameters</span></span>
<span data-ttu-id="32b56-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32b56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b56-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32b56-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b56-135">輸入</span><span class="sxs-lookup"><span data-stu-id="32b56-135">INPUTS</span></span>

### <span data-ttu-id="32b56-136">沒有</span><span class="sxs-lookup"><span data-stu-id="32b56-136">None</span></span>

## <span data-ttu-id="32b56-137">輸出</span><span class="sxs-lookup"><span data-stu-id="32b56-137">OUTPUTS</span></span>

### <span data-ttu-id="32b56-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="32b56-138">System.Void</span></span>

### <span data-ttu-id="32b56-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32b56-139">System.Boolean</span></span>

## <span data-ttu-id="32b56-140">筆記</span><span class="sxs-lookup"><span data-stu-id="32b56-140">NOTES</span></span>

## <span data-ttu-id="32b56-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="32b56-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136058"
---
# <span data-ttu-id="c48ff-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c48ff-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="c48ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c48ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c48ff-103">刪除 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="c48ff-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="c48ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="c48ff-104">SYNTAX</span></span>

### <span data-ttu-id="c48ff-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c48ff-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c48ff-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c48ff-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c48ff-107">說明</span><span class="sxs-lookup"><span data-stu-id="c48ff-107">DESCRIPTION</span></span>
<span data-ttu-id="c48ff-108">**AzCosmosDBSqlDatabase** Cmdlet 會刪除對應至指定 ResourceGroupName、AccountName 和 DatabaseName 的 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="c48ff-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="c48ff-109">示例</span><span class="sxs-lookup"><span data-stu-id="c48ff-109">EXAMPLES</span></span>

### <span data-ttu-id="c48ff-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c48ff-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="c48ff-111">參數</span><span class="sxs-lookup"><span data-stu-id="c48ff-111">PARAMETERS</span></span>

### <span data-ttu-id="c48ff-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c48ff-112">-AccountName</span></span>
<span data-ttu-id="c48ff-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c48ff-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c48ff-114">-確認</span><span class="sxs-lookup"><span data-stu-id="c48ff-114">-Confirm</span></span>
<span data-ttu-id="c48ff-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c48ff-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c48ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48ff-116">-DefaultProfile</span></span>
<span data-ttu-id="c48ff-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c48ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c48ff-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c48ff-118">-InputObject</span></span>
<span data-ttu-id="c48ff-119">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="c48ff-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ff-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c48ff-120">-Name</span></span>
<span data-ttu-id="c48ff-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c48ff-121">Database name.</span></span>

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

### <span data-ttu-id="c48ff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c48ff-122">-PassThru</span></span>
<span data-ttu-id="c48ff-123">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="c48ff-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c48ff-124">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c48ff-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c48ff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48ff-125">-ResourceGroupName</span></span>
<span data-ttu-id="c48ff-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c48ff-126">Name of resource group.</span></span>

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

### <span data-ttu-id="c48ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c48ff-127">-WhatIf</span></span>
<span data-ttu-id="c48ff-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c48ff-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c48ff-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c48ff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c48ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48ff-130">CommonParameters</span></span>
<span data-ttu-id="c48ff-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c48ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48ff-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c48ff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48ff-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c48ff-133">INPUTS</span></span>

### <span data-ttu-id="c48ff-134">所有</span><span class="sxs-lookup"><span data-stu-id="c48ff-134">None</span></span>

## <span data-ttu-id="c48ff-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c48ff-135">OUTPUTS</span></span>

### <span data-ttu-id="c48ff-136">System.void</span><span class="sxs-lookup"><span data-stu-id="c48ff-136">System.Void</span></span>

### <span data-ttu-id="c48ff-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c48ff-137">System.Boolean</span></span>

## <span data-ttu-id="c48ff-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c48ff-138">NOTES</span></span>

## <span data-ttu-id="c48ff-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c48ff-139">RELATED LINKS</span></span>
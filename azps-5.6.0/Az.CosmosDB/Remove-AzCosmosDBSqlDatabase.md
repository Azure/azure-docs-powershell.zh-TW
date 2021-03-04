---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: a56a7a091544bef7c66ab26c66c54aded8bebdf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904709"
---
# <span data-ttu-id="1fcb8-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1fcb8-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="1fcb8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1fcb8-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcb8-103">刪除一些系統管理資料庫。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="1fcb8-104">語法</span><span class="sxs-lookup"><span data-stu-id="1fcb8-104">SYNTAX</span></span>

### <span data-ttu-id="1fcb8-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fcb8-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fcb8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fcb8-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fcb8-107">描述</span><span class="sxs-lookup"><span data-stu-id="1fcb8-107">DESCRIPTION</span></span>
<span data-ttu-id="1fcb8-108">**Remove-AzCosmosDBSqlDatabase** Cmdlet 會刪除對應至給定 ResourceGroupName、AccountName 和 DatabaseName 的一個一切 Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="1fcb8-109">例子</span><span class="sxs-lookup"><span data-stu-id="1fcb8-109">EXAMPLES</span></span>

### <span data-ttu-id="1fcb8-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1fcb8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="1fcb8-111">參數</span><span class="sxs-lookup"><span data-stu-id="1fcb8-111">PARAMETERS</span></span>

### <span data-ttu-id="1fcb8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1fcb8-112">-AccountName</span></span>
<span data-ttu-id="1fcb8-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1fcb8-114">-確認</span><span class="sxs-lookup"><span data-stu-id="1fcb8-114">-Confirm</span></span>
<span data-ttu-id="1fcb8-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcb8-116">-DefaultProfile</span></span>
<span data-ttu-id="1fcb8-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fcb8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fcb8-118">-InputObject</span></span>
<span data-ttu-id="1fcb8-119">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-119">Sql Database object.</span></span>

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

### <span data-ttu-id="1fcb8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fcb8-120">-Name</span></span>
<span data-ttu-id="1fcb8-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-121">Database name.</span></span>

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

### <span data-ttu-id="1fcb8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fcb8-122">-PassThru</span></span>
<span data-ttu-id="1fcb8-123">如果使用者想要接收輸出，則設為 True。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="1fcb8-124">如果作業成功，則輸出為 True，若未成功，則系統即會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="1fcb8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcb8-125">-ResourceGroupName</span></span>
<span data-ttu-id="1fcb8-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-126">Name of resource group.</span></span>

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

### <span data-ttu-id="1fcb8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcb8-127">-WhatIf</span></span>
<span data-ttu-id="1fcb8-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fcb8-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcb8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcb8-130">CommonParameters</span></span>
<span data-ttu-id="1fcb8-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1fcb8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcb8-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fcb8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcb8-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1fcb8-133">INPUTS</span></span>

### <span data-ttu-id="1fcb8-134">沒有</span><span class="sxs-lookup"><span data-stu-id="1fcb8-134">None</span></span>

## <span data-ttu-id="1fcb8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1fcb8-135">OUTPUTS</span></span>

### <span data-ttu-id="1fcb8-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="1fcb8-136">System.Void</span></span>

### <span data-ttu-id="1fcb8-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1fcb8-137">System.Boolean</span></span>

## <span data-ttu-id="1fcb8-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1fcb8-138">NOTES</span></span>

## <span data-ttu-id="1fcb8-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fcb8-139">RELATED LINKS</span></span>

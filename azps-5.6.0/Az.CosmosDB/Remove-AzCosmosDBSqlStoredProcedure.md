---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 985c501f93f2d37900b8ad62acc16f8508e51023
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905593"
---
# <span data-ttu-id="84488-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="84488-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="84488-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84488-102">SYNOPSIS</span></span>
<span data-ttu-id="84488-103">刪除一切資訊庫 Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="84488-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="84488-104">語法</span><span class="sxs-lookup"><span data-stu-id="84488-104">SYNTAX</span></span>

### <span data-ttu-id="84488-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84488-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84488-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84488-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84488-107">描述</span><span class="sxs-lookup"><span data-stu-id="84488-107">DESCRIPTION</span></span>
<span data-ttu-id="84488-108">**Remove-AzCosmosDBSqlStoredProcedure Cmdlet** 會刪除對應至給定 ResourceGroupName、AccountName 和 DatabaseName 的一個系統管理中心 Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="84488-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="84488-109">例子</span><span class="sxs-lookup"><span data-stu-id="84488-109">EXAMPLES</span></span>

### <span data-ttu-id="84488-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="84488-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="84488-111">參數</span><span class="sxs-lookup"><span data-stu-id="84488-111">PARAMETERS</span></span>

### <span data-ttu-id="84488-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="84488-112">-AccountName</span></span>
<span data-ttu-id="84488-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="84488-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="84488-114">-確認</span><span class="sxs-lookup"><span data-stu-id="84488-114">-Confirm</span></span>
<span data-ttu-id="84488-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="84488-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84488-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="84488-116">-ContainerName</span></span>
<span data-ttu-id="84488-117">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="84488-117">Container name.</span></span>

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

### <span data-ttu-id="84488-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="84488-118">-DatabaseName</span></span>
<span data-ttu-id="84488-119">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="84488-119">Database name.</span></span>

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

### <span data-ttu-id="84488-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84488-120">-DefaultProfile</span></span>
<span data-ttu-id="84488-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84488-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84488-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84488-122">-InputObject</span></span>
<span data-ttu-id="84488-123">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="84488-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84488-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="84488-124">-Name</span></span>
<span data-ttu-id="84488-125">儲存的 Prcodecure 名稱。</span><span class="sxs-lookup"><span data-stu-id="84488-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="84488-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84488-126">-PassThru</span></span>
<span data-ttu-id="84488-127">如果使用者想要接收輸出，則設為 True。</span><span class="sxs-lookup"><span data-stu-id="84488-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="84488-128">如果作業成功，則輸出為 True，若未成功，則系統即會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="84488-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="84488-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84488-129">-ResourceGroupName</span></span>
<span data-ttu-id="84488-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84488-130">Name of resource group.</span></span>

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

### <span data-ttu-id="84488-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84488-131">-WhatIf</span></span>
<span data-ttu-id="84488-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84488-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84488-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84488-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84488-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84488-134">CommonParameters</span></span>
<span data-ttu-id="84488-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84488-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84488-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84488-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84488-137">輸入</span><span class="sxs-lookup"><span data-stu-id="84488-137">INPUTS</span></span>

### <span data-ttu-id="84488-138">沒有</span><span class="sxs-lookup"><span data-stu-id="84488-138">None</span></span>

## <span data-ttu-id="84488-139">輸出</span><span class="sxs-lookup"><span data-stu-id="84488-139">OUTPUTS</span></span>

### <span data-ttu-id="84488-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="84488-140">System.Void</span></span>

### <span data-ttu-id="84488-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84488-141">System.Boolean</span></span>

## <span data-ttu-id="84488-142">筆記</span><span class="sxs-lookup"><span data-stu-id="84488-142">NOTES</span></span>

## <span data-ttu-id="84488-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="84488-143">RELATED LINKS</span></span>

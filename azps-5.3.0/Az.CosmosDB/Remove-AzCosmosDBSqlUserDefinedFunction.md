---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446008"
---
# <span data-ttu-id="716bf-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="716bf-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="716bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="716bf-102">SYNOPSIS</span></span>
<span data-ttu-id="716bf-103">刪除 CosmosDB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="716bf-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="716bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="716bf-104">SYNTAX</span></span>

### <span data-ttu-id="716bf-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="716bf-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="716bf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="716bf-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="716bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="716bf-107">DESCRIPTION</span></span>
<span data-ttu-id="716bf-108">**AzCosmosDBSqlUserDefinedFunction** Cmdlet 會刪除對應于指定 ResourceGroupName、AccountName 和 DatabaseName 的 CosmosDB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="716bf-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="716bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="716bf-109">EXAMPLES</span></span>

### <span data-ttu-id="716bf-110">範例1</span><span class="sxs-lookup"><span data-stu-id="716bf-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="716bf-111">參數</span><span class="sxs-lookup"><span data-stu-id="716bf-111">PARAMETERS</span></span>

### <span data-ttu-id="716bf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="716bf-112">-AccountName</span></span>
<span data-ttu-id="716bf-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="716bf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="716bf-114">-確認</span><span class="sxs-lookup"><span data-stu-id="716bf-114">-Confirm</span></span>
<span data-ttu-id="716bf-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="716bf-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="716bf-116">-容器</span><span class="sxs-lookup"><span data-stu-id="716bf-116">-ContainerName</span></span>
<span data-ttu-id="716bf-117">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="716bf-117">Container name.</span></span>

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

### <span data-ttu-id="716bf-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="716bf-118">-DatabaseName</span></span>
<span data-ttu-id="716bf-119">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="716bf-119">Database name.</span></span>

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

### <span data-ttu-id="716bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716bf-120">-DefaultProfile</span></span>
<span data-ttu-id="716bf-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="716bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="716bf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="716bf-122">-InputObject</span></span>
<span data-ttu-id="716bf-123">Sql 使用者定義函數物件</span><span class="sxs-lookup"><span data-stu-id="716bf-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="716bf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="716bf-124">-Name</span></span>
<span data-ttu-id="716bf-125">使用者定義的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="716bf-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="716bf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="716bf-126">-PassThru</span></span>
<span data-ttu-id="716bf-127">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="716bf-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="716bf-128">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="716bf-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="716bf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716bf-129">-ResourceGroupName</span></span>
<span data-ttu-id="716bf-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="716bf-130">Name of resource group.</span></span>

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

### <span data-ttu-id="716bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="716bf-131">-WhatIf</span></span>
<span data-ttu-id="716bf-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="716bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="716bf-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="716bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="716bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716bf-134">CommonParameters</span></span>
<span data-ttu-id="716bf-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="716bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716bf-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="716bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716bf-137">輸入</span><span class="sxs-lookup"><span data-stu-id="716bf-137">INPUTS</span></span>

### <span data-ttu-id="716bf-138">所有</span><span class="sxs-lookup"><span data-stu-id="716bf-138">None</span></span>

## <span data-ttu-id="716bf-139">輸出</span><span class="sxs-lookup"><span data-stu-id="716bf-139">OUTPUTS</span></span>

### <span data-ttu-id="716bf-140">System.void</span><span class="sxs-lookup"><span data-stu-id="716bf-140">System.Void</span></span>

### <span data-ttu-id="716bf-141">System.object</span><span class="sxs-lookup"><span data-stu-id="716bf-141">System.Boolean</span></span>

## <span data-ttu-id="716bf-142">筆記</span><span class="sxs-lookup"><span data-stu-id="716bf-142">NOTES</span></span>

## <span data-ttu-id="716bf-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="716bf-143">RELATED LINKS</span></span>

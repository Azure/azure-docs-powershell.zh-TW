---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128799"
---
# <span data-ttu-id="007a2-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="007a2-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="007a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="007a2-102">SYNOPSIS</span></span>
<span data-ttu-id="007a2-103">刪除 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="007a2-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="007a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="007a2-104">SYNTAX</span></span>

### <span data-ttu-id="007a2-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="007a2-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007a2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="007a2-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="007a2-107">說明</span><span class="sxs-lookup"><span data-stu-id="007a2-107">DESCRIPTION</span></span>
<span data-ttu-id="007a2-108">AzCosmosDBSqlTrigger Cmdlet 會刪除對應至指定 ResourceGroupName、AccountName 和 DatabaseName 的 CosmosDB Sql 觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="007a2-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="007a2-109">示例</span><span class="sxs-lookup"><span data-stu-id="007a2-109">EXAMPLES</span></span>

### <span data-ttu-id="007a2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="007a2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="007a2-111">參數</span><span class="sxs-lookup"><span data-stu-id="007a2-111">PARAMETERS</span></span>

### <span data-ttu-id="007a2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="007a2-112">-AccountName</span></span>
<span data-ttu-id="007a2-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="007a2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="007a2-114">-確認</span><span class="sxs-lookup"><span data-stu-id="007a2-114">-Confirm</span></span>
<span data-ttu-id="007a2-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="007a2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="007a2-116">-容器</span><span class="sxs-lookup"><span data-stu-id="007a2-116">-ContainerName</span></span>
<span data-ttu-id="007a2-117">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="007a2-117">Container name.</span></span>

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

### <span data-ttu-id="007a2-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="007a2-118">-DatabaseName</span></span>
<span data-ttu-id="007a2-119">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="007a2-119">Database name.</span></span>

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

### <span data-ttu-id="007a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007a2-120">-DefaultProfile</span></span>
<span data-ttu-id="007a2-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="007a2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="007a2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="007a2-122">-InputObject</span></span>
<span data-ttu-id="007a2-123">Sql trigger 物件</span><span class="sxs-lookup"><span data-stu-id="007a2-123">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="007a2-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="007a2-124">-Name</span></span>
<span data-ttu-id="007a2-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="007a2-125">Trigger name.</span></span>

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

### <span data-ttu-id="007a2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="007a2-126">-PassThru</span></span>
<span data-ttu-id="007a2-127">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="007a2-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="007a2-128">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="007a2-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="007a2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="007a2-129">-ResourceGroupName</span></span>
<span data-ttu-id="007a2-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="007a2-130">Name of resource group.</span></span>

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

### <span data-ttu-id="007a2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="007a2-131">-WhatIf</span></span>
<span data-ttu-id="007a2-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="007a2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="007a2-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="007a2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="007a2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007a2-134">CommonParameters</span></span>
<span data-ttu-id="007a2-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="007a2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007a2-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="007a2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007a2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="007a2-137">INPUTS</span></span>

### <span data-ttu-id="007a2-138">所有</span><span class="sxs-lookup"><span data-stu-id="007a2-138">None</span></span>

## <span data-ttu-id="007a2-139">輸出</span><span class="sxs-lookup"><span data-stu-id="007a2-139">OUTPUTS</span></span>

### <span data-ttu-id="007a2-140">System.void</span><span class="sxs-lookup"><span data-stu-id="007a2-140">System.Void</span></span>

### <span data-ttu-id="007a2-141">System.object</span><span class="sxs-lookup"><span data-stu-id="007a2-141">System.Boolean</span></span>

## <span data-ttu-id="007a2-142">筆記</span><span class="sxs-lookup"><span data-stu-id="007a2-142">NOTES</span></span>

## <span data-ttu-id="007a2-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="007a2-143">RELATED LINKS</span></span>
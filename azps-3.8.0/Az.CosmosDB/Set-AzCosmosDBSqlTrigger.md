---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956492"
---
# <span data-ttu-id="6dfe2-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="6dfe2-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="6dfe2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6dfe2-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfe2-103">建立新的或更新現有的 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="6dfe2-104">句法</span><span class="sxs-lookup"><span data-stu-id="6dfe2-104">SYNTAX</span></span>

### <span data-ttu-id="6dfe2-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6dfe2-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dfe2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dfe2-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dfe2-107">說明</span><span class="sxs-lookup"><span data-stu-id="6dfe2-107">DESCRIPTION</span></span>
<span data-ttu-id="6dfe2-108">**AzCosmosDBSqlTrigger** Cmdlet 會建立新的或更新現有的 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="6dfe2-109">示例</span><span class="sxs-lookup"><span data-stu-id="6dfe2-109">EXAMPLES</span></span>

### <span data-ttu-id="6dfe2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6dfe2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="6dfe2-111">參數</span><span class="sxs-lookup"><span data-stu-id="6dfe2-111">PARAMETERS</span></span>

### <span data-ttu-id="6dfe2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6dfe2-112">-AccountName</span></span>
<span data-ttu-id="6dfe2-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6dfe2-114">-Body</span><span class="sxs-lookup"><span data-stu-id="6dfe2-114">-Body</span></span>
<span data-ttu-id="6dfe2-115">觸發程式的主體。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="6dfe2-116">-確認</span><span class="sxs-lookup"><span data-stu-id="6dfe2-116">-Confirm</span></span>
<span data-ttu-id="6dfe2-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dfe2-118">-容器</span><span class="sxs-lookup"><span data-stu-id="6dfe2-118">-ContainerName</span></span>
<span data-ttu-id="6dfe2-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-119">Container name.</span></span>

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

### <span data-ttu-id="6dfe2-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6dfe2-120">-DatabaseName</span></span>
<span data-ttu-id="6dfe2-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-121">Database name.</span></span>

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

### <span data-ttu-id="6dfe2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfe2-122">-DefaultProfile</span></span>
<span data-ttu-id="6dfe2-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dfe2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dfe2-124">-InputObject</span></span>
<span data-ttu-id="6dfe2-125">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-125">Sql Container object.</span></span>

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

### <span data-ttu-id="6dfe2-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="6dfe2-126">-Name</span></span>
<span data-ttu-id="6dfe2-127">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-127">Trigger name.</span></span>

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

### <span data-ttu-id="6dfe2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dfe2-128">-ResourceGroupName</span></span>
<span data-ttu-id="6dfe2-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-129">Name of resource group.</span></span>

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

### <span data-ttu-id="6dfe2-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="6dfe2-130">-TriggerOperation</span></span>
<span data-ttu-id="6dfe2-131">觸發程式所關聯的運算。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="6dfe2-132">可能的值包括： "All"、"Create"、"Update"、"Delete"、"Replace"</span><span class="sxs-lookup"><span data-stu-id="6dfe2-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfe2-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="6dfe2-133">-TriggerType</span></span>
<span data-ttu-id="6dfe2-134">觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-134">Type of the Trigger.</span></span>
<span data-ttu-id="6dfe2-135">可能的值包括：「Pre」、「張貼」</span><span class="sxs-lookup"><span data-stu-id="6dfe2-135">Possible values include: 'Pre', 'Post'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfe2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dfe2-136">-WhatIf</span></span>
<span data-ttu-id="6dfe2-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dfe2-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dfe2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfe2-139">CommonParameters</span></span>
<span data-ttu-id="6dfe2-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfe2-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfe2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6dfe2-142">INPUTS</span></span>

### <span data-ttu-id="6dfe2-143">所有</span><span class="sxs-lookup"><span data-stu-id="6dfe2-143">None</span></span>

## <span data-ttu-id="6dfe2-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6dfe2-144">OUTPUTS</span></span>

### <span data-ttu-id="6dfe2-145">PSSqlTriggerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6dfe2-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="6dfe2-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6dfe2-146">NOTES</span></span>

## <span data-ttu-id="6dfe2-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dfe2-147">RELATED LINKS</span></span>

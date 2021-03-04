---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a6808f6c2640a90006560b16dbfd452167e0d6fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906758"
---
# <span data-ttu-id="3378c-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="3378c-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="3378c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3378c-102">SYNOPSIS</span></span>
<span data-ttu-id="3378c-103">建立新一個管理中心 SQL 觸發器。</span><span class="sxs-lookup"><span data-stu-id="3378c-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="3378c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3378c-104">SYNTAX</span></span>

### <span data-ttu-id="3378c-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3378c-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3378c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3378c-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3378c-107">描述</span><span class="sxs-lookup"><span data-stu-id="3378c-107">DESCRIPTION</span></span>
<span data-ttu-id="3378c-108">建立新一個管理中心 SQL 觸發器。</span><span class="sxs-lookup"><span data-stu-id="3378c-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="3378c-109">例子</span><span class="sxs-lookup"><span data-stu-id="3378c-109">EXAMPLES</span></span>

### <span data-ttu-id="3378c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3378c-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="3378c-111">參數</span><span class="sxs-lookup"><span data-stu-id="3378c-111">PARAMETERS</span></span>

### <span data-ttu-id="3378c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3378c-112">-AccountName</span></span>
<span data-ttu-id="3378c-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3378c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3378c-114">-Body</span><span class="sxs-lookup"><span data-stu-id="3378c-114">-Body</span></span>
<span data-ttu-id="3378c-115">觸發的內體。</span><span class="sxs-lookup"><span data-stu-id="3378c-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="3378c-116">-確認</span><span class="sxs-lookup"><span data-stu-id="3378c-116">-Confirm</span></span>
<span data-ttu-id="3378c-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3378c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3378c-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3378c-118">-ContainerName</span></span>
<span data-ttu-id="3378c-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3378c-119">Container name.</span></span>

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

### <span data-ttu-id="3378c-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3378c-120">-DatabaseName</span></span>
<span data-ttu-id="3378c-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3378c-121">Database name.</span></span>

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

### <span data-ttu-id="3378c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3378c-122">-DefaultProfile</span></span>
<span data-ttu-id="3378c-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3378c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3378c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3378c-124">-Name</span></span>
<span data-ttu-id="3378c-125">觸發名稱。</span><span class="sxs-lookup"><span data-stu-id="3378c-125">Trigger name.</span></span>

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

### <span data-ttu-id="3378c-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3378c-126">-ParentObject</span></span>
<span data-ttu-id="3378c-127">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="3378c-127">Sql Container object.</span></span>

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

### <span data-ttu-id="3378c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3378c-128">-ResourceGroupName</span></span>
<span data-ttu-id="3378c-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3378c-129">Name of resource group.</span></span>

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

### <span data-ttu-id="3378c-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="3378c-130">-TriggerOperation</span></span>
<span data-ttu-id="3378c-131">與觸發人相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="3378c-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="3378c-132">可能的值包括：'全部'、'建立'、'更新'、'刪除'、'取代'</span><span class="sxs-lookup"><span data-stu-id="3378c-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="3378c-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="3378c-133">-TriggerType</span></span>
<span data-ttu-id="3378c-134">觸發的類型。</span><span class="sxs-lookup"><span data-stu-id="3378c-134">Type of the Trigger.</span></span>
<span data-ttu-id="3378c-135">可能的值包括：'Pre'， 'Post'</span><span class="sxs-lookup"><span data-stu-id="3378c-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="3378c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3378c-136">-WhatIf</span></span>
<span data-ttu-id="3378c-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3378c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3378c-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3378c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3378c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3378c-139">CommonParameters</span></span>
<span data-ttu-id="3378c-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3378c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3378c-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3378c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3378c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="3378c-142">INPUTS</span></span>

### <span data-ttu-id="3378c-143">Microsoft.Azure.Commands.AzsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="3378c-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="3378c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3378c-144">OUTPUTS</span></span>

### <span data-ttu-id="3378c-145">Microsoft.Azure.Commands.AzsDB.Models.PSSqlTrigetResults</span><span class="sxs-lookup"><span data-stu-id="3378c-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="3378c-146">Microsoft.Azure.Commands.AzsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="3378c-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="3378c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="3378c-147">NOTES</span></span>

## <span data-ttu-id="3378c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="3378c-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128809"
---
# <span data-ttu-id="f0356-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="f0356-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="f0356-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0356-102">SYNOPSIS</span></span>
<span data-ttu-id="f0356-103">建立新的 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="f0356-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="f0356-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0356-104">SYNTAX</span></span>

### <span data-ttu-id="f0356-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f0356-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0356-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0356-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0356-107">說明</span><span class="sxs-lookup"><span data-stu-id="f0356-107">DESCRIPTION</span></span>
<span data-ttu-id="f0356-108">建立新的 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="f0356-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="f0356-109">示例</span><span class="sxs-lookup"><span data-stu-id="f0356-109">EXAMPLES</span></span>

### <span data-ttu-id="f0356-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f0356-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="f0356-111">參數</span><span class="sxs-lookup"><span data-stu-id="f0356-111">PARAMETERS</span></span>

### <span data-ttu-id="f0356-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f0356-112">-AccountName</span></span>
<span data-ttu-id="f0356-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0356-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f0356-114">-Body</span><span class="sxs-lookup"><span data-stu-id="f0356-114">-Body</span></span>
<span data-ttu-id="f0356-115">觸發程式的主體。</span><span class="sxs-lookup"><span data-stu-id="f0356-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="f0356-116">-確認</span><span class="sxs-lookup"><span data-stu-id="f0356-116">-Confirm</span></span>
<span data-ttu-id="f0356-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0356-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0356-118">-容器</span><span class="sxs-lookup"><span data-stu-id="f0356-118">-ContainerName</span></span>
<span data-ttu-id="f0356-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="f0356-119">Container name.</span></span>

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

### <span data-ttu-id="f0356-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f0356-120">-DatabaseName</span></span>
<span data-ttu-id="f0356-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f0356-121">Database name.</span></span>

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

### <span data-ttu-id="f0356-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0356-122">-DefaultProfile</span></span>
<span data-ttu-id="f0356-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0356-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0356-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0356-124">-Name</span></span>
<span data-ttu-id="f0356-125">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f0356-125">Trigger name.</span></span>

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

### <span data-ttu-id="f0356-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f0356-126">-ParentObject</span></span>
<span data-ttu-id="f0356-127">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="f0356-127">Sql Container object.</span></span>

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

### <span data-ttu-id="f0356-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0356-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0356-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0356-129">Name of resource group.</span></span>

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

### <span data-ttu-id="f0356-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="f0356-130">-TriggerOperation</span></span>
<span data-ttu-id="f0356-131">觸發程式所關聯的運算。</span><span class="sxs-lookup"><span data-stu-id="f0356-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="f0356-132">可能的值包括： "All"、"Create"、"Update"、"Delete"、"Replace"</span><span class="sxs-lookup"><span data-stu-id="f0356-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="f0356-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="f0356-133">-TriggerType</span></span>
<span data-ttu-id="f0356-134">觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="f0356-134">Type of the Trigger.</span></span>
<span data-ttu-id="f0356-135">可能的值包括：「Pre」、「張貼」</span><span class="sxs-lookup"><span data-stu-id="f0356-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="f0356-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0356-136">-WhatIf</span></span>
<span data-ttu-id="f0356-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0356-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0356-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0356-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0356-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0356-139">CommonParameters</span></span>
<span data-ttu-id="f0356-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0356-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0356-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f0356-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0356-142">輸入</span><span class="sxs-lookup"><span data-stu-id="f0356-142">INPUTS</span></span>

### <span data-ttu-id="f0356-143">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f0356-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="f0356-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f0356-144">OUTPUTS</span></span>

### <span data-ttu-id="f0356-145">PSSqlTriggerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f0356-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="f0356-146">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="f0356-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f0356-147">筆記</span><span class="sxs-lookup"><span data-stu-id="f0356-147">NOTES</span></span>

## <span data-ttu-id="f0356-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0356-148">RELATED LINKS</span></span>
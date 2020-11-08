---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136518"
---
# <span data-ttu-id="5ae13-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="5ae13-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="5ae13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ae13-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae13-103">更新 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5ae13-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="5ae13-104">讀取現有的觸發程式，執行用戶端的修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="5ae13-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="5ae13-105">句法</span><span class="sxs-lookup"><span data-stu-id="5ae13-105">SYNTAX</span></span>

### <span data-ttu-id="5ae13-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5ae13-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ae13-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ae13-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ae13-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ae13-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ae13-109">說明</span><span class="sxs-lookup"><span data-stu-id="5ae13-109">DESCRIPTION</span></span>
<span data-ttu-id="5ae13-110">更新 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5ae13-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="5ae13-111">讀取現有的觸發程式，執行用戶端的修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="5ae13-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="5ae13-112">示例</span><span class="sxs-lookup"><span data-stu-id="5ae13-112">EXAMPLES</span></span>

### <span data-ttu-id="5ae13-113">範例1</span><span class="sxs-lookup"><span data-stu-id="5ae13-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="5ae13-114">參數</span><span class="sxs-lookup"><span data-stu-id="5ae13-114">PARAMETERS</span></span>

### <span data-ttu-id="5ae13-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5ae13-115">-AccountName</span></span>
<span data-ttu-id="5ae13-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ae13-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5ae13-117">-Body</span><span class="sxs-lookup"><span data-stu-id="5ae13-117">-Body</span></span>
<span data-ttu-id="5ae13-118">觸發程式的主體。</span><span class="sxs-lookup"><span data-stu-id="5ae13-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="5ae13-119">-確認</span><span class="sxs-lookup"><span data-stu-id="5ae13-119">-Confirm</span></span>
<span data-ttu-id="5ae13-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ae13-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ae13-121">-容器</span><span class="sxs-lookup"><span data-stu-id="5ae13-121">-ContainerName</span></span>
<span data-ttu-id="5ae13-122">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="5ae13-122">Container name.</span></span>

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

### <span data-ttu-id="5ae13-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ae13-123">-DatabaseName</span></span>
<span data-ttu-id="5ae13-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5ae13-124">Database name.</span></span>

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

### <span data-ttu-id="5ae13-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae13-125">-DefaultProfile</span></span>
<span data-ttu-id="5ae13-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ae13-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ae13-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ae13-127">-InputObject</span></span>
<span data-ttu-id="5ae13-128">Sql trigger 物件</span><span class="sxs-lookup"><span data-stu-id="5ae13-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="5ae13-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ae13-129">-Name</span></span>
<span data-ttu-id="5ae13-130">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="5ae13-130">Trigger name.</span></span>

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

### <span data-ttu-id="5ae13-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ae13-131">-ParentObject</span></span>
<span data-ttu-id="5ae13-132">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="5ae13-132">Sql Container object.</span></span>

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

### <span data-ttu-id="5ae13-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ae13-133">-ResourceGroupName</span></span>
<span data-ttu-id="5ae13-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ae13-134">Name of resource group.</span></span>

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

### <span data-ttu-id="5ae13-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="5ae13-135">-TriggerOperation</span></span>
<span data-ttu-id="5ae13-136">觸發程式所關聯的運算。</span><span class="sxs-lookup"><span data-stu-id="5ae13-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="5ae13-137">可能的值包括： "All"、"Create"、"Update"、"Delete"、"Replace"</span><span class="sxs-lookup"><span data-stu-id="5ae13-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="5ae13-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="5ae13-138">-TriggerType</span></span>
<span data-ttu-id="5ae13-139">觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="5ae13-139">Type of the Trigger.</span></span>
<span data-ttu-id="5ae13-140">可能的值包括：「Pre」、「張貼」</span><span class="sxs-lookup"><span data-stu-id="5ae13-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="5ae13-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ae13-141">-WhatIf</span></span>
<span data-ttu-id="5ae13-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ae13-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ae13-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ae13-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ae13-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae13-144">CommonParameters</span></span>
<span data-ttu-id="5ae13-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ae13-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae13-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5ae13-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae13-147">輸入</span><span class="sxs-lookup"><span data-stu-id="5ae13-147">INPUTS</span></span>

### <span data-ttu-id="5ae13-148">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5ae13-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="5ae13-149">PSSqlTriggerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5ae13-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="5ae13-150">輸出</span><span class="sxs-lookup"><span data-stu-id="5ae13-150">OUTPUTS</span></span>

### <span data-ttu-id="5ae13-151">PSSqlTriggerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5ae13-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="5ae13-152">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5ae13-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="5ae13-153">筆記</span><span class="sxs-lookup"><span data-stu-id="5ae13-153">NOTES</span></span>

## <span data-ttu-id="5ae13-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ae13-154">RELATED LINKS</span></span>
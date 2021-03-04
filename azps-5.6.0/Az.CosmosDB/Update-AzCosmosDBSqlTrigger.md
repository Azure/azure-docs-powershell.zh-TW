---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: bebf801316d18b29f6444b0b369833ae547e78d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916642"
---
# <span data-ttu-id="8be9f-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="8be9f-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="8be9f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8be9f-102">SYNOPSIS</span></span>
<span data-ttu-id="8be9f-103">更新了一些更新的一些 Sql Trigger。</span><span class="sxs-lookup"><span data-stu-id="8be9f-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="8be9f-104">讀取現有的觸發程式，以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="8be9f-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="8be9f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8be9f-105">SYNTAX</span></span>

### <span data-ttu-id="8be9f-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8be9f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be9f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8be9f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be9f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8be9f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be9f-109">描述</span><span class="sxs-lookup"><span data-stu-id="8be9f-109">DESCRIPTION</span></span>
<span data-ttu-id="8be9f-110">更新了一些更新的一些 Sql Trigger。</span><span class="sxs-lookup"><span data-stu-id="8be9f-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="8be9f-111">讀取現有的觸發程式，以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="8be9f-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="8be9f-112">例子</span><span class="sxs-lookup"><span data-stu-id="8be9f-112">EXAMPLES</span></span>

### <span data-ttu-id="8be9f-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="8be9f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="8be9f-114">參數</span><span class="sxs-lookup"><span data-stu-id="8be9f-114">PARAMETERS</span></span>

### <span data-ttu-id="8be9f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8be9f-115">-AccountName</span></span>
<span data-ttu-id="8be9f-116">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8be9f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8be9f-117">-Body</span><span class="sxs-lookup"><span data-stu-id="8be9f-117">-Body</span></span>
<span data-ttu-id="8be9f-118">觸發的內體。</span><span class="sxs-lookup"><span data-stu-id="8be9f-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="8be9f-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8be9f-119">-Confirm</span></span>
<span data-ttu-id="8be9f-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8be9f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be9f-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8be9f-121">-ContainerName</span></span>
<span data-ttu-id="8be9f-122">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="8be9f-122">Container name.</span></span>

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

### <span data-ttu-id="8be9f-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8be9f-123">-DatabaseName</span></span>
<span data-ttu-id="8be9f-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8be9f-124">Database name.</span></span>

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

### <span data-ttu-id="8be9f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be9f-125">-DefaultProfile</span></span>
<span data-ttu-id="8be9f-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8be9f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8be9f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8be9f-127">-InputObject</span></span>
<span data-ttu-id="8be9f-128">Sql 觸發物件</span><span class="sxs-lookup"><span data-stu-id="8be9f-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="8be9f-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8be9f-129">-Name</span></span>
<span data-ttu-id="8be9f-130">觸發名稱。</span><span class="sxs-lookup"><span data-stu-id="8be9f-130">Trigger name.</span></span>

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

### <span data-ttu-id="8be9f-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8be9f-131">-ParentObject</span></span>
<span data-ttu-id="8be9f-132">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="8be9f-132">Sql Container object.</span></span>

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

### <span data-ttu-id="8be9f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be9f-133">-ResourceGroupName</span></span>
<span data-ttu-id="8be9f-134">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8be9f-134">Name of resource group.</span></span>

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

### <span data-ttu-id="8be9f-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="8be9f-135">-TriggerOperation</span></span>
<span data-ttu-id="8be9f-136">與觸發人相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="8be9f-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="8be9f-137">可能的值包括：'全部'、'建立'、'更新'、'刪除'、'取代'</span><span class="sxs-lookup"><span data-stu-id="8be9f-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="8be9f-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="8be9f-138">-TriggerType</span></span>
<span data-ttu-id="8be9f-139">觸發的類型。</span><span class="sxs-lookup"><span data-stu-id="8be9f-139">Type of the Trigger.</span></span>
<span data-ttu-id="8be9f-140">可能的值包括：'Pre'， 'Post'</span><span class="sxs-lookup"><span data-stu-id="8be9f-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="8be9f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be9f-141">-WhatIf</span></span>
<span data-ttu-id="8be9f-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8be9f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be9f-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8be9f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be9f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be9f-144">CommonParameters</span></span>
<span data-ttu-id="8be9f-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8be9f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be9f-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8be9f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be9f-147">輸入</span><span class="sxs-lookup"><span data-stu-id="8be9f-147">INPUTS</span></span>

### <span data-ttu-id="8be9f-148">Microsoft.Azure.Commands.AzsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="8be9f-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="8be9f-149">Microsoft.Azure.Commands.AzsDB.Models.PSSqlTrigetResults</span><span class="sxs-lookup"><span data-stu-id="8be9f-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="8be9f-150">輸出</span><span class="sxs-lookup"><span data-stu-id="8be9f-150">OUTPUTS</span></span>

### <span data-ttu-id="8be9f-151">Microsoft.Azure.Commands.AzsDB.Models.PSSqlTrigetResults</span><span class="sxs-lookup"><span data-stu-id="8be9f-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="8be9f-152">Microsoft.Azure.Commands.AzsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8be9f-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="8be9f-153">筆記</span><span class="sxs-lookup"><span data-stu-id="8be9f-153">NOTES</span></span>

## <span data-ttu-id="8be9f-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="8be9f-154">RELATED LINKS</span></span>

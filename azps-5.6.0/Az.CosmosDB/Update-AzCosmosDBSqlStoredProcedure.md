---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 8a717b15268090a7e5ea356c49b11d9aba1ab009
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908210"
---
# <span data-ttu-id="d0e87-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="d0e87-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="d0e87-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d0e87-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e87-103">更新一些更新的一切資訊。</span><span class="sxs-lookup"><span data-stu-id="d0e87-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="d0e87-104">讀取現有的 StoredProcedure，以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="d0e87-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="d0e87-105">語法</span><span class="sxs-lookup"><span data-stu-id="d0e87-105">SYNTAX</span></span>

### <span data-ttu-id="d0e87-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d0e87-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e87-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e87-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e87-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e87-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0e87-109">描述</span><span class="sxs-lookup"><span data-stu-id="d0e87-109">DESCRIPTION</span></span>
<span data-ttu-id="d0e87-110">更新一些更新的一切資訊。</span><span class="sxs-lookup"><span data-stu-id="d0e87-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="d0e87-111">讀取現有的 StoredProcedure，以執行用戶端修補程式作業。</span><span class="sxs-lookup"><span data-stu-id="d0e87-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="d0e87-112">例子</span><span class="sxs-lookup"><span data-stu-id="d0e87-112">EXAMPLES</span></span>

### <span data-ttu-id="d0e87-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="d0e87-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="d0e87-114">參數</span><span class="sxs-lookup"><span data-stu-id="d0e87-114">PARAMETERS</span></span>

### <span data-ttu-id="d0e87-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0e87-115">-AccountName</span></span>
<span data-ttu-id="d0e87-116">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e87-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d0e87-117">-Body</span><span class="sxs-lookup"><span data-stu-id="d0e87-117">-Body</span></span>
<span data-ttu-id="d0e87-118">儲存程式的內體。</span><span class="sxs-lookup"><span data-stu-id="d0e87-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="d0e87-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d0e87-119">-Confirm</span></span>
<span data-ttu-id="d0e87-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d0e87-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e87-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d0e87-121">-ContainerName</span></span>
<span data-ttu-id="d0e87-122">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e87-122">Container name.</span></span>

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

### <span data-ttu-id="d0e87-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0e87-123">-DatabaseName</span></span>
<span data-ttu-id="d0e87-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e87-124">Database name.</span></span>

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

### <span data-ttu-id="d0e87-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e87-125">-DefaultProfile</span></span>
<span data-ttu-id="d0e87-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0e87-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0e87-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0e87-127">-InputObject</span></span>
<span data-ttu-id="d0e87-128">Sql 儲存程式物件</span><span class="sxs-lookup"><span data-stu-id="d0e87-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="d0e87-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0e87-129">-Name</span></span>
<span data-ttu-id="d0e87-130">儲存的 Prcodecure 名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e87-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="d0e87-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0e87-131">-ParentObject</span></span>
<span data-ttu-id="d0e87-132">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="d0e87-132">Sql Container object.</span></span>

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

### <span data-ttu-id="d0e87-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e87-133">-ResourceGroupName</span></span>
<span data-ttu-id="d0e87-134">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e87-134">Name of resource group.</span></span>

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

### <span data-ttu-id="d0e87-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e87-135">-WhatIf</span></span>
<span data-ttu-id="d0e87-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0e87-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e87-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0e87-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e87-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e87-138">CommonParameters</span></span>
<span data-ttu-id="d0e87-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d0e87-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e87-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0e87-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e87-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d0e87-141">INPUTS</span></span>

### <span data-ttu-id="d0e87-142">Microsoft.Azure.Commands.AzsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d0e87-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="d0e87-143">Microsoft.Azure.Commands.AzsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="d0e87-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="d0e87-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d0e87-144">OUTPUTS</span></span>

### <span data-ttu-id="d0e87-145">Microsoft.Azure.Commands.AzsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="d0e87-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="d0e87-146">Microsoft.Azure.Commands.AzsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d0e87-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d0e87-147">筆記</span><span class="sxs-lookup"><span data-stu-id="d0e87-147">NOTES</span></span>

## <span data-ttu-id="d0e87-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0e87-148">RELATED LINKS</span></span>

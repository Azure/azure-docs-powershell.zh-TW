---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 0ad79ff742647395b48c8af3b41140b1a7bda691
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909133"
---
# <span data-ttu-id="66bab-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="66bab-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="66bab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66bab-102">SYNOPSIS</span></span>
<span data-ttu-id="66bab-103">建立新一個因斯DB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="66bab-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="66bab-104">語法</span><span class="sxs-lookup"><span data-stu-id="66bab-104">SYNTAX</span></span>

### <span data-ttu-id="66bab-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="66bab-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66bab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66bab-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66bab-107">描述</span><span class="sxs-lookup"><span data-stu-id="66bab-107">DESCRIPTION</span></span>
<span data-ttu-id="66bab-108">建立新一個因斯DB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="66bab-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="66bab-109">例子</span><span class="sxs-lookup"><span data-stu-id="66bab-109">EXAMPLES</span></span>

### <span data-ttu-id="66bab-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="66bab-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="66bab-111">參數</span><span class="sxs-lookup"><span data-stu-id="66bab-111">PARAMETERS</span></span>

### <span data-ttu-id="66bab-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66bab-112">-AccountName</span></span>
<span data-ttu-id="66bab-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="66bab-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66bab-114">-Body</span><span class="sxs-lookup"><span data-stu-id="66bab-114">-Body</span></span>
<span data-ttu-id="66bab-115">使用者定義函數的內體。</span><span class="sxs-lookup"><span data-stu-id="66bab-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="66bab-116">-確認</span><span class="sxs-lookup"><span data-stu-id="66bab-116">-Confirm</span></span>
<span data-ttu-id="66bab-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="66bab-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66bab-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="66bab-118">-ContainerName</span></span>
<span data-ttu-id="66bab-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="66bab-119">Container name.</span></span>

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

### <span data-ttu-id="66bab-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66bab-120">-DatabaseName</span></span>
<span data-ttu-id="66bab-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="66bab-121">Database name.</span></span>

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

### <span data-ttu-id="66bab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bab-122">-DefaultProfile</span></span>
<span data-ttu-id="66bab-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="66bab-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66bab-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="66bab-124">-Name</span></span>
<span data-ttu-id="66bab-125">使用者定義函數名稱。</span><span class="sxs-lookup"><span data-stu-id="66bab-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="66bab-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="66bab-126">-ParentObject</span></span>
<span data-ttu-id="66bab-127">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="66bab-127">Sql Container object.</span></span>

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

### <span data-ttu-id="66bab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66bab-128">-ResourceGroupName</span></span>
<span data-ttu-id="66bab-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66bab-129">Name of resource group.</span></span>

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

### <span data-ttu-id="66bab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66bab-130">-WhatIf</span></span>
<span data-ttu-id="66bab-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66bab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66bab-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66bab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66bab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bab-133">CommonParameters</span></span>
<span data-ttu-id="66bab-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66bab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bab-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66bab-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bab-136">輸入</span><span class="sxs-lookup"><span data-stu-id="66bab-136">INPUTS</span></span>

### <span data-ttu-id="66bab-137">Microsoft.Azure.Commands.AzsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="66bab-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="66bab-138">輸出</span><span class="sxs-lookup"><span data-stu-id="66bab-138">OUTPUTS</span></span>

### <span data-ttu-id="66bab-139">Microsoft.Azure.Commands.AzsDB.models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="66bab-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="66bab-140">Microsoft.Azure.Commands.AzsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="66bab-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="66bab-141">筆記</span><span class="sxs-lookup"><span data-stu-id="66bab-141">NOTES</span></span>

## <span data-ttu-id="66bab-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="66bab-142">RELATED LINKS</span></span>

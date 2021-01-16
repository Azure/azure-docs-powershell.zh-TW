---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278452"
---
# <span data-ttu-id="849cf-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="849cf-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="849cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="849cf-102">SYNOPSIS</span></span>
<span data-ttu-id="849cf-103">建立新的 CosmosDB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="849cf-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="849cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="849cf-104">SYNTAX</span></span>

### <span data-ttu-id="849cf-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="849cf-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="849cf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="849cf-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="849cf-107">說明</span><span class="sxs-lookup"><span data-stu-id="849cf-107">DESCRIPTION</span></span>
<span data-ttu-id="849cf-108">建立新的 CosmosDB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="849cf-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="849cf-109">示例</span><span class="sxs-lookup"><span data-stu-id="849cf-109">EXAMPLES</span></span>

### <span data-ttu-id="849cf-110">範例1</span><span class="sxs-lookup"><span data-stu-id="849cf-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="849cf-111">參數</span><span class="sxs-lookup"><span data-stu-id="849cf-111">PARAMETERS</span></span>

### <span data-ttu-id="849cf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="849cf-112">-AccountName</span></span>
<span data-ttu-id="849cf-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="849cf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="849cf-114">-Body</span><span class="sxs-lookup"><span data-stu-id="849cf-114">-Body</span></span>
<span data-ttu-id="849cf-115">使用者定義函數的主體。</span><span class="sxs-lookup"><span data-stu-id="849cf-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="849cf-116">-確認</span><span class="sxs-lookup"><span data-stu-id="849cf-116">-Confirm</span></span>
<span data-ttu-id="849cf-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="849cf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="849cf-118">-容器</span><span class="sxs-lookup"><span data-stu-id="849cf-118">-ContainerName</span></span>
<span data-ttu-id="849cf-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="849cf-119">Container name.</span></span>

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

### <span data-ttu-id="849cf-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="849cf-120">-DatabaseName</span></span>
<span data-ttu-id="849cf-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="849cf-121">Database name.</span></span>

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

### <span data-ttu-id="849cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849cf-122">-DefaultProfile</span></span>
<span data-ttu-id="849cf-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="849cf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="849cf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="849cf-124">-Name</span></span>
<span data-ttu-id="849cf-125">使用者定義的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="849cf-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="849cf-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="849cf-126">-ParentObject</span></span>
<span data-ttu-id="849cf-127">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="849cf-127">Sql Container object.</span></span>

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

### <span data-ttu-id="849cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="849cf-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="849cf-129">Name of resource group.</span></span>

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

### <span data-ttu-id="849cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="849cf-130">-WhatIf</span></span>
<span data-ttu-id="849cf-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="849cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="849cf-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="849cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="849cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849cf-133">CommonParameters</span></span>
<span data-ttu-id="849cf-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="849cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849cf-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="849cf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849cf-136">輸入</span><span class="sxs-lookup"><span data-stu-id="849cf-136">INPUTS</span></span>

### <span data-ttu-id="849cf-137">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="849cf-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="849cf-138">輸出</span><span class="sxs-lookup"><span data-stu-id="849cf-138">OUTPUTS</span></span>

### <span data-ttu-id="849cf-139">PSSqlUserDefinedFunctionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="849cf-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="849cf-140">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="849cf-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="849cf-141">筆記</span><span class="sxs-lookup"><span data-stu-id="849cf-141">NOTES</span></span>

## <span data-ttu-id="849cf-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="849cf-142">RELATED LINKS</span></span>

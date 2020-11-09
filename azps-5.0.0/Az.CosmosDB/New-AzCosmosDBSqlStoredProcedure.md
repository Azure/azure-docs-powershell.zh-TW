---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285479"
---
# <span data-ttu-id="dba3e-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="dba3e-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="dba3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dba3e-102">SYNOPSIS</span></span>
<span data-ttu-id="dba3e-103">建立新的 CosmosDB Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="dba3e-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="dba3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="dba3e-104">SYNTAX</span></span>

### <span data-ttu-id="dba3e-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dba3e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba3e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba3e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba3e-107">說明</span><span class="sxs-lookup"><span data-stu-id="dba3e-107">DESCRIPTION</span></span>
<span data-ttu-id="dba3e-108">建立新的 CosmosDB Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="dba3e-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="dba3e-109">示例</span><span class="sxs-lookup"><span data-stu-id="dba3e-109">EXAMPLES</span></span>

### <span data-ttu-id="dba3e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="dba3e-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="dba3e-111">參數</span><span class="sxs-lookup"><span data-stu-id="dba3e-111">PARAMETERS</span></span>

### <span data-ttu-id="dba3e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dba3e-112">-AccountName</span></span>
<span data-ttu-id="dba3e-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dba3e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dba3e-114">-Body</span><span class="sxs-lookup"><span data-stu-id="dba3e-114">-Body</span></span>
<span data-ttu-id="dba3e-115">已儲存程式的內文。</span><span class="sxs-lookup"><span data-stu-id="dba3e-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="dba3e-116">-確認</span><span class="sxs-lookup"><span data-stu-id="dba3e-116">-Confirm</span></span>
<span data-ttu-id="dba3e-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dba3e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba3e-118">-容器</span><span class="sxs-lookup"><span data-stu-id="dba3e-118">-ContainerName</span></span>
<span data-ttu-id="dba3e-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="dba3e-119">Container name.</span></span>

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

### <span data-ttu-id="dba3e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dba3e-120">-DatabaseName</span></span>
<span data-ttu-id="dba3e-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="dba3e-121">Database name.</span></span>

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

### <span data-ttu-id="dba3e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba3e-122">-DefaultProfile</span></span>
<span data-ttu-id="dba3e-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dba3e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba3e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="dba3e-124">-Name</span></span>
<span data-ttu-id="dba3e-125">儲存的 Prcodecure 名稱。</span><span class="sxs-lookup"><span data-stu-id="dba3e-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="dba3e-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dba3e-126">-ParentObject</span></span>
<span data-ttu-id="dba3e-127">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="dba3e-127">Sql Container object.</span></span>

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

### <span data-ttu-id="dba3e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba3e-128">-ResourceGroupName</span></span>
<span data-ttu-id="dba3e-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dba3e-129">Name of resource group.</span></span>

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

### <span data-ttu-id="dba3e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba3e-130">-WhatIf</span></span>
<span data-ttu-id="dba3e-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dba3e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba3e-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dba3e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba3e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba3e-133">CommonParameters</span></span>
<span data-ttu-id="dba3e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dba3e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba3e-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dba3e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba3e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="dba3e-136">INPUTS</span></span>

### <span data-ttu-id="dba3e-137">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dba3e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="dba3e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="dba3e-138">OUTPUTS</span></span>

### <span data-ttu-id="dba3e-139">PSSqlStoredProcedureGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dba3e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="dba3e-140">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dba3e-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="dba3e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="dba3e-141">NOTES</span></span>

## <span data-ttu-id="dba3e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="dba3e-142">RELATED LINKS</span></span>

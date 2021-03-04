---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 5c7c26faa6171babd60f9d5fb406d3b3c08ef81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902117"
---
# <span data-ttu-id="3f932-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="3f932-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="3f932-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3f932-102">SYNOPSIS</span></span>
<span data-ttu-id="3f932-103">獲得集能DB Sql Container。</span><span class="sxs-lookup"><span data-stu-id="3f932-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="3f932-104">語法</span><span class="sxs-lookup"><span data-stu-id="3f932-104">SYNTAX</span></span>

### <span data-ttu-id="3f932-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3f932-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="3f932-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f932-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f932-107">描述</span><span class="sxs-lookup"><span data-stu-id="3f932-107">DESCRIPTION</span></span>
<span data-ttu-id="3f932-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span><span class="sxs-lookup"><span data-stu-id="3f932-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="3f932-109">例子</span><span class="sxs-lookup"><span data-stu-id="3f932-109">EXAMPLES</span></span>

### <span data-ttu-id="3f932-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3f932-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="3f932-111">參數</span><span class="sxs-lookup"><span data-stu-id="3f932-111">PARAMETERS</span></span>

### <span data-ttu-id="3f932-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3f932-112">-AccountName</span></span>
<span data-ttu-id="3f932-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f932-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3f932-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f932-114">-DatabaseName</span></span>
<span data-ttu-id="3f932-115">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3f932-115">Database name.</span></span>

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

### <span data-ttu-id="3f932-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f932-116">-DefaultProfile</span></span>
<span data-ttu-id="3f932-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f932-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f932-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f932-118">-Name</span></span>
<span data-ttu-id="3f932-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3f932-119">Container name.</span></span>

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

### <span data-ttu-id="3f932-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3f932-120">-ParentObject</span></span>
<span data-ttu-id="3f932-121">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="3f932-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f932-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f932-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f932-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f932-123">Name of resource group.</span></span>

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

### <span data-ttu-id="3f932-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f932-124">CommonParameters</span></span>
<span data-ttu-id="3f932-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3f932-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f932-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f932-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f932-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3f932-127">INPUTS</span></span>

### <span data-ttu-id="3f932-128">沒有</span><span class="sxs-lookup"><span data-stu-id="3f932-128">None</span></span>

## <span data-ttu-id="3f932-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3f932-129">OUTPUTS</span></span>

### <span data-ttu-id="3f932-130">Microsoft.Azure.Commands.AzsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="3f932-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="3f932-131">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3f932-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3f932-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3f932-132">NOTES</span></span>

## <span data-ttu-id="3f932-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f932-133">RELATED LINKS</span></span>

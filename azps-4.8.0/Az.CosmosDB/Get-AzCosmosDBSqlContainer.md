---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135655"
---
# <span data-ttu-id="7373c-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="7373c-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="7373c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7373c-102">SYNOPSIS</span></span>
<span data-ttu-id="7373c-103">取得 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="7373c-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="7373c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7373c-104">SYNTAX</span></span>

### <span data-ttu-id="7373c-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7373c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="7373c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7373c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7373c-107">說明</span><span class="sxs-lookup"><span data-stu-id="7373c-107">DESCRIPTION</span></span>
<span data-ttu-id="7373c-108">**AzCosmosDBSqlContainer** Cmdlet 會取得指定 ResourceGroupName、Accountname 和 databasename 之所有現有 CosmosDB sql 容器的清單，並取得特定 ResourceGroupName、Accountname、Databasename 和容器的單一 CosmosDB sql 容器。</span><span class="sxs-lookup"><span data-stu-id="7373c-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="7373c-109">示例</span><span class="sxs-lookup"><span data-stu-id="7373c-109">EXAMPLES</span></span>

### <span data-ttu-id="7373c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7373c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="7373c-111">參數</span><span class="sxs-lookup"><span data-stu-id="7373c-111">PARAMETERS</span></span>

### <span data-ttu-id="7373c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7373c-112">-AccountName</span></span>
<span data-ttu-id="7373c-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7373c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7373c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7373c-114">-DatabaseName</span></span>
<span data-ttu-id="7373c-115">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7373c-115">Database name.</span></span>

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

### <span data-ttu-id="7373c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7373c-116">-DefaultProfile</span></span>
<span data-ttu-id="7373c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7373c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7373c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7373c-118">-Name</span></span>
<span data-ttu-id="7373c-119">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="7373c-119">Container name.</span></span>

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

### <span data-ttu-id="7373c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7373c-120">-ParentObject</span></span>
<span data-ttu-id="7373c-121">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="7373c-121">Sql Database object.</span></span>

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

### <span data-ttu-id="7373c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7373c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7373c-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7373c-123">Name of resource group.</span></span>

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

### <span data-ttu-id="7373c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7373c-124">CommonParameters</span></span>
<span data-ttu-id="7373c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7373c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7373c-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7373c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7373c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7373c-127">INPUTS</span></span>

### <span data-ttu-id="7373c-128">所有</span><span class="sxs-lookup"><span data-stu-id="7373c-128">None</span></span>

## <span data-ttu-id="7373c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7373c-129">OUTPUTS</span></span>

### <span data-ttu-id="7373c-130">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7373c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="7373c-131">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="7373c-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7373c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7373c-132">NOTES</span></span>

## <span data-ttu-id="7373c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7373c-133">RELATED LINKS</span></span>

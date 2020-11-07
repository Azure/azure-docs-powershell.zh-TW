---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965554"
---
# <span data-ttu-id="2ad36-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="2ad36-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="2ad36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ad36-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad36-103">取得 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="2ad36-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="2ad36-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ad36-104">SYNTAX</span></span>

### <span data-ttu-id="2ad36-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2ad36-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="2ad36-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ad36-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ad36-107">說明</span><span class="sxs-lookup"><span data-stu-id="2ad36-107">DESCRIPTION</span></span>
<span data-ttu-id="2ad36-108">**AzCosmosDBSqlContainer** Cmdlet 會取得指定 ResourceGroupName、Accountname 和 databasename 之所有現有 CosmosDB sql 容器的清單，並取得特定 ResourceGroupName、Accountname、Databasename 和容器的單一 CosmosDB sql 容器。</span><span class="sxs-lookup"><span data-stu-id="2ad36-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="2ad36-109">示例</span><span class="sxs-lookup"><span data-stu-id="2ad36-109">EXAMPLES</span></span>

### <span data-ttu-id="2ad36-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2ad36-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="2ad36-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ad36-111">PARAMETERS</span></span>

### <span data-ttu-id="2ad36-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ad36-112">-AccountName</span></span>
<span data-ttu-id="2ad36-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ad36-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2ad36-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ad36-114">-DatabaseName</span></span>
<span data-ttu-id="2ad36-115">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2ad36-115">Database name.</span></span>

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

### <span data-ttu-id="2ad36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad36-116">-DefaultProfile</span></span>
<span data-ttu-id="2ad36-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ad36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad36-118">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="2ad36-118">-Detailed</span></span>
<span data-ttu-id="2ad36-119">如果提供此選項，則 Cmdlet 會傳回含輸送量值的容器。</span><span class="sxs-lookup"><span data-stu-id="2ad36-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad36-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad36-120">-InputObject</span></span>
<span data-ttu-id="2ad36-121">Sql Database 物件。</span><span class="sxs-lookup"><span data-stu-id="2ad36-121">Sql Database object.</span></span>

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

### <span data-ttu-id="2ad36-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ad36-122">-Name</span></span>
<span data-ttu-id="2ad36-123">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="2ad36-123">Container name.</span></span>

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

### <span data-ttu-id="2ad36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad36-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ad36-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ad36-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2ad36-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad36-126">CommonParameters</span></span>
<span data-ttu-id="2ad36-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ad36-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad36-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ad36-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad36-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2ad36-129">INPUTS</span></span>

### <span data-ttu-id="2ad36-130">所有</span><span class="sxs-lookup"><span data-stu-id="2ad36-130">None</span></span>

## <span data-ttu-id="2ad36-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2ad36-131">OUTPUTS</span></span>

### <span data-ttu-id="2ad36-132">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2ad36-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="2ad36-133">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2ad36-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2ad36-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2ad36-134">NOTES</span></span>

## <span data-ttu-id="2ad36-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ad36-135">RELATED LINKS</span></span>

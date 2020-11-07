---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798989"
---
# <span data-ttu-id="683e7-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="683e7-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="683e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="683e7-102">SYNOPSIS</span></span>
<span data-ttu-id="683e7-103">取得 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="683e7-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="683e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="683e7-104">SYNTAX</span></span>

### <span data-ttu-id="683e7-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="683e7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="683e7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="683e7-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="683e7-107">說明</span><span class="sxs-lookup"><span data-stu-id="683e7-107">DESCRIPTION</span></span>
<span data-ttu-id="683e7-108">**AzCosmosDBSqlDatabase** Cmdlet 會取得指定 ResourceGroupName 之所有現有 CosmosDB sql 資料庫的清單，並取得特定 ResourceGroupName、Accountname、DatabaseName 和容器的單一 CosmosDB sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="683e7-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="683e7-109">示例</span><span class="sxs-lookup"><span data-stu-id="683e7-109">EXAMPLES</span></span>

### <span data-ttu-id="683e7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="683e7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="683e7-111">參數</span><span class="sxs-lookup"><span data-stu-id="683e7-111">PARAMETERS</span></span>

### <span data-ttu-id="683e7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="683e7-112">-AccountName</span></span>
<span data-ttu-id="683e7-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="683e7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="683e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683e7-114">-DefaultProfile</span></span>
<span data-ttu-id="683e7-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="683e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="683e7-116">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="683e7-116">-Detailed</span></span>
<span data-ttu-id="683e7-117">如果提供此選項，則 Cmdlet 會傳回含輸送量值的容器。</span><span class="sxs-lookup"><span data-stu-id="683e7-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="683e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="683e7-118">-InputObject</span></span>
<span data-ttu-id="683e7-119">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="683e7-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="683e7-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="683e7-120">-Name</span></span>
<span data-ttu-id="683e7-121">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="683e7-121">Database name.</span></span>

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

### <span data-ttu-id="683e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="683e7-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="683e7-123">Name of resource group.</span></span>

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

### <span data-ttu-id="683e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683e7-124">CommonParameters</span></span>
<span data-ttu-id="683e7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="683e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683e7-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="683e7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683e7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="683e7-127">INPUTS</span></span>

### <span data-ttu-id="683e7-128">所有</span><span class="sxs-lookup"><span data-stu-id="683e7-128">None</span></span>

## <span data-ttu-id="683e7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="683e7-129">OUTPUTS</span></span>

### <span data-ttu-id="683e7-130">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="683e7-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="683e7-131">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="683e7-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="683e7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="683e7-132">NOTES</span></span>

## <span data-ttu-id="683e7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="683e7-133">RELATED LINKS</span></span>

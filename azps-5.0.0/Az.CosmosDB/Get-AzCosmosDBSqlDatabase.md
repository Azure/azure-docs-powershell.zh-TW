---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285569"
---
# <span data-ttu-id="b0bac-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b0bac-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="b0bac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0bac-102">SYNOPSIS</span></span>
<span data-ttu-id="b0bac-103">取得 CosmosDB Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b0bac-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="b0bac-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0bac-104">SYNTAX</span></span>

### <span data-ttu-id="b0bac-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b0bac-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0bac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0bac-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0bac-107">說明</span><span class="sxs-lookup"><span data-stu-id="b0bac-107">DESCRIPTION</span></span>
<span data-ttu-id="b0bac-108">**AzCosmosDBSqlDatabase** Cmdlet 會取得指定 ResourceGroupName 之所有現有 CosmosDB sql 資料庫的清單，並取得特定 ResourceGroupName、Accountname、DatabaseName 和容器的單一 CosmosDB sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b0bac-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="b0bac-109">示例</span><span class="sxs-lookup"><span data-stu-id="b0bac-109">EXAMPLES</span></span>

### <span data-ttu-id="b0bac-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b0bac-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="b0bac-111">參數</span><span class="sxs-lookup"><span data-stu-id="b0bac-111">PARAMETERS</span></span>

### <span data-ttu-id="b0bac-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0bac-112">-AccountName</span></span>
<span data-ttu-id="b0bac-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0bac-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b0bac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0bac-114">-DefaultProfile</span></span>
<span data-ttu-id="b0bac-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0bac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0bac-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0bac-116">-Name</span></span>
<span data-ttu-id="b0bac-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b0bac-117">Database name.</span></span>

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

### <span data-ttu-id="b0bac-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b0bac-118">-ParentObject</span></span>
<span data-ttu-id="b0bac-119">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="b0bac-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0bac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0bac-120">-ResourceGroupName</span></span>
<span data-ttu-id="b0bac-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0bac-121">Name of resource group.</span></span>

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

### <span data-ttu-id="b0bac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0bac-122">CommonParameters</span></span>
<span data-ttu-id="b0bac-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0bac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0bac-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b0bac-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0bac-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b0bac-125">INPUTS</span></span>

### <span data-ttu-id="b0bac-126">所有</span><span class="sxs-lookup"><span data-stu-id="b0bac-126">None</span></span>

## <span data-ttu-id="b0bac-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b0bac-127">OUTPUTS</span></span>

### <span data-ttu-id="b0bac-128">PSSqlDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="b0bac-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="b0bac-129">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="b0bac-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b0bac-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b0bac-130">NOTES</span></span>

## <span data-ttu-id="b0bac-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0bac-131">RELATED LINKS</span></span>

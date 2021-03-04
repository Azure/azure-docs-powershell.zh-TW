---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 6d0fe9565a969de19234d65378fd91a1af7a327f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917765"
---
# <span data-ttu-id="9808e-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9808e-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="9808e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9808e-102">SYNOPSIS</span></span>
<span data-ttu-id="9808e-103">獲得一個更新 Sql Database。</span><span class="sxs-lookup"><span data-stu-id="9808e-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9808e-104">語法</span><span class="sxs-lookup"><span data-stu-id="9808e-104">SYNTAX</span></span>

### <span data-ttu-id="9808e-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9808e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9808e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9808e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9808e-107">描述</span><span class="sxs-lookup"><span data-stu-id="9808e-107">DESCRIPTION</span></span>
<span data-ttu-id="9808e-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span><span class="sxs-lookup"><span data-stu-id="9808e-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="9808e-109">例子</span><span class="sxs-lookup"><span data-stu-id="9808e-109">EXAMPLES</span></span>

### <span data-ttu-id="9808e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="9808e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="9808e-111">參數</span><span class="sxs-lookup"><span data-stu-id="9808e-111">PARAMETERS</span></span>

### <span data-ttu-id="9808e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9808e-112">-AccountName</span></span>
<span data-ttu-id="9808e-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9808e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9808e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9808e-114">-DefaultProfile</span></span>
<span data-ttu-id="9808e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9808e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9808e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="9808e-116">-Name</span></span>
<span data-ttu-id="9808e-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9808e-117">Database name.</span></span>

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

### <span data-ttu-id="9808e-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9808e-118">-ParentObject</span></span>
<span data-ttu-id="9808e-119">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9808e-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9808e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9808e-120">-ResourceGroupName</span></span>
<span data-ttu-id="9808e-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9808e-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9808e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9808e-122">CommonParameters</span></span>
<span data-ttu-id="9808e-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9808e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9808e-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9808e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9808e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9808e-125">INPUTS</span></span>

### <span data-ttu-id="9808e-126">沒有</span><span class="sxs-lookup"><span data-stu-id="9808e-126">None</span></span>

## <span data-ttu-id="9808e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9808e-127">OUTPUTS</span></span>

### <span data-ttu-id="9808e-128">Microsoft.Azure.Commands.AzsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9808e-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="9808e-129">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9808e-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9808e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9808e-130">NOTES</span></span>

## <span data-ttu-id="9808e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9808e-131">RELATED LINKS</span></span>

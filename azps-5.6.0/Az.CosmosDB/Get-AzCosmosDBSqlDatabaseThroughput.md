---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 5bf35b43db1f1d961f24c1aa2c75c9f17c333345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903637"
---
# <span data-ttu-id="10ecf-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="10ecf-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="10ecf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="10ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="10ecf-103">獲得對應至一個更新資料庫的輸送量設定。</span><span class="sxs-lookup"><span data-stu-id="10ecf-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="10ecf-104">語法</span><span class="sxs-lookup"><span data-stu-id="10ecf-104">SYNTAX</span></span>

### <span data-ttu-id="10ecf-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="10ecf-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10ecf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10ecf-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10ecf-107">描述</span><span class="sxs-lookup"><span data-stu-id="10ecf-107">DESCRIPTION</span></span>
<span data-ttu-id="10ecf-108">**Get-AzCosmosDBSqlDatabaseThroughput** Cmdlet 會取得對應至一個 ThroughputsDB Sql Database 的輸送量設定。</span><span class="sxs-lookup"><span data-stu-id="10ecf-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="10ecf-109">例子</span><span class="sxs-lookup"><span data-stu-id="10ecf-109">EXAMPLES</span></span>

### <span data-ttu-id="10ecf-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="10ecf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="10ecf-111">參數</span><span class="sxs-lookup"><span data-stu-id="10ecf-111">PARAMETERS</span></span>

### <span data-ttu-id="10ecf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="10ecf-112">-AccountName</span></span>
<span data-ttu-id="10ecf-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="10ecf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="10ecf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ecf-114">-DefaultProfile</span></span>
<span data-ttu-id="10ecf-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="10ecf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10ecf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10ecf-116">-InputObject</span></span>
<span data-ttu-id="10ecf-117">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="10ecf-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="10ecf-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="10ecf-118">-Name</span></span>
<span data-ttu-id="10ecf-119">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="10ecf-119">Database name.</span></span>

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

### <span data-ttu-id="10ecf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ecf-120">-ResourceGroupName</span></span>
<span data-ttu-id="10ecf-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10ecf-121">Name of resource group.</span></span>

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

### <span data-ttu-id="10ecf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ecf-122">CommonParameters</span></span>
<span data-ttu-id="10ecf-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="10ecf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ecf-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10ecf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ecf-125">輸入</span><span class="sxs-lookup"><span data-stu-id="10ecf-125">INPUTS</span></span>

### <span data-ttu-id="10ecf-126">沒有</span><span class="sxs-lookup"><span data-stu-id="10ecf-126">None</span></span>

## <span data-ttu-id="10ecf-127">輸出</span><span class="sxs-lookup"><span data-stu-id="10ecf-127">OUTPUTS</span></span>

### <span data-ttu-id="10ecf-128">Microsoft.Azure.Commands.AzsDB.models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="10ecf-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="10ecf-129">筆記</span><span class="sxs-lookup"><span data-stu-id="10ecf-129">NOTES</span></span>

## <span data-ttu-id="10ecf-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="10ecf-130">RELATED LINKS</span></span>

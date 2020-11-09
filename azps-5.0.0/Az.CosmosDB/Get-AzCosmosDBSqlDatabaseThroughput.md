---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285570"
---
# <span data-ttu-id="9dd80-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="9dd80-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="9dd80-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9dd80-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd80-103">取得與 CosmosDB Sql 資料庫相對應的輸送量設定。</span><span class="sxs-lookup"><span data-stu-id="9dd80-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9dd80-104">句法</span><span class="sxs-lookup"><span data-stu-id="9dd80-104">SYNTAX</span></span>

### <span data-ttu-id="9dd80-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9dd80-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dd80-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dd80-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd80-107">說明</span><span class="sxs-lookup"><span data-stu-id="9dd80-107">DESCRIPTION</span></span>
<span data-ttu-id="9dd80-108">**AzCosmosDBSqlDatabaseThroughput** Cmdlet 會取得與 CosmosDB Sql 資料庫相對應的輸送量設定。</span><span class="sxs-lookup"><span data-stu-id="9dd80-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9dd80-109">示例</span><span class="sxs-lookup"><span data-stu-id="9dd80-109">EXAMPLES</span></span>

### <span data-ttu-id="9dd80-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9dd80-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="9dd80-111">參數</span><span class="sxs-lookup"><span data-stu-id="9dd80-111">PARAMETERS</span></span>

### <span data-ttu-id="9dd80-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9dd80-112">-AccountName</span></span>
<span data-ttu-id="9dd80-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dd80-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9dd80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd80-114">-DefaultProfile</span></span>
<span data-ttu-id="9dd80-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9dd80-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dd80-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dd80-116">-InputObject</span></span>
<span data-ttu-id="9dd80-117">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9dd80-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9dd80-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9dd80-118">-Name</span></span>
<span data-ttu-id="9dd80-119">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9dd80-119">Database name.</span></span>

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

### <span data-ttu-id="9dd80-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd80-120">-ResourceGroupName</span></span>
<span data-ttu-id="9dd80-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dd80-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9dd80-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd80-122">CommonParameters</span></span>
<span data-ttu-id="9dd80-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9dd80-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd80-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9dd80-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd80-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9dd80-125">INPUTS</span></span>

### <span data-ttu-id="9dd80-126">所有</span><span class="sxs-lookup"><span data-stu-id="9dd80-126">None</span></span>

## <span data-ttu-id="9dd80-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9dd80-127">OUTPUTS</span></span>

### <span data-ttu-id="9dd80-128">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="9dd80-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9dd80-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9dd80-129">NOTES</span></span>

## <span data-ttu-id="9dd80-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dd80-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: f1fb191a235cdf1c98768d3201cab49278f4403c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903634"
---
# <span data-ttu-id="436d4-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="436d4-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="436d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="436d4-102">SYNOPSIS</span></span>
<span data-ttu-id="436d4-103">獲得一個一切資訊。</span><span class="sxs-lookup"><span data-stu-id="436d4-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="436d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="436d4-104">SYNTAX</span></span>

### <span data-ttu-id="436d4-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="436d4-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="436d4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="436d4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="436d4-107">描述</span><span class="sxs-lookup"><span data-stu-id="436d4-107">DESCRIPTION</span></span>
<span data-ttu-id="436d4-108">**Get-AzCosmosDBSqlStoredProcedure Cmdlet** 會取得一個給定 ResourceGroupName、AccountName、DatabaseName 和 ContainerName 的所有現有一切現有管理專案清單，並取得一個適用于給定 ResourceGroupName、AccountName、DatabaseName、ContainerName 和 StoredProcedureName 的單一一個一體器。</span><span class="sxs-lookup"><span data-stu-id="436d4-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="436d4-109">例子</span><span class="sxs-lookup"><span data-stu-id="436d4-109">EXAMPLES</span></span>

### <span data-ttu-id="436d4-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="436d4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="436d4-111">參數</span><span class="sxs-lookup"><span data-stu-id="436d4-111">PARAMETERS</span></span>

### <span data-ttu-id="436d4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="436d4-112">-AccountName</span></span>
<span data-ttu-id="436d4-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="436d4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="436d4-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="436d4-114">-ContainerName</span></span>
<span data-ttu-id="436d4-115">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="436d4-115">Container name.</span></span>

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

### <span data-ttu-id="436d4-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="436d4-116">-DatabaseName</span></span>
<span data-ttu-id="436d4-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="436d4-117">Database name.</span></span>

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

### <span data-ttu-id="436d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436d4-118">-DefaultProfile</span></span>
<span data-ttu-id="436d4-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="436d4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="436d4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="436d4-120">-Name</span></span>
<span data-ttu-id="436d4-121">儲存的 Prcodecure 名稱。</span><span class="sxs-lookup"><span data-stu-id="436d4-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="436d4-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="436d4-122">-ParentObject</span></span>
<span data-ttu-id="436d4-123">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="436d4-123">Sql Container object.</span></span>

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

### <span data-ttu-id="436d4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="436d4-124">-ResourceGroupName</span></span>
<span data-ttu-id="436d4-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="436d4-125">Name of resource group.</span></span>

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

### <span data-ttu-id="436d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436d4-126">CommonParameters</span></span>
<span data-ttu-id="436d4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="436d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436d4-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="436d4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="436d4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="436d4-129">INPUTS</span></span>

### <span data-ttu-id="436d4-130">沒有</span><span class="sxs-lookup"><span data-stu-id="436d4-130">None</span></span>

## <span data-ttu-id="436d4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="436d4-131">OUTPUTS</span></span>

### <span data-ttu-id="436d4-132">Microsoft.Azure.Commands.AzsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="436d4-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="436d4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="436d4-133">NOTES</span></span>

## <span data-ttu-id="436d4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="436d4-134">RELATED LINKS</span></span>

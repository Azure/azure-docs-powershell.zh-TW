---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 0d422014d3cf2ca2ffa18b60c10b50b21bf91144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910738"
---
# <span data-ttu-id="8b934-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="8b934-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="8b934-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8b934-102">SYNOPSIS</span></span>
<span data-ttu-id="8b934-103">獲得一個以使用者定義方式定義的一個系統函數。</span><span class="sxs-lookup"><span data-stu-id="8b934-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="8b934-104">語法</span><span class="sxs-lookup"><span data-stu-id="8b934-104">SYNTAX</span></span>

### <span data-ttu-id="8b934-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b934-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b934-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b934-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b934-107">描述</span><span class="sxs-lookup"><span data-stu-id="8b934-107">DESCRIPTION</span></span>
<span data-ttu-id="8b934-108">**Get-AzCosmosDBSqlUserDefinedFunction Cmdlet** 會取得一個給定 ResourceGroupName、AccountName、DatabaseName 和 ContainerName 的所有現有一切現有一切資訊清單，並取得一個適用于給定 ResourceGroupName、AccountName、DatabaseName、ContainerName 和 UserDefinedFunctionName 的單一一個一次。。</span><span class="sxs-lookup"><span data-stu-id="8b934-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="8b934-109">例子</span><span class="sxs-lookup"><span data-stu-id="8b934-109">EXAMPLES</span></span>

### <span data-ttu-id="8b934-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="8b934-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="8b934-111">參數</span><span class="sxs-lookup"><span data-stu-id="8b934-111">PARAMETERS</span></span>

### <span data-ttu-id="8b934-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b934-112">-AccountName</span></span>
<span data-ttu-id="8b934-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b934-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8b934-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8b934-114">-ContainerName</span></span>
<span data-ttu-id="8b934-115">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="8b934-115">Container name.</span></span>

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

### <span data-ttu-id="8b934-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8b934-116">-DatabaseName</span></span>
<span data-ttu-id="8b934-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8b934-117">Database name.</span></span>

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

### <span data-ttu-id="8b934-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b934-118">-DefaultProfile</span></span>
<span data-ttu-id="8b934-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b934-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b934-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b934-120">-Name</span></span>
<span data-ttu-id="8b934-121">使用者定義函數名稱。</span><span class="sxs-lookup"><span data-stu-id="8b934-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="8b934-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8b934-122">-ParentObject</span></span>
<span data-ttu-id="8b934-123">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="8b934-123">Sql Container object.</span></span>

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

### <span data-ttu-id="8b934-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b934-124">-ResourceGroupName</span></span>
<span data-ttu-id="8b934-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b934-125">Name of resource group.</span></span>

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

### <span data-ttu-id="8b934-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b934-126">CommonParameters</span></span>
<span data-ttu-id="8b934-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8b934-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b934-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b934-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b934-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8b934-129">INPUTS</span></span>

### <span data-ttu-id="8b934-130">沒有</span><span class="sxs-lookup"><span data-stu-id="8b934-130">None</span></span>

## <span data-ttu-id="8b934-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8b934-131">OUTPUTS</span></span>

### <span data-ttu-id="8b934-132">Microsoft.Azure.Commands.AzsDB.models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="8b934-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="8b934-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8b934-133">NOTES</span></span>

## <span data-ttu-id="8b934-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b934-134">RELATED LINKS</span></span>

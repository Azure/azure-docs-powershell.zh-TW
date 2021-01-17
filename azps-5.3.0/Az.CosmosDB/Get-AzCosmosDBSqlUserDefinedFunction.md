---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449593"
---
# <span data-ttu-id="02dfa-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="02dfa-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="02dfa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="02dfa-103">取得 CosmosDB Sql 使用者定義的函數。</span><span class="sxs-lookup"><span data-stu-id="02dfa-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="02dfa-104">句法</span><span class="sxs-lookup"><span data-stu-id="02dfa-104">SYNTAX</span></span>

### <span data-ttu-id="02dfa-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="02dfa-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02dfa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02dfa-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02dfa-107">說明</span><span class="sxs-lookup"><span data-stu-id="02dfa-107">DESCRIPTION</span></span>
<span data-ttu-id="02dfa-108">**AzCosmosDBSqlUserDefinedFunction** Cmdlet 會取得特定 ResourceGroupName、Accountname、databasename 及的所有現有 CosmosDB sql UserDefinedFunctions 清單，並針對特定的 CosmosDB、Accountname、databasename、和 UserDefinedFunction 取得單一的 ResourceGroupName sql UserDefinedFunctionName。</span><span class="sxs-lookup"><span data-stu-id="02dfa-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="02dfa-109">示例</span><span class="sxs-lookup"><span data-stu-id="02dfa-109">EXAMPLES</span></span>

### <span data-ttu-id="02dfa-110">範例1</span><span class="sxs-lookup"><span data-stu-id="02dfa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="02dfa-111">參數</span><span class="sxs-lookup"><span data-stu-id="02dfa-111">PARAMETERS</span></span>

### <span data-ttu-id="02dfa-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02dfa-112">-AccountName</span></span>
<span data-ttu-id="02dfa-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="02dfa-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="02dfa-114">-容器</span><span class="sxs-lookup"><span data-stu-id="02dfa-114">-ContainerName</span></span>
<span data-ttu-id="02dfa-115">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="02dfa-115">Container name.</span></span>

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

### <span data-ttu-id="02dfa-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02dfa-116">-DatabaseName</span></span>
<span data-ttu-id="02dfa-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="02dfa-117">Database name.</span></span>

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

### <span data-ttu-id="02dfa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02dfa-118">-DefaultProfile</span></span>
<span data-ttu-id="02dfa-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02dfa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02dfa-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="02dfa-120">-Name</span></span>
<span data-ttu-id="02dfa-121">使用者定義的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="02dfa-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="02dfa-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02dfa-122">-ParentObject</span></span>
<span data-ttu-id="02dfa-123">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="02dfa-123">Sql Container object.</span></span>

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

### <span data-ttu-id="02dfa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02dfa-124">-ResourceGroupName</span></span>
<span data-ttu-id="02dfa-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="02dfa-125">Name of resource group.</span></span>

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

### <span data-ttu-id="02dfa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02dfa-126">CommonParameters</span></span>
<span data-ttu-id="02dfa-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02dfa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02dfa-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="02dfa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02dfa-129">輸入</span><span class="sxs-lookup"><span data-stu-id="02dfa-129">INPUTS</span></span>

### <span data-ttu-id="02dfa-130">所有</span><span class="sxs-lookup"><span data-stu-id="02dfa-130">None</span></span>

## <span data-ttu-id="02dfa-131">輸出</span><span class="sxs-lookup"><span data-stu-id="02dfa-131">OUTPUTS</span></span>

### <span data-ttu-id="02dfa-132">PSSqlUserDefinedFunctionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="02dfa-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="02dfa-133">筆記</span><span class="sxs-lookup"><span data-stu-id="02dfa-133">NOTES</span></span>

## <span data-ttu-id="02dfa-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="02dfa-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279445"
---
# <span data-ttu-id="6cc5e-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="6cc5e-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="6cc5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6cc5e-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc5e-103">取得 CosmosDB Sql 使用者定義的函數。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="6cc5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6cc5e-104">SYNTAX</span></span>

### <span data-ttu-id="6cc5e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cc5e-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cc5e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cc5e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cc5e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6cc5e-107">DESCRIPTION</span></span>
<span data-ttu-id="6cc5e-108">**AzCosmosDBSqlUserDefinedFunction** Cmdlet 會取得特定 ResourceGroupName、Accountname、databasename 及的所有現有 CosmosDB sql UserDefinedFunctions 清單，並針對特定的 CosmosDB、Accountname、databasename、和 UserDefinedFunction 取得單一的 ResourceGroupName sql UserDefinedFunctionName。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="6cc5e-109">示例</span><span class="sxs-lookup"><span data-stu-id="6cc5e-109">EXAMPLES</span></span>

### <span data-ttu-id="6cc5e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6cc5e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="6cc5e-111">參數</span><span class="sxs-lookup"><span data-stu-id="6cc5e-111">PARAMETERS</span></span>

### <span data-ttu-id="6cc5e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6cc5e-112">-AccountName</span></span>
<span data-ttu-id="6cc5e-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6cc5e-114">-容器</span><span class="sxs-lookup"><span data-stu-id="6cc5e-114">-ContainerName</span></span>
<span data-ttu-id="6cc5e-115">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-115">Container name.</span></span>

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

### <span data-ttu-id="6cc5e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cc5e-116">-DatabaseName</span></span>
<span data-ttu-id="6cc5e-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-117">Database name.</span></span>

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

### <span data-ttu-id="6cc5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc5e-118">-DefaultProfile</span></span>
<span data-ttu-id="6cc5e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cc5e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6cc5e-120">-Name</span></span>
<span data-ttu-id="6cc5e-121">使用者定義的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="6cc5e-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6cc5e-122">-ParentObject</span></span>
<span data-ttu-id="6cc5e-123">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-123">Sql Container object.</span></span>

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

### <span data-ttu-id="6cc5e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc5e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6cc5e-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="6cc5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc5e-126">CommonParameters</span></span>
<span data-ttu-id="6cc5e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc5e-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc5e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6cc5e-129">INPUTS</span></span>

### <span data-ttu-id="6cc5e-130">所有</span><span class="sxs-lookup"><span data-stu-id="6cc5e-130">None</span></span>

## <span data-ttu-id="6cc5e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6cc5e-131">OUTPUTS</span></span>

### <span data-ttu-id="6cc5e-132">PSSqlUserDefinedFunctionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6cc5e-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="6cc5e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6cc5e-133">NOTES</span></span>

## <span data-ttu-id="6cc5e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cc5e-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446015"
---
# <span data-ttu-id="be8ad-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="be8ad-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="be8ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="be8ad-103">刪除 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="be8ad-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="be8ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="be8ad-104">SYNTAX</span></span>

### <span data-ttu-id="be8ad-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="be8ad-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be8ad-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be8ad-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be8ad-107">說明</span><span class="sxs-lookup"><span data-stu-id="be8ad-107">DESCRIPTION</span></span>
<span data-ttu-id="be8ad-108">**AzCosmosDBSqlContainer** Cmdlet 會刪除對應至指定 ResourceGroupName、AccountName、DatabaseName 和容器的 CosmosDB Sql 容器。</span><span class="sxs-lookup"><span data-stu-id="be8ad-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="be8ad-109">示例</span><span class="sxs-lookup"><span data-stu-id="be8ad-109">EXAMPLES</span></span>

### <span data-ttu-id="be8ad-110">範例1</span><span class="sxs-lookup"><span data-stu-id="be8ad-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="be8ad-111">參數</span><span class="sxs-lookup"><span data-stu-id="be8ad-111">PARAMETERS</span></span>

### <span data-ttu-id="be8ad-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="be8ad-112">-AccountName</span></span>
<span data-ttu-id="be8ad-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="be8ad-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="be8ad-114">-確認</span><span class="sxs-lookup"><span data-stu-id="be8ad-114">-Confirm</span></span>
<span data-ttu-id="be8ad-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be8ad-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8ad-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="be8ad-116">-DatabaseName</span></span>
<span data-ttu-id="be8ad-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="be8ad-117">Database name.</span></span>

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

### <span data-ttu-id="be8ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8ad-118">-DefaultProfile</span></span>
<span data-ttu-id="be8ad-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be8ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be8ad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be8ad-120">-InputObject</span></span>
<span data-ttu-id="be8ad-121">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="be8ad-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be8ad-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="be8ad-122">-Name</span></span>
<span data-ttu-id="be8ad-123">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="be8ad-123">Container name.</span></span>

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

### <span data-ttu-id="be8ad-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be8ad-124">-PassThru</span></span>
<span data-ttu-id="be8ad-125">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="be8ad-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="be8ad-126">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="be8ad-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="be8ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be8ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="be8ad-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="be8ad-128">Name of resource group.</span></span>

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

### <span data-ttu-id="be8ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be8ad-129">-WhatIf</span></span>
<span data-ttu-id="be8ad-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be8ad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be8ad-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be8ad-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8ad-132">CommonParameters</span></span>
<span data-ttu-id="be8ad-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be8ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8ad-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="be8ad-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8ad-135">輸入</span><span class="sxs-lookup"><span data-stu-id="be8ad-135">INPUTS</span></span>

### <span data-ttu-id="be8ad-136">所有</span><span class="sxs-lookup"><span data-stu-id="be8ad-136">None</span></span>

## <span data-ttu-id="be8ad-137">輸出</span><span class="sxs-lookup"><span data-stu-id="be8ad-137">OUTPUTS</span></span>

### <span data-ttu-id="be8ad-138">System.void</span><span class="sxs-lookup"><span data-stu-id="be8ad-138">System.Void</span></span>

### <span data-ttu-id="be8ad-139">System.object</span><span class="sxs-lookup"><span data-stu-id="be8ad-139">System.Boolean</span></span>

## <span data-ttu-id="be8ad-140">筆記</span><span class="sxs-lookup"><span data-stu-id="be8ad-140">NOTES</span></span>

## <span data-ttu-id="be8ad-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="be8ad-141">RELATED LINKS</span></span>

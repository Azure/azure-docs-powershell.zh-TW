---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98445960"
---
# <span data-ttu-id="187d0-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="187d0-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="187d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="187d0-102">SYNOPSIS</span></span>
<span data-ttu-id="187d0-103">更新 CosmosDB 表。</span><span class="sxs-lookup"><span data-stu-id="187d0-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="187d0-104">讀取現有的資料表，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="187d0-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="187d0-105">句法</span><span class="sxs-lookup"><span data-stu-id="187d0-105">SYNTAX</span></span>

### <span data-ttu-id="187d0-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="187d0-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="187d0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="187d0-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="187d0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="187d0-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="187d0-109">說明</span><span class="sxs-lookup"><span data-stu-id="187d0-109">DESCRIPTION</span></span>
<span data-ttu-id="187d0-110">更新 CosmosDB 表。</span><span class="sxs-lookup"><span data-stu-id="187d0-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="187d0-111">讀取現有的資料表，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="187d0-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="187d0-112">示例</span><span class="sxs-lookup"><span data-stu-id="187d0-112">EXAMPLES</span></span>

### <span data-ttu-id="187d0-113">範例1</span><span class="sxs-lookup"><span data-stu-id="187d0-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="187d0-114">參數</span><span class="sxs-lookup"><span data-stu-id="187d0-114">PARAMETERS</span></span>

### <span data-ttu-id="187d0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="187d0-115">-AccountName</span></span>
<span data-ttu-id="187d0-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="187d0-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="187d0-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="187d0-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="187d0-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="187d0-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d0-119">-確認</span><span class="sxs-lookup"><span data-stu-id="187d0-119">-Confirm</span></span>
<span data-ttu-id="187d0-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="187d0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="187d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187d0-121">-DefaultProfile</span></span>
<span data-ttu-id="187d0-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="187d0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="187d0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="187d0-123">-InputObject</span></span>
<span data-ttu-id="187d0-124">Table 物件。</span><span class="sxs-lookup"><span data-stu-id="187d0-124">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="187d0-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="187d0-125">-Name</span></span>
<span data-ttu-id="187d0-126">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="187d0-126">Name of the Table.</span></span>

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

### <span data-ttu-id="187d0-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="187d0-127">-ParentObject</span></span>
<span data-ttu-id="187d0-128">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="187d0-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="187d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="187d0-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="187d0-130">Name of resource group.</span></span>

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

### <span data-ttu-id="187d0-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="187d0-131">-Throughput</span></span>
<span data-ttu-id="187d0-132">資料表 (RU/s) 的輸送量。</span><span class="sxs-lookup"><span data-stu-id="187d0-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="187d0-133">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="187d0-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187d0-134">-WhatIf</span></span>
<span data-ttu-id="187d0-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="187d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="187d0-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="187d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="187d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187d0-137">CommonParameters</span></span>
<span data-ttu-id="187d0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="187d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187d0-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="187d0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187d0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="187d0-140">INPUTS</span></span>

### <span data-ttu-id="187d0-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="187d0-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="187d0-142">PSTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="187d0-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="187d0-143">輸出</span><span class="sxs-lookup"><span data-stu-id="187d0-143">OUTPUTS</span></span>

### <span data-ttu-id="187d0-144">PSTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="187d0-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="187d0-145">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="187d0-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="187d0-146">筆記</span><span class="sxs-lookup"><span data-stu-id="187d0-146">NOTES</span></span>

## <span data-ttu-id="187d0-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="187d0-147">RELATED LINKS</span></span>

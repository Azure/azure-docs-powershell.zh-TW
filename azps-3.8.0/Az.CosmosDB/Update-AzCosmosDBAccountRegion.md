---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: dfc27ebad517a37fc2f78e99473d72fce568b56b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956488"
---
# <span data-ttu-id="61bbe-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="61bbe-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="61bbe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="61bbe-103">更新 CosmosDB 帳戶的地區。</span><span class="sxs-lookup"><span data-stu-id="61bbe-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="61bbe-104">句法</span><span class="sxs-lookup"><span data-stu-id="61bbe-104">SYNTAX</span></span>

### <span data-ttu-id="61bbe-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61bbe-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61bbe-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bbe-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bbe-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bbe-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccount> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61bbe-108">說明</span><span class="sxs-lookup"><span data-stu-id="61bbe-108">DESCRIPTION</span></span>
<span data-ttu-id="61bbe-109">更新 CosmosDB 帳戶的地區。</span><span class="sxs-lookup"><span data-stu-id="61bbe-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="61bbe-110">位置可以是以 PSLocation 類型的物件或以容錯移轉優先順序排序之位置名稱的字串形式提供。</span><span class="sxs-lookup"><span data-stu-id="61bbe-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="61bbe-111">LocationObject 參數預期 (容錯移轉 prioritiies 中的目前位置清單，新增的 LocationObjects 對應至要新增的新位置) 。</span><span class="sxs-lookup"><span data-stu-id="61bbe-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="61bbe-112">Location 參數預期目前位置的清單 (是依容錯移轉優先順序) 與新位置排序。</span><span class="sxs-lookup"><span data-stu-id="61bbe-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="61bbe-113">請注意，我們只支援新增地區。</span><span class="sxs-lookup"><span data-stu-id="61bbe-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="61bbe-114">請提供位置或 LocationObject。</span><span class="sxs-lookup"><span data-stu-id="61bbe-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="61bbe-115">示例</span><span class="sxs-lookup"><span data-stu-id="61bbe-115">EXAMPLES</span></span>

### <span data-ttu-id="61bbe-116">範例1</span><span class="sxs-lookup"><span data-stu-id="61bbe-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="61bbe-117">參數</span><span class="sxs-lookup"><span data-stu-id="61bbe-117">PARAMETERS</span></span>

### <span data-ttu-id="61bbe-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61bbe-118">-AsJob</span></span>
<span data-ttu-id="61bbe-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="61bbe-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61bbe-120">-確認</span><span class="sxs-lookup"><span data-stu-id="61bbe-120">-Confirm</span></span>
<span data-ttu-id="61bbe-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61bbe-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bbe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bbe-122">-DefaultProfile</span></span>
<span data-ttu-id="61bbe-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61bbe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61bbe-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61bbe-124">-InputObject</span></span>
<span data-ttu-id="61bbe-125">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="61bbe-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61bbe-126">-位置</span><span class="sxs-lookup"><span data-stu-id="61bbe-126">-Location</span></span>
<span data-ttu-id="61bbe-127">要新增之位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="61bbe-127">Name of the location to be added.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bbe-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="61bbe-128">-LocationObject</span></span>
<span data-ttu-id="61bbe-129">在 Cosmos DB 資料庫帳戶中新增位置。</span><span class="sxs-lookup"><span data-stu-id="61bbe-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="61bbe-130">PSLocation 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="61bbe-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bbe-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="61bbe-131">-Name</span></span>
<span data-ttu-id="61bbe-132">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="61bbe-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="61bbe-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bbe-133">-ResourceGroupName</span></span>
<span data-ttu-id="61bbe-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61bbe-134">Name of resource group.</span></span>

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

### <span data-ttu-id="61bbe-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61bbe-135">-ResourceId</span></span>
<span data-ttu-id="61bbe-136">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="61bbe-136">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bbe-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bbe-137">-WhatIf</span></span>
<span data-ttu-id="61bbe-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61bbe-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bbe-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61bbe-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bbe-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bbe-140">CommonParameters</span></span>
<span data-ttu-id="61bbe-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61bbe-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bbe-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61bbe-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bbe-143">輸入</span><span class="sxs-lookup"><span data-stu-id="61bbe-143">INPUTS</span></span>

### <span data-ttu-id="61bbe-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="61bbe-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="61bbe-145">輸出</span><span class="sxs-lookup"><span data-stu-id="61bbe-145">OUTPUTS</span></span>

### <span data-ttu-id="61bbe-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="61bbe-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="61bbe-147">筆記</span><span class="sxs-lookup"><span data-stu-id="61bbe-147">NOTES</span></span>

## <span data-ttu-id="61bbe-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="61bbe-148">RELATED LINKS</span></span>
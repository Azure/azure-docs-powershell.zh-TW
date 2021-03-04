---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: 643cdbf8aa0aed98dba7497fa0107d8d81583bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903630"
---
# <span data-ttu-id="37bb1-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="37bb1-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="37bb1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="37bb1-103">更新一個管理中心帳戶的區域。</span><span class="sxs-lookup"><span data-stu-id="37bb1-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="37bb1-104">語法</span><span class="sxs-lookup"><span data-stu-id="37bb1-104">SYNTAX</span></span>

### <span data-ttu-id="37bb1-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="37bb1-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37bb1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37bb1-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37bb1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37bb1-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37bb1-108">描述</span><span class="sxs-lookup"><span data-stu-id="37bb1-108">DESCRIPTION</span></span>
<span data-ttu-id="37bb1-109">更新一個管理中心帳戶的區域。</span><span class="sxs-lookup"><span data-stu-id="37bb1-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="37bb1-110">位置可以是 PSLocation 類型的物件，或以容錯移轉優先順序排序的位置名稱字串提供。</span><span class="sxs-lookup"><span data-stu-id="37bb1-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="37bb1-111">LocationObject 參數預期會新增對應至新位置的新 LocationObject (包含的目前位置清單) 容錯移轉先前的專案。</span><span class="sxs-lookup"><span data-stu-id="37bb1-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="37bb1-112">位置參數會預期目前位置清單 (容錯移轉優先順序和) 位置排序。</span><span class="sxs-lookup"><span data-stu-id="37bb1-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="37bb1-113">請注意，我們僅支援新增區域。</span><span class="sxs-lookup"><span data-stu-id="37bb1-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="37bb1-114">請提供位置或 LocationObject。</span><span class="sxs-lookup"><span data-stu-id="37bb1-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="37bb1-115">例子</span><span class="sxs-lookup"><span data-stu-id="37bb1-115">EXAMPLES</span></span>

### <span data-ttu-id="37bb1-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="37bb1-116">Example 1</span></span>
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

## <span data-ttu-id="37bb1-117">參數</span><span class="sxs-lookup"><span data-stu-id="37bb1-117">PARAMETERS</span></span>

### <span data-ttu-id="37bb1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37bb1-118">-AsJob</span></span>
<span data-ttu-id="37bb1-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="37bb1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37bb1-120">-確認</span><span class="sxs-lookup"><span data-stu-id="37bb1-120">-Confirm</span></span>
<span data-ttu-id="37bb1-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="37bb1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37bb1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37bb1-122">-DefaultProfile</span></span>
<span data-ttu-id="37bb1-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37bb1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37bb1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37bb1-124">-InputObject</span></span>
<span data-ttu-id="37bb1-125">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="37bb1-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37bb1-126">-位置</span><span class="sxs-lookup"><span data-stu-id="37bb1-126">-Location</span></span>
<span data-ttu-id="37bb1-127">要新增的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="37bb1-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="37bb1-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="37bb1-128">-LocationObject</span></span>
<span data-ttu-id="37bb1-129">新增位置至一個管理資料庫帳戶。</span><span class="sxs-lookup"><span data-stu-id="37bb1-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="37bb1-130">PSLocation 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="37bb1-130">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="37bb1-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="37bb1-131">-Name</span></span>
<span data-ttu-id="37bb1-132">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="37bb1-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="37bb1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37bb1-133">-ResourceGroupName</span></span>
<span data-ttu-id="37bb1-134">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37bb1-134">Name of resource group.</span></span>

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

### <span data-ttu-id="37bb1-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37bb1-135">-ResourceId</span></span>
<span data-ttu-id="37bb1-136">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="37bb1-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="37bb1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37bb1-137">-WhatIf</span></span>
<span data-ttu-id="37bb1-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37bb1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37bb1-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37bb1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37bb1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37bb1-140">CommonParameters</span></span>
<span data-ttu-id="37bb1-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37bb1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37bb1-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37bb1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37bb1-143">輸入</span><span class="sxs-lookup"><span data-stu-id="37bb1-143">INPUTS</span></span>

### <span data-ttu-id="37bb1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="37bb1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="37bb1-145">輸出</span><span class="sxs-lookup"><span data-stu-id="37bb1-145">OUTPUTS</span></span>

### <span data-ttu-id="37bb1-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="37bb1-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="37bb1-147">筆記</span><span class="sxs-lookup"><span data-stu-id="37bb1-147">NOTES</span></span>

## <span data-ttu-id="37bb1-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="37bb1-148">RELATED LINKS</span></span>

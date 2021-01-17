---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438352"
---
# <span data-ttu-id="147b2-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="147b2-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="147b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="147b2-102">SYNOPSIS</span></span>
<span data-ttu-id="147b2-103">更新函數 app 服務方案。</span><span class="sxs-lookup"><span data-stu-id="147b2-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="147b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="147b2-104">SYNTAX</span></span>

### <span data-ttu-id="147b2-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="147b2-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="147b2-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="147b2-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="147b2-107">說明</span><span class="sxs-lookup"><span data-stu-id="147b2-107">DESCRIPTION</span></span>
<span data-ttu-id="147b2-108">更新函數 app 服務方案。</span><span class="sxs-lookup"><span data-stu-id="147b2-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="147b2-109">示例</span><span class="sxs-lookup"><span data-stu-id="147b2-109">EXAMPLES</span></span>

### <span data-ttu-id="147b2-110">範例1：更新 app 服務方案以 EP2 含20個以上最大工人的 sku。</span><span class="sxs-lookup"><span data-stu-id="147b2-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="147b2-111">這個命令會更新應用程式服務方案，以 EP2 含二十個最大工人的 sku。</span><span class="sxs-lookup"><span data-stu-id="147b2-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="147b2-112">參數</span><span class="sxs-lookup"><span data-stu-id="147b2-112">PARAMETERS</span></span>

### <span data-ttu-id="147b2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="147b2-113">-AsJob</span></span>
<span data-ttu-id="147b2-114">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="147b2-114">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147b2-115">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="147b2-116">-InputObject</span></span>
<span data-ttu-id="147b2-117">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="147b2-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="147b2-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="147b2-119">App 服務方案的工作人數上限。</span><span class="sxs-lookup"><span data-stu-id="147b2-119">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="147b2-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="147b2-121">App 服務方案的工作人數最小值。</span><span class="sxs-lookup"><span data-stu-id="147b2-121">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="147b2-122">-Name</span></span>
<span data-ttu-id="147b2-123">App 服務方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="147b2-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="147b2-124">-NoWait</span></span>
<span data-ttu-id="147b2-125">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="147b2-125">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="147b2-127">資源所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="147b2-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="147b2-128">-Sku</span></span>
<span data-ttu-id="147b2-129">方案 sku。</span><span class="sxs-lookup"><span data-stu-id="147b2-129">The plan sku.</span></span>
<span data-ttu-id="147b2-130">有效的輸入為： EP1、EP2、EP3</span><span class="sxs-lookup"><span data-stu-id="147b2-130">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="147b2-131">-SubscriptionId</span></span>
<span data-ttu-id="147b2-132">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="147b2-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="147b2-133">-Tag</span></span>
<span data-ttu-id="147b2-134">資源標記。</span><span class="sxs-lookup"><span data-stu-id="147b2-134">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-135">-確認</span><span class="sxs-lookup"><span data-stu-id="147b2-135">-Confirm</span></span>
<span data-ttu-id="147b2-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="147b2-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="147b2-137">-WhatIf</span></span>
<span data-ttu-id="147b2-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="147b2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="147b2-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="147b2-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147b2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147b2-140">CommonParameters</span></span>
<span data-ttu-id="147b2-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="147b2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147b2-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="147b2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147b2-143">輸入</span><span class="sxs-lookup"><span data-stu-id="147b2-143">INPUTS</span></span>

### <span data-ttu-id="147b2-144">IAppServicePlan 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="147b2-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="147b2-145">輸出</span><span class="sxs-lookup"><span data-stu-id="147b2-145">OUTPUTS</span></span>

### <span data-ttu-id="147b2-146">IAppServicePlan 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="147b2-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="147b2-147">筆記</span><span class="sxs-lookup"><span data-stu-id="147b2-147">NOTES</span></span>

<span data-ttu-id="147b2-148">別名</span><span class="sxs-lookup"><span data-stu-id="147b2-148">ALIASES</span></span>

<span data-ttu-id="147b2-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="147b2-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="147b2-150">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="147b2-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="147b2-151">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="147b2-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="147b2-152">INPUTOBJECT <IAppServicePlan> ：</span><span class="sxs-lookup"><span data-stu-id="147b2-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="147b2-153">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="147b2-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="147b2-154">`[Kind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="147b2-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="147b2-155">`[Tag <IResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="147b2-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="147b2-156">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="147b2-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="147b2-157">`[Capacity <Int32?>]`：目前指派給資源的實例數。</span><span class="sxs-lookup"><span data-stu-id="147b2-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="147b2-158">`[FreeOfferExpirationTime <DateTime?>]`：伺服器場免費優惠到期的時間。</span><span class="sxs-lookup"><span data-stu-id="147b2-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="147b2-159">`[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="147b2-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="147b2-160">`[HyperV <Boolean?>]`：如果是 Hyper-v 容器 app 服務方案 <code>true</code> ，則 <code>false</code> 為。</span><span class="sxs-lookup"><span data-stu-id="147b2-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="147b2-161">`[IsSpot <Boolean?>]`： If <code>true</code> ，此 App 服務方案擁有的是污點實例。</span><span class="sxs-lookup"><span data-stu-id="147b2-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="147b2-162">`[IsXenon <Boolean?>]`：已過時：如果是 Hyper-v 容器 app 服務方案 <code>true</code> ，則 <code>false</code> 為。</span><span class="sxs-lookup"><span data-stu-id="147b2-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="147b2-163">`[MaximumElasticWorkerCount <Int32?>]`：此 ElasticScaleEnabled 應用程式服務方案允許的總工作人數上限</span><span class="sxs-lookup"><span data-stu-id="147b2-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="147b2-164">`[PerSiteScaling <Boolean?>]`： If <code>true</code> ，指派給這個 App 服務方案的應用程式可以獨立地伸縮。</span><span class="sxs-lookup"><span data-stu-id="147b2-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="147b2-165">如果 <code>false</code> 指派給這個 App 服務方案的應用程式將會縮放為方案的所有實例。</span><span class="sxs-lookup"><span data-stu-id="147b2-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="147b2-166">`[Reserved <Boolean?>]`：如果是 Linux app 服務方案 <code>true</code> ，則 <code>false</code> 為。</span><span class="sxs-lookup"><span data-stu-id="147b2-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="147b2-167">`[SkuCapability <ICapability[]>]`： SKU 的功能（例如，已啟用流量管理器）嗎？</span><span class="sxs-lookup"><span data-stu-id="147b2-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="147b2-168">`[Name <String>]`： SKU 功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="147b2-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="147b2-169">`[Reason <String>]`： SKU 功能的原因。</span><span class="sxs-lookup"><span data-stu-id="147b2-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="147b2-170">`[Value <String>]`： SKU 功能的值。</span><span class="sxs-lookup"><span data-stu-id="147b2-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="147b2-171">`[SkuCapacityDefault <Int32?>]`：此應用程式服務方案 SKU 的預設工作執行緒數。</span><span class="sxs-lookup"><span data-stu-id="147b2-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="147b2-172">`[SkuCapacityMaximum <Int32?>]`：此 App 服務方案 SKU 的最大工作人數。</span><span class="sxs-lookup"><span data-stu-id="147b2-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="147b2-173">`[SkuCapacityMinimum <Int32?>]`：此 App 服務方案 SKU 的最小員工數量。</span><span class="sxs-lookup"><span data-stu-id="147b2-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="147b2-174">`[SkuCapacityScaleType <String>]`：應用程式服務方案的可用縮放設定。</span><span class="sxs-lookup"><span data-stu-id="147b2-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="147b2-175">`[SkuFamily <String>]`：資源 SKU 的家用程式碼。</span><span class="sxs-lookup"><span data-stu-id="147b2-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="147b2-176">`[SkuLocation <String[]>]`： SKU 的位置。</span><span class="sxs-lookup"><span data-stu-id="147b2-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="147b2-177">`[SkuName <String>]`：資源 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="147b2-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="147b2-178">`[SkuSize <String>]`：資源 SKU 的大小指定符。</span><span class="sxs-lookup"><span data-stu-id="147b2-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="147b2-179">`[SkuTier <String>]`：資源 SKU 的服務層級。</span><span class="sxs-lookup"><span data-stu-id="147b2-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="147b2-180">`[SpotExpirationTime <DateTime?>]`：伺服器伺服器陣列的到期時間。</span><span class="sxs-lookup"><span data-stu-id="147b2-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="147b2-181">只有在它是專色伺服器群時才有效。</span><span class="sxs-lookup"><span data-stu-id="147b2-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="147b2-182">`[TargetWorkerCount <Int32?>]`：縮放工作人員計數。</span><span class="sxs-lookup"><span data-stu-id="147b2-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="147b2-183">`[TargetWorkerSizeId <Int32?>]`：縮放輔助角色大小 ID。</span><span class="sxs-lookup"><span data-stu-id="147b2-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="147b2-184">`[WorkerTierName <String>]`：指派給 App 服務方案的目標 worker 層。</span><span class="sxs-lookup"><span data-stu-id="147b2-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="147b2-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="147b2-185">RELATED LINKS</span></span>


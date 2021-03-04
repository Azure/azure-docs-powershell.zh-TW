---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904682"
---
# <span data-ttu-id="8f2c8-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="8f2c8-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="8f2c8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2c8-103">更新功能應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="8f2c8-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f2c8-104">SYNTAX</span></span>

### <span data-ttu-id="8f2c8-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="8f2c8-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f2c8-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="8f2c8-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f2c8-107">描述</span><span class="sxs-lookup"><span data-stu-id="8f2c8-107">DESCRIPTION</span></span>
<span data-ttu-id="8f2c8-108">更新功能應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="8f2c8-109">例子</span><span class="sxs-lookup"><span data-stu-id="8f2c8-109">EXAMPLES</span></span>

### <span data-ttu-id="8f2c8-110">範例 1：將 App 服務方案更新為 EP2 SKU，並包含最多二十名員工。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="8f2c8-111">此命令將 App 服務方案更新為 EP2 SKU，最多 20 位員工。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="8f2c8-112">參數</span><span class="sxs-lookup"><span data-stu-id="8f2c8-112">PARAMETERS</span></span>

### <span data-ttu-id="8f2c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f2c8-113">-AsJob</span></span>
<span data-ttu-id="8f2c8-114">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="8f2c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2c8-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="8f2c8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f2c8-116">-InputObject</span></span>
<span data-ttu-id="8f2c8-117">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8f2c8-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="8f2c8-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="8f2c8-119">應用程式服務方案的員工人數上限。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="8f2c8-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="8f2c8-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="8f2c8-121">應用程式服務方案的最小工作人員人數。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="8f2c8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f2c8-122">-Name</span></span>
<span data-ttu-id="8f2c8-123">應用程式服務方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="8f2c8-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8f2c8-124">-NoWait</span></span>
<span data-ttu-id="8f2c8-125">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8f2c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="8f2c8-127">資源所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="8f2c8-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="8f2c8-128">-Sku</span></span>
<span data-ttu-id="8f2c8-129">方案 SKU。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-129">The plan sku.</span></span>
<span data-ttu-id="8f2c8-130">有效的輸入為：EP1、EP2、EP3</span><span class="sxs-lookup"><span data-stu-id="8f2c8-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="8f2c8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f2c8-131">-SubscriptionId</span></span>
<span data-ttu-id="8f2c8-132">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="8f2c8-133">-標記</span><span class="sxs-lookup"><span data-stu-id="8f2c8-133">-Tag</span></span>
<span data-ttu-id="8f2c8-134">資源標記。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-134">Resource tags.</span></span>

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

### <span data-ttu-id="8f2c8-135">-確認</span><span class="sxs-lookup"><span data-stu-id="8f2c8-135">-Confirm</span></span>
<span data-ttu-id="8f2c8-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f2c8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2c8-137">-WhatIf</span></span>
<span data-ttu-id="8f2c8-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f2c8-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f2c8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2c8-140">CommonParameters</span></span>
<span data-ttu-id="8f2c8-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2c8-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f2c8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2c8-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8f2c8-143">INPUTS</span></span>

### <span data-ttu-id="8f2c8-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8f2c8-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="8f2c8-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8f2c8-145">OUTPUTS</span></span>

### <span data-ttu-id="8f2c8-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8f2c8-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="8f2c8-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8f2c8-147">NOTES</span></span>

<span data-ttu-id="8f2c8-148">別名</span><span class="sxs-lookup"><span data-stu-id="8f2c8-148">ALIASES</span></span>

<span data-ttu-id="8f2c8-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8f2c8-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f2c8-150">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f2c8-151">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f2c8-152">INPUTOBJECT： <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="8f2c8-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="8f2c8-153">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="8f2c8-154">`[Kind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="8f2c8-155">`[Tag <IResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8f2c8-156">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8f2c8-157">`[Capacity <Int32?>]`：指派給資源的目前實例數目。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="8f2c8-158">`[FreeOfferExpirationTime <DateTime?>]`：伺服器伺服器伺服器系列免費優惠到期的時間。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="8f2c8-159">`[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="8f2c8-160">`[HyperV <Boolean?>]`：如果 Hyper-V 容器應用程式服務方案， <code>true</code> 否則 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="8f2c8-161">`[IsSpot <Boolean?>]`：如果 <code>true</code> ，此應用程式服務方案擁有 spot 實例。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="8f2c8-162">`[IsXenon <Boolean?>]`：已過時：如果 Hyper-V 容器應用程式服務方案 <code>true</code> ，否則 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="8f2c8-163">`[MaximumElasticWorkerCount <Int32?>]`：此ScaleEnabled App 服務方案允許的工作者總數上限</span><span class="sxs-lookup"><span data-stu-id="8f2c8-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="8f2c8-164">`[PerSiteScaling <Boolean?>]`： <code>true</code> 如果 ，指派給此應用程式服務方案的應用程式可以獨立縮放。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="8f2c8-165">如果 <code>false</code> ，指派給此應用程式服務方案的應用程式會縮放至計畫的所有實例。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="8f2c8-166">`[Reserved <Boolean?>]`：否則，如果 Linux 應用程式服務方案 <code>true</code> <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="8f2c8-167">`[SkuCapability <ICapability[]>]`：SKU 的功能，例如，是否已啟用流量管理員？</span><span class="sxs-lookup"><span data-stu-id="8f2c8-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="8f2c8-168">`[Name <String>]`：SKU 功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="8f2c8-169">`[Reason <String>]`：SKU 功能的原因。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="8f2c8-170">`[Value <String>]`：SKU 功能的值。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="8f2c8-171">`[SkuCapacityDefault <Int32?>]`：此 App 服務方案 SKU 的預設工作人員人數。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="8f2c8-172">`[SkuCapacityMaximum <Int32?>]`：此 App 服務方案 SKU 的員工人數上限。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="8f2c8-173">`[SkuCapacityMinimum <Int32?>]`：此 App 服務方案 SKU 的最小員工人數。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="8f2c8-174">`[SkuCapacityScaleType <String>]`：應用程式服務方案可用的縮放比例組配置。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="8f2c8-175">`[SkuFamily <String>]`：資源 SKU 的家庭代碼。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="8f2c8-176">`[SkuLocation <String[]>]`：SKU 的位置。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="8f2c8-177">`[SkuName <String>]`：資源 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="8f2c8-178">`[SkuSize <String>]`：資源 SKU 的大小指定元。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="8f2c8-179">`[SkuTier <String>]`：資源 SKU 的服務層級。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="8f2c8-180">`[SpotExpirationTime <DateTime?>]`：伺服器伺服器伺服器組到期的時間。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="8f2c8-181">只有當它是 Spot 伺服器時，才有效。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="8f2c8-182">`[TargetWorkerCount <Int32?>]`：縮放員工計數。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="8f2c8-183">`[TargetWorkerSizeId <Int32?>]`：縮放員工大小識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="8f2c8-184">`[WorkerTierName <String>]`：指派給應用程式服務方案的目標員工層級。</span><span class="sxs-lookup"><span data-stu-id="8f2c8-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="8f2c8-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f2c8-185">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136863"
---
# <span data-ttu-id="6d17c-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="6d17c-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="6d17c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d17c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d17c-103">刪除函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="6d17c-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="6d17c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d17c-104">SYNTAX</span></span>

### <span data-ttu-id="6d17c-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="6d17c-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d17c-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="6d17c-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d17c-107">說明</span><span class="sxs-lookup"><span data-stu-id="6d17c-107">DESCRIPTION</span></span>
<span data-ttu-id="6d17c-108">刪除函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="6d17c-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="6d17c-109">示例</span><span class="sxs-lookup"><span data-stu-id="6d17c-109">EXAMPLES</span></span>

### <span data-ttu-id="6d17c-110">範例1：透過名稱取得函數 app 方案並刪除它。</span><span class="sxs-lookup"><span data-stu-id="6d17c-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="6d17c-111">這個命令會透過名稱來取得函式應用程式計畫，並將它刪除。</span><span class="sxs-lookup"><span data-stu-id="6d17c-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="6d17c-112">範例2：依名稱刪除函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="6d17c-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="6d17c-113">這個命令會依名稱刪除函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="6d17c-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="6d17c-114">參數</span><span class="sxs-lookup"><span data-stu-id="6d17c-114">PARAMETERS</span></span>

### <span data-ttu-id="6d17c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d17c-115">-DefaultProfile</span></span>
<span data-ttu-id="6d17c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d17c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d17c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6d17c-117">-Force</span></span>
<span data-ttu-id="6d17c-118">強制 Cmdlet 移除函數應用程式方案，但不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6d17c-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6d17c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d17c-119">-InputObject</span></span>
<span data-ttu-id="6d17c-120">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6d17c-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d17c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d17c-121">-Name</span></span>
<span data-ttu-id="6d17c-122">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d17c-122">The name of function app.</span></span>

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

### <span data-ttu-id="6d17c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d17c-123">-PassThru</span></span>
<span data-ttu-id="6d17c-124">當命令成功時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6d17c-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="6d17c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d17c-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="6d17c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d17c-126">-SubscriptionId</span></span>
<span data-ttu-id="6d17c-127">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6d17c-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="6d17c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6d17c-128">-Confirm</span></span>
<span data-ttu-id="6d17c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6d17c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d17c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d17c-130">-WhatIf</span></span>
<span data-ttu-id="6d17c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d17c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d17c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d17c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d17c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d17c-133">CommonParameters</span></span>
<span data-ttu-id="6d17c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d17c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d17c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6d17c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d17c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6d17c-136">INPUTS</span></span>

### <span data-ttu-id="6d17c-137">IAppServicePlan 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="6d17c-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="6d17c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6d17c-138">OUTPUTS</span></span>

### <span data-ttu-id="6d17c-139">System.object</span><span class="sxs-lookup"><span data-stu-id="6d17c-139">System.Boolean</span></span>

## <span data-ttu-id="6d17c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6d17c-140">NOTES</span></span>

<span data-ttu-id="6d17c-141">別名</span><span class="sxs-lookup"><span data-stu-id="6d17c-141">ALIASES</span></span>

<span data-ttu-id="6d17c-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6d17c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d17c-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6d17c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d17c-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6d17c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d17c-145">INPUTOBJECT <IAppServicePlan> ：</span><span class="sxs-lookup"><span data-stu-id="6d17c-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="6d17c-146">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="6d17c-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="6d17c-147">`[Kind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="6d17c-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="6d17c-148">`[Tag <IResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="6d17c-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="6d17c-149">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="6d17c-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6d17c-150">`[Capacity <Int32?>]`：目前指派給資源的實例數。</span><span class="sxs-lookup"><span data-stu-id="6d17c-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="6d17c-151">`[FreeOfferExpirationTime <DateTime?>]`：伺服器場免費優惠到期的時間。</span><span class="sxs-lookup"><span data-stu-id="6d17c-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="6d17c-152">`[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d17c-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="6d17c-153">`[HyperV <Boolean?>]`：如果是 Hyper-v 容器 app 服務方案 <code>true</code> ，則 <code>false</code> 為。</span><span class="sxs-lookup"><span data-stu-id="6d17c-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="6d17c-154">`[IsSpot <Boolean?>]`： If <code>true</code> ，此 App 服務方案擁有的是污點實例。</span><span class="sxs-lookup"><span data-stu-id="6d17c-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="6d17c-155">`[IsXenon <Boolean?>]`：已過時：如果是 Hyper-v 容器 app 服務方案 <code>true</code> ，則 <code>false</code> 為。</span><span class="sxs-lookup"><span data-stu-id="6d17c-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="6d17c-156">`[MaximumElasticWorkerCount <Int32?>]`：此 ElasticScaleEnabled 應用程式服務方案允許的總工作人數上限</span><span class="sxs-lookup"><span data-stu-id="6d17c-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="6d17c-157">`[PerSiteScaling <Boolean?>]`： If <code>true</code> ，指派給這個 App 服務方案的應用程式可以獨立地伸縮。</span><span class="sxs-lookup"><span data-stu-id="6d17c-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="6d17c-158">如果 <code>false</code> 指派給這個 App 服務方案的應用程式將會縮放為方案的所有實例。</span><span class="sxs-lookup"><span data-stu-id="6d17c-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="6d17c-159">`[Reserved <Boolean?>]`：如果是 Linux app 服務方案 <code>true</code> ，則 <code>false</code> 為。</span><span class="sxs-lookup"><span data-stu-id="6d17c-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="6d17c-160">`[SkuCapability <ICapability[]>]`： SKU 的功能（例如，已啟用流量管理器）嗎？</span><span class="sxs-lookup"><span data-stu-id="6d17c-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="6d17c-161">`[Name <String>]`： SKU 功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d17c-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="6d17c-162">`[Reason <String>]`： SKU 功能的原因。</span><span class="sxs-lookup"><span data-stu-id="6d17c-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="6d17c-163">`[Value <String>]`： SKU 功能的值。</span><span class="sxs-lookup"><span data-stu-id="6d17c-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="6d17c-164">`[SkuCapacityDefault <Int32?>]`：此應用程式服務方案 SKU 的預設工作執行緒數。</span><span class="sxs-lookup"><span data-stu-id="6d17c-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="6d17c-165">`[SkuCapacityMaximum <Int32?>]`：此 App 服務方案 SKU 的最大工作人數。</span><span class="sxs-lookup"><span data-stu-id="6d17c-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="6d17c-166">`[SkuCapacityMinimum <Int32?>]`：此 App 服務方案 SKU 的最小員工數量。</span><span class="sxs-lookup"><span data-stu-id="6d17c-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="6d17c-167">`[SkuCapacityScaleType <String>]`：應用程式服務方案的可用縮放設定。</span><span class="sxs-lookup"><span data-stu-id="6d17c-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="6d17c-168">`[SkuFamily <String>]`：資源 SKU 的家用程式碼。</span><span class="sxs-lookup"><span data-stu-id="6d17c-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="6d17c-169">`[SkuLocation <String[]>]`： SKU 的位置。</span><span class="sxs-lookup"><span data-stu-id="6d17c-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="6d17c-170">`[SkuName <String>]`：資源 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d17c-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="6d17c-171">`[SkuSize <String>]`：資源 SKU 的大小指定符。</span><span class="sxs-lookup"><span data-stu-id="6d17c-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="6d17c-172">`[SkuTier <String>]`：資源 SKU 的服務層級。</span><span class="sxs-lookup"><span data-stu-id="6d17c-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="6d17c-173">`[SpotExpirationTime <DateTime?>]`：伺服器伺服器陣列的到期時間。</span><span class="sxs-lookup"><span data-stu-id="6d17c-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="6d17c-174">只有在它是專色伺服器群時才有效。</span><span class="sxs-lookup"><span data-stu-id="6d17c-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="6d17c-175">`[TargetWorkerCount <Int32?>]`：縮放工作人員計數。</span><span class="sxs-lookup"><span data-stu-id="6d17c-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="6d17c-176">`[TargetWorkerSizeId <Int32?>]`：縮放輔助角色大小 ID。</span><span class="sxs-lookup"><span data-stu-id="6d17c-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="6d17c-177">`[WorkerTierName <String>]`：指派給 App 服務方案的目標 worker 層。</span><span class="sxs-lookup"><span data-stu-id="6d17c-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="6d17c-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d17c-178">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: e930a0848f39ec94cb6eeb4ef290b1842ea6793a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912833"
---
# <span data-ttu-id="a8f01-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a8f01-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a8f01-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a8f01-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f01-103">刪除功能應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="a8f01-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="a8f01-104">語法</span><span class="sxs-lookup"><span data-stu-id="a8f01-104">SYNTAX</span></span>

### <span data-ttu-id="a8f01-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a8f01-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a8f01-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="a8f01-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a8f01-107">描述</span><span class="sxs-lookup"><span data-stu-id="a8f01-107">DESCRIPTION</span></span>
<span data-ttu-id="a8f01-108">刪除功能應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="a8f01-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="a8f01-109">例子</span><span class="sxs-lookup"><span data-stu-id="a8f01-109">EXAMPLES</span></span>

### <span data-ttu-id="a8f01-110">範例 1：根據名稱取得函數應用程式計畫並將其刪除。</span><span class="sxs-lookup"><span data-stu-id="a8f01-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="a8f01-111">此命令會按名稱獲得函數應用程式計畫，並將其刪除。</span><span class="sxs-lookup"><span data-stu-id="a8f01-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="a8f01-112">範例 2：刪除函數應用程式計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8f01-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="a8f01-113">此命令會按名稱刪除函數應用程式計畫。</span><span class="sxs-lookup"><span data-stu-id="a8f01-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="a8f01-114">參數</span><span class="sxs-lookup"><span data-stu-id="a8f01-114">PARAMETERS</span></span>

### <span data-ttu-id="a8f01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f01-115">-DefaultProfile</span></span>
<span data-ttu-id="a8f01-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8f01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8f01-117">-強制</span><span class="sxs-lookup"><span data-stu-id="a8f01-117">-Force</span></span>
<span data-ttu-id="a8f01-118">強制 Cmdlet 移除功能應用程式方案，但不提示確認。</span><span class="sxs-lookup"><span data-stu-id="a8f01-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a8f01-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8f01-119">-InputObject</span></span>
<span data-ttu-id="a8f01-120">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a8f01-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a8f01-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8f01-121">-Name</span></span>
<span data-ttu-id="a8f01-122">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8f01-122">The name of function app.</span></span>

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

### <span data-ttu-id="a8f01-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8f01-123">-PassThru</span></span>
<span data-ttu-id="a8f01-124">命令成功時，會返回 True。</span><span class="sxs-lookup"><span data-stu-id="a8f01-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="a8f01-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f01-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="a8f01-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8f01-126">-SubscriptionId</span></span>
<span data-ttu-id="a8f01-127">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8f01-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a8f01-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a8f01-128">-Confirm</span></span>
<span data-ttu-id="a8f01-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a8f01-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8f01-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f01-130">-WhatIf</span></span>
<span data-ttu-id="a8f01-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8f01-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8f01-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8f01-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8f01-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f01-133">CommonParameters</span></span>
<span data-ttu-id="a8f01-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a8f01-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f01-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8f01-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f01-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a8f01-136">INPUTS</span></span>

### <span data-ttu-id="a8f01-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a8f01-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a8f01-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a8f01-138">OUTPUTS</span></span>

### <span data-ttu-id="a8f01-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8f01-139">System.Boolean</span></span>

## <span data-ttu-id="a8f01-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a8f01-140">NOTES</span></span>

<span data-ttu-id="a8f01-141">別名</span><span class="sxs-lookup"><span data-stu-id="a8f01-141">ALIASES</span></span>

<span data-ttu-id="a8f01-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a8f01-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8f01-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a8f01-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8f01-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a8f01-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8f01-145">INPUTOBJECT： <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="a8f01-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="a8f01-146">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="a8f01-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="a8f01-147">`[Kind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="a8f01-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="a8f01-148">`[Tag <IResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="a8f01-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a8f01-149">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="a8f01-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a8f01-150">`[Capacity <Int32?>]`：指派給資源的目前實例數目。</span><span class="sxs-lookup"><span data-stu-id="a8f01-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="a8f01-151">`[FreeOfferExpirationTime <DateTime?>]`：伺服器伺服器伺服器系列免費優惠到期的時間。</span><span class="sxs-lookup"><span data-stu-id="a8f01-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="a8f01-152">`[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8f01-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="a8f01-153">`[HyperV <Boolean?>]`：如果 Hyper-V 容器應用程式服務方案， <code>true</code> 否則 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="a8f01-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a8f01-154">`[IsSpot <Boolean?>]`：如果 <code>true</code> ，此應用程式服務方案擁有 spot 實例。</span><span class="sxs-lookup"><span data-stu-id="a8f01-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="a8f01-155">`[IsXenon <Boolean?>]`：已過時：如果 Hyper-V 容器應用程式服務方案 <code>true</code> ，否則 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="a8f01-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a8f01-156">`[MaximumElasticWorkerCount <Int32?>]`：此ScaleEnabled App 服務方案允許的工作者總數上限</span><span class="sxs-lookup"><span data-stu-id="a8f01-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="a8f01-157">`[PerSiteScaling <Boolean?>]`： <code>true</code> 如果 ，指派給此應用程式服務方案的應用程式可以獨立縮放。</span><span class="sxs-lookup"><span data-stu-id="a8f01-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="a8f01-158">如果 <code>false</code> ，指派給此應用程式服務方案的應用程式會縮放至計畫的所有實例。</span><span class="sxs-lookup"><span data-stu-id="a8f01-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="a8f01-159">`[Reserved <Boolean?>]`：否則，如果 Linux 應用程式服務方案 <code>true</code> <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="a8f01-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a8f01-160">`[SkuCapability <ICapability[]>]`：SKU 的功能，例如，是否已啟用流量管理員？</span><span class="sxs-lookup"><span data-stu-id="a8f01-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="a8f01-161">`[Name <String>]`：SKU 功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8f01-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="a8f01-162">`[Reason <String>]`：SKU 功能的原因。</span><span class="sxs-lookup"><span data-stu-id="a8f01-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="a8f01-163">`[Value <String>]`：SKU 功能的值。</span><span class="sxs-lookup"><span data-stu-id="a8f01-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="a8f01-164">`[SkuCapacityDefault <Int32?>]`：此 App 服務方案 SKU 的預設工作人員人數。</span><span class="sxs-lookup"><span data-stu-id="a8f01-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a8f01-165">`[SkuCapacityMaximum <Int32?>]`：此 App 服務方案 SKU 的員工人數上限。</span><span class="sxs-lookup"><span data-stu-id="a8f01-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a8f01-166">`[SkuCapacityMinimum <Int32?>]`：此 App 服務方案 SKU 的最小員工人數。</span><span class="sxs-lookup"><span data-stu-id="a8f01-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a8f01-167">`[SkuCapacityScaleType <String>]`：應用程式服務方案可用的縮放比例組配置。</span><span class="sxs-lookup"><span data-stu-id="a8f01-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="a8f01-168">`[SkuFamily <String>]`：資源 SKU 的家庭代碼。</span><span class="sxs-lookup"><span data-stu-id="a8f01-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="a8f01-169">`[SkuLocation <String[]>]`：SKU 的位置。</span><span class="sxs-lookup"><span data-stu-id="a8f01-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="a8f01-170">`[SkuName <String>]`：資源 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8f01-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="a8f01-171">`[SkuSize <String>]`：資源 SKU 的大小指定元。</span><span class="sxs-lookup"><span data-stu-id="a8f01-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="a8f01-172">`[SkuTier <String>]`：資源 SKU 的服務層級。</span><span class="sxs-lookup"><span data-stu-id="a8f01-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="a8f01-173">`[SpotExpirationTime <DateTime?>]`：伺服器伺服器伺服器組到期的時間。</span><span class="sxs-lookup"><span data-stu-id="a8f01-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="a8f01-174">只有當它是 Spot 伺服器時，才有效。</span><span class="sxs-lookup"><span data-stu-id="a8f01-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="a8f01-175">`[TargetWorkerCount <Int32?>]`：縮放員工計數。</span><span class="sxs-lookup"><span data-stu-id="a8f01-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="a8f01-176">`[TargetWorkerSizeId <Int32?>]`：縮放員工大小識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8f01-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="a8f01-177">`[WorkerTierName <String>]`：指派給應用程式服務方案的目標員工層級。</span><span class="sxs-lookup"><span data-stu-id="a8f01-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="a8f01-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8f01-178">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129591"
---
# <span data-ttu-id="acebd-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="acebd-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="acebd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acebd-102">SYNOPSIS</span></span>
<span data-ttu-id="acebd-103">建立或更新自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="acebd-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="acebd-104">句法</span><span class="sxs-lookup"><span data-stu-id="acebd-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="acebd-105">說明</span><span class="sxs-lookup"><span data-stu-id="acebd-105">DESCRIPTION</span></span>
<span data-ttu-id="acebd-106">建立或更新自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="acebd-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="acebd-107">示例</span><span class="sxs-lookup"><span data-stu-id="acebd-107">EXAMPLES</span></span>

### <span data-ttu-id="acebd-108">範例1：建立自訂提供者</span><span class="sxs-lookup"><span data-stu-id="acebd-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="acebd-109">建立自訂資源提供者</span><span class="sxs-lookup"><span data-stu-id="acebd-109">Create a custom resource provider</span></span>

### <span data-ttu-id="acebd-110">範例2：使用關聯建立自訂提供者</span><span class="sxs-lookup"><span data-stu-id="acebd-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="acebd-111">建立自訂提供者，並提供自訂提供者關聯的路線。</span><span class="sxs-lookup"><span data-stu-id="acebd-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="acebd-112">參數</span><span class="sxs-lookup"><span data-stu-id="acebd-112">PARAMETERS</span></span>

### <span data-ttu-id="acebd-113">-動作</span><span class="sxs-lookup"><span data-stu-id="acebd-113">-Action</span></span>
<span data-ttu-id="acebd-114">自訂資源提供者所實現的動作清單。</span><span class="sxs-lookup"><span data-stu-id="acebd-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="acebd-115">若要建立，請參閱 [記事] 區段，瞭解動作屬性及建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="acebd-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acebd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acebd-116">-AsJob</span></span>
<span data-ttu-id="acebd-117">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="acebd-117">Run the command as a job</span></span>

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

### <span data-ttu-id="acebd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acebd-118">-DefaultProfile</span></span>
<span data-ttu-id="acebd-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acebd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acebd-120">-位置</span><span class="sxs-lookup"><span data-stu-id="acebd-120">-Location</span></span>
<span data-ttu-id="acebd-121">資源位置</span><span class="sxs-lookup"><span data-stu-id="acebd-121">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acebd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="acebd-122">-Name</span></span>
<span data-ttu-id="acebd-123">資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="acebd-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acebd-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="acebd-124">-NoWait</span></span>
<span data-ttu-id="acebd-125">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="acebd-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="acebd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acebd-126">-ResourceGroupName</span></span>
<span data-ttu-id="acebd-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="acebd-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acebd-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="acebd-128">-ResourceType</span></span>
<span data-ttu-id="acebd-129">自訂資源提供者所實現的資源類型清單。</span><span class="sxs-lookup"><span data-stu-id="acebd-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="acebd-130">若要建立，請參閱 RESOURCETYPE 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="acebd-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acebd-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acebd-131">-SubscriptionId</span></span>
<span data-ttu-id="acebd-132">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="acebd-132">The Azure subscription ID.</span></span>
<span data-ttu-id="acebd-133">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="acebd-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acebd-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="acebd-134">-Tag</span></span>
<span data-ttu-id="acebd-135">資源標記</span><span class="sxs-lookup"><span data-stu-id="acebd-135">Resource tags</span></span>

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

### <span data-ttu-id="acebd-136">-驗證</span><span class="sxs-lookup"><span data-stu-id="acebd-136">-Validation</span></span>
<span data-ttu-id="acebd-137">要在自訂資源提供者的要求上執行的驗證清單。</span><span class="sxs-lookup"><span data-stu-id="acebd-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="acebd-138">若要建立，請參閱驗證屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="acebd-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acebd-139">-確認</span><span class="sxs-lookup"><span data-stu-id="acebd-139">-Confirm</span></span>
<span data-ttu-id="acebd-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="acebd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acebd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acebd-141">-WhatIf</span></span>
<span data-ttu-id="acebd-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acebd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acebd-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="acebd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acebd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acebd-144">CommonParameters</span></span>
<span data-ttu-id="acebd-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acebd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acebd-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="acebd-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acebd-147">輸入</span><span class="sxs-lookup"><span data-stu-id="acebd-147">INPUTS</span></span>

## <span data-ttu-id="acebd-148">輸出</span><span class="sxs-lookup"><span data-stu-id="acebd-148">OUTPUTS</span></span>

### <span data-ttu-id="acebd-149">ICustomRpManifest （CustomProviders）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="acebd-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="acebd-150">筆記</span><span class="sxs-lookup"><span data-stu-id="acebd-150">NOTES</span></span>

<span data-ttu-id="acebd-151">別名</span><span class="sxs-lookup"><span data-stu-id="acebd-151">ALIASES</span></span>

<span data-ttu-id="acebd-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="acebd-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="acebd-153">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="acebd-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="acebd-154">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="acebd-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="acebd-155">動作 <ICustomRpActionRouteDefinition [] >：自訂資源提供者所實現的動作清單。</span><span class="sxs-lookup"><span data-stu-id="acebd-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="acebd-156">`Endpoint <String>`：自訂資源提供者將向其發出代理要求的路由定義端點 URI。</span><span class="sxs-lookup"><span data-stu-id="acebd-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="acebd-157">這可能是一個平面 URI 的形式， (（例如 " https://testendpoint/ "） ) 或可以指定透過路徑 (（例如 '」）進行路由 https://testendpoint/{requestPath} ) </span><span class="sxs-lookup"><span data-stu-id="acebd-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="acebd-158">`Name <String>`：路線定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="acebd-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="acebd-159">這會成為 ARM 延伸 (的名稱，例如「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}」 ) </span><span class="sxs-lookup"><span data-stu-id="acebd-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="acebd-160">`[RoutingType <ActionRouting?>]`：動作要求支援的路由類型。</span><span class="sxs-lookup"><span data-stu-id="acebd-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="acebd-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >：自訂資源提供者所實現的資源類型清單。</span><span class="sxs-lookup"><span data-stu-id="acebd-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="acebd-162">`Endpoint <String>`：自訂資源提供者將向其發出代理要求的路由定義端點 URI。</span><span class="sxs-lookup"><span data-stu-id="acebd-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="acebd-163">這可能是一個平面 URI 的形式， (（例如 " https://testendpoint/ "） ) 或可以指定透過路徑 (（例如 '」）進行路由 https://testendpoint/{requestPath} ) </span><span class="sxs-lookup"><span data-stu-id="acebd-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="acebd-164">`Name <String>`：路線定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="acebd-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="acebd-165">這會成為 ARM 延伸 (的名稱，例如「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}」 ) </span><span class="sxs-lookup"><span data-stu-id="acebd-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="acebd-166">`[RoutingType <ResourceTypeRouting?>]`：資源要求支援的路由類型。</span><span class="sxs-lookup"><span data-stu-id="acebd-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="acebd-167">驗證 <ICustomRpValidations [] >：要在自訂資源提供者的要求上執行的驗證清單。</span><span class="sxs-lookup"><span data-stu-id="acebd-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="acebd-168">`Specification <String>`：驗證規格的連結。</span><span class="sxs-lookup"><span data-stu-id="acebd-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="acebd-169">規格必須寄宿在 raw.githubusercontent.com 上。</span><span class="sxs-lookup"><span data-stu-id="acebd-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="acebd-170">`[ValidationType <ValidationType?>]`：要針對相符要求執行的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="acebd-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="acebd-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="acebd-171">RELATED LINKS</span></span>


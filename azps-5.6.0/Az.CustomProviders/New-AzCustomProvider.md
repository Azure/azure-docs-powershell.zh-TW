---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: a3180cd693ae4c234656ba5d0812900ce8c308b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913946"
---
# <span data-ttu-id="9af4a-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="9af4a-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="9af4a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9af4a-102">SYNOPSIS</span></span>
<span data-ttu-id="9af4a-103">建立或更新自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="9af4a-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="9af4a-104">語法</span><span class="sxs-lookup"><span data-stu-id="9af4a-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9af4a-105">描述</span><span class="sxs-lookup"><span data-stu-id="9af4a-105">DESCRIPTION</span></span>
<span data-ttu-id="9af4a-106">建立或更新自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="9af4a-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="9af4a-107">例子</span><span class="sxs-lookup"><span data-stu-id="9af4a-107">EXAMPLES</span></span>

### <span data-ttu-id="9af4a-108">範例 1：建立自訂提供者</span><span class="sxs-lookup"><span data-stu-id="9af4a-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="9af4a-109">建立自訂資源提供者</span><span class="sxs-lookup"><span data-stu-id="9af4a-109">Create a custom resource provider</span></span>

### <span data-ttu-id="9af4a-110">範例 2：建立具有關聯之自訂提供者</span><span class="sxs-lookup"><span data-stu-id="9af4a-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="9af4a-111">使用自訂提供者關聯路由建立自訂提供者。</span><span class="sxs-lookup"><span data-stu-id="9af4a-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="9af4a-112">參數</span><span class="sxs-lookup"><span data-stu-id="9af4a-112">PARAMETERS</span></span>

### <span data-ttu-id="9af4a-113">-動作</span><span class="sxs-lookup"><span data-stu-id="9af4a-113">-Action</span></span>
<span data-ttu-id="9af4a-114">自訂資源提供者所執行的動作清單。</span><span class="sxs-lookup"><span data-stu-id="9af4a-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="9af4a-115">若要建構，請參閱 ACTION 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9af4a-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="9af4a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9af4a-116">-AsJob</span></span>
<span data-ttu-id="9af4a-117">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="9af4a-117">Run the command as a job</span></span>

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

### <span data-ttu-id="9af4a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af4a-118">-DefaultProfile</span></span>
<span data-ttu-id="9af4a-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9af4a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9af4a-120">-位置</span><span class="sxs-lookup"><span data-stu-id="9af4a-120">-Location</span></span>
<span data-ttu-id="9af4a-121">資源位置</span><span class="sxs-lookup"><span data-stu-id="9af4a-121">Resource location</span></span>

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

### <span data-ttu-id="9af4a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9af4a-122">-Name</span></span>
<span data-ttu-id="9af4a-123">資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af4a-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="9af4a-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9af4a-124">-NoWait</span></span>
<span data-ttu-id="9af4a-125">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="9af4a-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9af4a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af4a-126">-ResourceGroupName</span></span>
<span data-ttu-id="9af4a-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af4a-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9af4a-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9af4a-128">-ResourceType</span></span>
<span data-ttu-id="9af4a-129">自訂資源提供者所實施的資源類型清單。</span><span class="sxs-lookup"><span data-stu-id="9af4a-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="9af4a-130">若要建構，請參閱 RESOURCETYPE 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9af4a-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="9af4a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9af4a-131">-SubscriptionId</span></span>
<span data-ttu-id="9af4a-132">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9af4a-132">The Azure subscription ID.</span></span>
<span data-ttu-id="9af4a-133">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="9af4a-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="9af4a-134">-標記</span><span class="sxs-lookup"><span data-stu-id="9af4a-134">-Tag</span></span>
<span data-ttu-id="9af4a-135">資源標記</span><span class="sxs-lookup"><span data-stu-id="9af4a-135">Resource tags</span></span>

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

### <span data-ttu-id="9af4a-136">-驗證</span><span class="sxs-lookup"><span data-stu-id="9af4a-136">-Validation</span></span>
<span data-ttu-id="9af4a-137">要根據自訂資源提供者要求執行之驗證的清單。</span><span class="sxs-lookup"><span data-stu-id="9af4a-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="9af4a-138">若要建構，請參閱驗證屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9af4a-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="9af4a-139">-確認</span><span class="sxs-lookup"><span data-stu-id="9af4a-139">-Confirm</span></span>
<span data-ttu-id="9af4a-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9af4a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9af4a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af4a-141">-WhatIf</span></span>
<span data-ttu-id="9af4a-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9af4a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af4a-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9af4a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9af4a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af4a-144">CommonParameters</span></span>
<span data-ttu-id="9af4a-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9af4a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af4a-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9af4a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af4a-147">輸入</span><span class="sxs-lookup"><span data-stu-id="9af4a-147">INPUTS</span></span>

## <span data-ttu-id="9af4a-148">輸出</span><span class="sxs-lookup"><span data-stu-id="9af4a-148">OUTPUTS</span></span>

### <span data-ttu-id="9af4a-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="9af4a-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="9af4a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="9af4a-150">NOTES</span></span>

<span data-ttu-id="9af4a-151">別名</span><span class="sxs-lookup"><span data-stu-id="9af4a-151">ALIASES</span></span>

<span data-ttu-id="9af4a-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9af4a-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9af4a-153">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9af4a-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9af4a-154">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9af4a-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9af4a-155"><ICustomRpActionRouteDefinition[]>：自訂資源提供者所執行的動作清單。</span><span class="sxs-lookup"><span data-stu-id="9af4a-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="9af4a-156">`Endpoint <String>`：自訂資源提供者會要求路由定義端點 URI。</span><span class="sxs-lookup"><span data-stu-id="9af4a-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="9af4a-157">這可以是平面 URI (例如' ') 或指定透過路徑路由 https://testendpoint/ (例如' https://testendpoint/{requestPath} ') </span><span class="sxs-lookup"><span data-stu-id="9af4a-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="9af4a-158">`Name <String>`：路由定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af4a-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="9af4a-159">這會成為 ARM 擴充功能的名稱 (例如'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}') </span><span class="sxs-lookup"><span data-stu-id="9af4a-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="9af4a-160">`[RoutingType <ActionRouting?>]`：動作要求支援的路由類型。</span><span class="sxs-lookup"><span data-stu-id="9af4a-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="9af4a-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>：自訂資源提供者所實施的資源類型清單。</span><span class="sxs-lookup"><span data-stu-id="9af4a-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="9af4a-162">`Endpoint <String>`：自訂資源提供者會要求路由定義端點 URI。</span><span class="sxs-lookup"><span data-stu-id="9af4a-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="9af4a-163">這可以是平面 URI (例如' ') 或指定透過路徑路由 https://testendpoint/ (例如' https://testendpoint/{requestPath} ') </span><span class="sxs-lookup"><span data-stu-id="9af4a-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="9af4a-164">`Name <String>`：路由定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af4a-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="9af4a-165">這會成為 ARM 擴充功能的名稱 (例如'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}') </span><span class="sxs-lookup"><span data-stu-id="9af4a-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="9af4a-166">`[RoutingType <ResourceTypeRouting?>]`：資源要求支援的路由類型。</span><span class="sxs-lookup"><span data-stu-id="9af4a-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="9af4a-167">VALIDATION <ICustomRpValidations[]>：在自訂資源提供者的要求上執行驗證的清單。</span><span class="sxs-lookup"><span data-stu-id="9af4a-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="9af4a-168">`Specification <String>`：驗證規格的連結。</span><span class="sxs-lookup"><span data-stu-id="9af4a-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="9af4a-169">規格必須託管在 raw.githubusercontent.com。</span><span class="sxs-lookup"><span data-stu-id="9af4a-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="9af4a-170">`[ValidationType <ValidationType?>]`：針對比對要求執行驗證的類型。</span><span class="sxs-lookup"><span data-stu-id="9af4a-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="9af4a-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="9af4a-171">RELATED LINKS</span></span>


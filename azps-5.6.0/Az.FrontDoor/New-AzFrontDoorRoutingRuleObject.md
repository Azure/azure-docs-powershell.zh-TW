---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 3d66db0baeca0e371800c4544f2f0360c448b108
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906669"
---
# <span data-ttu-id="c8eb4-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="c8eb4-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="c8eb4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="c8eb4-103">建立 PSRoutingRuleObject 以建立門道</span><span class="sxs-lookup"><span data-stu-id="c8eb4-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c8eb4-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8eb4-104">SYNTAX</span></span>

### <span data-ttu-id="c8eb4-105">ByFieldsWithForwardingParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8eb4-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8eb4-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8eb4-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8eb4-107">描述</span><span class="sxs-lookup"><span data-stu-id="c8eb4-107">DESCRIPTION</span></span>
<span data-ttu-id="c8eb4-108">建立 PSRoutingRuleObject 以建立門道</span><span class="sxs-lookup"><span data-stu-id="c8eb4-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c8eb4-109">例子</span><span class="sxs-lookup"><span data-stu-id="c8eb4-109">EXAMPLES</span></span>

### <span data-ttu-id="c8eb4-110">範例 1：使用轉轉規則建立適用于前門的 PSRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="c8eb4-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="c8eb4-111">範例 2：使用重新導向規則建立適用于前門的 PSRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="c8eb4-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="c8eb4-112">建立 PSRoutingRuleObject 以建立門道</span><span class="sxs-lookup"><span data-stu-id="c8eb4-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c8eb4-113">參數</span><span class="sxs-lookup"><span data-stu-id="c8eb4-113">PARAMETERS</span></span>

### <span data-ttu-id="c8eb4-114">-已接受Protocol</span><span class="sxs-lookup"><span data-stu-id="c8eb4-114">-AcceptedProtocol</span></span>
<span data-ttu-id="c8eb4-115">符合此規則的通訊協定方案。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="c8eb4-116">預設值為 {HTTPs， HTTP}</span><span class="sxs-lookup"><span data-stu-id="c8eb4-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-117">-後端多工緩衝處理程式名稱</span><span class="sxs-lookup"><span data-stu-id="c8eb4-117">-BackendPoolName</span></span>
<span data-ttu-id="c8eb4-118">此規則路由至的後端多工緩衝處理程式資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c8eb4-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="c8eb4-119">-CustomForwardingPath</span></span>
<span data-ttu-id="c8eb4-120">用來重寫符合此規則之資源路徑的自訂路徑。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="c8eb4-121">保留空白以使用傳入路徑。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="c8eb4-122">-CustomFragment</span></span>
<span data-ttu-id="c8eb4-123">要新加入重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="c8eb4-124">片段是 #之後 URL 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="c8eb4-125">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="c8eb4-126">-CustomHost</span></span>
<span data-ttu-id="c8eb4-127">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-127">Host to redirect.</span></span> <span data-ttu-id="c8eb4-128">保留空白，以使用內接主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="c8eb4-129">-CustomPath</span></span>
<span data-ttu-id="c8eb4-130">重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-130">The full path to redirect.</span></span> <span data-ttu-id="c8eb4-131">路徑不能是空白的，必須以 /開始。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="c8eb4-132">保留空白，以使用內入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="c8eb4-133">-CustomQueryString</span></span>
<span data-ttu-id="c8eb4-134">這是要放在重新導向 URL 中的查詢字串集。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="c8eb4-135">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="c8eb4-136">查詢字串必須 <key>=</span><span class="sxs-lookup"><span data-stu-id="c8eb4-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="c8eb4-137">格式。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-137">format.</span></span> <span data-ttu-id="c8eb4-138">第一個？</span><span class="sxs-lookup"><span data-stu-id="c8eb4-138">The first ?</span></span> <span data-ttu-id="c8eb4-139">並且&自動新增，因此請不要在最前面加入查詢字串，但請以不同的查詢字串&。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8eb4-140">-DefaultProfile</span></span>
<span data-ttu-id="c8eb4-141">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="c8eb4-142">-DynamicCompression</span></span>
<span data-ttu-id="c8eb4-143">啟用緩存時，是否要對緩存內容啟用動態壓縮。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="c8eb4-144">預設值為啟用</span><span class="sxs-lookup"><span data-stu-id="c8eb4-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="c8eb4-145">-EnableCaching</span></span>
<span data-ttu-id="c8eb4-146">是否要啟用此路由的緩存。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="c8eb4-147">預設值為 False</span><span class="sxs-lookup"><span data-stu-id="c8eb4-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c8eb4-148">-EnabledState</span></span>
<span data-ttu-id="c8eb4-149">是否要啟用使用此規則。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="c8eb4-150">預設值為啟用</span><span class="sxs-lookup"><span data-stu-id="c8eb4-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="c8eb4-151">-ForwardingProtocol</span></span>
<span data-ttu-id="c8eb4-152">將流量轉往後端時，此規則將使用的通訊協定預設值為 MatchRequest。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c8eb4-153">-FrontDoorName</span></span>
<span data-ttu-id="c8eb4-154">此路由規則所屬的前門名稱。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="c8eb4-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="c8eb4-155">-FrontendEndpointName</span></span>
<span data-ttu-id="c8eb4-156">與此規則相關聯的 Frontend 端點名稱</span><span class="sxs-lookup"><span data-stu-id="c8eb4-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-157">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8eb4-157">-Name</span></span>
<span data-ttu-id="c8eb4-158">RoutingRule name.</span><span class="sxs-lookup"><span data-stu-id="c8eb4-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="c8eb4-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="c8eb4-159">-PatternToMatch</span></span>
<span data-ttu-id="c8eb4-160">規則的路由模式，不得有任何 \*，除非可能在路徑結尾的最後 /之後。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="c8eb4-161">預設值為 /\*</span><span class="sxs-lookup"><span data-stu-id="c8eb4-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="c8eb4-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="c8eb4-163">形成緩存鍵時，URL 查詢字詞的處理方式。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="c8eb4-164">預設值為 StripAll</span><span class="sxs-lookup"><span data-stu-id="c8eb4-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="c8eb4-165">-RedirectProtocol</span></span>
<span data-ttu-id="c8eb4-166">重新導向流量目的地的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="c8eb4-167">預設值為 MatchRequest</span><span class="sxs-lookup"><span data-stu-id="c8eb4-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="c8eb4-168">-RedirectType</span></span>
<span data-ttu-id="c8eb4-169">重新導向規則會用於重新導向流量的重新導向類型。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="c8eb4-170">已移動預設值</span><span class="sxs-lookup"><span data-stu-id="c8eb4-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eb4-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8eb4-171">-ResourceGroupName</span></span>
<span data-ttu-id="c8eb4-172">要建立 RoutingRule 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="c8eb4-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="c8eb4-173">-RulesEngineName</span></span>
<span data-ttu-id="c8eb4-174">要適用于此路由的特定規則引擎組配置的參照。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="c8eb4-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8eb4-175">CommonParameters</span></span>
<span data-ttu-id="c8eb4-176">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8eb4-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8eb4-177">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8eb4-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8eb4-178">輸入</span><span class="sxs-lookup"><span data-stu-id="c8eb4-178">INPUTS</span></span>

### <span data-ttu-id="c8eb4-179">沒有</span><span class="sxs-lookup"><span data-stu-id="c8eb4-179">None</span></span>

## <span data-ttu-id="c8eb4-180">輸出</span><span class="sxs-lookup"><span data-stu-id="c8eb4-180">OUTPUTS</span></span>

### <span data-ttu-id="c8eb4-181">Microsoft.Azure.Commands.FrontDoor.models.PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8eb4-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="c8eb4-182">筆記</span><span class="sxs-lookup"><span data-stu-id="c8eb4-182">NOTES</span></span>

## <span data-ttu-id="c8eb4-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8eb4-183">RELATED LINKS</span></span>

<span data-ttu-id="c8eb4-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="c8eb4-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>

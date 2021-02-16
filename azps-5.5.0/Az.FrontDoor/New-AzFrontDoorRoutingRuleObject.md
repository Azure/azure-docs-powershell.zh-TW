---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139166"
---
# <span data-ttu-id="38b1b-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="38b1b-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="38b1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="38b1b-103">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="38b1b-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="38b1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="38b1b-104">SYNTAX</span></span>

### <span data-ttu-id="38b1b-105">ByFieldsWithForwardingParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="38b1b-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38b1b-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38b1b-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38b1b-107">說明</span><span class="sxs-lookup"><span data-stu-id="38b1b-107">DESCRIPTION</span></span>
<span data-ttu-id="38b1b-108">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="38b1b-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="38b1b-109">示例</span><span class="sxs-lookup"><span data-stu-id="38b1b-109">EXAMPLES</span></span>

### <span data-ttu-id="38b1b-110">範例1：使用轉寄規則建立供前蓋建立的 PSRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="38b1b-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
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

### <span data-ttu-id="38b1b-111">範例2：使用重新導向規則建立供前蓋建立的 PSRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="38b1b-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
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

<span data-ttu-id="38b1b-112">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="38b1b-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="38b1b-113">參數</span><span class="sxs-lookup"><span data-stu-id="38b1b-113">PARAMETERS</span></span>

### <span data-ttu-id="38b1b-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="38b1b-114">-AcceptedProtocol</span></span>
<span data-ttu-id="38b1b-115">此規則要符合的通訊協定方案。</span><span class="sxs-lookup"><span data-stu-id="38b1b-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="38b1b-116">預設值為 {Https、Http}</span><span class="sxs-lookup"><span data-stu-id="38b1b-116">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="38b1b-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="38b1b-117">-BackendPoolName</span></span>
<span data-ttu-id="38b1b-118">此規則路由之 BackendPool 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="38b1b-118">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="38b1b-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="38b1b-119">-CustomForwardingPath</span></span>
<span data-ttu-id="38b1b-120">用來重新寫入此規則所符合之資源路徑的自訂路徑。</span><span class="sxs-lookup"><span data-stu-id="38b1b-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="38b1b-121">若要使用傳入路徑，請保留空白。</span><span class="sxs-lookup"><span data-stu-id="38b1b-121">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="38b1b-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="38b1b-122">-CustomFragment</span></span>
<span data-ttu-id="38b1b-123">要新增至重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="38b1b-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="38b1b-124">[片段] 是位於 # 之後的 URL 部分。</span><span class="sxs-lookup"><span data-stu-id="38b1b-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="38b1b-125">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="38b1b-125">Do not include the #.</span></span>

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

### <span data-ttu-id="38b1b-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="38b1b-126">-CustomHost</span></span>
<span data-ttu-id="38b1b-127">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="38b1b-127">Host to redirect.</span></span> <span data-ttu-id="38b1b-128">[留空] 可將傳入主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="38b1b-128">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="38b1b-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="38b1b-129">-CustomPath</span></span>
<span data-ttu-id="38b1b-130">要重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="38b1b-130">The full path to redirect.</span></span> <span data-ttu-id="38b1b-131">Path 不能為空白，且必須以/開頭。</span><span class="sxs-lookup"><span data-stu-id="38b1b-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="38b1b-132">[留空] 可使用傳入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="38b1b-132">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="38b1b-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="38b1b-133">-CustomQueryString</span></span>
<span data-ttu-id="38b1b-134">要放在重新導向 URL 中的一組查詢字串。</span><span class="sxs-lookup"><span data-stu-id="38b1b-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="38b1b-135">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="38b1b-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="38b1b-136">查詢字串必須在 <key>=</span><span class="sxs-lookup"><span data-stu-id="38b1b-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="38b1b-137">設置.</span><span class="sxs-lookup"><span data-stu-id="38b1b-137">format.</span></span> <span data-ttu-id="38b1b-138">第一個？</span><span class="sxs-lookup"><span data-stu-id="38b1b-138">The first ?</span></span> <span data-ttu-id="38b1b-139">而且 & 將會自動新增，因此不要將它們包含在前面，但使用 & 來分隔多個查詢字串。</span><span class="sxs-lookup"><span data-stu-id="38b1b-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="38b1b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b1b-140">-DefaultProfile</span></span>
<span data-ttu-id="38b1b-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38b1b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b1b-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="38b1b-142">-DynamicCompression</span></span>
<span data-ttu-id="38b1b-143">啟用快取時是否要針對快取的內容啟用動態壓縮。</span><span class="sxs-lookup"><span data-stu-id="38b1b-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="38b1b-144">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="38b1b-144">Default value is Enabled</span></span>

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

### <span data-ttu-id="38b1b-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="38b1b-145">-EnableCaching</span></span>
<span data-ttu-id="38b1b-146">是否要啟用此路由的快取。</span><span class="sxs-lookup"><span data-stu-id="38b1b-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="38b1b-147">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="38b1b-147">Default value is false</span></span>

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

### <span data-ttu-id="38b1b-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="38b1b-148">-EnabledState</span></span>
<span data-ttu-id="38b1b-149">是否啟用此規則的使用。</span><span class="sxs-lookup"><span data-stu-id="38b1b-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="38b1b-150">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="38b1b-150">Default value is Enabled</span></span>

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

### <span data-ttu-id="38b1b-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="38b1b-151">-ForwardingProtocol</span></span>
<span data-ttu-id="38b1b-152">當您將流量轉寄到 backends 預設值時，此規則將使用的通訊協定 MatchRequest。</span><span class="sxs-lookup"><span data-stu-id="38b1b-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

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

### <span data-ttu-id="38b1b-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="38b1b-153">-FrontDoorName</span></span>
<span data-ttu-id="38b1b-154">此傳送規則所屬之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="38b1b-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="38b1b-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="38b1b-155">-FrontendEndpointName</span></span>
<span data-ttu-id="38b1b-156">與此規則關聯之前端端點的名稱</span><span class="sxs-lookup"><span data-stu-id="38b1b-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="38b1b-157">-名稱</span><span class="sxs-lookup"><span data-stu-id="38b1b-157">-Name</span></span>
<span data-ttu-id="38b1b-158">RoutingRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="38b1b-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="38b1b-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="38b1b-159">-PatternToMatch</span></span>
<span data-ttu-id="38b1b-160">規則的路由模式，除了可能位於路徑最後/結尾的以外，不能有任何 \*。</span><span class="sxs-lookup"><span data-stu-id="38b1b-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="38b1b-161">預設值為/\*</span><span class="sxs-lookup"><span data-stu-id="38b1b-161">Default value is /\*</span></span>

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

### <span data-ttu-id="38b1b-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="38b1b-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="38b1b-163">在形成快取鍵時處理 URL 查詢字詞。</span><span class="sxs-lookup"><span data-stu-id="38b1b-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="38b1b-164">預設值為 StripAll</span><span class="sxs-lookup"><span data-stu-id="38b1b-164">Default value is StripAll</span></span>

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

### <span data-ttu-id="38b1b-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="38b1b-165">-RedirectProtocol</span></span>
<span data-ttu-id="38b1b-166">要將流量重新導向至其中的目的地通訊協定。</span><span class="sxs-lookup"><span data-stu-id="38b1b-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="38b1b-167">預設值為 MatchRequest</span><span class="sxs-lookup"><span data-stu-id="38b1b-167">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="38b1b-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="38b1b-168">-RedirectType</span></span>
<span data-ttu-id="38b1b-169">當您重新導向流量時，規則將使用的重定向類型。</span><span class="sxs-lookup"><span data-stu-id="38b1b-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="38b1b-170">預設值會移動</span><span class="sxs-lookup"><span data-stu-id="38b1b-170">Default Value is Moved</span></span>

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

### <span data-ttu-id="38b1b-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b1b-171">-ResourceGroupName</span></span>
<span data-ttu-id="38b1b-172">將在其中建立 RoutingRule 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="38b1b-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="38b1b-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="38b1b-173">-RulesEngineName</span></span>
<span data-ttu-id="38b1b-174">對特定規則引擎設定的參照，以套用至此路線。</span><span class="sxs-lookup"><span data-stu-id="38b1b-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="38b1b-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b1b-175">CommonParameters</span></span>
<span data-ttu-id="38b1b-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38b1b-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b1b-177">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38b1b-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b1b-178">輸入</span><span class="sxs-lookup"><span data-stu-id="38b1b-178">INPUTS</span></span>

### <span data-ttu-id="38b1b-179">所有</span><span class="sxs-lookup"><span data-stu-id="38b1b-179">None</span></span>

## <span data-ttu-id="38b1b-180">輸出</span><span class="sxs-lookup"><span data-stu-id="38b1b-180">OUTPUTS</span></span>

### <span data-ttu-id="38b1b-181">PSRoutingRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="38b1b-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="38b1b-182">筆記</span><span class="sxs-lookup"><span data-stu-id="38b1b-182">NOTES</span></span>

## <span data-ttu-id="38b1b-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="38b1b-183">RELATED LINKS</span></span>

<span data-ttu-id="38b1b-184">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="38b1b-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>

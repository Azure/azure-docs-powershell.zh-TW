---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 4d13df2e498dd3af0c0a29660673e61233e1d4bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906665"
---
# <span data-ttu-id="90b84-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="90b84-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="90b84-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90b84-102">SYNOPSIS</span></span>
<span data-ttu-id="90b84-103">建立 PSRulesEngineAction 物件以建立規則引擎規則。</span><span class="sxs-lookup"><span data-stu-id="90b84-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="90b84-104">語法</span><span class="sxs-lookup"><span data-stu-id="90b84-104">SYNTAX</span></span>

### <span data-ttu-id="90b84-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="90b84-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90b84-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90b84-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90b84-107">描述</span><span class="sxs-lookup"><span data-stu-id="90b84-107">DESCRIPTION</span></span>
<span data-ttu-id="90b84-108">建立 PSRulesEngineAction 物件以建立規則引擎規則。</span><span class="sxs-lookup"><span data-stu-id="90b84-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="90b84-109">使用 Cmdlet "New-AzFrontDoorHeaderActionObject" 來建立 PSHeaderObjects，以進入參數 "-RequestHeaderActions" 和 "-ResponseHeaderActions"。</span><span class="sxs-lookup"><span data-stu-id="90b84-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="90b84-110">例子</span><span class="sxs-lookup"><span data-stu-id="90b84-110">EXAMPLES</span></span>

### <span data-ttu-id="90b84-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="90b84-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="90b84-112">建立規則引擎動作，並顯示如何查看所建立之規則引擎動作的屬性。</span><span class="sxs-lookup"><span data-stu-id="90b84-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="90b84-113">參數</span><span class="sxs-lookup"><span data-stu-id="90b84-113">PARAMETERS</span></span>

### <span data-ttu-id="90b84-114">-後端多工緩衝處理程式名稱</span><span class="sxs-lookup"><span data-stu-id="90b84-114">-BackendPoolName</span></span>
<span data-ttu-id="90b84-115">此規則路由至的後端多工緩衝處理程式名稱</span><span class="sxs-lookup"><span data-stu-id="90b84-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="90b84-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="90b84-116">-CustomForwardingPath</span></span>
<span data-ttu-id="90b84-117">用來重寫符合此規則之資源路徑的自訂路徑。</span><span class="sxs-lookup"><span data-stu-id="90b84-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="90b84-118">保留空白以使用傳入路徑。</span><span class="sxs-lookup"><span data-stu-id="90b84-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="90b84-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="90b84-119">-CustomFragment</span></span>
<span data-ttu-id="90b84-120">要新加入重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="90b84-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="90b84-121">片段是 #之後 URL 的一部分。</span><span class="sxs-lookup"><span data-stu-id="90b84-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="90b84-122">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="90b84-122">Do not include the #.</span></span>

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

### <span data-ttu-id="90b84-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="90b84-123">-CustomHost</span></span>
<span data-ttu-id="90b84-124">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="90b84-124">Host to redirect.</span></span>
<span data-ttu-id="90b84-125">保留空白，以使用內接主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="90b84-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="90b84-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="90b84-126">-CustomPath</span></span>
<span data-ttu-id="90b84-127">重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="90b84-127">The full path to redirect.</span></span>
<span data-ttu-id="90b84-128">路徑不能是空白的，必須以 /開始。</span><span class="sxs-lookup"><span data-stu-id="90b84-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="90b84-129">保留空白，以使用內入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="90b84-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="90b84-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="90b84-130">-CustomQueryString</span></span>
<span data-ttu-id="90b84-131">這是要放在重新導向 URL 中的查詢字串集。</span><span class="sxs-lookup"><span data-stu-id="90b84-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="90b84-132">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="90b84-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="90b84-133">查詢字串必須採用 \<key\> = \<value\> 格式。</span><span class="sxs-lookup"><span data-stu-id="90b84-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="90b84-134">第一個？</span><span class="sxs-lookup"><span data-stu-id="90b84-134">The first ?</span></span>
<span data-ttu-id="90b84-135">並且&自動新增，因此請不要在最前面加入查詢字串，但請以不同的查詢字串&。</span><span class="sxs-lookup"><span data-stu-id="90b84-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="90b84-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b84-136">-DefaultProfile</span></span>
<span data-ttu-id="90b84-137">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90b84-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90b84-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="90b84-138">-DynamicCompression</span></span>
<span data-ttu-id="90b84-139">是否要針對緩存內容啟用動態壓縮。</span><span class="sxs-lookup"><span data-stu-id="90b84-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="90b84-140">預設值為啟用</span><span class="sxs-lookup"><span data-stu-id="90b84-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="90b84-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="90b84-141">-EnableCaching</span></span>
<span data-ttu-id="90b84-142">是否要啟用此路由的緩存。</span><span class="sxs-lookup"><span data-stu-id="90b84-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="90b84-143">預設值為 False</span><span class="sxs-lookup"><span data-stu-id="90b84-143">Default value is false</span></span>

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

### <span data-ttu-id="90b84-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="90b84-144">-ForwardingProtocol</span></span>
<span data-ttu-id="90b84-145">將流量轉往後端時，此規則會使用通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90b84-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="90b84-146">預設值為 MatchRequest</span><span class="sxs-lookup"><span data-stu-id="90b84-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="90b84-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="90b84-147">-FrontDoorName</span></span>
<span data-ttu-id="90b84-148">此路由規則所屬的前門名稱。</span><span class="sxs-lookup"><span data-stu-id="90b84-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="90b84-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="90b84-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="90b84-150">形成緩存鍵時，URL 查詢字詞的處理方式。</span><span class="sxs-lookup"><span data-stu-id="90b84-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="90b84-151">預設值為 StripAll</span><span class="sxs-lookup"><span data-stu-id="90b84-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="90b84-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="90b84-152">-RedirectProtocol</span></span>
<span data-ttu-id="90b84-153">重新導向流量目的地的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90b84-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="90b84-154">預設值為 MatchRequest</span><span class="sxs-lookup"><span data-stu-id="90b84-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="90b84-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="90b84-155">-RedirectType</span></span>
<span data-ttu-id="90b84-156">重新導向規則會用於重新導向流量的重新導向類型。</span><span class="sxs-lookup"><span data-stu-id="90b84-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="90b84-157">已移動預設值</span><span class="sxs-lookup"><span data-stu-id="90b84-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="90b84-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="90b84-158">-RequestHeaderAction</span></span>
<span data-ttu-id="90b84-159">從 AFD 要求到來源的頁首動作清單。</span><span class="sxs-lookup"><span data-stu-id="90b84-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b84-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b84-160">-ResourceGroupName</span></span>
<span data-ttu-id="90b84-161">要建立 RoutingRule 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="90b84-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="90b84-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="90b84-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="90b84-163">從 AFD 回復到用戶端的頁首動作清單。</span><span class="sxs-lookup"><span data-stu-id="90b84-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b84-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b84-164">CommonParameters</span></span>
<span data-ttu-id="90b84-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90b84-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b84-166">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90b84-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b84-167">輸入</span><span class="sxs-lookup"><span data-stu-id="90b84-167">INPUTS</span></span>

### <span data-ttu-id="90b84-168">沒有</span><span class="sxs-lookup"><span data-stu-id="90b84-168">None</span></span>

## <span data-ttu-id="90b84-169">輸出</span><span class="sxs-lookup"><span data-stu-id="90b84-169">OUTPUTS</span></span>

### <span data-ttu-id="90b84-170">Microsoft.Azure.Commands.FrontDoor.models.PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="90b84-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="90b84-171">筆記</span><span class="sxs-lookup"><span data-stu-id="90b84-171">NOTES</span></span>

## <span data-ttu-id="90b84-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="90b84-172">RELATED LINKS</span></span>

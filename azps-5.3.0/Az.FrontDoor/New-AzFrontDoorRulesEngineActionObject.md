---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435108"
---
# <span data-ttu-id="f0151-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="f0151-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="f0151-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0151-102">SYNOPSIS</span></span>
<span data-ttu-id="f0151-103">建立建立規則引擎規則的 PSRulesEngineAction 物件。</span><span class="sxs-lookup"><span data-stu-id="f0151-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="f0151-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0151-104">SYNTAX</span></span>

### <span data-ttu-id="f0151-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0151-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0151-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0151-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0151-107">說明</span><span class="sxs-lookup"><span data-stu-id="f0151-107">DESCRIPTION</span></span>
<span data-ttu-id="f0151-108">建立建立規則引擎規則的 PSRulesEngineAction 物件。</span><span class="sxs-lookup"><span data-stu-id="f0151-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="f0151-109">使用 Cmdlet "New-AzFrontDoorHeaderActionObject" 建立 PSHeaderObjects，以傳送到參數 "-RequestHeaderActions" 和 "-ResponseHeaderActions"。」</span><span class="sxs-lookup"><span data-stu-id="f0151-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="f0151-110">示例</span><span class="sxs-lookup"><span data-stu-id="f0151-110">EXAMPLES</span></span>

### <span data-ttu-id="f0151-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f0151-111">Example 1</span></span>
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

<span data-ttu-id="f0151-112">建立規則引擎動作，並示範如何查看已建立規則引擎動作的屬性。</span><span class="sxs-lookup"><span data-stu-id="f0151-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="f0151-113">參數</span><span class="sxs-lookup"><span data-stu-id="f0151-113">PARAMETERS</span></span>

### <span data-ttu-id="f0151-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="f0151-114">-BackendPoolName</span></span>
<span data-ttu-id="f0151-115">此規則路由的 BackendPool 名稱</span><span class="sxs-lookup"><span data-stu-id="f0151-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="f0151-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="f0151-116">-CustomForwardingPath</span></span>
<span data-ttu-id="f0151-117">用來重新寫入此規則所符合之資源路徑的自訂路徑。</span><span class="sxs-lookup"><span data-stu-id="f0151-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="f0151-118">若要使用傳入路徑，請保留空白。</span><span class="sxs-lookup"><span data-stu-id="f0151-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="f0151-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="f0151-119">-CustomFragment</span></span>
<span data-ttu-id="f0151-120">要新增至重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="f0151-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="f0151-121">[片段] 是位於 # 之後的 URL 部分。</span><span class="sxs-lookup"><span data-stu-id="f0151-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="f0151-122">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="f0151-122">Do not include the #.</span></span>

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

### <span data-ttu-id="f0151-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="f0151-123">-CustomHost</span></span>
<span data-ttu-id="f0151-124">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="f0151-124">Host to redirect.</span></span>
<span data-ttu-id="f0151-125">[留空] 可將傳入主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="f0151-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="f0151-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="f0151-126">-CustomPath</span></span>
<span data-ttu-id="f0151-127">要重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f0151-127">The full path to redirect.</span></span>
<span data-ttu-id="f0151-128">Path 不能為空白，且必須以/開頭。</span><span class="sxs-lookup"><span data-stu-id="f0151-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="f0151-129">[留空] 可使用傳入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="f0151-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="f0151-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="f0151-130">-CustomQueryString</span></span>
<span data-ttu-id="f0151-131">要放在重新導向 URL 中的一組查詢字串。</span><span class="sxs-lookup"><span data-stu-id="f0151-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="f0151-132">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="f0151-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="f0151-133">查詢字串必須是 \<key\> = \<value\> 格式。</span><span class="sxs-lookup"><span data-stu-id="f0151-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="f0151-134">第一個？</span><span class="sxs-lookup"><span data-stu-id="f0151-134">The first ?</span></span>
<span data-ttu-id="f0151-135">而且 & 將會自動新增，因此不要將它們包含在前面，但使用 & 來分隔多個查詢字串。</span><span class="sxs-lookup"><span data-stu-id="f0151-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="f0151-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0151-136">-DefaultProfile</span></span>
<span data-ttu-id="f0151-137">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0151-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0151-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="f0151-138">-DynamicCompression</span></span>
<span data-ttu-id="f0151-139">是否為快取的內容啟用動態壓縮。</span><span class="sxs-lookup"><span data-stu-id="f0151-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="f0151-140">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="f0151-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="f0151-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="f0151-141">-EnableCaching</span></span>
<span data-ttu-id="f0151-142">是否要啟用此路由的快取。</span><span class="sxs-lookup"><span data-stu-id="f0151-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="f0151-143">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="f0151-143">Default value is false</span></span>

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

### <span data-ttu-id="f0151-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="f0151-144">-ForwardingProtocol</span></span>
<span data-ttu-id="f0151-145">將流量轉寄至 backends 時，此規則將使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f0151-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="f0151-146">預設值為 MatchRequest</span><span class="sxs-lookup"><span data-stu-id="f0151-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="f0151-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="f0151-147">-FrontDoorName</span></span>
<span data-ttu-id="f0151-148">此傳送規則所屬之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0151-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="f0151-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="f0151-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="f0151-150">在形成快取鍵時處理 URL 查詢字詞。</span><span class="sxs-lookup"><span data-stu-id="f0151-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="f0151-151">預設值為 StripAll</span><span class="sxs-lookup"><span data-stu-id="f0151-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="f0151-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="f0151-152">-RedirectProtocol</span></span>
<span data-ttu-id="f0151-153">要將流量重新導向至其中的目的地通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f0151-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="f0151-154">預設值為 MatchRequest</span><span class="sxs-lookup"><span data-stu-id="f0151-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="f0151-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="f0151-155">-RedirectType</span></span>
<span data-ttu-id="f0151-156">當您重新導向流量時，規則將使用的重定向類型。</span><span class="sxs-lookup"><span data-stu-id="f0151-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="f0151-157">預設值會移動</span><span class="sxs-lookup"><span data-stu-id="f0151-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="f0151-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="f0151-158">-RequestHeaderAction</span></span>
<span data-ttu-id="f0151-159">從 AFD 到來源的要求套用的標題動作清單。</span><span class="sxs-lookup"><span data-stu-id="f0151-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

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

### <span data-ttu-id="f0151-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0151-160">-ResourceGroupName</span></span>
<span data-ttu-id="f0151-161">將在其中建立 RoutingRule 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f0151-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="f0151-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="f0151-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="f0151-163">從 AFD 向用戶端回應套用的標頭動作清單。</span><span class="sxs-lookup"><span data-stu-id="f0151-163">A list of header actions to apply from the response from AFD to the client.</span></span>

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

### <span data-ttu-id="f0151-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0151-164">CommonParameters</span></span>
<span data-ttu-id="f0151-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0151-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0151-166">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f0151-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0151-167">輸入</span><span class="sxs-lookup"><span data-stu-id="f0151-167">INPUTS</span></span>

### <span data-ttu-id="f0151-168">所有</span><span class="sxs-lookup"><span data-stu-id="f0151-168">None</span></span>

## <span data-ttu-id="f0151-169">輸出</span><span class="sxs-lookup"><span data-stu-id="f0151-169">OUTPUTS</span></span>

### <span data-ttu-id="f0151-170">PSRulesEngineAction 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="f0151-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="f0151-171">筆記</span><span class="sxs-lookup"><span data-stu-id="f0151-171">NOTES</span></span>

## <span data-ttu-id="f0151-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0151-172">RELATED LINKS</span></span>

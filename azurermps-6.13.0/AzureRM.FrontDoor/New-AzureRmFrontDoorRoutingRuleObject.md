---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451151"
---
# <span data-ttu-id="3fe1a-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="3fe1a-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="3fe1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fe1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe1a-103">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="3fe1a-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fe1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fe1a-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fe1a-105">說明</span><span class="sxs-lookup"><span data-stu-id="3fe1a-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe1a-106">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="3fe1a-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="3fe1a-107">示例</span><span class="sxs-lookup"><span data-stu-id="3fe1a-107">EXAMPLES</span></span>

### <span data-ttu-id="3fe1a-108">範例1：建立 PSRoutingRuleObject 以使用前門建立</span><span class="sxs-lookup"><span data-stu-id="3fe1a-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="3fe1a-109">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="3fe1a-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="3fe1a-110">參數</span><span class="sxs-lookup"><span data-stu-id="3fe1a-110">PARAMETERS</span></span>

### <span data-ttu-id="3fe1a-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="3fe1a-111">-AcceptedProtocol</span></span>
<span data-ttu-id="3fe1a-112">此規則要符合的通訊協定方案。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="3fe1a-113">預設值為 {Https、Http}</span><span class="sxs-lookup"><span data-stu-id="3fe1a-113">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="3fe1a-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="3fe1a-114">-BackendPoolName</span></span>
<span data-ttu-id="3fe1a-115">此規則路由之 BackendPool 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3fe1a-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="3fe1a-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="3fe1a-116">-CustomForwardingPath</span></span>
<span data-ttu-id="3fe1a-117">用來重新寫入此規則所符合之資源路徑的自訂路徑。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="3fe1a-118">若要使用傳入路徑，請保留空白。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="3fe1a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe1a-119">-DefaultProfile</span></span>
<span data-ttu-id="3fe1a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe1a-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="3fe1a-121">-DynamicCompression</span></span>
<span data-ttu-id="3fe1a-122">啟用快取時是否要針對快取的內容啟用動態壓縮。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="3fe1a-123">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="3fe1a-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="3fe1a-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="3fe1a-124">-EnableCaching</span></span>
<span data-ttu-id="3fe1a-125">是否要啟用此路由的快取。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="3fe1a-126">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="3fe1a-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe1a-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="3fe1a-127">-EnabledState</span></span>
<span data-ttu-id="3fe1a-128">是否啟用此規則的使用。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="3fe1a-129">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="3fe1a-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="3fe1a-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="3fe1a-130">-ForwardingProtocol</span></span>
<span data-ttu-id="3fe1a-131">當您將流量轉寄到 backends 預設值時，此規則將使用的通訊協定 MatchRequest。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe1a-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3fe1a-132">-FrontDoorName</span></span>
<span data-ttu-id="3fe1a-133">此傳送規則所屬之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="3fe1a-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="3fe1a-134">-FrontendEndpointName</span></span>
<span data-ttu-id="3fe1a-135">與此規則關聯之前端端點的名稱</span><span class="sxs-lookup"><span data-stu-id="3fe1a-135">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="3fe1a-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fe1a-136">-Name</span></span>
<span data-ttu-id="3fe1a-137">RoutingRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="3fe1a-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="3fe1a-138">-PatternToMatch</span></span>
<span data-ttu-id="3fe1a-139">規則的路由模式，除了可能位於路徑最後/結尾的以外，不能有任何 \*。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="3fe1a-140">預設值為/\*</span><span class="sxs-lookup"><span data-stu-id="3fe1a-140">Default value is /\*</span></span>

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

### <span data-ttu-id="3fe1a-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="3fe1a-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="3fe1a-142">在形成快取鍵時處理 URL 查詢字詞。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="3fe1a-143">預設值為 StripAll</span><span class="sxs-lookup"><span data-stu-id="3fe1a-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe1a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe1a-144">-ResourceGroupName</span></span>
<span data-ttu-id="3fe1a-145">將在其中建立 RoutingRule 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="3fe1a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe1a-146">CommonParameters</span></span>
<span data-ttu-id="3fe1a-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe1a-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe1a-149">輸入</span><span class="sxs-lookup"><span data-stu-id="3fe1a-149">INPUTS</span></span>

### <span data-ttu-id="3fe1a-150">所有</span><span class="sxs-lookup"><span data-stu-id="3fe1a-150">None</span></span>

## <span data-ttu-id="3fe1a-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3fe1a-151">OUTPUTS</span></span>

### <span data-ttu-id="3fe1a-152">PSRoutingRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="3fe1a-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="3fe1a-153">筆記</span><span class="sxs-lookup"><span data-stu-id="3fe1a-153">NOTES</span></span>

## <span data-ttu-id="3fe1a-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fe1a-154">RELATED LINKS</span></span>

<span data-ttu-id="3fe1a-155">[新-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="3fe1a-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>

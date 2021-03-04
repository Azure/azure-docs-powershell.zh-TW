---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b343ecbabd66f32be30f4aff1b0a44c7ddf186d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910438"
---
# <span data-ttu-id="31f7f-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31f7f-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="31f7f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="31f7f-103">建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="31f7f-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="31f7f-104">語法</span><span class="sxs-lookup"><span data-stu-id="31f7f-104">SYNTAX</span></span>

### <span data-ttu-id="31f7f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="31f7f-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f7f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="31f7f-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f7f-107">描述</span><span class="sxs-lookup"><span data-stu-id="31f7f-107">DESCRIPTION</span></span>
<span data-ttu-id="31f7f-108">**New-AzApplicationGatewayPathRuleConfig** Cmdlet 會建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="31f7f-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="31f7f-109">此 Cmdlet 所建立的規則可以新增到 URL 路徑地圖設定設定集合，然後指派給閘道。</span><span class="sxs-lookup"><span data-stu-id="31f7f-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="31f7f-110">路徑圖設定設定用於應用程式閘道負載平衡。</span><span class="sxs-lookup"><span data-stu-id="31f7f-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="31f7f-111">例子</span><span class="sxs-lookup"><span data-stu-id="31f7f-111">EXAMPLES</span></span>

### <span data-ttu-id="31f7f-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="31f7f-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="31f7f-113">這些命令會建立新的應用程式閘道路徑規則，然後使用 **Add-AzApplicationGatewayUrlPathMapConfig** Cmdlet 將規則指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="31f7f-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="31f7f-114">若要這麼做，第一個命令會建立閘道 ContosoApplicationGateway 的物件參照。</span><span class="sxs-lookup"><span data-stu-id="31f7f-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="31f7f-115">此物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="31f7f-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="31f7f-116">接下來兩個命令會建立後端位址集區及後端 HTTP 設定物件;這些物件 (儲存在$AddressPool和$HttpSettings) ，才能建立路徑規則物件。</span><span class="sxs-lookup"><span data-stu-id="31f7f-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="31f7f-117">第四個命令會建立路徑規則物件，並儲存在名為 $PathRuleConfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="31f7f-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="31f7f-118">第五個命令使用 **Add-AzApplicationGatewayUrlPathMapConfig，** 將設定設定和這些設定中包含的新路徑規則新增到 ContosoApplicationGateway。</span><span class="sxs-lookup"><span data-stu-id="31f7f-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="31f7f-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="31f7f-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="31f7f-120">這些命令會建立路徑規則，名稱為"base"、Path as "/base"、後端AddressPool as $AddressPool、後端HttpSettings as $HttpSettings 和 FirewallPolicy as $firewallPolicy.ngs，以及這些設定中包含的新路徑規則至 ContosoApplicationGateway。</span><span class="sxs-lookup"><span data-stu-id="31f7f-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="31f7f-121">參數</span><span class="sxs-lookup"><span data-stu-id="31f7f-121">PARAMETERS</span></span>

### <span data-ttu-id="31f7f-122">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="31f7f-122">-BackendAddressPool</span></span>
<span data-ttu-id="31f7f-123">指定要新增到閘道路徑規則設定設定之後端位址集區設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="31f7f-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="31f7f-124">您可以使用類似以下的 Cmdlet New-AzApplicationGatewayBackendAddressPool建立此物件參照： `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="31f7f-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="31f7f-125">上述命令會將兩個 IP 位址 (192.16.1.1 和 192.168.1.2) 到位址區段。</span><span class="sxs-lookup"><span data-stu-id="31f7f-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="31f7f-126">請注意，IP 位址會以引號括住，並且使用逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="31f7f-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="31f7f-127">結果變數 $AddressPool，然後可以用來做為 *DefaultBackendAddressPool* 參數的參數值。</span><span class="sxs-lookup"><span data-stu-id="31f7f-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="31f7f-128">後端位址資料庫代表後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="31f7f-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="31f7f-129">這些 IP 位址應屬於虛擬網路子網，或應為公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="31f7f-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="31f7f-130">如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendAddressPoolId* 參數。</span><span class="sxs-lookup"><span data-stu-id="31f7f-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-131">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="31f7f-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="31f7f-132">指定可以新加入閘道路徑規則設定設定的現有後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="31f7f-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="31f7f-133">您可以使用 Cmdlet 來Get-AzApplicationGatewayBackendAddressPool位址。</span><span class="sxs-lookup"><span data-stu-id="31f7f-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="31f7f-134">在您擁有識別碼之後，就可以使用 *DefaultBackendAddressPoolId* 參數，而不是 *DefaultBackendAddressPool* 參數。</span><span class="sxs-lookup"><span data-stu-id="31f7f-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="31f7f-135">例如：-DefaultBackendAddressPoolId"/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10 /resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/後端AddressPools/ContosoAddressPool" 後端位址資料庫代表後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="31f7f-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="31f7f-136">這些 IP 位址應屬於虛擬網路子網，或應為公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="31f7f-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-137">-後端HttpSettings</span><span class="sxs-lookup"><span data-stu-id="31f7f-137">-BackendHttpSettings</span></span>
<span data-ttu-id="31f7f-138">指定要新加入閘道路徑規則設定設定之後端 HTTP 設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="31f7f-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="31f7f-139">您可以使用類似以下的 New-AzApplicationGatewayBackendHttpSettings Cmdlet 和語法來建立此物件參照：$HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "HTTP" -CookieBasedAffinity "Disabled" 產生的變數， $HttpSettings，然後可以用來做為 *DefaultBackendAddressPool* 參數的參數值：-DefaultBackendHttpSettings $HttpSettings 後端 HTTP 設定會為後端資料庫設定埠、通訊協定和 Cookie 型關聯等屬性。</span><span class="sxs-lookup"><span data-stu-id="31f7f-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="31f7f-140">如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendHttpSettingsId* 參數。</span><span class="sxs-lookup"><span data-stu-id="31f7f-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-141">-後端HttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="31f7f-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="31f7f-142">指定可以新加入閘道路徑規則設定設定的現有後端 HTTP 設定集合識別碼。</span><span class="sxs-lookup"><span data-stu-id="31f7f-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="31f7f-143">HTTP 設定 ID 可以使用 Cmdlet Get-AzApplicationGatewayBackendHttpSettings回。</span><span class="sxs-lookup"><span data-stu-id="31f7f-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="31f7f-144">在您擁有識別碼之後，就可以使用 *DefaultBackendHttpSettingsId* 參數，而不是 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="31f7f-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="31f7f-145">例如：-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/後端HttpSettingsCollection/ContosoHttpSettings" 後端 HTTP 設定設定屬性，例如埠， 協定，以及後端資料庫的 Cookie 型關聯。</span><span class="sxs-lookup"><span data-stu-id="31f7f-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="31f7f-146">如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="31f7f-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="31f7f-147">-FirewallPolicy</span></span>
<span data-ttu-id="31f7f-148">指定頂層防火牆政策的物件參照。</span><span class="sxs-lookup"><span data-stu-id="31f7f-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="31f7f-149">您可以使用 Cmdlet 建立New-AzApplicationGatewayWebApplicationFirewallPolicy參照。</span><span class="sxs-lookup"><span data-stu-id="31f7f-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="31f7f-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" 使用上述命令建立防火牆原則，可以在路徑規則層級中參考。</span><span class="sxs-lookup"><span data-stu-id="31f7f-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="31f7f-151">上方命令會建立預設原則設定和受管理規則。</span><span class="sxs-lookup"><span data-stu-id="31f7f-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="31f7f-152">使用者可以指定 PolicySettings、ManagedRules，而不使用預設值，New-AzApplicationGatewayFirewallPolicySettings和New-AzApplicationGatewayFirewallPolicyManagedRules設定。</span><span class="sxs-lookup"><span data-stu-id="31f7f-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="31f7f-153">-FirewallPolicyId</span></span>
<span data-ttu-id="31f7f-154">指定現有頂層 Web 應用程式防火牆資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="31f7f-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="31f7f-155">防火牆策略的 ID 可以使用 Get-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31f7f-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="31f7f-156">當我們有識別碼之後，您可以使用 *FirewallPolicyId* 參數，而不是 *FirewallPolicy* 參數。</span><span class="sxs-lookup"><span data-stu-id="31f7f-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="31f7f-157">例如：-FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="31f7f-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f7f-158">-DefaultProfile</span></span>
<span data-ttu-id="31f7f-159">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31f7f-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31f7f-160">-名稱</span><span class="sxs-lookup"><span data-stu-id="31f7f-160">-Name</span></span>
<span data-ttu-id="31f7f-161">指定此 Cmdlet 所建立的路徑規則組組名稱。</span><span class="sxs-lookup"><span data-stu-id="31f7f-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="31f7f-162">-路徑</span><span class="sxs-lookup"><span data-stu-id="31f7f-162">-Paths</span></span>
<span data-ttu-id="31f7f-163">指定一或多個應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="31f7f-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="31f7f-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="31f7f-164">-RedirectConfiguration</span></span>
<span data-ttu-id="31f7f-165">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="31f7f-165">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="31f7f-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="31f7f-167">應用程式閘道 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="31f7f-167">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31f7f-168">-RewriteRuleSet</span></span>
<span data-ttu-id="31f7f-169">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31f7f-169">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="31f7f-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="31f7f-171">應用程式閘道 RewriteRuleSet 的識別碼</span><span class="sxs-lookup"><span data-stu-id="31f7f-171">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7f-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f7f-172">CommonParameters</span></span>
<span data-ttu-id="31f7f-173">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31f7f-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f7f-174">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="31f7f-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f7f-175">輸入</span><span class="sxs-lookup"><span data-stu-id="31f7f-175">INPUTS</span></span>

### <span data-ttu-id="31f7f-176">沒有</span><span class="sxs-lookup"><span data-stu-id="31f7f-176">None</span></span>

## <span data-ttu-id="31f7f-177">輸出</span><span class="sxs-lookup"><span data-stu-id="31f7f-177">OUTPUTS</span></span>

### <span data-ttu-id="31f7f-178">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="31f7f-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="31f7f-179">筆記</span><span class="sxs-lookup"><span data-stu-id="31f7f-179">NOTES</span></span>

## <span data-ttu-id="31f7f-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="31f7f-180">RELATED LINKS</span></span>

[<span data-ttu-id="31f7f-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="31f7f-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="31f7f-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31f7f-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="31f7f-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="31f7f-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="31f7f-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="31f7f-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="31f7f-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="31f7f-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="31f7f-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31f7f-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="31f7f-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="31f7f-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="31f7f-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="31f7f-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="31f7f-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="31f7f-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)



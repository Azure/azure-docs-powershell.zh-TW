---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141120"
---
# <span data-ttu-id="e46e0-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e46e0-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="e46e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e46e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e46e0-103">建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="e46e0-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="e46e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="e46e0-104">SYNTAX</span></span>

### <span data-ttu-id="e46e0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e46e0-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e46e0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e46e0-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e46e0-107">說明</span><span class="sxs-lookup"><span data-stu-id="e46e0-107">DESCRIPTION</span></span>
<span data-ttu-id="e46e0-108">**新的-AzApplicationGatewayPathRuleConfig** Cmdlet 會建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="e46e0-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="e46e0-109">您可以將由此 Cmdlet 建立的規則新增至 URL 路徑對應設定的集合，然後指派給閘道。</span><span class="sxs-lookup"><span data-stu-id="e46e0-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="e46e0-110">路徑對應設定是在應用程式閘道負載平衡中使用。</span><span class="sxs-lookup"><span data-stu-id="e46e0-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="e46e0-111">示例</span><span class="sxs-lookup"><span data-stu-id="e46e0-111">EXAMPLES</span></span>

### <span data-ttu-id="e46e0-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e46e0-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="e46e0-113">這些命令會建立新的應用程式閘道路徑規則，然後使用 **AzApplicationGatewayUrlPathMapConfig** Cmdlet 將該規則指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e46e0-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="e46e0-114">若要這樣做，第一個命令會建立對閘道 ContosoApplicationGateway 的物件參照。</span><span class="sxs-lookup"><span data-stu-id="e46e0-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="e46e0-115">這個物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e46e0-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="e46e0-116">接下來的兩個命令會建立後端位址集區和後端 HTTP 設定物件;這些物件 (儲存在 $AddressPool 變數中，而且需要 $HttpSettings) ，才能建立路徑規則物件。</span><span class="sxs-lookup"><span data-stu-id="e46e0-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="e46e0-117">第四個命令會建立路徑規則物件，並儲存在名為 $PathRuleConfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e46e0-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="e46e0-118">第五個命令使用 [ **載入 AzApplicationGatewayUrlPathMapConfig** ]，將配置設定和包含在這些設定中的新路徑規則新增到 ContosoApplicationGateway。</span><span class="sxs-lookup"><span data-stu-id="e46e0-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="e46e0-119">範例2</span><span class="sxs-lookup"><span data-stu-id="e46e0-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="e46e0-120">這些命令會建立名稱為 "base"、路徑為 "/base"、BackendAddressPool 為 $AddressPool 的路徑規則，BackendHttpSettings $HttpSettings 為 [ngs] 和 [$firewallPolicy FirewallPolicy]，將這些設定中所包含的新路徑規則加入 ContosoApplicationGateway。</span><span class="sxs-lookup"><span data-stu-id="e46e0-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="e46e0-121">參數</span><span class="sxs-lookup"><span data-stu-id="e46e0-121">PARAMETERS</span></span>

### <span data-ttu-id="e46e0-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e46e0-122">-BackendAddressPool</span></span>
<span data-ttu-id="e46e0-123">指定要新增至 [閘道路徑規則設定] 的後端位址集區設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="e46e0-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="e46e0-124">您可以使用 New-AzApplicationGatewayBackendAddressPool Cmdlet 及如下所示的語法來建立此物件參照： `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="e46e0-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="e46e0-125">上述命令會將兩個 IP 位址 (192.16.1.1 和 192.168.1.2) 新增到位址集區中。</span><span class="sxs-lookup"><span data-stu-id="e46e0-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="e46e0-126">請注意，IP 位址括在引號中，並以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="e46e0-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="e46e0-127">產生的變數 $AddressPool，就可以用來做為 *DefaultBackendAddressPool* 參數的參數值。</span><span class="sxs-lookup"><span data-stu-id="e46e0-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="e46e0-128">後端位址集區代表後端伺服器上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e46e0-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="e46e0-129">這些 IP 位址應該是屬於虛擬網路子網，或是公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e46e0-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="e46e0-130">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendAddressPoolId* 參數。</span><span class="sxs-lookup"><span data-stu-id="e46e0-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="e46e0-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e46e0-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="e46e0-132">指定可新增至 [閘道路徑規則設定] 的現有後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="e46e0-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="e46e0-133">您可以使用 Get-AzApplicationGatewayBackendAddressPool Cmdlet 傳回位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="e46e0-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="e46e0-134">在您擁有 ID 之後，您就可以使用 *DefaultBackendAddressPoolId* 參數，而不是 *DefaultBackendAddressPool* 參數。</span><span class="sxs-lookup"><span data-stu-id="e46e0-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="e46e0-135">例如：-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 後端位址集區代表後端伺服器上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e46e0-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="e46e0-136">這些 IP 位址應該是屬於虛擬網路子網，或是公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e46e0-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="e46e0-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e46e0-137">-BackendHttpSettings</span></span>
<span data-ttu-id="e46e0-138">指定要新增至 [閘道路徑規則設定] 的後端 HTTP 設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="e46e0-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="e46e0-139">您可以使用 New-AzApplicationGatewayBackendHttpSettings Cmdlet 及如下所示的語法來建立此物件參照： $HttpSettings = New-AzApplicationGatewayBackendHttpSettings 名稱 "ContosoHttpSettings"-Port 80-通訊協定 "Http"-CookieBasedAffinity "Disabled" 所產生的變數（$HttpSettings）隨後可用作 *DefaultBackendAddressPool* 參數的參數值：-DefaultBackendHttpSettings $HttpSettings 後端 Http 設定會針對後端池設定屬性，例如埠、通訊協定和 cookie 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="e46e0-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="e46e0-140">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendHttpSettingsId* 參數。</span><span class="sxs-lookup"><span data-stu-id="e46e0-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="e46e0-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e46e0-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e46e0-142">指定現有後端 HTTP 設定集合的識別碼，該集合可以新增至 [閘道路徑規則] 設定設定。</span><span class="sxs-lookup"><span data-stu-id="e46e0-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="e46e0-143">您可以使用 Get-AzApplicationGatewayBackendHttpSettings Cmdlet 傳回 HTTP 設定 Id。</span><span class="sxs-lookup"><span data-stu-id="e46e0-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="e46e0-144">在您擁有 ID 之後，您就可以使用 *DefaultBackendHttpSettingsId* 參數，而不是 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="e46e0-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="e46e0-145">例如：-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 後端 HTTP 設定會為後端池設定屬性，例如埠、通訊協定及 cookie 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="e46e0-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="e46e0-146">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="e46e0-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="e46e0-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e46e0-147">-FirewallPolicy</span></span>
<span data-ttu-id="e46e0-148">指定對頂層防火牆原則的物件參考。</span><span class="sxs-lookup"><span data-stu-id="e46e0-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="e46e0-149">您可以使用 New-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet 來建立物件參考。</span><span class="sxs-lookup"><span data-stu-id="e46e0-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="e46e0-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy 名稱 "wafPolicy1"-ResourceGroup "rgName" 使用上述的 commandlet 建立的防火牆原則，可以在 path 規則層級引用。</span><span class="sxs-lookup"><span data-stu-id="e46e0-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="e46e0-151">上述命令會建立預設的原則設定和受管理的規則。</span><span class="sxs-lookup"><span data-stu-id="e46e0-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="e46e0-152">使用者可以使用 New-AzApplicationGatewayFirewallPolicySettings 和 New-AzApplicationGatewayFirewallPolicyManagedRules 分別指定 PolicySettings、ManagedRules，而不是預設值。</span><span class="sxs-lookup"><span data-stu-id="e46e0-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46e0-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e46e0-153">-FirewallPolicyId</span></span>
<span data-ttu-id="e46e0-154">指定現有最上層 web 應用程式防火牆資源的 ID。</span><span class="sxs-lookup"><span data-stu-id="e46e0-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="e46e0-155">您可以使用 Get-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet 傳回防火牆原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="e46e0-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="e46e0-156">我們擁有 ID 之後，您可以使用 *FirewallPolicyId* 參數，而不是 *FirewallPolicy* 參數。</span><span class="sxs-lookup"><span data-stu-id="e46e0-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="e46e0-157">例如：-FirewallPolicyId "/subscriptions/<訂閱識別碼>/resourceGroups/<資源群組-識別碼>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="e46e0-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46e0-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46e0-158">-DefaultProfile</span></span>
<span data-ttu-id="e46e0-159">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e46e0-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e46e0-160">-名稱</span><span class="sxs-lookup"><span data-stu-id="e46e0-160">-Name</span></span>
<span data-ttu-id="e46e0-161">指定此 Cmdlet 所建立之路徑規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e46e0-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e46e0-162">-路徑</span><span class="sxs-lookup"><span data-stu-id="e46e0-162">-Paths</span></span>
<span data-ttu-id="e46e0-163">指定一個或多個應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="e46e0-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="e46e0-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e46e0-164">-RedirectConfiguration</span></span>
<span data-ttu-id="e46e0-165">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e46e0-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e46e0-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e46e0-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="e46e0-167">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="e46e0-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e46e0-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e46e0-168">-RewriteRuleSet</span></span>
<span data-ttu-id="e46e0-169">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e46e0-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e46e0-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="e46e0-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="e46e0-171">應用程式閘道 RewriteRuleSet 的 ID</span><span class="sxs-lookup"><span data-stu-id="e46e0-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e46e0-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46e0-172">CommonParameters</span></span>
<span data-ttu-id="e46e0-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e46e0-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46e0-174">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e46e0-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46e0-175">輸入</span><span class="sxs-lookup"><span data-stu-id="e46e0-175">INPUTS</span></span>

### <span data-ttu-id="e46e0-176">所有</span><span class="sxs-lookup"><span data-stu-id="e46e0-176">None</span></span>

## <span data-ttu-id="e46e0-177">輸出</span><span class="sxs-lookup"><span data-stu-id="e46e0-177">OUTPUTS</span></span>

### <span data-ttu-id="e46e0-178">PSApplicationGatewayPathRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e46e0-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="e46e0-179">筆記</span><span class="sxs-lookup"><span data-stu-id="e46e0-179">NOTES</span></span>

## <span data-ttu-id="e46e0-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="e46e0-180">RELATED LINKS</span></span>

[<span data-ttu-id="e46e0-181">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e46e0-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e46e0-182">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e46e0-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="e46e0-183">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e46e0-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e46e0-184">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e46e0-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e46e0-185">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e46e0-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e46e0-186">新-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e46e0-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="e46e0-187">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e46e0-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e46e0-188">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e46e0-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e46e0-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e46e0-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


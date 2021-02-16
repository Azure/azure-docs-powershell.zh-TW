---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 94fbc1e9a4ae8b7befe6961a9648174770458583
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400207"
---
# <span data-ttu-id="056e5-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="056e5-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="056e5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="056e5-102">SYNOPSIS</span></span>
<span data-ttu-id="056e5-103">建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="056e5-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="056e5-104">語法</span><span class="sxs-lookup"><span data-stu-id="056e5-104">SYNTAX</span></span>

### <span data-ttu-id="056e5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="056e5-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="056e5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="056e5-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="056e5-107">描述</span><span class="sxs-lookup"><span data-stu-id="056e5-107">DESCRIPTION</span></span>
<span data-ttu-id="056e5-108">**New-AzApplicationGatewayPathRuleConfig** Cmdlet 會建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="056e5-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="056e5-109">此 Cmdlet 所建立的規則可以新增到 URL 路徑地圖設定設定集合，然後指派給閘道。</span><span class="sxs-lookup"><span data-stu-id="056e5-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="056e5-110">路徑圖設定設定用於應用程式閘道負載平衡。</span><span class="sxs-lookup"><span data-stu-id="056e5-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="056e5-111">例子</span><span class="sxs-lookup"><span data-stu-id="056e5-111">EXAMPLES</span></span>

### <span data-ttu-id="056e5-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="056e5-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="056e5-113">這些命令會建立新的應用程式閘道路徑規則，然後使用 **Add-AzApplicationGatewayUrlPathMapConfig** Cmdlet 將規則指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="056e5-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="056e5-114">若要這麼做，第一個命令會建立閘道 ContosoApplicationGateway 的物件參照。</span><span class="sxs-lookup"><span data-stu-id="056e5-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="056e5-115">此物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="056e5-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="056e5-116">接下來兩個命令會建立後端位址集區及後端 HTTP 設定物件;這些物件 (儲存在$AddressPool$HttpSettings) ，才能建立路徑規則物件。</span><span class="sxs-lookup"><span data-stu-id="056e5-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="056e5-117">第四個命令會建立路徑規則物件，並儲存在名為 $PathRuleConfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="056e5-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="056e5-118">第五個命令使用 **Add-AzApplicationGatewayUrlPathMapConfig，在 ContosoApplicationGateway** 中新增設定設定和這些設定中包含的新路徑規則。</span><span class="sxs-lookup"><span data-stu-id="056e5-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="056e5-119">參數</span><span class="sxs-lookup"><span data-stu-id="056e5-119">PARAMETERS</span></span>

### <span data-ttu-id="056e5-120">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="056e5-120">-BackendAddressPool</span></span>
<span data-ttu-id="056e5-121">指定要新增到閘道路徑規則設定設定之後端位址集區設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="056e5-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="056e5-122">您可以使用類似以下的 Cmdlet New-AzApplicationGatewayBackendAddressPool建立此物件參照： `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="056e5-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="056e5-123">上述命令會將兩個 IP 位址 (192.16.1.1 和 192.168.1.2) 到位址區段。</span><span class="sxs-lookup"><span data-stu-id="056e5-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="056e5-124">請注意，IP 位址會以引號括住，並且使用逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="056e5-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="056e5-125">結果變數 $AddressPool，然後可以用來做為 *DefaultBackendAddressPool* 參數的參數值。</span><span class="sxs-lookup"><span data-stu-id="056e5-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="056e5-126">後端位址資料庫代表後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="056e5-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="056e5-127">這些 IP 位址應屬於虛擬網路子網，或應為公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="056e5-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="056e5-128">如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendAddressPoolId* 參數。</span><span class="sxs-lookup"><span data-stu-id="056e5-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="056e5-129">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="056e5-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="056e5-130">指定可以新加入閘道路徑規則設定設定的現有後端位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="056e5-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="056e5-131">您可以使用 Cmdlet 來Get-AzApplicationGatewayBackendAddressPool位址。</span><span class="sxs-lookup"><span data-stu-id="056e5-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="056e5-132">在您擁有識別碼之後，就可以使用 *DefaultBackendAddressPoolId* 參數，而不是 *DefaultBackendAddressPool* 參數。</span><span class="sxs-lookup"><span data-stu-id="056e5-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="056e5-133">例如：-DefaultBackendAddressPoolId"/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10 /resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/後端AddressPools/ContosoAddressPool" 後端位址資料庫代表後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="056e5-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="056e5-134">這些 IP 位址應屬於虛擬網路子網，或應為公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="056e5-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="056e5-135">-後端HttpSettings</span><span class="sxs-lookup"><span data-stu-id="056e5-135">-BackendHttpSettings</span></span>
<span data-ttu-id="056e5-136">指定要新增到閘道路徑規則設定設定之後端 HTTP 設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="056e5-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="056e5-137">您可以使用 New-AzApplicationGatewayBackendHttpSettings Cmdlet 和類似以下的語法來建立此物件參照：$HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "HTTP" -CookieBasedAffinity "Disabled" 產生的變數， $HttpSettings，然後可以用來做為 *DefaultBackendAddressPool* 參數的參數值：-DefaultBackendHttpSettings $HttpSettings 後端 HTTP 設定會為後端資料庫設定埠、通訊協定和 Cookie 型關聯等屬性。</span><span class="sxs-lookup"><span data-stu-id="056e5-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="056e5-138">如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendHttpSettingsId* 參數。</span><span class="sxs-lookup"><span data-stu-id="056e5-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="056e5-139">-後端HttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="056e5-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="056e5-140">指定可以新加入閘道路徑規則設定設定的現有後端 HTTP 設定集合識別碼。</span><span class="sxs-lookup"><span data-stu-id="056e5-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="056e5-141">HTTP 設定 ID 可以使用 Cmdlet Get-AzApplicationGatewayBackendHttpSettings回。</span><span class="sxs-lookup"><span data-stu-id="056e5-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="056e5-142">在您擁有識別碼之後，就可以使用 *DefaultBackendHttpSettingsId* 參數，而不是 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="056e5-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="056e5-143">例如：-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/後端HttpSettingsCollection/ContosoHttpSettings" 後端 HTTP 設定設定屬性，例如埠， 協定，以及後端資料庫的 Cookie 型關聯。</span><span class="sxs-lookup"><span data-stu-id="056e5-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="056e5-144">如果您使用此參數，就無法在同一個命令中使用 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="056e5-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="056e5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="056e5-145">-DefaultProfile</span></span>
<span data-ttu-id="056e5-146">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="056e5-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="056e5-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="056e5-147">-Name</span></span>
<span data-ttu-id="056e5-148">指定此 Cmdlet 建立的路徑規則組組名稱。</span><span class="sxs-lookup"><span data-stu-id="056e5-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="056e5-149">-路徑</span><span class="sxs-lookup"><span data-stu-id="056e5-149">-Paths</span></span>
<span data-ttu-id="056e5-150">指定一或多個應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="056e5-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="056e5-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="056e5-151">-RedirectConfiguration</span></span>
<span data-ttu-id="056e5-152">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="056e5-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="056e5-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="056e5-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="056e5-154">應用程式閘道 RedirectConfiguration 的識別碼</span><span class="sxs-lookup"><span data-stu-id="056e5-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="056e5-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="056e5-155">-RewriteRuleSet</span></span>
<span data-ttu-id="056e5-156">應用程式閘道 RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="056e5-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="056e5-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="056e5-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="056e5-158">應用程式閘道 RewriteRuleSet 的識別碼</span><span class="sxs-lookup"><span data-stu-id="056e5-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="056e5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="056e5-159">CommonParameters</span></span>
<span data-ttu-id="056e5-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="056e5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="056e5-161">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="056e5-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="056e5-162">輸入</span><span class="sxs-lookup"><span data-stu-id="056e5-162">INPUTS</span></span>

### <span data-ttu-id="056e5-163">沒有</span><span class="sxs-lookup"><span data-stu-id="056e5-163">None</span></span>

## <span data-ttu-id="056e5-164">輸出</span><span class="sxs-lookup"><span data-stu-id="056e5-164">OUTPUTS</span></span>

### <span data-ttu-id="056e5-165">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="056e5-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="056e5-166">筆記</span><span class="sxs-lookup"><span data-stu-id="056e5-166">NOTES</span></span>

## <span data-ttu-id="056e5-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="056e5-167">RELATED LINKS</span></span>

[<span data-ttu-id="056e5-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="056e5-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="056e5-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="056e5-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="056e5-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="056e5-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="056e5-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="056e5-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="056e5-172">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="056e5-172">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="056e5-173">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="056e5-173">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="056e5-174">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="056e5-174">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="056e5-175">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="056e5-175">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)



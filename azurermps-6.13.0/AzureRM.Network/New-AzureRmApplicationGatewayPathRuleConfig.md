---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: f8d9a4266474f18a2dd20fd4ddc0746320359f59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451856"
---
# <span data-ttu-id="04be0-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04be0-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="04be0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04be0-102">SYNOPSIS</span></span>
<span data-ttu-id="04be0-103">建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="04be0-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04be0-104">句法</span><span class="sxs-lookup"><span data-stu-id="04be0-104">SYNTAX</span></span>

### <span data-ttu-id="04be0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="04be0-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04be0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="04be0-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04be0-107">說明</span><span class="sxs-lookup"><span data-stu-id="04be0-107">DESCRIPTION</span></span>
<span data-ttu-id="04be0-108">**新的-AzureRmApplicationGatewayPathRuleConfig** Cmdlet 會建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="04be0-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="04be0-109">您可以將由此 Cmdlet 建立的規則新增至 URL 路徑對應設定的集合，然後指派給閘道。</span><span class="sxs-lookup"><span data-stu-id="04be0-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="04be0-110">路徑對應設定是在應用程式閘道負載平衡中使用。</span><span class="sxs-lookup"><span data-stu-id="04be0-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="04be0-111">示例</span><span class="sxs-lookup"><span data-stu-id="04be0-111">EXAMPLES</span></span>

### <span data-ttu-id="04be0-112">範例1</span><span class="sxs-lookup"><span data-stu-id="04be0-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="04be0-113">這些命令會建立新的應用程式閘道路徑規則，然後使用 **AzureRmApplicationGatewayUrlPathMapConfig** Cmdlet 將該規則指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="04be0-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="04be0-114">若要這樣做，第一個命令會建立對閘道 ContosoApplicationGateway 的物件參照。</span><span class="sxs-lookup"><span data-stu-id="04be0-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="04be0-115">這個物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="04be0-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="04be0-116">接下來的兩個命令會建立後端位址集區和後端 HTTP 設定物件;這些物件 (儲存在 $AddressPool 變數中，而且需要 $HttpSettings) ，才能建立路徑規則物件。</span><span class="sxs-lookup"><span data-stu-id="04be0-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="04be0-117">第四個命令會建立路徑規則物件，並儲存在名為 $PathRuleConfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="04be0-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="04be0-118">第五個命令使用 [ **載入 AzureRmApplicationGatewayUrlPathMapConfig** ]，將配置設定和包含在這些設定中的新路徑規則新增到 ContosoApplicationGateway。</span><span class="sxs-lookup"><span data-stu-id="04be0-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="04be0-119">參數</span><span class="sxs-lookup"><span data-stu-id="04be0-119">PARAMETERS</span></span>

### <span data-ttu-id="04be0-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="04be0-120">-BackendAddressPool</span></span>
<span data-ttu-id="04be0-121">指定要新增至 [閘道路徑規則設定] 的後端位址集區設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="04be0-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="04be0-122">您可以使用 New-AzureRmApplicationGatewayBackendAddressPool Cmdlet 及如下所示的語法來建立此物件參照： `$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="04be0-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="04be0-123">上述命令會將兩個 IP 位址 (192.16.1.1 和 192.168.1.2) 新增到位址集區中。</span><span class="sxs-lookup"><span data-stu-id="04be0-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="04be0-124">請注意，IP 位址括在引號中，並以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="04be0-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="04be0-125">產生的變數 $AddressPool，就可以用來做為 *DefaultBackendAddressPool* 參數的參數值。</span><span class="sxs-lookup"><span data-stu-id="04be0-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="04be0-126">後端位址集區代表後端伺服器上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="04be0-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="04be0-127">這些 IP 位址應該是屬於虛擬網路子網，或是公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="04be0-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="04be0-128">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendAddressPoolId* 參數。</span><span class="sxs-lookup"><span data-stu-id="04be0-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="04be0-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="04be0-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="04be0-130">指定可新增至 [閘道路徑規則設定] 的現有後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="04be0-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="04be0-131">您可以使用 Get-AzureRmApplicationGatewayBackendAddressPool Cmdlet 傳回位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="04be0-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="04be0-132">在您擁有 ID 之後，您就可以使用 *DefaultBackendAddressPoolId* 參數，而不是 *DefaultBackendAddressPool* 參數。</span><span class="sxs-lookup"><span data-stu-id="04be0-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="04be0-133">例如：-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 後端位址集區代表後端伺服器上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="04be0-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="04be0-134">這些 IP 位址應該是屬於虛擬網路子網，或是公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="04be0-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="04be0-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="04be0-135">-BackendHttpSettings</span></span>
<span data-ttu-id="04be0-136">指定要新增至 [閘道路徑規則設定] 的後端 HTTP 設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="04be0-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="04be0-137">您可以使用 New-AzureRmApplicationGatewayBackendHttpSettings Cmdlet 及如下所示的語法來建立此物件參照： $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings 名稱 "ContosoHttpSetings"-Port 80-通訊協定 "Http"-CookieBasedAffinity "Disabled" 所產生的變數（$HttpSettings）隨後可用作 *DefaultBackendAddressPool* 參數的參數值：-DefaultBackendHttpSettings $HttpSettings 後端 Http 設定會針對後端池設定屬性，例如埠、通訊協定和 cookie 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="04be0-137">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="04be0-138">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendHttpSettingsId* 參數。</span><span class="sxs-lookup"><span data-stu-id="04be0-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="04be0-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="04be0-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="04be0-140">指定現有後端 HTTP 設定集合的識別碼，該集合可以新增至 [閘道路徑規則] 設定設定。</span><span class="sxs-lookup"><span data-stu-id="04be0-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="04be0-141">您可以使用 Get-AzureRmApplicationGatewayBackendHttpSettings Cmdlet 傳回 HTTP 設定 Id。</span><span class="sxs-lookup"><span data-stu-id="04be0-141">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="04be0-142">在您擁有 ID 之後，您就可以使用 *DefaultBackendHttpSettingsId* 參數，而不是 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="04be0-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="04be0-143">例如：-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 後端 HTTP 設定會為後端池設定屬性，例如埠、通訊協定及 cookie 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="04be0-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="04be0-144">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="04be0-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="04be0-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04be0-145">-DefaultProfile</span></span>
<span data-ttu-id="04be0-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04be0-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04be0-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="04be0-147">-Name</span></span>
<span data-ttu-id="04be0-148">指定此 Cmdlet 所建立之路徑規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="04be0-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="04be0-149">-路徑</span><span class="sxs-lookup"><span data-stu-id="04be0-149">-Paths</span></span>
<span data-ttu-id="04be0-150">指定一個或多個應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="04be0-150">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04be0-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="04be0-151">-RedirectConfiguration</span></span>
<span data-ttu-id="04be0-152">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="04be0-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="04be0-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="04be0-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="04be0-154">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="04be0-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="04be0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04be0-155">CommonParameters</span></span>
<span data-ttu-id="04be0-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04be0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04be0-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04be0-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04be0-158">輸入</span><span class="sxs-lookup"><span data-stu-id="04be0-158">INPUTS</span></span>

### <span data-ttu-id="04be0-159">所有</span><span class="sxs-lookup"><span data-stu-id="04be0-159">None</span></span>

## <span data-ttu-id="04be0-160">輸出</span><span class="sxs-lookup"><span data-stu-id="04be0-160">OUTPUTS</span></span>

### <span data-ttu-id="04be0-161">PSApplicationGatewayPathRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="04be0-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="04be0-162">筆記</span><span class="sxs-lookup"><span data-stu-id="04be0-162">NOTES</span></span>

## <span data-ttu-id="04be0-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="04be0-163">RELATED LINKS</span></span>

[<span data-ttu-id="04be0-164">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04be0-164">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="04be0-165">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04be0-165">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="04be0-166">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04be0-166">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="04be0-167">新-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="04be0-167">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="04be0-168">新-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="04be0-168">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="04be0-169">新-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04be0-169">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="04be0-170">新-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04be0-170">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="04be0-171">移除-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04be0-171">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="04be0-172">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04be0-172">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)



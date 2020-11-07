---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794307"
---
# <span data-ttu-id="7bf31-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7bf31-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="7bf31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bf31-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf31-103">建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="7bf31-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="7bf31-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bf31-104">SYNTAX</span></span>

### <span data-ttu-id="7bf31-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7bf31-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bf31-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7bf31-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bf31-107">說明</span><span class="sxs-lookup"><span data-stu-id="7bf31-107">DESCRIPTION</span></span>
<span data-ttu-id="7bf31-108">**新的-AzApplicationGatewayPathRuleConfig** Cmdlet 會建立應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="7bf31-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="7bf31-109">您可以將由此 Cmdlet 建立的規則新增至 URL 路徑對應設定的集合，然後指派給閘道。</span><span class="sxs-lookup"><span data-stu-id="7bf31-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="7bf31-110">路徑對應設定是在應用程式閘道負載平衡中使用。</span><span class="sxs-lookup"><span data-stu-id="7bf31-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="7bf31-111">示例</span><span class="sxs-lookup"><span data-stu-id="7bf31-111">EXAMPLES</span></span>

### <span data-ttu-id="7bf31-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7bf31-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="7bf31-113">這些命令會建立新的應用程式閘道路徑規則，然後使用 **AzApplicationGatewayUrlPathMapConfig** Cmdlet 將該規則指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7bf31-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="7bf31-114">若要這樣做，第一個命令會建立對閘道 ContosoApplicationGateway 的物件參照。</span><span class="sxs-lookup"><span data-stu-id="7bf31-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="7bf31-115">這個物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7bf31-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="7bf31-116">接下來的兩個命令會建立後端位址集區和後端 HTTP 設定物件;這些物件 (儲存在 $AddressPool 變數中，而且需要 $HttpSettings) ，才能建立路徑規則物件。</span><span class="sxs-lookup"><span data-stu-id="7bf31-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="7bf31-117">第四個命令會建立路徑規則物件，並儲存在名為 $PathRuleConfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7bf31-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="7bf31-118">第五個命令使用 [ **載入 AzApplicationGatewayUrlPathMapConfig** ]，將配置設定和包含在這些設定中的新路徑規則新增到 ContosoApplicationGateway。</span><span class="sxs-lookup"><span data-stu-id="7bf31-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="7bf31-119">參數</span><span class="sxs-lookup"><span data-stu-id="7bf31-119">PARAMETERS</span></span>

### <span data-ttu-id="7bf31-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7bf31-120">-BackendAddressPool</span></span>
<span data-ttu-id="7bf31-121">指定要新增至 [閘道路徑規則設定] 的後端位址集區設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="7bf31-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="7bf31-122">您可以使用 New-AzApplicationGatewayBackendAddressPool Cmdlet 及如下所示的語法來建立此物件參照：</span><span class="sxs-lookup"><span data-stu-id="7bf31-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="7bf31-123">上述命令會將兩個 IP 位址 (192.16.1.1 和 192.168.1.2) 新增到位址集區中。</span><span class="sxs-lookup"><span data-stu-id="7bf31-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="7bf31-124">請注意，IP 位址括在引號中，並以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="7bf31-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="7bf31-125">產生的變數 $AddressPool，就可以用來做為 *DefaultBackendAddressPool* 參數的參數值。</span><span class="sxs-lookup"><span data-stu-id="7bf31-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="7bf31-126">後端位址集區代表後端伺服器上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7bf31-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="7bf31-127">這些 IP 位址應該是屬於虛擬網路子網，或是公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7bf31-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="7bf31-128">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendAddressPoolId* 參數。</span><span class="sxs-lookup"><span data-stu-id="7bf31-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf31-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7bf31-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="7bf31-130">指定可新增至 [閘道路徑規則設定] 的現有後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="7bf31-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="7bf31-131">您可以使用 Get-AzApplicationGatewayBackendAddressPool Cmdlet 傳回位址集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bf31-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="7bf31-132">在您擁有 ID 之後，您就可以使用 *DefaultBackendAddressPoolId* 參數，而不是 *DefaultBackendAddressPool* 參數。</span><span class="sxs-lookup"><span data-stu-id="7bf31-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="7bf31-133">例如：</span><span class="sxs-lookup"><span data-stu-id="7bf31-133">For instance:</span></span>

<span data-ttu-id="7bf31-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="7bf31-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="7bf31-135">後端位址集區代表後端伺服器上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7bf31-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="7bf31-136">這些 IP 位址應該是屬於虛擬網路子網，或是公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7bf31-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf31-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7bf31-137">-BackendHttpSettings</span></span>
<span data-ttu-id="7bf31-138">指定要新增至 [閘道路徑規則設定] 的後端 HTTP 設定集合的物件參照。</span><span class="sxs-lookup"><span data-stu-id="7bf31-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="7bf31-139">您可以使用 New-AzApplicationGatewayBackendHttpSetting Cmdlet 及如下所示的語法來建立此物件參照：</span><span class="sxs-lookup"><span data-stu-id="7bf31-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSetting cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="7bf31-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-Name "ContosoHttpSetings"-Port 80-Protocol "Https"-CookieBasedAffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="7bf31-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="7bf31-141">產生的變數，$HttpSettings，可以用來做為 *DefaultBackendAddressPool* 參數的參數值：</span><span class="sxs-lookup"><span data-stu-id="7bf31-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="7bf31-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="7bf31-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="7bf31-143">後端 HTTP 設定會為後端池設定屬性，例如埠、通訊協定及 cookie 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="7bf31-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="7bf31-144">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendHttpSettingsId* 參數。</span><span class="sxs-lookup"><span data-stu-id="7bf31-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf31-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7bf31-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="7bf31-146">指定現有後端 HTTP 設定集合的識別碼，該集合可以新增至 [閘道路徑規則] 設定設定。</span><span class="sxs-lookup"><span data-stu-id="7bf31-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="7bf31-147">您可以使用 Get-AzApplicationGatewayBackendHttpSetting Cmdlet 傳回 HTTP 設定 Id。</span><span class="sxs-lookup"><span data-stu-id="7bf31-147">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span></span>
<span data-ttu-id="7bf31-148">在您擁有 ID 之後，您就可以使用 *DefaultBackendHttpSettingsId* 參數，而不是 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="7bf31-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="7bf31-149">例如：</span><span class="sxs-lookup"><span data-stu-id="7bf31-149">For instance:</span></span>

<span data-ttu-id="7bf31-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="7bf31-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="7bf31-151">後端 HTTP 設定會為後端池設定屬性，例如埠、通訊協定及 cookie 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="7bf31-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="7bf31-152">如果您使用這個參數，就不能在相同的命令中使用 *DefaultBackendHttpSettings* 參數。</span><span class="sxs-lookup"><span data-stu-id="7bf31-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf31-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf31-153">-DefaultProfile</span></span>
<span data-ttu-id="7bf31-154">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bf31-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf31-155">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bf31-155">-Name</span></span>
<span data-ttu-id="7bf31-156">指定此 Cmdlet 所建立之路徑規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bf31-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf31-157">-路徑</span><span class="sxs-lookup"><span data-stu-id="7bf31-157">-Paths</span></span>
<span data-ttu-id="7bf31-158">指定一個或多個應用程式閘道路徑規則。</span><span class="sxs-lookup"><span data-stu-id="7bf31-158">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="7bf31-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bf31-159">-RedirectConfiguration</span></span>
<span data-ttu-id="7bf31-160">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bf31-160">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf31-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7bf31-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="7bf31-162">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="7bf31-162">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf31-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf31-163">CommonParameters</span></span>
<span data-ttu-id="7bf31-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bf31-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf31-165">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7bf31-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf31-166">輸入</span><span class="sxs-lookup"><span data-stu-id="7bf31-166">INPUTS</span></span>

###  
<span data-ttu-id="7bf31-167">**新的-AzApplicationGatewayPathRuleConfig** 不接受流水線輸入。</span><span class="sxs-lookup"><span data-stu-id="7bf31-167">**New-AzApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="7bf31-168">輸出</span><span class="sxs-lookup"><span data-stu-id="7bf31-168">OUTPUTS</span></span>

###  
<span data-ttu-id="7bf31-169">[ **新-AzApplicationGatewayPathRuleConfig** ] 會建立 **PSApplicationGatewayPathRule** 物件的新實例。</span><span class="sxs-lookup"><span data-stu-id="7bf31-169">**New-AzApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="7bf31-170">筆記</span><span class="sxs-lookup"><span data-stu-id="7bf31-170">NOTES</span></span>

## <span data-ttu-id="7bf31-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bf31-171">RELATED LINKS</span></span>

[<span data-ttu-id="7bf31-172">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7bf31-172">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7bf31-173">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bf31-173">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="7bf31-174">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7bf31-174">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7bf31-175">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7bf31-175">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7bf31-176">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7bf31-176">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7bf31-177">新-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7bf31-177">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="7bf31-178">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7bf31-178">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7bf31-179">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7bf31-179">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7bf31-180">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7bf31-180">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)



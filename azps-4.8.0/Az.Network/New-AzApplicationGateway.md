---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 5f91f333cf7983d50ba2984fcf01845a6c555e83
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136328"
---
# <span data-ttu-id="8e376-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e376-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="8e376-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e376-102">SYNOPSIS</span></span>
<span data-ttu-id="8e376-103">建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8e376-103">Creates an application gateway.</span></span>

## <span data-ttu-id="8e376-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e376-104">SYNTAX</span></span>

### <span data-ttu-id="8e376-105">IdentityByUserAssignedIdentityId (預設) </span><span class="sxs-lookup"><span data-stu-id="8e376-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e376-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e376-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e376-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8e376-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e376-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="8e376-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e376-109">說明</span><span class="sxs-lookup"><span data-stu-id="8e376-109">DESCRIPTION</span></span>
<span data-ttu-id="8e376-110">**新的-AzApplicationGateway** Cmdlet 會建立 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8e376-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="8e376-111">應用程式閘道需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="8e376-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="8e376-112">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="8e376-112">A resource group.</span></span>
- <span data-ttu-id="8e376-113">虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="8e376-113">A virtual network.</span></span>
- <span data-ttu-id="8e376-114">後端伺服器池，包含後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8e376-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="8e376-115">後端伺服器池設定。</span><span class="sxs-lookup"><span data-stu-id="8e376-115">Back-end server pool settings.</span></span> <span data-ttu-id="8e376-116">每個池都有套用至池中所有伺服器的埠、通訊協定及 cookie 關聯性等設定。</span><span class="sxs-lookup"><span data-stu-id="8e376-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="8e376-117">前端 IP 位址，也就是在應用程式閘道開啟的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8e376-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="8e376-118">前端 IP 位址可以是公用 IP 位址或內部 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8e376-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="8e376-119">前端埠，即是在應用程式閘道開啟的公用埠。</span><span class="sxs-lookup"><span data-stu-id="8e376-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="8e376-120">擊中這些埠的流量會重新導向到後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="8e376-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="8e376-121">系結監聽器與後端伺服器池的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="8e376-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="8e376-122">規則會定義當通信量擊中特定的監聽程式時，應該會將它導向到哪個後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="8e376-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="8e376-123">偵聽程式有前端埠、前端 IP 位址、通訊協定 (HTTP 或 HTTPS) 以及安全通訊端層 (SSL) 憑證名 (如果設定 SSL 卸載) 。</span><span class="sxs-lookup"><span data-stu-id="8e376-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="8e376-124">示例</span><span class="sxs-lookup"><span data-stu-id="8e376-124">EXAMPLES</span></span>

### <span data-ttu-id="8e376-125">範例1：建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="8e376-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="8e376-126">下列範例會先建立資源群組和虛擬網路，以及下列專案來建立應用程式閘道：</span><span class="sxs-lookup"><span data-stu-id="8e376-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="8e376-127">後端伺服器池</span><span class="sxs-lookup"><span data-stu-id="8e376-127">A back-end server pool</span></span>
- <span data-ttu-id="8e376-128">後端伺服器池設定</span><span class="sxs-lookup"><span data-stu-id="8e376-128">Back-end server pool settings</span></span>
- <span data-ttu-id="8e376-129">前端埠</span><span class="sxs-lookup"><span data-stu-id="8e376-129">Front-end ports</span></span>
- <span data-ttu-id="8e376-130">前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="8e376-130">Front-end IP addresses</span></span>
- <span data-ttu-id="8e376-131">要求路由規則這四個命令會建立一個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="8e376-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="8e376-132">第一個命令會建立子網配置。</span><span class="sxs-lookup"><span data-stu-id="8e376-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="8e376-133">第二個命令會建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="8e376-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="8e376-134">第三個命令會驗證子網設定，而第四個命令會驗證虛擬網路已順利建立。</span><span class="sxs-lookup"><span data-stu-id="8e376-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="8e376-135">下列命令會建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8e376-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="8e376-136">第一個命令會為先前建立的子網建立名為 GatewayIp01 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="8e376-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="8e376-137">第二個命令會使用後端 IP 位址清單來建立名為 Pool01 的後端伺服器池，並將該池儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e376-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="8e376-138">第三個命令會建立後端伺服器池的設定，並將設定儲存在 $PoolSetting 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e376-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="8e376-139">第四個命令會在埠80建立前端埠，將它命名為 FrontEndPort01，並將埠儲存在 $FrontEndPort 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e376-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="8e376-140">第五個命令會使用新的 AzPublicIpAddress 建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8e376-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="8e376-141">第六個命令會使用 $PublicIp 建立前端 IP 設定，並將其命名為 FrontEndPortConfig01，並將它儲存在 $FrontEndIpConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e376-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="8e376-142">第七個命令會使用先前建立的 $FrontEndIpConfig $FrontEndPort 來建立偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="8e376-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="8e376-143">第八個命令會建立監聽程式的規則。</span><span class="sxs-lookup"><span data-stu-id="8e376-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="8e376-144">第九個命令會設定 SKU。</span><span class="sxs-lookup"><span data-stu-id="8e376-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="8e376-145">第10個命令會使用先前命令所設定的物件來建立閘道。</span><span class="sxs-lookup"><span data-stu-id="8e376-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="8e376-146">範例2：使用 UserAssigned 身分識別來建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="8e376-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="8e376-147">參數</span><span class="sxs-lookup"><span data-stu-id="8e376-147">PARAMETERS</span></span>

### <span data-ttu-id="8e376-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e376-148">-AsJob</span></span>
<span data-ttu-id="8e376-149">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e376-149">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="8e376-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="8e376-151">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="8e376-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e376-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="8e376-153">自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="8e376-153">Autoscale Configuration</span></span>

```yaml
Type: PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="8e376-154">-BackendAddressPools</span></span>
<span data-ttu-id="8e376-155">指定應用程式閘道的後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="8e376-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="8e376-157">指定應用程式閘道的後端 HTTP 設定清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e376-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="8e376-159">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="8e376-159">Customer error of an application gateway</span></span>

```yaml
Type: PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e376-160">-DefaultProfile</span></span>
<span data-ttu-id="8e376-161">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e376-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="8e376-162">-EnableFIPS</span></span>
<span data-ttu-id="8e376-163">是否已啟用 FIPS。</span><span class="sxs-lookup"><span data-stu-id="8e376-163">Whether FIPS is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="8e376-164">-EnableHttp2</span></span>
<span data-ttu-id="8e376-165">是否已啟用 HTTP2。</span><span class="sxs-lookup"><span data-stu-id="8e376-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8e376-166">-FirewallPolicy</span></span>
<span data-ttu-id="8e376-167">防火牆設定</span><span class="sxs-lookup"><span data-stu-id="8e376-167">Firewall configuration</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8e376-168">-FirewallPolicyId</span></span>
<span data-ttu-id="8e376-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8e376-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="8e376-170">-Force</span><span class="sxs-lookup"><span data-stu-id="8e376-170">-Force</span></span>
<span data-ttu-id="8e376-171">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8e376-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="8e376-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="8e376-173">是否啟用 [強制 firewallPolicy 關聯]。</span><span class="sxs-lookup"><span data-stu-id="8e376-173">Whether Force firewallPolicy association is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="8e376-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="8e376-175">指定應用程式閘道的前端 IP 配置清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="8e376-176">-FrontendPorts</span></span>
<span data-ttu-id="8e376-177">指定應用程式閘道的前端埠清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="8e376-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="8e376-179">指定應用程式閘道的 IP 配置清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="8e376-180">-HttpListeners</span></span>
<span data-ttu-id="8e376-181">指定應用程式閘道的 HTTP 攔截器清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-182">身分識別</span><span class="sxs-lookup"><span data-stu-id="8e376-182">-Identity</span></span>
<span data-ttu-id="8e376-183">要指派給應用程式閘道的應用程式閘道身分識別。</span><span class="sxs-lookup"><span data-stu-id="8e376-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-184">-位置</span><span class="sxs-lookup"><span data-stu-id="8e376-184">-Location</span></span>
<span data-ttu-id="8e376-185">指定要在其中建立應用程式閘道的區域。</span><span class="sxs-lookup"><span data-stu-id="8e376-185">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-186">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e376-186">-Name</span></span>
<span data-ttu-id="8e376-187">指定應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e376-187">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e376-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="8e376-189">PrivateLink 配置清單</span><span class="sxs-lookup"><span data-stu-id="8e376-189">The list of privateLink Configuration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-190">-探針</span><span class="sxs-lookup"><span data-stu-id="8e376-190">-Probes</span></span>
<span data-ttu-id="8e376-191">指定應用程式閘道的探測器。</span><span class="sxs-lookup"><span data-stu-id="8e376-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="8e376-192">-RedirectConfigurations</span></span>
<span data-ttu-id="8e376-193">重新導向配置清單</span><span class="sxs-lookup"><span data-stu-id="8e376-193">The list of redirect configuration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="8e376-194">-RequestRoutingRules</span></span>
<span data-ttu-id="8e376-195">指定應用程式閘道的要求路由規則清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e376-196">-ResourceGroupName</span></span>
<span data-ttu-id="8e376-197">指定要在其中建立應用程式閘道的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e376-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e376-198">-RewriteRuleSet</span></span>
<span data-ttu-id="8e376-199">RewriteRuleSet 清單</span><span class="sxs-lookup"><span data-stu-id="8e376-199">The list of RewriteRuleSet</span></span>

```yaml
Type: PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-200">-Sku</span><span class="sxs-lookup"><span data-stu-id="8e376-200">-Sku</span></span>
<span data-ttu-id="8e376-201">指定應用程式閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="8e376-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="8e376-202">-SslCertificates</span></span>
<span data-ttu-id="8e376-203">指定 (SSL) 應用程式閘道憑證的安全通訊端層的清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="8e376-204">-SslPolicy</span></span>
<span data-ttu-id="8e376-205">指定應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="8e376-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-206">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e376-206">-Tag</span></span>
<span data-ttu-id="8e376-207">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="8e376-207">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8e376-208">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8e376-208">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-209">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e376-209">-TrustedRootCertificate</span></span>
<span data-ttu-id="8e376-210">受信任的根憑證清單</span><span class="sxs-lookup"><span data-stu-id="8e376-210">The list of trusted root certificates</span></span>

```yaml
Type: PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-211">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="8e376-211">-UrlPathMaps</span></span>
<span data-ttu-id="8e376-212">指定應用程式閘道的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="8e376-212">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-213">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="8e376-213">-UserAssignedIdentityId</span></span>
<span data-ttu-id="8e376-214">指派給應用程式閘道的使用者指派身分識別的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="8e376-214">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-215">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e376-215">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="8e376-216">指定 (WAF) 設定的 web 應用程式防火牆。</span><span class="sxs-lookup"><span data-stu-id="8e376-216">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="8e376-217">您可以使用 Get-AzApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 來取得 WAF。</span><span class="sxs-lookup"><span data-stu-id="8e376-217">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-218">-Zone</span><span class="sxs-lookup"><span data-stu-id="8e376-218">-Zone</span></span>
<span data-ttu-id="8e376-219">顯示應用程式閘道需要來源之位置的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="8e376-219">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-220">-確認</span><span class="sxs-lookup"><span data-stu-id="8e376-220">-Confirm</span></span>
<span data-ttu-id="8e376-221">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e376-221">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e376-222">-WhatIf</span></span>
<span data-ttu-id="8e376-223">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e376-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e376-224">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e376-224">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e376-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e376-225">CommonParameters</span></span>
<span data-ttu-id="8e376-226">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e376-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e376-227">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e376-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e376-228">輸入</span><span class="sxs-lookup"><span data-stu-id="8e376-228">INPUTS</span></span>

### <span data-ttu-id="8e376-229">System.object</span><span class="sxs-lookup"><span data-stu-id="8e376-229">System.String</span></span>

### <span data-ttu-id="8e376-230">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e376-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="8e376-231">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e376-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="8e376-232">PSApplicationGatewayIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="8e376-233">PSApplicationGatewaySslCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="8e376-234">PSApplicationGatewayAuthenticationCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="8e376-235">PSApplicationGatewayTrustedRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="8e376-236">PSApplicationGatewayFrontendIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="8e376-237">PSApplicationGatewayFrontendPort [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="8e376-238">PSApplicationGatewayProbe [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="8e376-239">PSApplicationGatewayBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="8e376-240">PSApplicationGatewayBackendHttpSettings [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="8e376-241">PSApplicationGatewayHttpListener [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="8e376-242">PSApplicationGatewayUrlPathMap [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="8e376-243">PSApplicationGatewayRequestRoutingRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="8e376-244">PSApplicationGatewayRewriteRuleSet [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="8e376-245">PSApplicationGatewayRedirectConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8e376-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="8e376-246">PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e376-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="8e376-247">PSApplicationGatewayAutoscaleConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e376-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="8e376-248">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e376-248">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8e376-249">PSManagedServiceIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e376-249">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="8e376-250">輸出</span><span class="sxs-lookup"><span data-stu-id="8e376-250">OUTPUTS</span></span>

### <span data-ttu-id="8e376-251">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e376-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e376-252">筆記</span><span class="sxs-lookup"><span data-stu-id="8e376-252">NOTES</span></span>

## <span data-ttu-id="8e376-253">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e376-253">RELATED LINKS</span></span>

[<span data-ttu-id="8e376-254">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8e376-254">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8e376-255">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8e376-255">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="8e376-256">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8e376-256">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8e376-257">新-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8e376-257">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8e376-258">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8e376-258">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="8e376-259">新-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e376-259">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8e376-260">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8e376-260">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8e376-261">新-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="8e376-261">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="8e376-262">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8e376-262">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="8e376-263">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8e376-263">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
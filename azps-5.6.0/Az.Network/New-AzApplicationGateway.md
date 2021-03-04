---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 00e1cb4856afc00f13730dbee55de9499d603290
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904362"
---
# <span data-ttu-id="acf22-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="acf22-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="acf22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="acf22-102">SYNOPSIS</span></span>
<span data-ttu-id="acf22-103">建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="acf22-103">Creates an application gateway.</span></span>

## <span data-ttu-id="acf22-104">語法</span><span class="sxs-lookup"><span data-stu-id="acf22-104">SYNTAX</span></span>

### <span data-ttu-id="acf22-105">IdentityByUserAssignedIdentityId (預設) </span><span class="sxs-lookup"><span data-stu-id="acf22-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="acf22-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="acf22-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="acf22-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="acf22-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="acf22-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="acf22-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

## <span data-ttu-id="acf22-109">描述</span><span class="sxs-lookup"><span data-stu-id="acf22-109">DESCRIPTION</span></span>
<span data-ttu-id="acf22-110">**New-AzApplicationGateway** Cmdlet 會建立 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="acf22-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="acf22-111">應用程式閘道需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="acf22-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="acf22-112">資源群組。</span><span class="sxs-lookup"><span data-stu-id="acf22-112">A resource group.</span></span>
- <span data-ttu-id="acf22-113">一個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="acf22-113">A virtual network.</span></span>
- <span data-ttu-id="acf22-114">後端伺服器資料庫，包含後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="acf22-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="acf22-115">後端伺服器資料庫設定。</span><span class="sxs-lookup"><span data-stu-id="acf22-115">Back-end server pool settings.</span></span> <span data-ttu-id="acf22-116">每個資料庫都有埠、通訊協定和 Cookie 型關聯等設定，這些設定會適用于資料庫內的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="acf22-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="acf22-117">前端 IP 位址，即應用程式閘道上開啟的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="acf22-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="acf22-118">前端 IP 位址可以是公用 IP 位址或內部 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="acf22-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="acf22-119">前端埠，即應用程式閘道上開啟的公用埠。</span><span class="sxs-lookup"><span data-stu-id="acf22-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="acf22-120">到達這些埠的流量會重新導向至後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="acf22-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="acf22-121">將聆聽者與後端伺服器集區綁定的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="acf22-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="acf22-122">規則會定義當流量到達特定聆聽者時，該流量應導向至哪個後端伺服器集區。</span><span class="sxs-lookup"><span data-stu-id="acf22-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="acf22-123">聆聽者擁有前端埠、前端 IP 位址、通訊協定 (HTTP 或 HTTPS) ，以及安全通訊端層 (SSL) 憑證名稱 (若已) 。</span><span class="sxs-lookup"><span data-stu-id="acf22-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="acf22-124">例子</span><span class="sxs-lookup"><span data-stu-id="acf22-124">EXAMPLES</span></span>

### <span data-ttu-id="acf22-125">範例 1：建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="acf22-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="acf22-126">下列範例會先建立資源群組和虛擬網路來建立應用程式閘道，以及下列各項：</span><span class="sxs-lookup"><span data-stu-id="acf22-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="acf22-127">後端伺服器資料庫</span><span class="sxs-lookup"><span data-stu-id="acf22-127">A back-end server pool</span></span>
- <span data-ttu-id="acf22-128">後端伺服器資料庫設定</span><span class="sxs-lookup"><span data-stu-id="acf22-128">Back-end server pool settings</span></span>
- <span data-ttu-id="acf22-129">前端埠</span><span class="sxs-lookup"><span data-stu-id="acf22-129">Front-end ports</span></span>
- <span data-ttu-id="acf22-130">前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="acf22-130">Front-end IP addresses</span></span>
- <span data-ttu-id="acf22-131">要求路由規則 這四個命令會建立一個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="acf22-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="acf22-132">第一個命令會建立子網組配置。</span><span class="sxs-lookup"><span data-stu-id="acf22-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="acf22-133">第二個命令會建立一個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="acf22-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="acf22-134">第三個命令會驗證子網組配置，第四個命令會驗證已成功建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="acf22-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="acf22-135">下列命令會建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="acf22-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="acf22-136">第一個命令會針對先前建立之子網建立名為 GatewayIp01 的 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="acf22-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="acf22-137">第二個命令會建立名為 Pool01 的後端伺服器資料庫，並包含後端 IP 位址清單，並且將該$Pool變數。</span><span class="sxs-lookup"><span data-stu-id="acf22-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="acf22-138">第三個命令會建立後端伺服器資料庫的設定，並且將設定儲存在$PoolSetting變數。</span><span class="sxs-lookup"><span data-stu-id="acf22-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="acf22-139">第四個命令在埠 80 上建立前端埠，將它命名為 FrontEndPort01，並且將埠儲存在 $FrontEndPort 變數中。</span><span class="sxs-lookup"><span data-stu-id="acf22-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="acf22-140">第五個命令會使用 New-AzPublicIpAddress 建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="acf22-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="acf22-141">第六個命令會使用 $PublicIp 建立前端 IP 組$PublicIp，將它命名為 FrontEndPortConfig01，然後儲存在 $FrontEndIpConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="acf22-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="acf22-142">第七個命令會使用先前建立$FrontEndIpConfig $FrontEndPort。</span><span class="sxs-lookup"><span data-stu-id="acf22-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="acf22-143">第八個命令會為聆聽者建立規則。</span><span class="sxs-lookup"><span data-stu-id="acf22-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="acf22-144">第九個命令會設定 SKU。</span><span class="sxs-lookup"><span data-stu-id="acf22-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="acf22-145">第十個命令會使用先前命令所設定的物件來建立閘道。</span><span class="sxs-lookup"><span data-stu-id="acf22-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="acf22-146">範例 2：使用 UserAssigned 身分識別建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="acf22-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="acf22-147">參數</span><span class="sxs-lookup"><span data-stu-id="acf22-147">PARAMETERS</span></span>

### <span data-ttu-id="acf22-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acf22-148">-AsJob</span></span>
<span data-ttu-id="acf22-149">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="acf22-149">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="acf22-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="acf22-151">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="acf22-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf22-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="acf22-153">自動縮放組配置</span><span class="sxs-lookup"><span data-stu-id="acf22-153">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-154">-後端AddressPools</span><span class="sxs-lookup"><span data-stu-id="acf22-154">-BackendAddressPools</span></span>
<span data-ttu-id="acf22-155">指定應用程式閘道的後端位址資料庫清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-156">-後端HttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="acf22-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="acf22-157">指定應用程式閘道的後端 HTTP 設定清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf22-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="acf22-159">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="acf22-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf22-160">-DefaultProfile</span></span>
<span data-ttu-id="acf22-161">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="acf22-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acf22-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="acf22-162">-EnableFIPS</span></span>
<span data-ttu-id="acf22-163">是否已啟用 FIPS。</span><span class="sxs-lookup"><span data-stu-id="acf22-163">Whether FIPS is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="acf22-164">-EnableHttp2</span></span>
<span data-ttu-id="acf22-165">是否已啟用 HTTP2。</span><span class="sxs-lookup"><span data-stu-id="acf22-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="acf22-166">-FirewallPolicy</span></span>
<span data-ttu-id="acf22-167">防火牆組</span><span class="sxs-lookup"><span data-stu-id="acf22-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="acf22-168">-FirewallPolicyId</span></span>
<span data-ttu-id="acf22-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="acf22-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="acf22-170">-強制</span><span class="sxs-lookup"><span data-stu-id="acf22-170">-Force</span></span>
<span data-ttu-id="acf22-171">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="acf22-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="acf22-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="acf22-173">是否已啟用強制防火牆策略關聯。</span><span class="sxs-lookup"><span data-stu-id="acf22-173">Whether Force firewallPolicy association is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="acf22-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="acf22-175">指定應用程式閘道的前端 IP 群組原則清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="acf22-176">-FrontendPorts</span></span>
<span data-ttu-id="acf22-177">指定應用程式閘道的前端埠清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="acf22-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="acf22-179">指定應用程式閘道的 IP 群組原則清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-180">-HTTPListeners</span><span class="sxs-lookup"><span data-stu-id="acf22-180">-HttpListeners</span></span>
<span data-ttu-id="acf22-181">指定應用程式閘道的 HTTP 聆聽者清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-182">-身分識別</span><span class="sxs-lookup"><span data-stu-id="acf22-182">-Identity</span></span>
<span data-ttu-id="acf22-183">要指派給應用程式閘道的應用程式閘道身分識別。</span><span class="sxs-lookup"><span data-stu-id="acf22-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-184">-位置</span><span class="sxs-lookup"><span data-stu-id="acf22-184">-Location</span></span>
<span data-ttu-id="acf22-185">指定要建立應用程式閘道的區域。</span><span class="sxs-lookup"><span data-stu-id="acf22-185">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-186">-名稱</span><span class="sxs-lookup"><span data-stu-id="acf22-186">-Name</span></span>
<span data-ttu-id="acf22-187">指定應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="acf22-187">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf22-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="acf22-189">privateLink 組配置清單</span><span class="sxs-lookup"><span data-stu-id="acf22-189">The list of privateLink Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-190">-進位器</span><span class="sxs-lookup"><span data-stu-id="acf22-190">-Probes</span></span>
<span data-ttu-id="acf22-191">指定應用程式閘道的介面。</span><span class="sxs-lookup"><span data-stu-id="acf22-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="acf22-192">-RedirectConfigurations</span></span>
<span data-ttu-id="acf22-193">重新導向組配置清單</span><span class="sxs-lookup"><span data-stu-id="acf22-193">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="acf22-194">-RequestRoutingRules</span></span>
<span data-ttu-id="acf22-195">指定應用程式閘道的要求路由規則清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf22-196">-ResourceGroupName</span></span>
<span data-ttu-id="acf22-197">指定要建立應用程式閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="acf22-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="acf22-198">-RewriteRuleSet</span></span>
<span data-ttu-id="acf22-199">RewriteRuleSet 清單</span><span class="sxs-lookup"><span data-stu-id="acf22-199">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="acf22-200">-Sku</span></span>
<span data-ttu-id="acf22-201">指定應用程式閘道 (SKU) 庫存單位。</span><span class="sxs-lookup"><span data-stu-id="acf22-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="acf22-202">-SslCertificates</span></span>
<span data-ttu-id="acf22-203">指定應用程式閘道的安全通訊端層 (SSL) 憑證清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="acf22-204">-SslPolicy</span></span>
<span data-ttu-id="acf22-205">指定應用程式閘道的 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="acf22-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-206">-SslProfiles</span><span class="sxs-lookup"><span data-stu-id="acf22-206">-SslProfiles</span></span>
<span data-ttu-id="acf22-207">ssl 配置檔案清單</span><span class="sxs-lookup"><span data-stu-id="acf22-207">The list of ssl profiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-208">-標記</span><span class="sxs-lookup"><span data-stu-id="acf22-208">-Tag</span></span>
<span data-ttu-id="acf22-209">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="acf22-209">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="acf22-210">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="acf22-210">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-211">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="acf22-211">-TrustedClientCertificates</span></span>
<span data-ttu-id="acf22-212">信任的用戶端 CA 憑證鏈清單</span><span class="sxs-lookup"><span data-stu-id="acf22-212">The list of trusted client CA certificate chains</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-213">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="acf22-213">-TrustedRootCertificate</span></span>
<span data-ttu-id="acf22-214">信任的根憑證清單</span><span class="sxs-lookup"><span data-stu-id="acf22-214">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-215">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="acf22-215">-UrlPathMaps</span></span>
<span data-ttu-id="acf22-216">指定應用程式閘道的 URL 路徑地圖。</span><span class="sxs-lookup"><span data-stu-id="acf22-216">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-217">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="acf22-217">-UserAssignedIdentityId</span></span>
<span data-ttu-id="acf22-218">指派身分識別給使用者的 ResourceId，指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="acf22-218">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-219">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf22-219">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="acf22-220">指定 Web 應用程式防火牆 (WAF) 組。</span><span class="sxs-lookup"><span data-stu-id="acf22-220">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="acf22-221">您可以使用 Cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration取得 WAF。</span><span class="sxs-lookup"><span data-stu-id="acf22-221">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-222">-區域</span><span class="sxs-lookup"><span data-stu-id="acf22-222">-Zone</span></span>
<span data-ttu-id="acf22-223">表示應用程式閘道需要來自何處的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="acf22-223">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="acf22-224">-確認</span><span class="sxs-lookup"><span data-stu-id="acf22-224">-Confirm</span></span>
<span data-ttu-id="acf22-225">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="acf22-225">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-226">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf22-226">-WhatIf</span></span>
<span data-ttu-id="acf22-227">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acf22-227">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf22-228">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="acf22-228">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf22-229">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf22-229">CommonParameters</span></span>
<span data-ttu-id="acf22-230">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="acf22-230">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf22-231">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acf22-231">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf22-232">輸入</span><span class="sxs-lookup"><span data-stu-id="acf22-232">INPUTS</span></span>

### <span data-ttu-id="acf22-233">System.String</span><span class="sxs-lookup"><span data-stu-id="acf22-233">System.String</span></span>

### <span data-ttu-id="acf22-234">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="acf22-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="acf22-235">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="acf22-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="acf22-236">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="acf22-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="acf22-237">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslCertificate[]</span><span class="sxs-lookup"><span data-stu-id="acf22-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="acf22-238">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAuthenticationCertificate[]</span><span class="sxs-lookup"><span data-stu-id="acf22-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="acf22-239">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayTrustedRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="acf22-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="acf22-240">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="acf22-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="acf22-241">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFrontendPort[]</span><span class="sxs-lookup"><span data-stu-id="acf22-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="acf22-242">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayProbe[]</span><span class="sxs-lookup"><span data-stu-id="acf22-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="acf22-243">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="acf22-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="acf22-244">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHttpSettings[]</span><span class="sxs-lookup"><span data-stu-id="acf22-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="acf22-245">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHttpListener[]</span><span class="sxs-lookup"><span data-stu-id="acf22-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="acf22-246">Microsoft.Azure.Commands.network.models.PSApplicationGatewayUrlPathMap[]</span><span class="sxs-lookup"><span data-stu-id="acf22-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="acf22-247">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRequestRoutingRule[]</span><span class="sxs-lookup"><span data-stu-id="acf22-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="acf22-248">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRewriteRuleSet[]</span><span class="sxs-lookup"><span data-stu-id="acf22-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="acf22-249">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRedirectConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="acf22-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="acf22-250">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf22-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="acf22-251">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf22-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="acf22-252">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="acf22-252">System.Collections.Hashtable</span></span>

### <span data-ttu-id="acf22-253">Microsoft.Azure.Commands.Network.models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="acf22-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="acf22-254">輸出</span><span class="sxs-lookup"><span data-stu-id="acf22-254">OUTPUTS</span></span>

### <span data-ttu-id="acf22-255">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="acf22-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="acf22-256">筆記</span><span class="sxs-lookup"><span data-stu-id="acf22-256">NOTES</span></span>

## <span data-ttu-id="acf22-257">相關連結</span><span class="sxs-lookup"><span data-stu-id="acf22-257">RELATED LINKS</span></span>

[<span data-ttu-id="acf22-258">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="acf22-258">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="acf22-259">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="acf22-259">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="acf22-260">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="acf22-260">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="acf22-261">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="acf22-261">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="acf22-262">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="acf22-262">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="acf22-263">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf22-263">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="acf22-264">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="acf22-264">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="acf22-265">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="acf22-265">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="acf22-266">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="acf22-266">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="acf22-267">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="acf22-267">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

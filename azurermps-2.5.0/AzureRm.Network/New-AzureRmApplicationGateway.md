---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 73b72c6585fb4c7487b43dc99b3494cdc99bf7a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800818"
---
# <span data-ttu-id="68507-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68507-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="68507-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68507-102">SYNOPSIS</span></span>
<span data-ttu-id="68507-103">建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="68507-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68507-104">句法</span><span class="sxs-lookup"><span data-stu-id="68507-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68507-105">說明</span><span class="sxs-lookup"><span data-stu-id="68507-105">DESCRIPTION</span></span>
<span data-ttu-id="68507-106">**新的-AzureRmApplicationGateway** Cmdlet 會建立 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="68507-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="68507-107">應用程式閘道需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="68507-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="68507-108">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="68507-108">A resource group.</span></span>
- <span data-ttu-id="68507-109">虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="68507-109">A virtual network.</span></span>
- <span data-ttu-id="68507-110">後端伺服器池，包含後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="68507-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="68507-111">後端伺服器池設定。</span><span class="sxs-lookup"><span data-stu-id="68507-111">Back-end server pool settings.</span></span> <span data-ttu-id="68507-112">每個池都有套用至池中所有伺服器的埠、通訊協定及 cookie 關聯性等設定。</span><span class="sxs-lookup"><span data-stu-id="68507-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="68507-113">前端 IP 位址，也就是在應用程式閘道開啟的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="68507-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="68507-114">前端 IP 位址可以是公用 IP 位址或內部 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="68507-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="68507-115">前端埠，即是在應用程式閘道開啟的公用埠。</span><span class="sxs-lookup"><span data-stu-id="68507-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="68507-116">擊中這些埠的流量會重新導向到後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="68507-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="68507-117">系結監聽器與後端伺服器池的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="68507-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="68507-118">規則會定義當通信量擊中特定的監聽程式時，應該會將它導向到哪個後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="68507-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="68507-119">偵聽程式有前端埠、前端 IP 位址、通訊協定 (HTTP 或 HTTPS) 以及安全通訊端層 (SSL) 憑證名 (如果設定 SSL 卸載) 。</span><span class="sxs-lookup"><span data-stu-id="68507-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="68507-120">示例</span><span class="sxs-lookup"><span data-stu-id="68507-120">EXAMPLES</span></span>

### <span data-ttu-id="68507-121">範例1：建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="68507-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="68507-122">下列範例會先建立資源群組和虛擬網路，以及下列專案來建立應用程式閘道：</span><span class="sxs-lookup"><span data-stu-id="68507-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="68507-123">後端伺服器池</span><span class="sxs-lookup"><span data-stu-id="68507-123">A back-end server pool</span></span>
- <span data-ttu-id="68507-124">後端伺服器池設定</span><span class="sxs-lookup"><span data-stu-id="68507-124">Back-end server pool settings</span></span>
- <span data-ttu-id="68507-125">前端埠</span><span class="sxs-lookup"><span data-stu-id="68507-125">Front-end ports</span></span>
- <span data-ttu-id="68507-126">前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="68507-126">Front-end IP addresses</span></span>
- <span data-ttu-id="68507-127">要求路由規則</span><span class="sxs-lookup"><span data-stu-id="68507-127">A request routing rule</span></span>

<span data-ttu-id="68507-128">這四個命令會建立一個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="68507-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="68507-129">第一個命令會建立子網配置。</span><span class="sxs-lookup"><span data-stu-id="68507-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="68507-130">第二個命令會建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="68507-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="68507-131">第三個命令會驗證子網設定，而第四個命令會驗證虛擬網路已順利建立。</span><span class="sxs-lookup"><span data-stu-id="68507-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="68507-132">下列命令會建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="68507-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="68507-133">第一個命令會為先前建立的子網建立名為 GatewayIp01 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="68507-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="68507-134">第二個命令會使用後端 IP 位址清單來建立名為 Pool01 的後端伺服器池，並將該池儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="68507-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="68507-135">第三個命令會建立後端伺服器池的設定，並將設定儲存在 $PoolSetting 變數中。</span><span class="sxs-lookup"><span data-stu-id="68507-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="68507-136">第四個命令會在埠80建立前端埠，將它命名為 FrontEndPort01，並將埠儲存在 $FrontEndPort 變數中。</span><span class="sxs-lookup"><span data-stu-id="68507-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="68507-137">第五個命令會使用新的 AzureRmPublicIpAddress 建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="68507-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="68507-138">第六個命令會使用 $PublicIp 建立前端 IP 設定，並將其命名為 FrontEndPortConfig01，並將它儲存在 $FrontEndIpConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="68507-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="68507-139">第七個命令會使用先前建立的 $FrontEndIpConfig $FrontEndPort 來建立偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="68507-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="68507-140">第八個命令會建立監聽程式的規則。</span><span class="sxs-lookup"><span data-stu-id="68507-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="68507-141">第九個命令會設定 SKU。</span><span class="sxs-lookup"><span data-stu-id="68507-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="68507-142">第10個命令會使用先前命令所設定的物件來建立閘道。</span><span class="sxs-lookup"><span data-stu-id="68507-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="68507-143">參數</span><span class="sxs-lookup"><span data-stu-id="68507-143">PARAMETERS</span></span>

### <span data-ttu-id="68507-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68507-144">-AsJob</span></span>
<span data-ttu-id="68507-145">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="68507-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68507-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="68507-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="68507-147">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="68507-147">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="68507-148">-BackendAddressPools</span></span>
<span data-ttu-id="68507-149">指定應用程式閘道的後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="68507-149">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="68507-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="68507-151">指定應用程式閘道的後端 HTTP 設定清單。</span><span class="sxs-lookup"><span data-stu-id="68507-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68507-152">-DefaultProfile</span></span>
<span data-ttu-id="68507-153">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68507-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68507-154">-Force</span><span class="sxs-lookup"><span data-stu-id="68507-154">-Force</span></span>
<span data-ttu-id="68507-155">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="68507-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68507-156">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="68507-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="68507-157">指定應用程式閘道的前端 IP 配置清單。</span><span class="sxs-lookup"><span data-stu-id="68507-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-158">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="68507-158">-FrontendPorts</span></span>
<span data-ttu-id="68507-159">指定應用程式閘道的前端埠清單。</span><span class="sxs-lookup"><span data-stu-id="68507-159">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-160">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="68507-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="68507-161">指定應用程式閘道的 IP 配置清單。</span><span class="sxs-lookup"><span data-stu-id="68507-161">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="68507-162">-HttpListeners</span></span>
<span data-ttu-id="68507-163">指定應用程式閘道的 HTTP 攔截器清單。</span><span class="sxs-lookup"><span data-stu-id="68507-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-164">-位置</span><span class="sxs-lookup"><span data-stu-id="68507-164">-Location</span></span>
<span data-ttu-id="68507-165">指定要在其中建立應用程式閘道的區域。</span><span class="sxs-lookup"><span data-stu-id="68507-165">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="68507-166">-名稱</span><span class="sxs-lookup"><span data-stu-id="68507-166">-Name</span></span>
<span data-ttu-id="68507-167">指定應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="68507-167">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="68507-168">-探針</span><span class="sxs-lookup"><span data-stu-id="68507-168">-Probes</span></span>
<span data-ttu-id="68507-169">指定應用程式閘道的探測器。</span><span class="sxs-lookup"><span data-stu-id="68507-169">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="68507-170">-RedirectConfigurations</span></span>
<span data-ttu-id="68507-171">重新導向配置清單</span><span class="sxs-lookup"><span data-stu-id="68507-171">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="68507-172">-RequestRoutingRules</span></span>
<span data-ttu-id="68507-173">指定應用程式閘道的要求路由規則清單。</span><span class="sxs-lookup"><span data-stu-id="68507-173">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68507-174">-ResourceGroupName</span></span>
<span data-ttu-id="68507-175">指定要在其中建立應用程式閘道的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68507-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="68507-176">-Sku</span><span class="sxs-lookup"><span data-stu-id="68507-176">-Sku</span></span>
<span data-ttu-id="68507-177">指定應用程式閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="68507-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="68507-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="68507-178">-SslCertificates</span></span>
<span data-ttu-id="68507-179">指定 (SSL) 應用程式閘道憑證的安全通訊端層的清單。</span><span class="sxs-lookup"><span data-stu-id="68507-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="68507-180">-SslPolicy</span></span>
<span data-ttu-id="68507-181">指定應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="68507-181">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="68507-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="68507-182">-Tag</span></span>
<span data-ttu-id="68507-183">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="68507-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="68507-184">例如：</span><span class="sxs-lookup"><span data-stu-id="68507-184">For example:</span></span>

<span data-ttu-id="68507-185">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="68507-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="68507-186">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="68507-186">-UrlPathMaps</span></span>
<span data-ttu-id="68507-187">指定應用程式閘道的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="68507-187">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68507-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="68507-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="68507-189">指定 (WAF) 設定的 web 應用程式防火牆。</span><span class="sxs-lookup"><span data-stu-id="68507-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="68507-190">您可以使用 Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 來取得 WAF。</span><span class="sxs-lookup"><span data-stu-id="68507-190">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="68507-191">-確認</span><span class="sxs-lookup"><span data-stu-id="68507-191">-Confirm</span></span>
<span data-ttu-id="68507-192">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68507-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68507-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68507-193">-WhatIf</span></span>
<span data-ttu-id="68507-194">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68507-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68507-195">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68507-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68507-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68507-196">CommonParameters</span></span>
<span data-ttu-id="68507-197">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68507-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68507-198">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68507-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68507-199">輸入</span><span class="sxs-lookup"><span data-stu-id="68507-199">INPUTS</span></span>

## <span data-ttu-id="68507-200">輸出</span><span class="sxs-lookup"><span data-stu-id="68507-200">OUTPUTS</span></span>

### <span data-ttu-id="68507-201">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="68507-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68507-202">筆記</span><span class="sxs-lookup"><span data-stu-id="68507-202">NOTES</span></span>

## <span data-ttu-id="68507-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="68507-203">RELATED LINKS</span></span>

[<span data-ttu-id="68507-204">新-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="68507-204">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="68507-205">新-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="68507-205">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="68507-206">新-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="68507-206">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="68507-207">新-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="68507-207">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="68507-208">新-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="68507-208">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="68507-209">新-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="68507-209">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="68507-210">新-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68507-210">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="68507-211">新-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="68507-211">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="68507-212">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68507-212">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="68507-213">新-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="68507-213">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

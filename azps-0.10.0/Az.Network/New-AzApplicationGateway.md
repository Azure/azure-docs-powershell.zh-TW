---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 1945ceb84f6ccc9af38f4336ab12b01e0021f337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794328"
---
# <span data-ttu-id="2b6c1-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b6c1-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="2b6c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6c1-103">建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-103">Creates an application gateway.</span></span>

## <span data-ttu-id="2b6c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b6c1-104">SYNTAX</span></span>

```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
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

## <span data-ttu-id="2b6c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b6c1-105">DESCRIPTION</span></span>
<span data-ttu-id="2b6c1-106">**新的-AzApplicationGateway** Cmdlet 會建立 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-106">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="2b6c1-107">應用程式閘道需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="2b6c1-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="2b6c1-108">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-108">A resource group.</span></span>
- <span data-ttu-id="2b6c1-109">虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-109">A virtual network.</span></span>
- <span data-ttu-id="2b6c1-110">後端伺服器池，包含後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="2b6c1-111">後端伺服器池設定。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-111">Back-end server pool settings.</span></span> <span data-ttu-id="2b6c1-112">每個池都有套用至池中所有伺服器的埠、通訊協定及 cookie 關聯性等設定。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="2b6c1-113">前端 IP 位址，也就是在應用程式閘道開啟的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="2b6c1-114">前端 IP 位址可以是公用 IP 位址或內部 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="2b6c1-115">前端埠，即是在應用程式閘道開啟的公用埠。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="2b6c1-116">擊中這些埠的流量會重新導向到後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="2b6c1-117">系結監聽器與後端伺服器池的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="2b6c1-118">規則會定義當通信量擊中特定的監聽程式時，應該會將它導向到哪個後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="2b6c1-119">偵聽程式有前端埠、前端 IP 位址、通訊協定 (HTTP 或 HTTPS) 以及安全通訊端層 (SSL) 憑證名 (如果設定 SSL 卸載) 。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="2b6c1-120">示例</span><span class="sxs-lookup"><span data-stu-id="2b6c1-120">EXAMPLES</span></span>

### <span data-ttu-id="2b6c1-121">範例1：建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="2b6c1-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSetting -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="2b6c1-122">下列範例會先建立資源群組和虛擬網路，以及下列專案來建立應用程式閘道：</span><span class="sxs-lookup"><span data-stu-id="2b6c1-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="2b6c1-123">後端伺服器池</span><span class="sxs-lookup"><span data-stu-id="2b6c1-123">A back-end server pool</span></span>
- <span data-ttu-id="2b6c1-124">後端伺服器池設定</span><span class="sxs-lookup"><span data-stu-id="2b6c1-124">Back-end server pool settings</span></span>
- <span data-ttu-id="2b6c1-125">前端埠</span><span class="sxs-lookup"><span data-stu-id="2b6c1-125">Front-end ports</span></span>
- <span data-ttu-id="2b6c1-126">前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="2b6c1-126">Front-end IP addresses</span></span>
- <span data-ttu-id="2b6c1-127">要求路由規則</span><span class="sxs-lookup"><span data-stu-id="2b6c1-127">A request routing rule</span></span>

<span data-ttu-id="2b6c1-128">這四個命令會建立一個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="2b6c1-129">第一個命令會建立子網配置。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="2b6c1-130">第二個命令會建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="2b6c1-131">第三個命令會驗證子網設定，而第四個命令會驗證虛擬網路已順利建立。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="2b6c1-132">下列命令會建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="2b6c1-133">第一個命令會為先前建立的子網建立名為 GatewayIp01 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="2b6c1-134">第二個命令會使用後端 IP 位址清單來建立名為 Pool01 的後端伺服器池，並將該池儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="2b6c1-135">第三個命令會建立後端伺服器池的設定，並將設定儲存在 $PoolSetting 變數中。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="2b6c1-136">第四個命令會在埠80建立前端埠，將它命名為 FrontEndPort01，並將埠儲存在 $FrontEndPort 變數中。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="2b6c1-137">第五個命令會使用新的 AzPublicIpAddress 建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-137">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="2b6c1-138">第六個命令會使用 $PublicIp 建立前端 IP 設定，並將其命名為 FrontEndPortConfig01，並將它儲存在 $FrontEndIpConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="2b6c1-139">第七個命令會使用先前建立的 $FrontEndIpConfig $FrontEndPort 來建立偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="2b6c1-140">第八個命令會建立監聽程式的規則。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="2b6c1-141">第九個命令會設定 SKU。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="2b6c1-142">第10個命令會使用先前命令所設定的物件來建立閘道。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="2b6c1-143">參數</span><span class="sxs-lookup"><span data-stu-id="2b6c1-143">PARAMETERS</span></span>

### <span data-ttu-id="2b6c1-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b6c1-144">-AsJob</span></span>
<span data-ttu-id="2b6c1-145">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b6c1-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b6c1-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="2b6c1-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="2b6c1-147">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-147">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="2b6c1-148">-BackendAddressPools</span></span>
<span data-ttu-id="2b6c1-149">指定應用程式閘道的後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-149">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="2b6c1-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="2b6c1-151">指定應用程式閘道的後端 HTTP 設定清單。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6c1-152">-DefaultProfile</span></span>
<span data-ttu-id="2b6c1-153">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b6c1-154">-Force</span><span class="sxs-lookup"><span data-stu-id="2b6c1-154">-Force</span></span>
<span data-ttu-id="2b6c1-155">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b6c1-156">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="2b6c1-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="2b6c1-157">指定應用程式閘道的前端 IP 配置清單。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-158">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="2b6c1-158">-FrontendPorts</span></span>
<span data-ttu-id="2b6c1-159">指定應用程式閘道的前端埠清單。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-159">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-160">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="2b6c1-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="2b6c1-161">指定應用程式閘道的 IP 配置清單。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-161">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="2b6c1-162">-HttpListeners</span></span>
<span data-ttu-id="2b6c1-163">指定應用程式閘道的 HTTP 攔截器清單。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-164">-位置</span><span class="sxs-lookup"><span data-stu-id="2b6c1-164">-Location</span></span>
<span data-ttu-id="2b6c1-165">指定要在其中建立應用程式閘道的區域。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-165">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-166">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b6c1-166">-Name</span></span>
<span data-ttu-id="2b6c1-167">指定應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-167">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-168">-探針</span><span class="sxs-lookup"><span data-stu-id="2b6c1-168">-Probes</span></span>
<span data-ttu-id="2b6c1-169">指定應用程式閘道的探測器。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-169">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="2b6c1-170">-RedirectConfigurations</span></span>
<span data-ttu-id="2b6c1-171">重新導向配置清單</span><span class="sxs-lookup"><span data-stu-id="2b6c1-171">The list of redirect configuration</span></span>

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

### <span data-ttu-id="2b6c1-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="2b6c1-172">-RequestRoutingRules</span></span>
<span data-ttu-id="2b6c1-173">指定應用程式閘道的要求路由規則清單。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-173">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b6c1-174">-ResourceGroupName</span></span>
<span data-ttu-id="2b6c1-175">指定要在其中建立應用程式閘道的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-176">-Sku</span><span class="sxs-lookup"><span data-stu-id="2b6c1-176">-Sku</span></span>
<span data-ttu-id="2b6c1-177">指定應用程式閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="2b6c1-178">-SslCertificates</span></span>
<span data-ttu-id="2b6c1-179">指定 (SSL) 應用程式閘道憑證的安全通訊端層的清單。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="2b6c1-180">-SslPolicy</span></span>
<span data-ttu-id="2b6c1-181">指定應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-181">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b6c1-182">-Tag</span></span>
<span data-ttu-id="2b6c1-183">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b6c1-184">例如：</span><span class="sxs-lookup"><span data-stu-id="2b6c1-184">For example:</span></span>

<span data-ttu-id="2b6c1-185">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2b6c1-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2b6c1-186">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="2b6c1-186">-UrlPathMaps</span></span>
<span data-ttu-id="2b6c1-187">指定應用程式閘道的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-187">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="2b6c1-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b6c1-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="2b6c1-189">指定 (WAF) 設定的 web 應用程式防火牆。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="2b6c1-190">您可以使用 Get-AzApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 來取得 WAF。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-190">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="2b6c1-191">-確認</span><span class="sxs-lookup"><span data-stu-id="2b6c1-191">-Confirm</span></span>
<span data-ttu-id="2b6c1-192">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b6c1-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b6c1-193">-WhatIf</span></span>
<span data-ttu-id="2b6c1-194">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b6c1-195">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b6c1-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6c1-196">CommonParameters</span></span>
<span data-ttu-id="2b6c1-197">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6c1-198">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b6c1-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6c1-199">輸入</span><span class="sxs-lookup"><span data-stu-id="2b6c1-199">INPUTS</span></span>

## <span data-ttu-id="2b6c1-200">輸出</span><span class="sxs-lookup"><span data-stu-id="2b6c1-200">OUTPUTS</span></span>

### <span data-ttu-id="2b6c1-201">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2b6c1-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b6c1-202">筆記</span><span class="sxs-lookup"><span data-stu-id="2b6c1-202">NOTES</span></span>

## <span data-ttu-id="2b6c1-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b6c1-203">RELATED LINKS</span></span>

[<span data-ttu-id="2b6c1-204">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2b6c1-204">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="2b6c1-205">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2b6c1-205">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2b6c1-206">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2b6c1-206">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2b6c1-207">新-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2b6c1-207">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2b6c1-208">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2b6c1-208">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="2b6c1-209">新-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b6c1-209">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2b6c1-210">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2b6c1-210">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2b6c1-211">新-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2b6c1-211">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="2b6c1-212">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b6c1-212">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="2b6c1-213">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b6c1-213">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

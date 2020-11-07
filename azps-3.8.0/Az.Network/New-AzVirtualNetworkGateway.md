---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 3c30f7a341615b7e12843f3cd745cd691fa205aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959175"
---
# <span data-ttu-id="f268d-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f268d-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f268d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f268d-102">SYNOPSIS</span></span>
<span data-ttu-id="f268d-103">建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f268d-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="f268d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f268d-104">SYNTAX</span></span>

### <span data-ttu-id="f268d-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="f268d-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f268d-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f268d-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f268d-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f268d-107">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f268d-108">說明</span><span class="sxs-lookup"><span data-stu-id="f268d-108">DESCRIPTION</span></span>
<span data-ttu-id="f268d-109">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="f268d-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f268d-110">**新的-AzVirtualNetworkGateway** Cmdlet 會根據名稱、資源群組名稱、位置和 IP 設定以及閘道類型，以及 vpn 類型（如果 vpn），在 Azure 中建立閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="f268d-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="f268d-111">您也可以為閘道 SKU 命名。</span><span class="sxs-lookup"><span data-stu-id="f268d-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="f268d-112">如果此閘道是用來進行點對點連線，您也需要加入 VPN 用戶端位址集區，以便將位址指派給連線用戶端，以及用來驗證連接至閘道之 VPN 用戶端的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="f268d-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="f268d-113">您也可以選擇包含 BGP 與作用中的其他功能（例如 BGP 和作用中作用）。</span><span class="sxs-lookup"><span data-stu-id="f268d-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="f268d-114">示例</span><span class="sxs-lookup"><span data-stu-id="f268d-114">EXAMPLES</span></span>

### <span data-ttu-id="f268d-115">1：建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f268d-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f268d-116">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f268d-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f268d-117">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="f268d-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="f268d-118">2：使用外部 Radius 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f268d-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f268d-119">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f268d-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f268d-120">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="f268d-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f268d-121">它也會新增位址為 "TestRadiusServer" 的外部 radius 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f268d-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="f268d-122">它也會設定由客戶在閘道所指定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f268d-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f268d-123">3：使用 P2S 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f268d-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f268d-124">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及使用 P2S 設定（例如 VpnProtocol、VpnClientAddressPool、VpnClientRootCertificates、VpnClientIpsecPolicy 等）建立虛擬網路閘道。在 Azure 中。</span><span class="sxs-lookup"><span data-stu-id="f268d-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="f268d-125">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 配置儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型 "RouteBased" 和 sku "VpnGw1"。</span><span class="sxs-lookup"><span data-stu-id="f268d-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="f268d-126">Vpn 設定將會在閘道上設定（例如 VpnProtocol 設為 Ikev2、VpnClientAddressPool 為 "201.169.0.0/16"）、VpnClientRootCertificate 設定為傳遞一個： clientRootCertName 和自訂 vpn ipsec 原則： $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="f268d-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="f268d-127">它也會設定由客戶在閘道所指定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f268d-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f268d-128">4：使用 AAD 驗證配置建立虛擬網路閘道，以 VpnClient 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f268d-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="f268d-129">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f268d-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f268d-130">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="f268d-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f268d-131">它也會設定 AAD 驗證配置： AadTenantUri、AadIssuerUri 和 AadAudienceId，以 VpnClient 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f268d-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="f268d-132">5：使用 VpnGatewayGeneration 建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f268d-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="f268d-133">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f268d-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f268d-134">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在「ngwIPConfig」、「VPN」的閘道類型、vpn 類型「RouteBased」、sku "VpnGw4" 以及 VpnGatewayGeneration Generation2。</span><span class="sxs-lookup"><span data-stu-id="f268d-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="f268d-135">6：使用 IpConfigurationBgpPeeringAddresses 建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f268d-135">6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="f268d-136">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f268d-136">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f268d-137">ipconfigurationId1 的閘道 ipconfiguration 剛剛建立並儲存在 ngwipconfig 中。</span><span class="sxs-lookup"><span data-stu-id="f268d-137">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="f268d-138">閘道將會在 [英國西部] 位置的資源群組 "resourcegroup1resourcegroup1" 中稱為「gateway1」，並將先前建立的 IP 配置 Bgppeering 位址儲存在變數「gw1ipconfBgp1」、「VPN」的閘道類型、vpn 類型「RouteBased」、sku "VpnGw4" 以及 VpnGatewayGeneration Generation2 已啟用。</span><span class="sxs-lookup"><span data-stu-id="f268d-138">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="f268d-139">參數</span><span class="sxs-lookup"><span data-stu-id="f268d-139">PARAMETERS</span></span>

### <span data-ttu-id="f268d-140">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="f268d-140">-AadAudienceId</span></span>
<span data-ttu-id="f268d-141">P2S AAD 驗證選項： AadAudienceId。</span><span class="sxs-lookup"><span data-stu-id="f268d-141">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-142">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="f268d-142">-AadIssuerUri</span></span>
<span data-ttu-id="f268d-143">P2S AAD 驗證選項： AadIssuerUri。</span><span class="sxs-lookup"><span data-stu-id="f268d-143">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-144">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="f268d-144">-AadTenantUri</span></span>
<span data-ttu-id="f268d-145">P2S AAD 驗證選項： AadTenantUri。</span><span class="sxs-lookup"><span data-stu-id="f268d-145">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f268d-146">-AsJob</span></span>
<span data-ttu-id="f268d-147">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f268d-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f268d-148">-Asn</span><span class="sxs-lookup"><span data-stu-id="f268d-148">-Asn</span></span>
<span data-ttu-id="f268d-149">在 VPN 上針對 BGP 的虛擬網路閘道的 ASN</span><span class="sxs-lookup"><span data-stu-id="f268d-149">The virtual network gateway's ASN for BGP over VPN</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-150">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="f268d-150">-CustomRoute</span></span>
<span data-ttu-id="f268d-151">客戶指定的自訂路由 AddressPool</span><span class="sxs-lookup"><span data-stu-id="f268d-151">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f268d-152">-DefaultProfile</span></span>
<span data-ttu-id="f268d-153">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f268d-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f268d-154">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="f268d-154">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="f268d-155">在虛擬網路閘道上啟用作用中作用功能的標誌</span><span class="sxs-lookup"><span data-stu-id="f268d-155">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="f268d-156">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f268d-156">-EnableBgp</span></span>
<span data-ttu-id="f268d-157">EnableBgp 旗標</span><span class="sxs-lookup"><span data-stu-id="f268d-157">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-158">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f268d-158">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="f268d-159">在虛擬網路閘道上啟用專用 IPAddress 的標誌</span><span class="sxs-lookup"><span data-stu-id="f268d-159">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="f268d-160">-Force</span><span class="sxs-lookup"><span data-stu-id="f268d-160">-Force</span></span>
<span data-ttu-id="f268d-161">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="f268d-161">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f268d-162">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f268d-162">-GatewayDefaultSite</span></span>
<span data-ttu-id="f268d-163">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f268d-163">GatewayDefaultSite</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-164">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="f268d-164">-GatewaySku</span></span>
<span data-ttu-id="f268d-165">閘道 Sku 層</span><span class="sxs-lookup"><span data-stu-id="f268d-165">The Gateway Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-166">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="f268d-166">-GatewayType</span></span>
<span data-ttu-id="f268d-167">此虛擬網路閘道的類型： Vpn、ExoressRoute</span><span class="sxs-lookup"><span data-stu-id="f268d-167">The type of this virtual network gateway: Vpn, ExoressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-168">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="f268d-168">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="f268d-169">虛擬網路閘道 bgpsettings 的 BgpPeeringAddresses。</span><span class="sxs-lookup"><span data-stu-id="f268d-169">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-170">-Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="f268d-170">-IpConfigurations</span></span>
<span data-ttu-id="f268d-171">虛擬網路閘道的 Ipconfiguration。</span><span class="sxs-lookup"><span data-stu-id="f268d-171">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-172">-位置</span><span class="sxs-lookup"><span data-stu-id="f268d-172">-Location</span></span>
<span data-ttu-id="f268d-173">位於.</span><span class="sxs-lookup"><span data-stu-id="f268d-173">location.</span></span>

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

### <span data-ttu-id="f268d-174">-名稱</span><span class="sxs-lookup"><span data-stu-id="f268d-174">-Name</span></span>
<span data-ttu-id="f268d-175">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f268d-175">The resource name.</span></span>

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

### <span data-ttu-id="f268d-176">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f268d-176">-PeerWeight</span></span>
<span data-ttu-id="f268d-177">透過此虛擬網路閘道透過 BGP 所學到的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="f268d-177">The weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-178">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f268d-178">-RadiusServerAddress</span></span>
<span data-ttu-id="f268d-179">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="f268d-179">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-180">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f268d-180">-RadiusServerSecret</span></span>
<span data-ttu-id="f268d-181">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="f268d-181">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f268d-182">-ResourceGroupName</span></span>
<span data-ttu-id="f268d-183">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f268d-183">The resource group name.</span></span>

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

### <span data-ttu-id="f268d-184">-Tag</span><span class="sxs-lookup"><span data-stu-id="f268d-184">-Tag</span></span>
<span data-ttu-id="f268d-185">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="f268d-185">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f268d-186">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="f268d-186">-VpnClientAddressPool</span></span>
<span data-ttu-id="f268d-187">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="f268d-187">P2S VpnClient AddressPool</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-188">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f268d-188">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="f268d-189">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="f268d-189">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-190">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="f268d-190">-VpnClientProtocol</span></span>
<span data-ttu-id="f268d-191">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="f268d-191">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-192">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="f268d-192">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="f268d-193">要廢除的 VpnClientCertificates 清單。</span><span class="sxs-lookup"><span data-stu-id="f268d-193">The list of VpnClientCertificates to be revoked.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-194">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="f268d-194">-VpnClientRootCertificates</span></span>
<span data-ttu-id="f268d-195">要新增的 VpnClientRootCertificates 清單。</span><span class="sxs-lookup"><span data-stu-id="f268d-195">The list of VpnClientRootCertificates to be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-196">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f268d-196">-VpnGatewayGeneration</span></span>
<span data-ttu-id="f268d-197">此 VirtualNetwork VPN 閘道的產生。</span><span class="sxs-lookup"><span data-stu-id="f268d-197">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="f268d-198">如果 GatewayType 不是 VPN，則必須是 None。</span><span class="sxs-lookup"><span data-stu-id="f268d-198">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="f268d-199">-VpnType</span><span class="sxs-lookup"><span data-stu-id="f268d-199">-VpnType</span></span>
<span data-ttu-id="f268d-200">Vpn 類型： PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="f268d-200">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-201">-確認</span><span class="sxs-lookup"><span data-stu-id="f268d-201">-Confirm</span></span>
<span data-ttu-id="f268d-202">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f268d-202">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f268d-203">-WhatIf</span></span>
<span data-ttu-id="f268d-204">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f268d-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f268d-205">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f268d-205">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f268d-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f268d-206">CommonParameters</span></span>
<span data-ttu-id="f268d-207">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f268d-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f268d-208">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f268d-208">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f268d-209">輸入</span><span class="sxs-lookup"><span data-stu-id="f268d-209">INPUTS</span></span>

### <span data-ttu-id="f268d-210">System.object</span><span class="sxs-lookup"><span data-stu-id="f268d-210">System.String</span></span>

### <span data-ttu-id="f268d-211">PSVirtualNetworkGatewayIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f268d-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="f268d-212">System.object</span><span class="sxs-lookup"><span data-stu-id="f268d-212">System.Boolean</span></span>

### <span data-ttu-id="f268d-213">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f268d-213">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f268d-214">System.object []</span><span class="sxs-lookup"><span data-stu-id="f268d-214">System.String[]</span></span>

### <span data-ttu-id="f268d-215">PSVpnClientRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f268d-215">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="f268d-216">PSVpnClientRevokedCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f268d-216">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="f268d-217">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f268d-217">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f268d-218">UInt32</span><span class="sxs-lookup"><span data-stu-id="f268d-218">System.UInt32</span></span>

### <span data-ttu-id="f268d-219">System.object</span><span class="sxs-lookup"><span data-stu-id="f268d-219">System.Int32</span></span>

### <span data-ttu-id="f268d-220">PSIpConfigurationBgpPeeringAddress [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f268d-220">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="f268d-221">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f268d-221">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f268d-222">SecureString</span><span class="sxs-lookup"><span data-stu-id="f268d-222">System.Security.SecureString</span></span>

## <span data-ttu-id="f268d-223">輸出</span><span class="sxs-lookup"><span data-stu-id="f268d-223">OUTPUTS</span></span>

### <span data-ttu-id="f268d-224">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f268d-224">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f268d-225">筆記</span><span class="sxs-lookup"><span data-stu-id="f268d-225">NOTES</span></span>

## <span data-ttu-id="f268d-226">相關連結</span><span class="sxs-lookup"><span data-stu-id="f268d-226">RELATED LINKS</span></span>

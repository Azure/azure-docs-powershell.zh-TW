---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438799"
---
# <span data-ttu-id="6d2a3-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6d2a3-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="6d2a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2a3-103">建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6d2a3-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="6d2a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d2a3-104">SYNTAX</span></span>

### <span data-ttu-id="6d2a3-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="6d2a3-105">Default (Default)</span></span>
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

### <span data-ttu-id="6d2a3-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d2a3-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d2a3-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d2a3-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="6d2a3-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d2a3-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="6d2a3-109">說明</span><span class="sxs-lookup"><span data-stu-id="6d2a3-109">DESCRIPTION</span></span>
<span data-ttu-id="6d2a3-110">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="6d2a3-111">**新的-AzVirtualNetworkGateway** Cmdlet 會根據名稱、資源群組名稱、位置和 IP 設定以及閘道類型，以及 vpn 類型（如果 vpn），在 Azure 中建立閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="6d2a3-112">您也可以為閘道 SKU 命名。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="6d2a3-113">如果此閘道是用來進行點對點連線，您也需要加入 VPN 用戶端位址集區，以便將位址指派給連線用戶端，以及用來驗證連接至閘道之 VPN 用戶端的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="6d2a3-114">您也可以選擇包含 BGP 與作用中的其他功能（例如 BGP 和作用中作用）。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="6d2a3-115">示例</span><span class="sxs-lookup"><span data-stu-id="6d2a3-115">EXAMPLES</span></span>

### <span data-ttu-id="6d2a3-116">範例1：建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6d2a3-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="6d2a3-117">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="6d2a3-118">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="6d2a3-119">範例2：使用外部 Radius 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6d2a3-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="6d2a3-120">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="6d2a3-121">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="6d2a3-122">它也會新增位址為 "TestRadiusServer" 的外部 radius 伺服器。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="6d2a3-123">它也會設定由客戶在閘道所指定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="6d2a3-124">範例3：使用 P2S 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6d2a3-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
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

<span data-ttu-id="6d2a3-125">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及使用 P2S 設定（例如 VpnProtocol、VpnClientAddressPool、VpnClientRootCertificates、VpnClientIpsecPolicy 等）建立虛擬網路閘道。在 Azure 中。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="6d2a3-126">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 配置儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型 "RouteBased" 和 sku "VpnGw1"。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="6d2a3-127">Vpn 設定將會在閘道上設定（例如 VpnProtocol 設為 Ikev2、VpnClientAddressPool 為 "201.169.0.0/16"）、VpnClientRootCertificate 設定為傳遞一個： clientRootCertName 和自訂 vpn ipsec 原則： $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="6d2a3-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="6d2a3-128">它也會設定由客戶在閘道所指定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="6d2a3-129">範例4：使用 AAD 驗證設定建立虛擬網路閘道，以 VpnClient 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="6d2a3-130">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="6d2a3-131">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="6d2a3-132">它也會設定 AAD 驗證配置： AadTenantUri、AadIssuerUri 和 AadAudienceId，以 VpnClient 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="6d2a3-133">範例5：使用 VpnGatewayGeneration 建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6d2a3-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="6d2a3-134">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="6d2a3-135">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在「ngwIPConfig」、「VPN」的閘道類型、vpn 類型「RouteBased」、sku "VpnGw4" 以及 VpnGatewayGeneration Generation2。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="6d2a3-136">範例6：使用 IpConfigurationBgpPeeringAddresses 建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6d2a3-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
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

<span data-ttu-id="6d2a3-137">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="6d2a3-138">ipconfigurationId1 的閘道 ipconfiguration 剛剛建立並儲存在 ngwipconfig 中。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="6d2a3-139">閘道將會在 [英國西部] 位置的資源群組 "resourcegroup1resourcegroup1" 中稱為「gateway1」，並將先前建立的 IP 配置 Bgppeering 位址儲存在變數「gw1ipconfBgp1」、「VPN」的閘道類型、vpn 類型「RouteBased」、sku "VpnGw4" 以及 VpnGatewayGeneration Generation2 已啟用。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="6d2a3-140">參數</span><span class="sxs-lookup"><span data-stu-id="6d2a3-140">PARAMETERS</span></span>

### <span data-ttu-id="6d2a3-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="6d2a3-141">-AadAudienceId</span></span>
<span data-ttu-id="6d2a3-142">P2S AAD 驗證選項： AadAudienceId。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="6d2a3-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="6d2a3-143">-AadIssuerUri</span></span>
<span data-ttu-id="6d2a3-144">P2S AAD 驗證選項： AadIssuerUri。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="6d2a3-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="6d2a3-145">-AadTenantUri</span></span>
<span data-ttu-id="6d2a3-146">P2S AAD 驗證選項： AadTenantUri。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="6d2a3-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d2a3-147">-AsJob</span></span>
<span data-ttu-id="6d2a3-148">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6d2a3-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d2a3-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="6d2a3-149">-Asn</span></span>
<span data-ttu-id="6d2a3-150">在 VPN 上針對 BGP 的虛擬網路閘道的 ASN</span><span class="sxs-lookup"><span data-stu-id="6d2a3-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="6d2a3-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="6d2a3-151">-CustomRoute</span></span>
<span data-ttu-id="6d2a3-152">客戶指定的自訂路由 AddressPool</span><span class="sxs-lookup"><span data-stu-id="6d2a3-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="6d2a3-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2a3-153">-DefaultProfile</span></span>
<span data-ttu-id="6d2a3-154">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d2a3-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="6d2a3-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="6d2a3-156">在虛擬網路閘道上啟用作用中作用功能的標誌</span><span class="sxs-lookup"><span data-stu-id="6d2a3-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="6d2a3-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6d2a3-157">-EnableBgp</span></span>
<span data-ttu-id="6d2a3-158">EnableBgp 旗標</span><span class="sxs-lookup"><span data-stu-id="6d2a3-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="6d2a3-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d2a3-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="6d2a3-160">在虛擬網路閘道上啟用專用 IPAddress 的標誌</span><span class="sxs-lookup"><span data-stu-id="6d2a3-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="6d2a3-161">-Force</span><span class="sxs-lookup"><span data-stu-id="6d2a3-161">-Force</span></span>
<span data-ttu-id="6d2a3-162">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="6d2a3-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6d2a3-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="6d2a3-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="6d2a3-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="6d2a3-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="6d2a3-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="6d2a3-165">-GatewaySku</span></span>
<span data-ttu-id="6d2a3-166">閘道 Sku 層</span><span class="sxs-lookup"><span data-stu-id="6d2a3-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="6d2a3-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="6d2a3-167">-GatewayType</span></span>
<span data-ttu-id="6d2a3-168">此虛擬網路閘道的類型： Vpn、ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6d2a3-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="6d2a3-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="6d2a3-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="6d2a3-170">虛擬網路閘道 bgpsettings 的 BgpPeeringAddresses。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="6d2a3-171">-Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="6d2a3-171">-IpConfigurations</span></span>
<span data-ttu-id="6d2a3-172">虛擬網路閘道的 Ipconfiguration。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="6d2a3-173">-位置</span><span class="sxs-lookup"><span data-stu-id="6d2a3-173">-Location</span></span>
<span data-ttu-id="6d2a3-174">位於.</span><span class="sxs-lookup"><span data-stu-id="6d2a3-174">location.</span></span>

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

### <span data-ttu-id="6d2a3-175">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d2a3-175">-Name</span></span>
<span data-ttu-id="6d2a3-176">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-176">The resource name.</span></span>

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

### <span data-ttu-id="6d2a3-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="6d2a3-177">-PeerWeight</span></span>
<span data-ttu-id="6d2a3-178">透過此虛擬網路閘道透過 BGP 所學到的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="6d2a3-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="6d2a3-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="6d2a3-179">-RadiusServerAddress</span></span>
<span data-ttu-id="6d2a3-180">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="6d2a3-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="6d2a3-181">-RadiusServerList</span></span>
<span data-ttu-id="6d2a3-182">P2S 多個外部 Radius 伺服器伺服器。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-182">P2S multiple external Radius server servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d2a3-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="6d2a3-183">-RadiusServerSecret</span></span>
<span data-ttu-id="6d2a3-184">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="6d2a3-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d2a3-185">-ResourceGroupName</span></span>
<span data-ttu-id="6d2a3-186">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-186">The resource group name.</span></span>

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

### <span data-ttu-id="6d2a3-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="6d2a3-187">-Tag</span></span>
<span data-ttu-id="6d2a3-188">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6d2a3-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="6d2a3-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="6d2a3-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="6d2a3-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="6d2a3-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="6d2a3-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="6d2a3-192">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="6d2a3-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="6d2a3-193">-VpnClientProtocol</span></span>
<span data-ttu-id="6d2a3-194">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="6d2a3-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="6d2a3-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="6d2a3-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="6d2a3-196">要廢除的 VpnClientCertificates 清單。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="6d2a3-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="6d2a3-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="6d2a3-198">要新增的 VpnClientRootCertificates 清單。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="6d2a3-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="6d2a3-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="6d2a3-200">此 VirtualNetwork VPN 閘道的產生。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="6d2a3-201">如果 GatewayType 不是 VPN，則必須是 None。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="6d2a3-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="6d2a3-202">-VpnType</span></span>
<span data-ttu-id="6d2a3-203">Vpn 類型： PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="6d2a3-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="6d2a3-204">-確認</span><span class="sxs-lookup"><span data-stu-id="6d2a3-204">-Confirm</span></span>
<span data-ttu-id="6d2a3-205">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d2a3-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d2a3-206">-WhatIf</span></span>
<span data-ttu-id="6d2a3-207">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d2a3-208">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d2a3-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2a3-209">CommonParameters</span></span>
<span data-ttu-id="6d2a3-210">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2a3-211">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6d2a3-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2a3-212">輸入</span><span class="sxs-lookup"><span data-stu-id="6d2a3-212">INPUTS</span></span>

### <span data-ttu-id="6d2a3-213">System.object</span><span class="sxs-lookup"><span data-stu-id="6d2a3-213">System.String</span></span>

### <span data-ttu-id="6d2a3-214">PSVirtualNetworkGatewayIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6d2a3-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="6d2a3-215">System.object</span><span class="sxs-lookup"><span data-stu-id="6d2a3-215">System.Boolean</span></span>

### <span data-ttu-id="6d2a3-216">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6d2a3-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="6d2a3-217">System.object []</span><span class="sxs-lookup"><span data-stu-id="6d2a3-217">System.String[]</span></span>

### <span data-ttu-id="6d2a3-218">PSVpnClientRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6d2a3-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="6d2a3-219">PSVpnClientRevokedCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6d2a3-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="6d2a3-220">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6d2a3-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="6d2a3-221">UInt32</span><span class="sxs-lookup"><span data-stu-id="6d2a3-221">System.UInt32</span></span>

### <span data-ttu-id="6d2a3-222">System.object</span><span class="sxs-lookup"><span data-stu-id="6d2a3-222">System.Int32</span></span>

### <span data-ttu-id="6d2a3-223">PSIpConfigurationBgpPeeringAddress [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6d2a3-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="6d2a3-224">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6d2a3-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6d2a3-225">SecureString</span><span class="sxs-lookup"><span data-stu-id="6d2a3-225">System.Security.SecureString</span></span>

## <span data-ttu-id="6d2a3-226">輸出</span><span class="sxs-lookup"><span data-stu-id="6d2a3-226">OUTPUTS</span></span>

### <span data-ttu-id="6d2a3-227">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6d2a3-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6d2a3-228">筆記</span><span class="sxs-lookup"><span data-stu-id="6d2a3-228">NOTES</span></span>

## <span data-ttu-id="6d2a3-229">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d2a3-229">RELATED LINKS</span></span>

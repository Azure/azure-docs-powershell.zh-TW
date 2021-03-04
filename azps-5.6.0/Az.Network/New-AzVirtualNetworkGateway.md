---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c9729dd81dc5ff287ab032fdce6ad937c282e1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908393"
---
# <span data-ttu-id="f1f0d-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1f0d-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f1f0d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f0d-103">建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f1f0d-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="f1f0d-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1f0d-104">SYNTAX</span></span>

### <span data-ttu-id="f1f0d-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="f1f0d-105">Default (Default)</span></span>
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

### <span data-ttu-id="f1f0d-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1f0d-106">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="f1f0d-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1f0d-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="f1f0d-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1f0d-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="f1f0d-109">描述</span><span class="sxs-lookup"><span data-stu-id="f1f0d-109">DESCRIPTION</span></span>
<span data-ttu-id="f1f0d-110">虛擬網路閘道是代表 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f1f0d-111">**New-AzVirtualNetworkGateway** Cmdlet 會依據名稱、資源組名、位置和 IP 組式，以及閘道類型以及 VPN 類型 ，在 Azure 中建立閘道物件。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="f1f0d-112">您也可以為閘道 SKU 命名。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="f1f0d-113">如果此閘道用於點對網站連接，您也需要包含 VPN 用戶端位址集區，以指派位址給連接用戶端，以及用來驗證 VPN 用戶端連接至閘道的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="f1f0d-114">您也可以選擇包含 BGP 和 Active-Active 等其他功能。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="f1f0d-115">例子</span><span class="sxs-lookup"><span data-stu-id="f1f0d-115">EXAMPLES</span></span>

### <span data-ttu-id="f1f0d-116">範例 1：建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f1f0d-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f1f0d-117">上述步驟將建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及建立 Azure 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f1f0d-118">閘道在資源群組 "vnet-gateway" 中稱為 "myNGW"，位置為 "UK West"，先前建立 IP 組式會儲存于變數 "ngwIPConfig"，即閘道類型 "VPN"，vpn 類型 "RouteBased" 和 SKU "Basic"。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="f1f0d-119">範例 2：建立具有外部弧線配置的虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f1f0d-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="f1f0d-120">上述步驟將建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及建立 Azure 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f1f0d-121">閘道在資源群組 "vnet-gateway" 中稱為 "myNGW"，位置為 "UK West"，先前建立 IP 組式會儲存于變數 "ngwIPConfig"，即閘道類型 "VPN"，vpn 類型 "RouteBased" 和 SKU "Basic"。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f1f0d-122">它也新增位址為 "TestRadiusServer" 的外部弧線伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="f1f0d-123">它也將會設定客戶在閘道上指定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f1f0d-124">範例 3：使用 P2S 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f1f0d-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="f1f0d-125">上述將建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及建立具有 P2S 設定之虛擬網路閘道，例如 Azure 中的 VpnProtocol、VpnClientAddressPool、VpnClientRootCertificates、VpnClientIpsecPolicy 等。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="f1f0d-126">閘道在資源群組 「vnet-gateway」中稱為「myNGW」，位置為「英國西部」，且先前建立 IP 組式會儲存于變數「ngwIPConfig」、閘道類型「VPN」、vpn 類型「RouteBased」和 SKU 「VpnGw1」。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="f1f0d-127">Vpn 設定將在閘道上設定，例如 VpnProtocol set as Ikev2，VpnClientAddressPool as "201.169.0.0/16"， VpnClientRootCertificate set as passed one： clientRootCertName and custom vpn ipsec policy passed in object：$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="f1f0d-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="f1f0d-128">它也將會設定客戶在閘道上指定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f1f0d-129">範例 4：使用虛擬網路閘道的 VpnClient 的 AAD 驗證組建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="f1f0d-130">上述步驟將建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及建立 Azure 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f1f0d-131">閘道在資源群組 "vnet-gateway" 中稱為 "myNGW"，位置為 "UK West"，先前建立 IP 組式會儲存于變數 "ngwIPConfig"，即閘道類型 "VPN"，vpn 類型 "RouteBased" 和 SKU "Basic"。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f1f0d-132">它也設定 AAD 驗證設定：AadTenantUri、AadIssuerUri 和 AadAudienceId for VpnClient 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="f1f0d-133">範例 5：使用 VpnGatewayGeneration 建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f1f0d-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="f1f0d-134">上述步驟將建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及建立 Azure 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f1f0d-135">閘道在資源群組 "vnet-gateway" 中稱為"myNGW"，位置為"英國西部"，先前建立 IP 組式會儲存于變數 "ngwIPConfig"，即閘道類型 "VPN"，vpn 類型 "RouteBased"，SKU "VpnGw4" 和 VpnGatewayGeneration Generation2 啟用。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="f1f0d-136">範例 6：使用 IpConfigurationBgpPeeringAddresses 建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f1f0d-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
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

<span data-ttu-id="f1f0d-137">上述步驟將建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及建立 Azure 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f1f0d-138">ipconfigurationId1 的閘道 ipconfigururation 剛剛建立並儲存在 ngwipconfig 中。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="f1f0d-139">閘道在資源群組"resourcegroup1resourcegroup1"中稱為「閘道1」，位置為「英國西部」，且先前所建立 IP 組式 Bgppeering 位址儲存于變數 "gw1ipconfBgp1"，即閘道類型的"VPN"，即 vpn 類型 "RouteBased"，SKU "VpnGw4" 和 VpnGatewayGeneration Generation2 啟用。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="f1f0d-140">參數</span><span class="sxs-lookup"><span data-stu-id="f1f0d-140">PARAMETERS</span></span>

### <span data-ttu-id="f1f0d-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="f1f0d-141">-AadAudienceId</span></span>
<span data-ttu-id="f1f0d-142">P2S AAD 驗證選項：AadAudienceId。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="f1f0d-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="f1f0d-143">-AadIssuerUri</span></span>
<span data-ttu-id="f1f0d-144">P2S AAD 驗證選項：AadIssuerUri。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="f1f0d-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="f1f0d-145">-AadTenantUri</span></span>
<span data-ttu-id="f1f0d-146">P2S AAD 驗證選項：AadTenantUri。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="f1f0d-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1f0d-147">-AsJob</span></span>
<span data-ttu-id="f1f0d-148">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f1f0d-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1f0d-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="f1f0d-149">-Asn</span></span>
<span data-ttu-id="f1f0d-150">虛擬網路閘道的 ASN for BGP over VPN</span><span class="sxs-lookup"><span data-stu-id="f1f0d-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="f1f0d-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="f1f0d-151">-CustomRoute</span></span>
<span data-ttu-id="f1f0d-152">客戶指定的自訂路由 AddressPool</span><span class="sxs-lookup"><span data-stu-id="f1f0d-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="f1f0d-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f0d-153">-DefaultProfile</span></span>
<span data-ttu-id="f1f0d-154">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f0d-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="f1f0d-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="f1f0d-156">在虛擬網路閘道上啟用 Active Active 功能的標誌</span><span class="sxs-lookup"><span data-stu-id="f1f0d-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="f1f0d-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f1f0d-157">-EnableBgp</span></span>
<span data-ttu-id="f1f0d-158">EnableBgp 旗標</span><span class="sxs-lookup"><span data-stu-id="f1f0d-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="f1f0d-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f1f0d-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="f1f0d-160">在虛擬網路閘道上啟用私人 IPAddress 的標標</span><span class="sxs-lookup"><span data-stu-id="f1f0d-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="f1f0d-161">-強制</span><span class="sxs-lookup"><span data-stu-id="f1f0d-161">-Force</span></span>
<span data-ttu-id="f1f0d-162">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="f1f0d-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f1f0d-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f1f0d-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="f1f0d-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f1f0d-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="f1f0d-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="f1f0d-165">-GatewaySku</span></span>
<span data-ttu-id="f1f0d-166">閘道 SKU 層</span><span class="sxs-lookup"><span data-stu-id="f1f0d-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="f1f0d-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="f1f0d-167">-GatewayType</span></span>
<span data-ttu-id="f1f0d-168">此虛擬網路閘道的類型：Vpn、ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f1f0d-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="f1f0d-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="f1f0d-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="f1f0d-170">BgpPeeringAddresses for Virtual Network gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="f1f0d-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="f1f0d-171">-IpConfigurations</span></span>
<span data-ttu-id="f1f0d-172">虛擬網路閘道的 IpConfigurations。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="f1f0d-173">-位置</span><span class="sxs-lookup"><span data-stu-id="f1f0d-173">-Location</span></span>
<span data-ttu-id="f1f0d-174">位置。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-174">location.</span></span>

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

### <span data-ttu-id="f1f0d-175">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1f0d-175">-Name</span></span>
<span data-ttu-id="f1f0d-176">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-176">The resource name.</span></span>

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

### <span data-ttu-id="f1f0d-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f1f0d-177">-PeerWeight</span></span>
<span data-ttu-id="f1f0d-178">從這個虛擬網路閘道從 BGP 得知的路由所增加的權重</span><span class="sxs-lookup"><span data-stu-id="f1f0d-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="f1f0d-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f1f0d-179">-RadiusServerAddress</span></span>
<span data-ttu-id="f1f0d-180">P2S 外部範圍伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="f1f0d-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="f1f0d-181">-RadiusServerList</span></span>
<span data-ttu-id="f1f0d-182">P2S 多個外部弧線伺服器伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="f1f0d-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f1f0d-183">-RadiusServerSecret</span></span>
<span data-ttu-id="f1f0d-184">P2S 外部弧線伺服器機密。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="f1f0d-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f0d-185">-ResourceGroupName</span></span>
<span data-ttu-id="f1f0d-186">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-186">The resource group name.</span></span>

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

### <span data-ttu-id="f1f0d-187">-標記</span><span class="sxs-lookup"><span data-stu-id="f1f0d-187">-Tag</span></span>
<span data-ttu-id="f1f0d-188">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f1f0d-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="f1f0d-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="f1f0d-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="f1f0d-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="f1f0d-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f1f0d-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="f1f0d-192">P2S VPN 用戶端用戶端服務通訊協定之 IPSec 策略清單。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="f1f0d-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="f1f0d-193">-VpnClientProtocol</span></span>
<span data-ttu-id="f1f0d-194">P2S VPN 用戶端路由通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="f1f0d-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="f1f0d-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="f1f0d-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="f1f0d-196">要撤銷的 VpnClientCertificates 清單。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="f1f0d-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="f1f0d-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="f1f0d-198">要新增的 VpnClientRootCertificates 清單。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="f1f0d-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f1f0d-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="f1f0d-200">此 VirtualNetwork VPN 閘道的新一代。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="f1f0d-201">如果 GatewayType 不是 VPN，則必須為 None。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="f1f0d-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="f1f0d-202">-VpnType</span></span>
<span data-ttu-id="f1f0d-203">Vpn：PolicyBased/RouteBased 的類型</span><span class="sxs-lookup"><span data-stu-id="f1f0d-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="f1f0d-204">-確認</span><span class="sxs-lookup"><span data-stu-id="f1f0d-204">-Confirm</span></span>
<span data-ttu-id="f1f0d-205">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f0d-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f0d-206">-WhatIf</span></span>
<span data-ttu-id="f1f0d-207">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f0d-208">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f0d-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f0d-209">CommonParameters</span></span>
<span data-ttu-id="f1f0d-210">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1f0d-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f0d-211">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1f0d-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f0d-212">輸入</span><span class="sxs-lookup"><span data-stu-id="f1f0d-212">INPUTS</span></span>

### <span data-ttu-id="f1f0d-213">System.String</span><span class="sxs-lookup"><span data-stu-id="f1f0d-213">System.String</span></span>

### <span data-ttu-id="f1f0d-214">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="f1f0d-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="f1f0d-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1f0d-215">System.Boolean</span></span>

### <span data-ttu-id="f1f0d-216">Microsoft.Azure.Commands.Network.models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1f0d-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f1f0d-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f1f0d-217">System.String[]</span></span>

### <span data-ttu-id="f1f0d-218">Microsoft.Azure.Commands.network.models.PS VpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="f1f0d-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="f1f0d-219">Microsoft.Azure.Commands.Network.models.PS VpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="f1f0d-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="f1f0d-220">Microsoft.Azure.Commands.Network.models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="f1f0d-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f1f0d-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="f1f0d-221">System.UInt32</span></span>

### <span data-ttu-id="f1f0d-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f1f0d-222">System.Int32</span></span>

### <span data-ttu-id="f1f0d-223">Microsoft.Azure.Commands.Network.models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="f1f0d-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="f1f0d-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1f0d-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f1f0d-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="f1f0d-225">System.Security.SecureString</span></span>

## <span data-ttu-id="f1f0d-226">輸出</span><span class="sxs-lookup"><span data-stu-id="f1f0d-226">OUTPUTS</span></span>

### <span data-ttu-id="f1f0d-227">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1f0d-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f1f0d-228">筆記</span><span class="sxs-lookup"><span data-stu-id="f1f0d-228">NOTES</span></span>

## <span data-ttu-id="f1f0d-229">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1f0d-229">RELATED LINKS</span></span>

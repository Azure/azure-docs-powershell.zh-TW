---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 75857d2c97ace9b06e3f7cdd7f672ac35a6fe34e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789250"
---
# <span data-ttu-id="c26e6-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c26e6-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c26e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c26e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c26e6-103">建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c26e6-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="c26e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c26e6-104">SYNTAX</span></span>

### <span data-ttu-id="c26e6-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c26e6-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c26e6-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c26e6-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c26e6-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="c26e6-107">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c26e6-108">說明</span><span class="sxs-lookup"><span data-stu-id="c26e6-108">DESCRIPTION</span></span>
<span data-ttu-id="c26e6-109">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="c26e6-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="c26e6-110">**新的-AzVirtualNetworkGateway** Cmdlet 會根據名稱、資源群組名稱、位置和 IP 設定以及閘道類型，以及 vpn 類型（如果 vpn），在 Azure 中建立閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="c26e6-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="c26e6-111">您也可以為閘道 SKU 命名。</span><span class="sxs-lookup"><span data-stu-id="c26e6-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="c26e6-112">如果此閘道是用來進行點對點連線，您也需要加入 VPN 用戶端位址集區，以便將位址指派給連線用戶端，以及用來驗證連接至閘道之 VPN 用戶端的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="c26e6-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="c26e6-113">您也可以選擇包含 BGP 與作用中的其他功能（例如 BGP 和作用中作用）。</span><span class="sxs-lookup"><span data-stu-id="c26e6-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="c26e6-114">示例</span><span class="sxs-lookup"><span data-stu-id="c26e6-114">EXAMPLES</span></span>

### <span data-ttu-id="c26e6-115">1：建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c26e6-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="c26e6-116">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c26e6-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="c26e6-117">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="c26e6-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="c26e6-118">2：使用外部 Radius 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c26e6-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="c26e6-119">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c26e6-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="c26e6-120">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="c26e6-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="c26e6-121">它也會新增位址為 "TestRadiusServer" 的外部 radius 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c26e6-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="c26e6-122">它也會設定由客戶在閘道所指定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="c26e6-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="c26e6-123">3：使用 P2S 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c26e6-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="c26e6-124">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及使用 P2S 設定（例如 VpnProtocol、VpnClientAddressPool、VpnClientRootCertificates、VpnClientIpsecPolicy 等）建立虛擬網路閘道。在 Azure 中。</span><span class="sxs-lookup"><span data-stu-id="c26e6-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="c26e6-125">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 配置儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型 "RouteBased" 和 sku "VpnGw1"。</span><span class="sxs-lookup"><span data-stu-id="c26e6-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="c26e6-126">Vpn 設定將會在閘道上設定（例如 VpnProtocol 設為 Ikev2、VpnClientAddressPool 為 "201.169.0.0/16"）、VpnClientRootCertificate 設定為傳遞一個： clientRootCertName 和自訂 vpn ipsec 原則： $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="c26e6-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="c26e6-127">它也會設定由客戶在閘道所指定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="c26e6-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="c26e6-128">4：使用 AAD 驗證配置建立虛擬網路閘道，以 VpnClient 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c26e6-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="c26e6-129">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c26e6-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="c26e6-130">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="c26e6-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="c26e6-131">它也會設定 AAD 驗證配置： AadTenantUri、AadIssuerUri 和 AadAudienceId，以 VpnClient 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c26e6-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="c26e6-132">5：使用 VpnGatewayGeneration 建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c26e6-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="c26e6-133">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c26e6-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="c26e6-134">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在「ngwIPConfig」、「VPN」的閘道類型、vpn 類型「RouteBased」、sku "VpnGw4" 以及 VpnGatewayGeneration Generation2。</span><span class="sxs-lookup"><span data-stu-id="c26e6-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="c26e6-135">參數</span><span class="sxs-lookup"><span data-stu-id="c26e6-135">PARAMETERS</span></span>

### <span data-ttu-id="c26e6-136">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="c26e6-136">-AadAudienceId</span></span>
<span data-ttu-id="c26e6-137">P2S AAD 驗證選項： AadAudienceId。</span><span class="sxs-lookup"><span data-stu-id="c26e6-137">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="c26e6-138">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="c26e6-138">-AadIssuerUri</span></span>
<span data-ttu-id="c26e6-139">P2S AAD 驗證選項： AadIssuerUri。</span><span class="sxs-lookup"><span data-stu-id="c26e6-139">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="c26e6-140">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="c26e6-140">-AadTenantUri</span></span>
<span data-ttu-id="c26e6-141">P2S AAD 驗證選項： AadTenantUri。</span><span class="sxs-lookup"><span data-stu-id="c26e6-141">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="c26e6-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c26e6-142">-AsJob</span></span>
<span data-ttu-id="c26e6-143">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c26e6-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c26e6-144">-Asn</span><span class="sxs-lookup"><span data-stu-id="c26e6-144">-Asn</span></span>

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

### <span data-ttu-id="c26e6-145">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="c26e6-145">-CustomRoute</span></span>
<span data-ttu-id="c26e6-146">客戶指定的自訂路由 AddressPool</span><span class="sxs-lookup"><span data-stu-id="c26e6-146">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="c26e6-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26e6-147">-DefaultProfile</span></span>
<span data-ttu-id="c26e6-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c26e6-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c26e6-149">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c26e6-149">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="c26e6-150">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="c26e6-150">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="c26e6-151">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c26e6-151">-EnableBgp</span></span>

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

### <span data-ttu-id="c26e6-152">-Force</span><span class="sxs-lookup"><span data-stu-id="c26e6-152">-Force</span></span>
<span data-ttu-id="c26e6-153">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c26e6-153">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c26e6-154">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c26e6-154">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="c26e6-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="c26e6-155">-GatewaySku</span></span>

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

### <span data-ttu-id="c26e6-156">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="c26e6-156">-GatewayType</span></span>

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

### <span data-ttu-id="c26e6-157">-Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="c26e6-157">-IpConfigurations</span></span>

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

### <span data-ttu-id="c26e6-158">-位置</span><span class="sxs-lookup"><span data-stu-id="c26e6-158">-Location</span></span>

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

### <span data-ttu-id="c26e6-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="c26e6-159">-Name</span></span>

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

### <span data-ttu-id="c26e6-160">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c26e6-160">-PeerWeight</span></span>

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

### <span data-ttu-id="c26e6-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c26e6-161">-RadiusServerAddress</span></span>
<span data-ttu-id="c26e6-162">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="c26e6-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="c26e6-163">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c26e6-163">-RadiusServerSecret</span></span>
<span data-ttu-id="c26e6-164">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="c26e6-164">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="c26e6-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c26e6-165">-ResourceGroupName</span></span>

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

### <span data-ttu-id="c26e6-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="c26e6-166">-Tag</span></span>
<span data-ttu-id="c26e6-167">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c26e6-167">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c26e6-168">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c26e6-168">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c26e6-169">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="c26e6-169">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="c26e6-170">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c26e6-170">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="c26e6-171">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="c26e6-171">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c26e6-172">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="c26e6-172">-VpnClientProtocol</span></span>
<span data-ttu-id="c26e6-173">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="c26e6-173">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="c26e6-174">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="c26e6-174">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="c26e6-175">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="c26e6-175">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="c26e6-176">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="c26e6-176">-VpnGatewayGeneration</span></span>
<span data-ttu-id="c26e6-177">此 VirtualNetwork VPN 閘道的產生。</span><span class="sxs-lookup"><span data-stu-id="c26e6-177">The generation for this VirtualNetwork VPN gateway.</span></span> <span data-ttu-id="c26e6-178">如果 GatewayType 不是 VPN，則必須是 None。</span><span class="sxs-lookup"><span data-stu-id="c26e6-178">Must be None if GatewayType is not VPN.</span></span> <span data-ttu-id="c26e6-179">設定之後，就無法在閘道的生命週期中變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c26e6-179">Once set, this property cannot be changed over the lifetime of the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, Generation1, Generation2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26e6-180">-VpnType</span><span class="sxs-lookup"><span data-stu-id="c26e6-180">-VpnType</span></span>

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

### <span data-ttu-id="c26e6-181">-確認</span><span class="sxs-lookup"><span data-stu-id="c26e6-181">-Confirm</span></span>
<span data-ttu-id="c26e6-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c26e6-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c26e6-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c26e6-183">-WhatIf</span></span>
<span data-ttu-id="c26e6-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c26e6-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c26e6-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c26e6-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c26e6-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26e6-186">CommonParameters</span></span>
<span data-ttu-id="c26e6-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c26e6-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26e6-188">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c26e6-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26e6-189">輸入</span><span class="sxs-lookup"><span data-stu-id="c26e6-189">INPUTS</span></span>

### <span data-ttu-id="c26e6-190">System.object</span><span class="sxs-lookup"><span data-stu-id="c26e6-190">System.String</span></span>

### <span data-ttu-id="c26e6-191">PSVirtualNetworkGatewayIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="c26e6-191">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="c26e6-192">System.object</span><span class="sxs-lookup"><span data-stu-id="c26e6-192">System.Boolean</span></span>

### <span data-ttu-id="c26e6-193">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c26e6-193">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="c26e6-194">System.object []</span><span class="sxs-lookup"><span data-stu-id="c26e6-194">System.String[]</span></span>

### <span data-ttu-id="c26e6-195">PSVpnClientRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="c26e6-195">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="c26e6-196">PSVpnClientRevokedCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="c26e6-196">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="c26e6-197">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="c26e6-197">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="c26e6-198">UInt32</span><span class="sxs-lookup"><span data-stu-id="c26e6-198">System.UInt32</span></span>

### <span data-ttu-id="c26e6-199">System.object</span><span class="sxs-lookup"><span data-stu-id="c26e6-199">System.Int32</span></span>

### <span data-ttu-id="c26e6-200">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c26e6-200">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c26e6-201">SecureString</span><span class="sxs-lookup"><span data-stu-id="c26e6-201">System.Security.SecureString</span></span>

## <span data-ttu-id="c26e6-202">輸出</span><span class="sxs-lookup"><span data-stu-id="c26e6-202">OUTPUTS</span></span>

### <span data-ttu-id="c26e6-203">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c26e6-203">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c26e6-204">筆記</span><span class="sxs-lookup"><span data-stu-id="c26e6-204">NOTES</span></span>

## <span data-ttu-id="c26e6-205">相關連結</span><span class="sxs-lookup"><span data-stu-id="c26e6-205">RELATED LINKS</span></span>

[<span data-ttu-id="c26e6-206">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c26e6-206">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c26e6-207">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c26e6-207">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c26e6-208">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c26e6-208">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c26e6-209">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c26e6-209">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c26e6-210">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c26e6-210">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

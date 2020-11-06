---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9b8ee02cbe28784ff1fd5789881dd62add62d674
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621707"
---
# <span data-ttu-id="2fe16-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2fe16-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="2fe16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fe16-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe16-103">建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="2fe16-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="2fe16-104">句法</span><span class="sxs-lookup"><span data-stu-id="2fe16-104">SYNTAX</span></span>

### <span data-ttu-id="2fe16-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="2fe16-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fe16-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fe16-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fe16-107">說明</span><span class="sxs-lookup"><span data-stu-id="2fe16-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe16-108">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="2fe16-108">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="2fe16-109">**新的-AzVirtualNetworkGateway** Cmdlet 會根據名稱、資源群組名稱、位置和 IP 設定以及閘道類型，以及 vpn 類型（如果 vpn），在 Azure 中建立閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="2fe16-109">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="2fe16-110">您也可以為閘道 SKU 命名。</span><span class="sxs-lookup"><span data-stu-id="2fe16-110">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="2fe16-111">如果此閘道是用來進行點對點連線，您也需要加入 VPN 用戶端位址集區，以便將位址指派給連線用戶端，以及用來驗證連接至閘道之 VPN 用戶端的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="2fe16-111">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="2fe16-112">您也可以選擇包含 BGP 與作用中的其他功能（例如 BGP 和作用中作用）。</span><span class="sxs-lookup"><span data-stu-id="2fe16-112">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="2fe16-113">示例</span><span class="sxs-lookup"><span data-stu-id="2fe16-113">EXAMPLES</span></span>

### <span data-ttu-id="2fe16-114">1：建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="2fe16-114">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="2fe16-115">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="2fe16-115">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="2fe16-116">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="2fe16-116">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="2fe16-117">2：使用外部 Radius 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="2fe16-117">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="2fe16-118">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="2fe16-118">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="2fe16-119">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="2fe16-119">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="2fe16-120">它也會新增位址為 "TestRadiusServer" 的外部 radius 伺服器</span><span class="sxs-lookup"><span data-stu-id="2fe16-120">It also adds an external radius server with address "TestRadiusServer"</span></span>

### <span data-ttu-id="2fe16-121">1：使用 P2S 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="2fe16-121">1: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="2fe16-122">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及使用 P2S 設定（例如 VpnProtocol、VpnClientAddressPool、VpnClientRootCertificates、VpnClientIpsecPolicy 等）建立虛擬網路閘道。在 Azure 中。</span><span class="sxs-lookup"><span data-stu-id="2fe16-122">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="2fe16-123">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 配置儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型 "RouteBased" 和 sku "VpnGw1"。</span><span class="sxs-lookup"><span data-stu-id="2fe16-123">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="2fe16-124">Vpn 設定將會在閘道上設定（例如 VpnProtocol 設為 Ikev2、VpnClientAddressPool 為 "201.169.0.0/16"）、VpnClientRootCertificate 設定為傳遞一個： clientRootCertName 和自訂 vpn ipsec 原則： $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="2fe16-124">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  

## <span data-ttu-id="2fe16-125">參數</span><span class="sxs-lookup"><span data-stu-id="2fe16-125">PARAMETERS</span></span>

### <span data-ttu-id="2fe16-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fe16-126">-AsJob</span></span>
<span data-ttu-id="2fe16-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2fe16-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fe16-128">-Asn</span><span class="sxs-lookup"><span data-stu-id="2fe16-128">-Asn</span></span>

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

### <span data-ttu-id="2fe16-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe16-129">-DefaultProfile</span></span>
<span data-ttu-id="2fe16-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fe16-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fe16-131">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="2fe16-131">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="2fe16-132">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="2fe16-132">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="2fe16-133">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2fe16-133">-EnableBgp</span></span>

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

### <span data-ttu-id="2fe16-134">-Force</span><span class="sxs-lookup"><span data-stu-id="2fe16-134">-Force</span></span>
<span data-ttu-id="2fe16-135">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2fe16-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fe16-136">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="2fe16-136">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="2fe16-137">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="2fe16-137">-GatewaySku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe16-138">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="2fe16-138">-GatewayType</span></span>

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

### <span data-ttu-id="2fe16-139">-Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="2fe16-139">-IpConfigurations</span></span>

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

### <span data-ttu-id="2fe16-140">-位置</span><span class="sxs-lookup"><span data-stu-id="2fe16-140">-Location</span></span>

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

### <span data-ttu-id="2fe16-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fe16-141">-Name</span></span>

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

### <span data-ttu-id="2fe16-142">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2fe16-142">-PeerWeight</span></span>

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

### <span data-ttu-id="2fe16-143">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="2fe16-143">-RadiusServerAddress</span></span>
<span data-ttu-id="2fe16-144">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="2fe16-144">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="2fe16-145">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="2fe16-145">-RadiusServerSecret</span></span>
<span data-ttu-id="2fe16-146">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="2fe16-146">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="2fe16-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe16-147">-ResourceGroupName</span></span>

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

### <span data-ttu-id="2fe16-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fe16-148">-Tag</span></span>
<span data-ttu-id="2fe16-149">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2fe16-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2fe16-150">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2fe16-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2fe16-151">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="2fe16-151">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="2fe16-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2fe16-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="2fe16-153">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="2fe16-153">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="2fe16-154">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="2fe16-154">-VpnClientProtocol</span></span>
<span data-ttu-id="2fe16-155">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="2fe16-155">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="2fe16-156">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="2fe16-156">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="2fe16-157">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="2fe16-157">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="2fe16-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="2fe16-158">-VpnType</span></span>

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

### <span data-ttu-id="2fe16-159">-確認</span><span class="sxs-lookup"><span data-stu-id="2fe16-159">-Confirm</span></span>
<span data-ttu-id="2fe16-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2fe16-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fe16-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fe16-161">-WhatIf</span></span>
<span data-ttu-id="2fe16-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fe16-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fe16-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fe16-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fe16-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe16-164">CommonParameters</span></span>
<span data-ttu-id="2fe16-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fe16-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe16-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2fe16-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe16-167">輸入</span><span class="sxs-lookup"><span data-stu-id="2fe16-167">INPUTS</span></span>

### <span data-ttu-id="2fe16-168">System.object</span><span class="sxs-lookup"><span data-stu-id="2fe16-168">System.String</span></span>

### <span data-ttu-id="2fe16-169">PSVirtualNetworkGatewayIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="2fe16-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="2fe16-170">System.object</span><span class="sxs-lookup"><span data-stu-id="2fe16-170">System.Boolean</span></span>

### <span data-ttu-id="2fe16-171">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2fe16-171">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="2fe16-172">System.object []</span><span class="sxs-lookup"><span data-stu-id="2fe16-172">System.String[]</span></span>

### <span data-ttu-id="2fe16-173">PSVpnClientRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="2fe16-173">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="2fe16-174">PSVpnClientRevokedCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="2fe16-174">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="2fe16-175">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="2fe16-175">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="2fe16-176">UInt32</span><span class="sxs-lookup"><span data-stu-id="2fe16-176">System.UInt32</span></span>

### <span data-ttu-id="2fe16-177">System.object</span><span class="sxs-lookup"><span data-stu-id="2fe16-177">System.Int32</span></span>

### <span data-ttu-id="2fe16-178">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2fe16-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2fe16-179">SecureString</span><span class="sxs-lookup"><span data-stu-id="2fe16-179">System.Security.SecureString</span></span>

## <span data-ttu-id="2fe16-180">輸出</span><span class="sxs-lookup"><span data-stu-id="2fe16-180">OUTPUTS</span></span>

### <span data-ttu-id="2fe16-181">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2fe16-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2fe16-182">筆記</span><span class="sxs-lookup"><span data-stu-id="2fe16-182">NOTES</span></span>

## <span data-ttu-id="2fe16-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fe16-183">RELATED LINKS</span></span>

[<span data-ttu-id="2fe16-184">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2fe16-184">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2fe16-185">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2fe16-185">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2fe16-186">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2fe16-186">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2fe16-187">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2fe16-187">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2fe16-188">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2fe16-188">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

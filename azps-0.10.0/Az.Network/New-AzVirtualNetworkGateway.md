---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: a19cc1484a00b60eb27723621e05aa67634e8732
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794232"
---
# <span data-ttu-id="c4c5f-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c5f-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c4c5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c5f-103">建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c4c5f-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="c4c5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4c5f-104">SYNTAX</span></span>

### <span data-ttu-id="c4c5f-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c4c5f-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c5f-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4c5f-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4c5f-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c4c5f-107">SetByResource</span></span>
```
New-AzVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4c5f-108">說明</span><span class="sxs-lookup"><span data-stu-id="c4c5f-108">DESCRIPTION</span></span>
<span data-ttu-id="c4c5f-109">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="c4c5f-110">**新的-AzVirtualNetworkGateway** Cmdlet 會根據名稱、資源群組名稱、位置和 IP 設定以及閘道類型，以及 vpn 類型（如果 vpn），在 Azure 中建立閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="c4c5f-111">您也可以為閘道 SKU 命名。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="c4c5f-112">如果此閘道是用來進行點對點連線，您也需要加入 VPN 用戶端位址集區，以便將位址指派給連線用戶端，以及用來驗證連接至閘道之 VPN 用戶端的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="c4c5f-113">您也可以選擇包含 BGP 與作用中的其他功能（例如 BGP 和作用中作用）。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="c4c5f-114">示例</span><span class="sxs-lookup"><span data-stu-id="c4c5f-114">EXAMPLES</span></span>

### <span data-ttu-id="c4c5f-115">1：建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c4c5f-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="c4c5f-116">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="c4c5f-117">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="c4c5f-118">2：使用外部 Radius 設定建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c4c5f-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="c4c5f-119">上述將會建立資源群組、要求公用 IP 位址、建立虛擬網路和子網，以及在 Azure 中建立虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="c4c5f-120">閘道將會在位置 "vnet-gateway" 中的資源群組 "vnet-閘道" 中稱為「myNGW」，並將先前建立的 IP 設定儲存在變數 "ngwIPConfig"、"VPN" 的閘道類型、vpn 類型 "RouteBased" 和 sku "Basic"。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="c4c5f-121">它也會新增位址為 "TestRadiusServer" 的外部 radius 伺服器</span><span class="sxs-lookup"><span data-stu-id="c4c5f-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="c4c5f-122">參數</span><span class="sxs-lookup"><span data-stu-id="c4c5f-122">PARAMETERS</span></span>

### <span data-ttu-id="c4c5f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4c5f-123">-AsJob</span></span>
<span data-ttu-id="c4c5f-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4c5f-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4c5f-125">-Asn</span><span class="sxs-lookup"><span data-stu-id="c4c5f-125">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c5f-126">-DefaultProfile</span></span>
<span data-ttu-id="c4c5f-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="c4c5f-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c4c5f-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="c4c5f-129">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-129">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="c4c5f-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c4c5f-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-131">-Force</span><span class="sxs-lookup"><span data-stu-id="c4c5f-131">-Force</span></span>
<span data-ttu-id="c4c5f-132">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4c5f-133">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c4c5f-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-134">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="c4c5f-134">-GatewaySku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-135">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="c4c5f-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-136">-Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="c4c5f-136">-IpConfigurations</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-137">-位置</span><span class="sxs-lookup"><span data-stu-id="c4c5f-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4c5f-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c4c5f-139">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c4c5f-140">-RadiusServerAddress</span></span>
<span data-ttu-id="c4c5f-141">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-141">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c4c5f-142">-RadiusServerSecret</span></span>
<span data-ttu-id="c4c5f-143">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-143">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4c5f-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4c5f-145">-Tag</span></span>
<span data-ttu-id="c4c5f-146">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c4c5f-147">例如：</span><span class="sxs-lookup"><span data-stu-id="c4c5f-147">For example:</span></span>

<span data-ttu-id="c4c5f-148">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c4c5f-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c4c5f-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="c4c5f-149">-VpnClientAddressPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="c4c5f-150">-VpnClientProtocol</span></span>
<span data-ttu-id="c4c5f-151">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="c4c5f-151">The list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-152">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="c4c5f-152">-VpnClientRevokedCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="c4c5f-153">-VpnClientRootCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="c4c5f-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5f-155">-確認</span><span class="sxs-lookup"><span data-stu-id="c4c5f-155">-Confirm</span></span>
<span data-ttu-id="c4c5f-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c5f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c5f-157">-WhatIf</span></span>
<span data-ttu-id="c4c5f-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c5f-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c5f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c5f-160">CommonParameters</span></span>
<span data-ttu-id="c4c5f-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c5f-162">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4c5f-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c5f-163">輸入</span><span class="sxs-lookup"><span data-stu-id="c4c5f-163">INPUTS</span></span>

## <span data-ttu-id="c4c5f-164">輸出</span><span class="sxs-lookup"><span data-stu-id="c4c5f-164">OUTPUTS</span></span>

### <span data-ttu-id="c4c5f-165">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c4c5f-165">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c4c5f-166">筆記</span><span class="sxs-lookup"><span data-stu-id="c4c5f-166">NOTES</span></span>

## <span data-ttu-id="c4c5f-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4c5f-167">RELATED LINKS</span></span>

[<span data-ttu-id="c4c5f-168">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c5f-168">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c4c5f-169">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c5f-169">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c4c5f-170">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c5f-170">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c4c5f-171">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c5f-171">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c4c5f-172">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c5f-172">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791565"
---
# <span data-ttu-id="c2548-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2548-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c2548-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2548-102">SYNOPSIS</span></span>
<span data-ttu-id="c2548-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c2548-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="c2548-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2548-104">SYNTAX</span></span>

### <span data-ttu-id="c2548-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c2548-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2548-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2548-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2548-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="c2548-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2548-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2548-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2548-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="c2548-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2548-110">說明</span><span class="sxs-lookup"><span data-stu-id="c2548-110">DESCRIPTION</span></span>
<span data-ttu-id="c2548-111">**AzVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c2548-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="c2548-112">示例</span><span class="sxs-lookup"><span data-stu-id="c2548-112">EXAMPLES</span></span>

### <span data-ttu-id="c2548-113">範例1：更新虛擬網路閘道的 ASN</span><span class="sxs-lookup"><span data-stu-id="c2548-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="c2548-114">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數會更新儲存在 variable $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c2548-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="c2548-115">此命令也會將 ASN 設定為1337。</span><span class="sxs-lookup"><span data-stu-id="c2548-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="c2548-116">範例2：新增 IPsec 原則至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c2548-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="c2548-117">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令所建立的 Vpn ipsec 原則物件，就像每個指定的 ipsec 參數一樣。</span><span class="sxs-lookup"><span data-stu-id="c2548-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="c2548-118">第三個命令會更新儲存在 variable $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="c2548-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="c2548-119">此命令也會設定在虛擬網路閘道的 $vpnclientipsecpolicy 物件中指定的自訂 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="c2548-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="c2548-120">範例3：新增/更新標籤至現有的虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="c2548-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="c2548-121">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數，以 @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"} 更新虛擬網路閘道 Gateway01。</span><span class="sxs-lookup"><span data-stu-id="c2548-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="c2548-122">範例4：針對現有虛擬網路閘道的 VpnClient 新增/更新 AAD 驗證配置</span><span class="sxs-lookup"><span data-stu-id="c2548-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="c2548-123">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令使用 AAD 驗證設定 params （aadTenantUri、aadAudienceId、aadIssuerUri for VpnClient）來更新虛擬網路閘道 Gateway01。</span><span class="sxs-lookup"><span data-stu-id="c2548-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="c2548-124">第三個命令會從虛擬網路閘道的 VpnClient 中移除 AAD 驗證設定。</span><span class="sxs-lookup"><span data-stu-id="c2548-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="c2548-125">參數</span><span class="sxs-lookup"><span data-stu-id="c2548-125">PARAMETERS</span></span>

### <span data-ttu-id="c2548-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="c2548-126">-AadAudienceId</span></span>
<span data-ttu-id="c2548-127">P2S AAD 驗證選項： AadAudienceId。</span><span class="sxs-lookup"><span data-stu-id="c2548-127">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="c2548-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="c2548-128">-AadIssuerUri</span></span>
<span data-ttu-id="c2548-129">P2S AAD 驗證選項： AadIssuerUri。</span><span class="sxs-lookup"><span data-stu-id="c2548-129">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="c2548-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="c2548-130">-AadTenantUri</span></span>
<span data-ttu-id="c2548-131">P2S AAD 驗證選項： AadTenantUri。</span><span class="sxs-lookup"><span data-stu-id="c2548-131">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="c2548-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2548-132">-AsJob</span></span>
<span data-ttu-id="c2548-133">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2548-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2548-134">-Asn</span><span class="sxs-lookup"><span data-stu-id="c2548-134">-Asn</span></span>
<span data-ttu-id="c2548-135">指定虛擬網路閘道自治系統號碼 (ASN) ，用來設定在 IPsec 隧道內 (BGP) 會話的邊界閘道通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c2548-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="c2548-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="c2548-136">-CustomRoute</span></span>
<span data-ttu-id="c2548-137">客戶指定的自訂路由 AddressPool</span><span class="sxs-lookup"><span data-stu-id="c2548-137">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="c2548-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2548-138">-DefaultProfile</span></span>
<span data-ttu-id="c2548-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2548-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2548-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c2548-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="c2548-141">停用作用中的功能。</span><span class="sxs-lookup"><span data-stu-id="c2548-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="c2548-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c2548-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="c2548-143">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="c2548-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="c2548-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c2548-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="c2548-145">指定要用於強制隧道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="c2548-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="c2548-146">如果指定了預設網站，閘道的虛擬私人網路 (VPN) 的所有網際網路流量都會路由到該網站。</span><span class="sxs-lookup"><span data-stu-id="c2548-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="c2548-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="c2548-147">-GatewaySku</span></span>
<span data-ttu-id="c2548-148">指定虛擬網路閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="c2548-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="c2548-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c2548-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2548-150">空白</span><span class="sxs-lookup"><span data-stu-id="c2548-150">Basic</span></span>
- <span data-ttu-id="c2548-151">標準</span><span class="sxs-lookup"><span data-stu-id="c2548-151">Standard</span></span>
- <span data-ttu-id="c2548-152">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="c2548-152">HighPerformance</span></span>
- <span data-ttu-id="c2548-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="c2548-153">VpnGw1</span></span>
- <span data-ttu-id="c2548-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="c2548-154">VpnGw2</span></span>
- <span data-ttu-id="c2548-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="c2548-155">VpnGw3</span></span>
- <span data-ttu-id="c2548-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="c2548-156">VpnGw1AZ</span></span>
- <span data-ttu-id="c2548-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="c2548-157">VpnGw2AZ</span></span>
- <span data-ttu-id="c2548-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="c2548-158">VpnGw3AZ</span></span>
- <span data-ttu-id="c2548-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="c2548-159">ErGw1AZ</span></span>
- <span data-ttu-id="c2548-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="c2548-160">ErGw2AZ</span></span>
- <span data-ttu-id="c2548-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="c2548-161">ErGw3AZ</span></span>

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

### <span data-ttu-id="c2548-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c2548-162">-PeerWeight</span></span>
<span data-ttu-id="c2548-163">指定透過此虛擬網路閘道通過 BGP 瞭解的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="c2548-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="c2548-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c2548-164">-RadiusServerAddress</span></span>
<span data-ttu-id="c2548-165">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="c2548-165">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2548-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c2548-166">-RadiusServerSecret</span></span>
<span data-ttu-id="c2548-167">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="c2548-167">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2548-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="c2548-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="c2548-169">[標記] 可從虛擬網路閘道中移除 P2S 用戶端的 AAD 驗證。</span><span class="sxs-lookup"><span data-stu-id="c2548-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="c2548-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2548-170">-Tag</span></span>
<span data-ttu-id="c2548-171">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="c2548-171">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2548-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2548-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c2548-173">指定要作為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="c2548-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="c2548-174">您可以使用 Get-AzVirtualNetworkGateway Cmdlet 來取得虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="c2548-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2548-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2548-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="c2548-176">指定此 Cmdlet 用來從哪個位址空間來指派 VPN 用戶端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c2548-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="c2548-177">這不應與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="c2548-177">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="c2548-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c2548-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="c2548-179">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="c2548-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c2548-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="c2548-180">-VpnClientProtocol</span></span>
<span data-ttu-id="c2548-181">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="c2548-181">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="c2548-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="c2548-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="c2548-183">指定已吊銷之 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="c2548-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="c2548-184">VPN 用戶端會移除與其中一個相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="c2548-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="c2548-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="c2548-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="c2548-186">指定要用於 VPN 用戶端驗證的 VPN 用戶端根憑證清單。</span><span class="sxs-lookup"><span data-stu-id="c2548-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="c2548-187">[連線 VPN 用戶端] 必須出示從這些根憑證的其中一個證書產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="c2548-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="c2548-188">-確認</span><span class="sxs-lookup"><span data-stu-id="c2548-188">-Confirm</span></span>
<span data-ttu-id="c2548-189">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2548-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2548-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2548-190">-WhatIf</span></span>
<span data-ttu-id="c2548-191">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2548-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2548-192">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2548-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2548-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2548-193">CommonParameters</span></span>
<span data-ttu-id="c2548-194">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2548-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2548-195">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2548-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2548-196">輸入</span><span class="sxs-lookup"><span data-stu-id="c2548-196">INPUTS</span></span>

### <span data-ttu-id="c2548-197">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2548-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="c2548-198">System.object</span><span class="sxs-lookup"><span data-stu-id="c2548-198">System.String</span></span>

### <span data-ttu-id="c2548-199">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2548-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="c2548-200">System.object []</span><span class="sxs-lookup"><span data-stu-id="c2548-200">System.String[]</span></span>

### <span data-ttu-id="c2548-201">PSVpnClientRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="c2548-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="c2548-202">PSVpnClientRevokedCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="c2548-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="c2548-203">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="c2548-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="c2548-204">UInt32</span><span class="sxs-lookup"><span data-stu-id="c2548-204">System.UInt32</span></span>

### <span data-ttu-id="c2548-205">System.object</span><span class="sxs-lookup"><span data-stu-id="c2548-205">System.Int32</span></span>

### <span data-ttu-id="c2548-206">SecureString</span><span class="sxs-lookup"><span data-stu-id="c2548-206">System.Security.SecureString</span></span>

## <span data-ttu-id="c2548-207">輸出</span><span class="sxs-lookup"><span data-stu-id="c2548-207">OUTPUTS</span></span>

### <span data-ttu-id="c2548-208">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2548-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c2548-209">筆記</span><span class="sxs-lookup"><span data-stu-id="c2548-209">NOTES</span></span>
* <span data-ttu-id="c2548-210">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="c2548-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c2548-211">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2548-211">RELATED LINKS</span></span>

[<span data-ttu-id="c2548-212">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2548-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c2548-213">新-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2548-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c2548-214">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2548-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c2548-215">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2548-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c2548-216">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2548-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

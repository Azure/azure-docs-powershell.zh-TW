---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: e5216d3a5727c32bd5e9f185cd48ace068a890b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956605"
---
# <span data-ttu-id="bce7d-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bce7d-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="bce7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bce7d-102">SYNOPSIS</span></span>
<span data-ttu-id="bce7d-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="bce7d-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="bce7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="bce7d-104">SYNTAX</span></span>

### <span data-ttu-id="bce7d-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="bce7d-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bce7d-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bce7d-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce7d-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="bce7d-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce7d-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="bce7d-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce7d-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="bce7d-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce7d-110">說明</span><span class="sxs-lookup"><span data-stu-id="bce7d-110">DESCRIPTION</span></span>
<span data-ttu-id="bce7d-111">**AzVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="bce7d-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="bce7d-112">示例</span><span class="sxs-lookup"><span data-stu-id="bce7d-112">EXAMPLES</span></span>

### <span data-ttu-id="bce7d-113">範例1：更新虛擬網路閘道的 ASN</span><span class="sxs-lookup"><span data-stu-id="bce7d-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="bce7d-114">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數會更新儲存在 variable $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="bce7d-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="bce7d-115">此命令也會將 ASN 設定為1337。</span><span class="sxs-lookup"><span data-stu-id="bce7d-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="bce7d-116">範例2：新增 IPsec 原則至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="bce7d-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="bce7d-117">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令所建立的 Vpn ipsec 原則物件，就像每個指定的 ipsec 參數一樣。</span><span class="sxs-lookup"><span data-stu-id="bce7d-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="bce7d-118">第三個命令會更新儲存在 variable $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="bce7d-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="bce7d-119">此命令也會設定在虛擬網路閘道的 $vpnclientipsecpolicy 物件中指定的自訂 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="bce7d-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="bce7d-120">範例3：新增/更新標籤至現有的虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="bce7d-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="bce7d-121">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數，以 @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"} 更新虛擬網路閘道 Gateway01。</span><span class="sxs-lookup"><span data-stu-id="bce7d-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="bce7d-122">範例4：針對現有虛擬網路閘道的 VpnClient 新增/更新 AAD 驗證配置</span><span class="sxs-lookup"><span data-stu-id="bce7d-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="bce7d-123">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令使用 AAD 驗證設定 params （aadTenantUri、aadAudienceId、aadIssuerUri for VpnClient）來更新虛擬網路閘道 Gateway01。</span><span class="sxs-lookup"><span data-stu-id="bce7d-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="bce7d-124">第三個命令會從虛擬網路閘道的 VpnClient 中移除 AAD 驗證設定。</span><span class="sxs-lookup"><span data-stu-id="bce7d-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="bce7d-125">範例5：新增/更新 IpConfigurationBgpPeeringAddresses 至現有的虛擬閘道</span><span class="sxs-lookup"><span data-stu-id="bce7d-125">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
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
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="bce7d-126">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數會將虛擬網路閘道 Gateway01 IpConfiguration Id 的值指派給 variable ipconfigurationId1。</span><span class="sxs-lookup"><span data-stu-id="bce7d-126">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="bce7d-127">第三個命令會將地址清單指派至 addresslist1。</span><span class="sxs-lookup"><span data-stu-id="bce7d-127">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="bce7d-128">第四個命令建立了 PSIpConfigurationBgpPeeringAddress 物件。</span><span class="sxs-lookup"><span data-stu-id="bce7d-128">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="bce7d-129">第五個命令會將這個新建立的 PSIpConfigurationBgpPeeringAddress 設定為 IpConfigurationBgpPeeringAddresses 並更新閘道。</span><span class="sxs-lookup"><span data-stu-id="bce7d-129">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="bce7d-130">參數</span><span class="sxs-lookup"><span data-stu-id="bce7d-130">PARAMETERS</span></span>

### <span data-ttu-id="bce7d-131">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="bce7d-131">-AadAudienceId</span></span>
<span data-ttu-id="bce7d-132">P2S AAD 驗證選項： AadAudienceId。</span><span class="sxs-lookup"><span data-stu-id="bce7d-132">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="bce7d-133">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="bce7d-133">-AadIssuerUri</span></span>
<span data-ttu-id="bce7d-134">P2S AAD 驗證選項： AadIssuerUri。</span><span class="sxs-lookup"><span data-stu-id="bce7d-134">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="bce7d-135">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="bce7d-135">-AadTenantUri</span></span>
<span data-ttu-id="bce7d-136">P2S AAD 驗證選項： AadTenantUri。</span><span class="sxs-lookup"><span data-stu-id="bce7d-136">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="bce7d-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bce7d-137">-AsJob</span></span>
<span data-ttu-id="bce7d-138">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bce7d-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bce7d-139">-Asn</span><span class="sxs-lookup"><span data-stu-id="bce7d-139">-Asn</span></span>
<span data-ttu-id="bce7d-140">虛擬網路閘道的 ASN，用來在 IPsec 隧道內設定 BGP 會話</span><span class="sxs-lookup"><span data-stu-id="bce7d-140">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="bce7d-141">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="bce7d-141">-CustomRoute</span></span>
<span data-ttu-id="bce7d-142">客戶指定的自訂路由 AddressPool</span><span class="sxs-lookup"><span data-stu-id="bce7d-142">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="bce7d-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce7d-143">-DefaultProfile</span></span>
<span data-ttu-id="bce7d-144">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bce7d-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce7d-145">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bce7d-145">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="bce7d-146">在虛擬網路閘道上停用使用中作用中功能的標誌</span><span class="sxs-lookup"><span data-stu-id="bce7d-146">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="bce7d-147">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bce7d-147">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="bce7d-148">在虛擬網路閘道上啟用作用中作用功能的標誌</span><span class="sxs-lookup"><span data-stu-id="bce7d-148">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="bce7d-149">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bce7d-149">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="bce7d-150">在虛擬網路閘道上啟用作用中作用功能的標誌</span><span class="sxs-lookup"><span data-stu-id="bce7d-150">Flag to enable Active Active feature on virtual network gateway</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce7d-151">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="bce7d-151">-GatewayDefaultSite</span></span>
<span data-ttu-id="bce7d-152">要用來強制執行隧道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="bce7d-152">The default site to use for force tunneling.</span></span>
<span data-ttu-id="bce7d-153">如果指定預設網站，來自閘道的 vnet 的所有網際網路流量都會路由到該網站。</span><span class="sxs-lookup"><span data-stu-id="bce7d-153">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="bce7d-154">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="bce7d-154">-GatewaySku</span></span>
<span data-ttu-id="bce7d-155">虛擬網路閘道的 SKU</span><span class="sxs-lookup"><span data-stu-id="bce7d-155">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="bce7d-156">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="bce7d-156">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="bce7d-157">虛擬網路閘道 bgpsettings 的 BgpPeeringAddresses。</span><span class="sxs-lookup"><span data-stu-id="bce7d-157">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="bce7d-158">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="bce7d-158">-PeerWeight</span></span>
<span data-ttu-id="bce7d-159">透過此虛擬網路閘道透過 BGP 所學到的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="bce7d-159">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="bce7d-160">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="bce7d-160">-RadiusServerAddress</span></span>
<span data-ttu-id="bce7d-161">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="bce7d-161">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="bce7d-162">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="bce7d-162">-RadiusServerSecret</span></span>
<span data-ttu-id="bce7d-163">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="bce7d-163">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="bce7d-164">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="bce7d-164">-RemoveAadAuthentication</span></span>
<span data-ttu-id="bce7d-165">[標記] 可從虛擬網路閘道中移除 P2S 用戶端的 AAD 驗證。</span><span class="sxs-lookup"><span data-stu-id="bce7d-165">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="bce7d-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="bce7d-166">-Tag</span></span>
<span data-ttu-id="bce7d-167">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="bce7d-167">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="bce7d-168">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bce7d-168">-VirtualNetworkGateway</span></span>
<span data-ttu-id="bce7d-169">要作為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="bce7d-169">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="bce7d-170">這可以使用 Get-AzVirtualNetworkGateway 來檢索</span><span class="sxs-lookup"><span data-stu-id="bce7d-170">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="bce7d-171">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="bce7d-171">-VpnClientAddressPool</span></span>
<span data-ttu-id="bce7d-172">要從中指派 VPN 用戶端 IP 位址的位址空間。</span><span class="sxs-lookup"><span data-stu-id="bce7d-172">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="bce7d-173">這不應與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="bce7d-173">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="bce7d-174">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="bce7d-174">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="bce7d-175">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="bce7d-175">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="bce7d-176">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="bce7d-176">-VpnClientProtocol</span></span>
<span data-ttu-id="bce7d-177">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="bce7d-177">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="bce7d-178">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="bce7d-178">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="bce7d-179">已吊銷之 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="bce7d-179">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="bce7d-180">會告知 VPN 用戶端出示與其中一個證書相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="bce7d-180">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="bce7d-181">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="bce7d-181">-VpnClientRootCertificates</span></span>
<span data-ttu-id="bce7d-182">要用於 VPN 用戶端驗證的 VPN 用戶端根憑證清單。</span><span class="sxs-lookup"><span data-stu-id="bce7d-182">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="bce7d-183">[連線 VPN 用戶端] 必須出示從這些根憑證的其中一個證書產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="bce7d-183">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="bce7d-184">-確認</span><span class="sxs-lookup"><span data-stu-id="bce7d-184">-Confirm</span></span>
<span data-ttu-id="bce7d-185">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bce7d-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce7d-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce7d-186">-WhatIf</span></span>
<span data-ttu-id="bce7d-187">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bce7d-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce7d-188">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bce7d-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce7d-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce7d-189">CommonParameters</span></span>
<span data-ttu-id="bce7d-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bce7d-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce7d-191">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bce7d-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce7d-192">輸入</span><span class="sxs-lookup"><span data-stu-id="bce7d-192">INPUTS</span></span>

### <span data-ttu-id="bce7d-193">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bce7d-193">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="bce7d-194">System.object</span><span class="sxs-lookup"><span data-stu-id="bce7d-194">System.String</span></span>

### <span data-ttu-id="bce7d-195">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bce7d-195">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="bce7d-196">System.object []</span><span class="sxs-lookup"><span data-stu-id="bce7d-196">System.String[]</span></span>

### <span data-ttu-id="bce7d-197">PSVpnClientRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="bce7d-197">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="bce7d-198">PSVpnClientRevokedCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="bce7d-198">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="bce7d-199">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="bce7d-199">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="bce7d-200">UInt32</span><span class="sxs-lookup"><span data-stu-id="bce7d-200">System.UInt32</span></span>

### <span data-ttu-id="bce7d-201">System.object</span><span class="sxs-lookup"><span data-stu-id="bce7d-201">System.Int32</span></span>

### <span data-ttu-id="bce7d-202">PSIpConfigurationBgpPeeringAddress [] （[]）</span><span class="sxs-lookup"><span data-stu-id="bce7d-202">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="bce7d-203">SecureString</span><span class="sxs-lookup"><span data-stu-id="bce7d-203">System.Security.SecureString</span></span>

## <span data-ttu-id="bce7d-204">輸出</span><span class="sxs-lookup"><span data-stu-id="bce7d-204">OUTPUTS</span></span>

### <span data-ttu-id="bce7d-205">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bce7d-205">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bce7d-206">筆記</span><span class="sxs-lookup"><span data-stu-id="bce7d-206">NOTES</span></span>

## <span data-ttu-id="bce7d-207">相關連結</span><span class="sxs-lookup"><span data-stu-id="bce7d-207">RELATED LINKS</span></span>

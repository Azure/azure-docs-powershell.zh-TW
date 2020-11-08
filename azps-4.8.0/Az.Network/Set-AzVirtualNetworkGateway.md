---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135503"
---
# <span data-ttu-id="7ccad-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ccad-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="7ccad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ccad-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccad-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="7ccad-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="7ccad-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ccad-104">SYNTAX</span></span>

### <span data-ttu-id="7ccad-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="7ccad-105">Default (Default)</span></span>
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

### <span data-ttu-id="7ccad-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ccad-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="7ccad-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="7ccad-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
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

### <span data-ttu-id="7ccad-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ccad-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccad-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ccad-109">AadAuthenticationConfiguration</span></span>
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

### <span data-ttu-id="7ccad-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="7ccad-110">UpdateResourceWithTags</span></span>
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

## <span data-ttu-id="7ccad-111">說明</span><span class="sxs-lookup"><span data-stu-id="7ccad-111">DESCRIPTION</span></span>
<span data-ttu-id="7ccad-112">**AzVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="7ccad-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="7ccad-113">示例</span><span class="sxs-lookup"><span data-stu-id="7ccad-113">EXAMPLES</span></span>

### <span data-ttu-id="7ccad-114">範例1：更新虛擬網路閘道的 ASN</span><span class="sxs-lookup"><span data-stu-id="7ccad-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="7ccad-115">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數會更新儲存在 variable $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="7ccad-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="7ccad-116">此命令也會將 ASN 設定為1337。</span><span class="sxs-lookup"><span data-stu-id="7ccad-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="7ccad-117">範例2：新增 IPsec 原則至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="7ccad-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="7ccad-118">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令所建立的 Vpn ipsec 原則物件，就像每個指定的 ipsec 參數一樣。</span><span class="sxs-lookup"><span data-stu-id="7ccad-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="7ccad-119">第三個命令會更新儲存在 variable $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="7ccad-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="7ccad-120">此命令也會設定在虛擬網路閘道的 $vpnclientipsecpolicy 物件中指定的自訂 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="7ccad-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="7ccad-121">範例3：新增/更新標籤至現有的虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="7ccad-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="7ccad-122">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數，以 @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"} 更新虛擬網路閘道 Gateway01。</span><span class="sxs-lookup"><span data-stu-id="7ccad-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="7ccad-123">範例4：針對現有虛擬網路閘道的 VpnClient 新增/更新 AAD 驗證配置</span><span class="sxs-lookup"><span data-stu-id="7ccad-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="7ccad-124">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令使用 AAD 驗證設定 params （aadTenantUri、aadAudienceId、aadIssuerUri for VpnClient）來更新虛擬網路閘道 Gateway01。</span><span class="sxs-lookup"><span data-stu-id="7ccad-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="7ccad-125">第三個命令會從虛擬網路閘道的 VpnClient 中移除 AAD 驗證設定。</span><span class="sxs-lookup"><span data-stu-id="7ccad-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="7ccad-126">範例5：新增/更新 IpConfigurationBgpPeeringAddresses 至現有的虛擬閘道</span><span class="sxs-lookup"><span data-stu-id="7ccad-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
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

<span data-ttu-id="7ccad-127">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數會將虛擬網路閘道 Gateway01 IpConfiguration Id 的值指派給 variable ipconfigurationId1。</span><span class="sxs-lookup"><span data-stu-id="7ccad-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="7ccad-128">第三個命令會將地址清單指派至 addresslist1。</span><span class="sxs-lookup"><span data-stu-id="7ccad-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="7ccad-129">第四個命令建立了 PSIpConfigurationBgpPeeringAddress 物件。</span><span class="sxs-lookup"><span data-stu-id="7ccad-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="7ccad-130">第五個命令會將這個新建立的 PSIpConfigurationBgpPeeringAddress 設定為 IpConfigurationBgpPeeringAddresses 並更新閘道。</span><span class="sxs-lookup"><span data-stu-id="7ccad-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="7ccad-131">參數</span><span class="sxs-lookup"><span data-stu-id="7ccad-131">PARAMETERS</span></span>

### <span data-ttu-id="7ccad-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="7ccad-132">-AadAudienceId</span></span>
<span data-ttu-id="7ccad-133">P2S AAD 驗證選項： AadAudienceId。</span><span class="sxs-lookup"><span data-stu-id="7ccad-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="7ccad-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="7ccad-134">-AadIssuerUri</span></span>
<span data-ttu-id="7ccad-135">P2S AAD 驗證選項： AadIssuerUri。</span><span class="sxs-lookup"><span data-stu-id="7ccad-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="7ccad-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="7ccad-136">-AadTenantUri</span></span>
<span data-ttu-id="7ccad-137">P2S AAD 驗證選項： AadTenantUri。</span><span class="sxs-lookup"><span data-stu-id="7ccad-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="7ccad-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ccad-138">-AsJob</span></span>
<span data-ttu-id="7ccad-139">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ccad-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ccad-140">-Asn</span><span class="sxs-lookup"><span data-stu-id="7ccad-140">-Asn</span></span>
<span data-ttu-id="7ccad-141">虛擬網路閘道的 ASN，用來在 IPsec 隧道內設定 BGP 會話</span><span class="sxs-lookup"><span data-stu-id="7ccad-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="7ccad-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="7ccad-142">-CustomRoute</span></span>
<span data-ttu-id="7ccad-143">客戶指定的自訂路由 AddressPool</span><span class="sxs-lookup"><span data-stu-id="7ccad-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="7ccad-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccad-144">-DefaultProfile</span></span>
<span data-ttu-id="7ccad-145">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ccad-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ccad-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7ccad-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="7ccad-147">在虛擬網路閘道上停用使用中作用中功能的標誌</span><span class="sxs-lookup"><span data-stu-id="7ccad-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7ccad-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7ccad-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="7ccad-149">在虛擬網路閘道上啟用作用中作用功能的標誌</span><span class="sxs-lookup"><span data-stu-id="7ccad-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7ccad-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ccad-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="7ccad-151">在虛擬網路閘道上啟用作用中作用功能的標誌</span><span class="sxs-lookup"><span data-stu-id="7ccad-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7ccad-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7ccad-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="7ccad-153">要用來強制執行隧道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="7ccad-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="7ccad-154">如果指定預設網站，來自閘道的 vnet 的所有網際網路流量都會路由到該網站。</span><span class="sxs-lookup"><span data-stu-id="7ccad-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="7ccad-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7ccad-155">-GatewaySku</span></span>
<span data-ttu-id="7ccad-156">虛擬網路閘道的 SKU</span><span class="sxs-lookup"><span data-stu-id="7ccad-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="7ccad-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="7ccad-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="7ccad-158">虛擬網路閘道 bgpsettings 的 BgpPeeringAddresses。</span><span class="sxs-lookup"><span data-stu-id="7ccad-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="7ccad-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="7ccad-159">-PeerWeight</span></span>
<span data-ttu-id="7ccad-160">透過此虛擬網路閘道透過 BGP 所學到的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="7ccad-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="7ccad-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="7ccad-161">-RadiusServerAddress</span></span>
<span data-ttu-id="7ccad-162">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="7ccad-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="7ccad-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="7ccad-163">-RadiusServerList</span></span>
<span data-ttu-id="7ccad-164">P2S 多個外部 Radius 伺服器。</span><span class="sxs-lookup"><span data-stu-id="7ccad-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="7ccad-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="7ccad-165">-RadiusServerSecret</span></span>
<span data-ttu-id="7ccad-166">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="7ccad-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="7ccad-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="7ccad-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="7ccad-168">[標記] 可從虛擬網路閘道中移除 P2S 用戶端的 AAD 驗證。</span><span class="sxs-lookup"><span data-stu-id="7ccad-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="7ccad-169">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ccad-169">-Tag</span></span>
<span data-ttu-id="7ccad-170">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="7ccad-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="7ccad-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ccad-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7ccad-172">要作為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="7ccad-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="7ccad-173">這可以使用 Get-AzVirtualNetworkGateway 來檢索</span><span class="sxs-lookup"><span data-stu-id="7ccad-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="7ccad-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="7ccad-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="7ccad-175">要從中指派 VPN 用戶端 IP 位址的位址空間。</span><span class="sxs-lookup"><span data-stu-id="7ccad-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="7ccad-176">這不應與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="7ccad-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="7ccad-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="7ccad-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="7ccad-178">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="7ccad-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="7ccad-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7ccad-179">-VpnClientProtocol</span></span>
<span data-ttu-id="7ccad-180">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="7ccad-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="7ccad-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="7ccad-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="7ccad-182">已吊銷之 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="7ccad-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="7ccad-183">會告知 VPN 用戶端出示與其中一個證書相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="7ccad-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="7ccad-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="7ccad-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="7ccad-185">要用於 VPN 用戶端驗證的 VPN 用戶端根憑證清單。</span><span class="sxs-lookup"><span data-stu-id="7ccad-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="7ccad-186">[連線 VPN 用戶端] 必須出示從這些根憑證的其中一個證書產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="7ccad-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="7ccad-187">-確認</span><span class="sxs-lookup"><span data-stu-id="7ccad-187">-Confirm</span></span>
<span data-ttu-id="7ccad-188">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7ccad-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ccad-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ccad-189">-WhatIf</span></span>
<span data-ttu-id="7ccad-190">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ccad-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ccad-191">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ccad-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ccad-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccad-192">CommonParameters</span></span>
<span data-ttu-id="7ccad-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ccad-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccad-194">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7ccad-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccad-195">輸入</span><span class="sxs-lookup"><span data-stu-id="7ccad-195">INPUTS</span></span>

### <span data-ttu-id="7ccad-196">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ccad-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7ccad-197">System.object</span><span class="sxs-lookup"><span data-stu-id="7ccad-197">System.String</span></span>

### <span data-ttu-id="7ccad-198">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ccad-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="7ccad-199">System.object []</span><span class="sxs-lookup"><span data-stu-id="7ccad-199">System.String[]</span></span>

### <span data-ttu-id="7ccad-200">PSVpnClientRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7ccad-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="7ccad-201">PSVpnClientRevokedCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7ccad-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="7ccad-202">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7ccad-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="7ccad-203">UInt32</span><span class="sxs-lookup"><span data-stu-id="7ccad-203">System.UInt32</span></span>

### <span data-ttu-id="7ccad-204">System.object</span><span class="sxs-lookup"><span data-stu-id="7ccad-204">System.Int32</span></span>

### <span data-ttu-id="7ccad-205">PSIpConfigurationBgpPeeringAddress [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7ccad-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="7ccad-206">SecureString</span><span class="sxs-lookup"><span data-stu-id="7ccad-206">System.Security.SecureString</span></span>

## <span data-ttu-id="7ccad-207">輸出</span><span class="sxs-lookup"><span data-stu-id="7ccad-207">OUTPUTS</span></span>

### <span data-ttu-id="7ccad-208">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ccad-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7ccad-209">筆記</span><span class="sxs-lookup"><span data-stu-id="7ccad-209">NOTES</span></span>

## <span data-ttu-id="7ccad-210">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ccad-210">RELATED LINKS</span></span>
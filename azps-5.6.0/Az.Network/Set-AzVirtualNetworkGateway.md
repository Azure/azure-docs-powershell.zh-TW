---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 17d9e024d13db1871bfab3b5b7230391fe22d192
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911618"
---
# <span data-ttu-id="aec03-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aec03-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="aec03-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aec03-102">SYNOPSIS</span></span>
<span data-ttu-id="aec03-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="aec03-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="aec03-104">語法</span><span class="sxs-lookup"><span data-stu-id="aec03-104">SYNTAX</span></span>

### <span data-ttu-id="aec03-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="aec03-105">Default (Default)</span></span>
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

### <span data-ttu-id="aec03-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="aec03-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="aec03-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="aec03-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
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

### <span data-ttu-id="aec03-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="aec03-108">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="aec03-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="aec03-109">AadAuthenticationConfiguration</span></span>
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

### <span data-ttu-id="aec03-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="aec03-110">UpdateResourceWithTags</span></span>
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

## <span data-ttu-id="aec03-111">描述</span><span class="sxs-lookup"><span data-stu-id="aec03-111">DESCRIPTION</span></span>
<span data-ttu-id="aec03-112">**Set-AzVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="aec03-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="aec03-113">例子</span><span class="sxs-lookup"><span data-stu-id="aec03-113">EXAMPLES</span></span>

### <span data-ttu-id="aec03-114">範例 1：更新虛擬網路閘道的 ASN</span><span class="sxs-lookup"><span data-stu-id="aec03-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="aec03-115">第一個命令會獲得一個名為 Gateway01 的虛擬網路閘道，該閘道屬於資源群組 ResourceGroup001，並儲存到名為 $Gateway 的變數。第二個命令會更新儲存在變數 $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="aec03-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="aec03-116">命令也會將 ASN 設定為 1337。</span><span class="sxs-lookup"><span data-stu-id="aec03-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="aec03-117">範例 2：新增 IPsec 策略至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="aec03-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="aec03-118">第一個命令會獲得一個名為 Gateway01 的虛擬網路閘道，該閘道屬於資源群組 ResourceGroup001，並儲存到名為 $Gateway 的變數。第二個命令會根據指定的 ipsec 參數建立 Vpn ipsec 策略物件。</span><span class="sxs-lookup"><span data-stu-id="aec03-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="aec03-119">第三個命令會更新儲存在變數變數中的$Gateway。</span><span class="sxs-lookup"><span data-stu-id="aec03-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="aec03-120">該命令也會設定在虛擬網路閘道上$vpnclientipsecpolicy的自訂 vpn ipsec 策略。</span><span class="sxs-lookup"><span data-stu-id="aec03-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="aec03-121">範例 3：新增/更新標籤至現有的虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="aec03-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="aec03-122">第一個命令會獲得一個名為 Gateway01 的虛擬網路閘道，該閘道屬於資源群組 ResourceGroup001，並儲存到名為 $Gateway 的第二個命令會以標籤 @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }更新虛擬網路閘道閘道01。</span><span class="sxs-lookup"><span data-stu-id="aec03-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="aec03-123">範例 4：新增/更新現有虛擬網路閘道 VpnClient 的 AAD 驗證組</span><span class="sxs-lookup"><span data-stu-id="aec03-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="aec03-124">第一個命令會獲得一個名為 Gateway01 的虛擬網路閘道，該閘道屬於資源群組 ResourceGroup001，並儲存到名為 $Gateway 的變數。第二個命令會以 AAD 驗證組組參數更新虛擬網路閘道閘道01：aadTenantUri、aadAudienceId、aadIssuerUri for VpnClient。</span><span class="sxs-lookup"><span data-stu-id="aec03-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="aec03-125">第三個命令會從虛擬網路閘道的 VpnClient 移除 AAD 驗證組式。</span><span class="sxs-lookup"><span data-stu-id="aec03-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="aec03-126">範例 5：新增/更新 IpConfigurationBgpPeeringAddresses 到現有的虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="aec03-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
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

<span data-ttu-id="aec03-127">第一個命令會獲得一個名為 Gateway01 的虛擬網路閘道，該閘道屬於資源群組 ResourceGroup001，並將它儲存至名為 $Gateway 的變數。第二個命令會指派虛擬網路閘道 Gateway01 IpConfiguration Id 的值至變數 ipconfigurationId1。</span><span class="sxs-lookup"><span data-stu-id="aec03-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="aec03-128">第三個命令會指派地址清單至地址清單1。</span><span class="sxs-lookup"><span data-stu-id="aec03-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="aec03-129">第四個命令會建立 PSIpConfigurationBgpPeeringAddress 物件。</span><span class="sxs-lookup"><span data-stu-id="aec03-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="aec03-130">此新建立 PSIpConfigurationBgpPeeringAddress 到 IpConfigurationBgpPeeringAddresses 及更新閘道的第五個命令集。</span><span class="sxs-lookup"><span data-stu-id="aec03-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="aec03-131">參數</span><span class="sxs-lookup"><span data-stu-id="aec03-131">PARAMETERS</span></span>

### <span data-ttu-id="aec03-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="aec03-132">-AadAudienceId</span></span>
<span data-ttu-id="aec03-133">P2S AAD 驗證選項：AadAudienceId。</span><span class="sxs-lookup"><span data-stu-id="aec03-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="aec03-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="aec03-134">-AadIssuerUri</span></span>
<span data-ttu-id="aec03-135">P2S AAD 驗證選項：AadIssuerUri。</span><span class="sxs-lookup"><span data-stu-id="aec03-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="aec03-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="aec03-136">-AadTenantUri</span></span>
<span data-ttu-id="aec03-137">P2S AAD 驗證選項：AadTenantUri。</span><span class="sxs-lookup"><span data-stu-id="aec03-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="aec03-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aec03-138">-AsJob</span></span>
<span data-ttu-id="aec03-139">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aec03-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aec03-140">-Asn</span><span class="sxs-lookup"><span data-stu-id="aec03-140">-Asn</span></span>
<span data-ttu-id="aec03-141">虛擬網路閘道的 ASN，用來在 IPsec 內設定 BGP 會話</span><span class="sxs-lookup"><span data-stu-id="aec03-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="aec03-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="aec03-142">-CustomRoute</span></span>
<span data-ttu-id="aec03-143">客戶指定的自訂路由 AddressPool</span><span class="sxs-lookup"><span data-stu-id="aec03-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="aec03-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec03-144">-DefaultProfile</span></span>
<span data-ttu-id="aec03-145">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aec03-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aec03-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="aec03-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="aec03-147">標為停用虛擬網路閘道上的 Active Active 功能</span><span class="sxs-lookup"><span data-stu-id="aec03-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="aec03-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="aec03-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="aec03-149">在虛擬網路閘道上啟用 Active Active 功能的標誌</span><span class="sxs-lookup"><span data-stu-id="aec03-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="aec03-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="aec03-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="aec03-151">在虛擬網路閘道上啟用 Active Active 功能的標誌</span><span class="sxs-lookup"><span data-stu-id="aec03-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="aec03-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="aec03-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="aec03-153">用於強制強制設置的預設網站。</span><span class="sxs-lookup"><span data-stu-id="aec03-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="aec03-154">如果已指定預設網站，閘道 vnet 的所有網際網路流量會路由至該網站。</span><span class="sxs-lookup"><span data-stu-id="aec03-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="aec03-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="aec03-155">-GatewaySku</span></span>
<span data-ttu-id="aec03-156">虛擬網路閘道的 SKU</span><span class="sxs-lookup"><span data-stu-id="aec03-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="aec03-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="aec03-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="aec03-158">BgpPeeringAddresses for Virtual Network gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="aec03-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="aec03-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="aec03-159">-PeerWeight</span></span>
<span data-ttu-id="aec03-160">從這個虛擬網路閘道從 BGP 得知的路由所增加的權重</span><span class="sxs-lookup"><span data-stu-id="aec03-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="aec03-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="aec03-161">-RadiusServerAddress</span></span>
<span data-ttu-id="aec03-162">P2S 外部範圍伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="aec03-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="aec03-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="aec03-163">-RadiusServerList</span></span>
<span data-ttu-id="aec03-164">P2S 多個外部範圍伺服器。</span><span class="sxs-lookup"><span data-stu-id="aec03-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="aec03-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="aec03-165">-RadiusServerSecret</span></span>
<span data-ttu-id="aec03-166">P2S 外部弧線伺服器機密。</span><span class="sxs-lookup"><span data-stu-id="aec03-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="aec03-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="aec03-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="aec03-168">標出以從虛擬網路閘道移除 P2S 用戶端的 AAD 驗證。</span><span class="sxs-lookup"><span data-stu-id="aec03-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="aec03-169">-標記</span><span class="sxs-lookup"><span data-stu-id="aec03-169">-Tag</span></span>
<span data-ttu-id="aec03-170">P2S 外部範圍伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="aec03-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="aec03-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aec03-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="aec03-172">做為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="aec03-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="aec03-173">這可以使用資料Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aec03-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="aec03-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="aec03-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="aec03-175">配置 VPN 用戶端 IP 位址的位址空間。</span><span class="sxs-lookup"><span data-stu-id="aec03-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="aec03-176">這不應該與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="aec03-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="aec03-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="aec03-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="aec03-178">P2S VPN 用戶端用戶端服務通訊協定之 IPSec 策略清單。</span><span class="sxs-lookup"><span data-stu-id="aec03-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="aec03-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="aec03-179">-VpnClientProtocol</span></span>
<span data-ttu-id="aec03-180">P2S VPN 用戶端路由通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="aec03-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="aec03-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="aec03-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="aec03-182">已撤銷 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="aec03-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="aec03-183">如果 VPN 用戶端展示的憑證符合其中一項，系統將會要求離開。</span><span class="sxs-lookup"><span data-stu-id="aec03-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="aec03-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="aec03-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="aec03-185">VPN 用戶端根憑證清單，用於 VPN 用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="aec03-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="aec03-186">連接 VPN 用戶端必須呈現這些根憑證之一產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="aec03-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="aec03-187">-確認</span><span class="sxs-lookup"><span data-stu-id="aec03-187">-Confirm</span></span>
<span data-ttu-id="aec03-188">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="aec03-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec03-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec03-189">-WhatIf</span></span>
<span data-ttu-id="aec03-190">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aec03-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec03-191">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aec03-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec03-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec03-192">CommonParameters</span></span>
<span data-ttu-id="aec03-193">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aec03-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec03-194">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aec03-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec03-195">輸入</span><span class="sxs-lookup"><span data-stu-id="aec03-195">INPUTS</span></span>

### <span data-ttu-id="aec03-196">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aec03-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="aec03-197">System.String</span><span class="sxs-lookup"><span data-stu-id="aec03-197">System.String</span></span>

### <span data-ttu-id="aec03-198">Microsoft.Azure.Commands.Network.models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aec03-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="aec03-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="aec03-199">System.String[]</span></span>

### <span data-ttu-id="aec03-200">Microsoft.Azure.Commands.network.models.PS VpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="aec03-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="aec03-201">Microsoft.Azure.Commands.Network.models.PS VpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="aec03-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="aec03-202">Microsoft.Azure.Commands.Network.models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="aec03-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="aec03-203">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="aec03-203">System.UInt32</span></span>

### <span data-ttu-id="aec03-204">System.Int32</span><span class="sxs-lookup"><span data-stu-id="aec03-204">System.Int32</span></span>

### <span data-ttu-id="aec03-205">Microsoft.Azure.Commands.Network.models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="aec03-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="aec03-206">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="aec03-206">System.Security.SecureString</span></span>

## <span data-ttu-id="aec03-207">輸出</span><span class="sxs-lookup"><span data-stu-id="aec03-207">OUTPUTS</span></span>

### <span data-ttu-id="aec03-208">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aec03-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="aec03-209">筆記</span><span class="sxs-lookup"><span data-stu-id="aec03-209">NOTES</span></span>

## <span data-ttu-id="aec03-210">相關連結</span><span class="sxs-lookup"><span data-stu-id="aec03-210">RELATED LINKS</span></span>

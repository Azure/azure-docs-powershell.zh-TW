---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 92eab91d06a8624c00973bb35cc1a56dfd096a89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910022"
---
# <span data-ttu-id="d3e16-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d3e16-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="d3e16-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d3e16-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e16-103">建立 IPSec 連接，將 VpnGateway 連接至以 RM 表示為 VpnSite 的遠端客戶分支。</span><span class="sxs-lookup"><span data-stu-id="d3e16-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="d3e16-104">語法</span><span class="sxs-lookup"><span data-stu-id="d3e16-104">SYNTAX</span></span>

### <span data-ttu-id="d3e16-105">By VpnGatewayNameBy VpnSiteObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d3e16-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3e16-106">By VpnGatewayNameBy VpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e16-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e16-107">By VpnGatewayObjectBy VpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="d3e16-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e16-108">By VpnGatewayObjectBy VpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e16-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e16-109">By VpnGatewayResourceIdBy VpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="d3e16-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e16-110">By VpnGatewayResourceIdBy VpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e16-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e16-111">描述</span><span class="sxs-lookup"><span data-stu-id="d3e16-111">DESCRIPTION</span></span>
<span data-ttu-id="d3e16-112">建立 IPSec 連接，將 VpnGateway 連接至以 RM 表示為 VpnSite 的遠端客戶分支。</span><span class="sxs-lookup"><span data-stu-id="d3e16-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="d3e16-113">例子</span><span class="sxs-lookup"><span data-stu-id="d3e16-113">EXAMPLES</span></span>

### <span data-ttu-id="d3e16-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="d3e16-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="d3e16-115">上述步驟將在 Azure 的 「testRG」資源群組中，建立美國西部的資源群組、虛擬 WAN、虛擬網路、虛擬中樞和 VpnS 網站。</span><span class="sxs-lookup"><span data-stu-id="d3e16-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d3e16-116">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="d3e16-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d3e16-117">閘道建立完成後，即會使用 New-AzVpnConnection 命令連接到 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="d3e16-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="d3e16-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="d3e16-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="d3e16-119">上述專案將在 Azure 的 「testRG」資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞，以及美國西部有 1 個 VpnSiteLink 的 VpnSite 網站。</span><span class="sxs-lookup"><span data-stu-id="d3e16-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="d3e16-120">在此之後，將在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="d3e16-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="d3e16-121">閘道建立之後，它會使用 New-AzVpnConnection 命令與 1 個 VpnSiteLinkConnections 連接至 VpnSiteLink VpnSiteLink。</span><span class="sxs-lookup"><span data-stu-id="d3e16-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="d3e16-122">參數</span><span class="sxs-lookup"><span data-stu-id="d3e16-122">PARAMETERS</span></span>

### <span data-ttu-id="d3e16-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3e16-123">-AsJob</span></span>
<span data-ttu-id="d3e16-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d3e16-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3e16-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="d3e16-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="d3e16-126">此連接需要處理的頻寬 ，以 mbps 表示。</span><span class="sxs-lookup"><span data-stu-id="d3e16-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e16-127">-DefaultProfile</span></span>
<span data-ttu-id="d3e16-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3e16-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d3e16-129">-EnableBgp</span></span>
<span data-ttu-id="d3e16-130">為此連接啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="d3e16-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="d3e16-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d3e16-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="d3e16-132">啟用此連接的網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="d3e16-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="d3e16-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="d3e16-133">-IpSecPolicy</span></span>
<span data-ttu-id="d3e16-134">此連接需要處理的頻寬 ，以 mbps 表示。</span><span class="sxs-lookup"><span data-stu-id="d3e16-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3e16-135">-Name</span></span>
<span data-ttu-id="d3e16-136">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d3e16-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3e16-137">-ParentObject</span></span>
<span data-ttu-id="d3e16-138">此連接的父 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="d3e16-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e16-139">-ParentResourceId</span></span>
<span data-ttu-id="d3e16-140">此連接之父 VpnGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3e16-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d3e16-141">-ParentResourceName</span></span>
<span data-ttu-id="d3e16-142">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d3e16-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e16-143">-ResourceGroupName</span></span>
<span data-ttu-id="d3e16-144">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d3e16-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3e16-145">-RoutingConfiguration</span></span>
<span data-ttu-id="d3e16-146">此連接的路由群組原則</span><span class="sxs-lookup"><span data-stu-id="d3e16-146">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d3e16-147">-SharedKey</span></span>
<span data-ttu-id="d3e16-148">設定此連接所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="d3e16-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3e16-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="d3e16-150">啟動連接時，請使用本地 azure ip 位址做為來源位址。</span><span class="sxs-lookup"><span data-stu-id="d3e16-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="d3e16-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="d3e16-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="d3e16-152">針對此連接使用以策略為基礎的流量選取器。</span><span class="sxs-lookup"><span data-stu-id="d3e16-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="d3e16-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="d3e16-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="d3e16-154">閘道連接通訊協定：IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="d3e16-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-155">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d3e16-155">-VpnSite</span></span>
<span data-ttu-id="d3e16-156">此中樞虛擬網路連接所連接的遠端 vpn 網站。</span><span class="sxs-lookup"><span data-stu-id="d3e16-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="d3e16-157">-VpnSiteId</span></span>
<span data-ttu-id="d3e16-158">此中樞虛擬網路連接所連接的遠端 vpn 網站。</span><span class="sxs-lookup"><span data-stu-id="d3e16-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d3e16-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="d3e16-160">此 VpnConnection 的 VpnSiteLinkConnection 清單。</span><span class="sxs-lookup"><span data-stu-id="d3e16-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-161">-確認</span><span class="sxs-lookup"><span data-stu-id="d3e16-161">-Confirm</span></span>
<span data-ttu-id="d3e16-162">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d3e16-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e16-163">-WhatIf</span></span>
<span data-ttu-id="d3e16-164">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3e16-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e16-165">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3e16-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e16-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e16-166">CommonParameters</span></span>
<span data-ttu-id="d3e16-167">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d3e16-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e16-168">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3e16-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e16-169">輸入</span><span class="sxs-lookup"><span data-stu-id="d3e16-169">INPUTS</span></span>

### <span data-ttu-id="d3e16-170">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d3e16-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="d3e16-171">System.String</span><span class="sxs-lookup"><span data-stu-id="d3e16-171">System.String</span></span>

## <span data-ttu-id="d3e16-172">輸出</span><span class="sxs-lookup"><span data-stu-id="d3e16-172">OUTPUTS</span></span>

### <span data-ttu-id="d3e16-173">Microsoft.Azure.Commands.Network.models.PS VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d3e16-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="d3e16-174">筆記</span><span class="sxs-lookup"><span data-stu-id="d3e16-174">NOTES</span></span>

## <span data-ttu-id="d3e16-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3e16-175">RELATED LINKS</span></span>

[<span data-ttu-id="d3e16-176">Get-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d3e16-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="d3e16-177">Remove-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d3e16-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="d3e16-178">Update-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d3e16-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="d3e16-179">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3e16-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)

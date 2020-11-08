---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 3b7bf41818ded2b866ea72a81ff1c17ccc365358
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139759"
---
# <span data-ttu-id="6f82b-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6f82b-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="6f82b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f82b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f82b-103">建立可將 VpnGateway 連線至 RM 中所代表的遠端客戶分支的 IPSec 連線，成為 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="6f82b-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="6f82b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f82b-104">SYNTAX</span></span>

### <span data-ttu-id="6f82b-105">ByVpnGatewayNameByVpnSiteObject (預設) </span><span class="sxs-lookup"><span data-stu-id="6f82b-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f82b-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="6f82b-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f82b-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="6f82b-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f82b-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="6f82b-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f82b-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="6f82b-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f82b-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="6f82b-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f82b-111">說明</span><span class="sxs-lookup"><span data-stu-id="6f82b-111">DESCRIPTION</span></span>
<span data-ttu-id="6f82b-112">建立可將 VpnGateway 連線至 RM 中所代表的遠端客戶分支的 IPSec 連線，成為 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="6f82b-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="6f82b-113">示例</span><span class="sxs-lookup"><span data-stu-id="6f82b-113">EXAMPLES</span></span>

### <span data-ttu-id="6f82b-114">範例1</span><span class="sxs-lookup"><span data-stu-id="6f82b-114">Example 1</span></span>

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

<span data-ttu-id="6f82b-115">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="6f82b-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6f82b-116">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="6f82b-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="6f82b-117">建立閘道之後，就會使用 [New-AzVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="6f82b-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="6f82b-118">範例2</span><span class="sxs-lookup"><span data-stu-id="6f82b-118">Example 2</span></span>
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

<span data-ttu-id="6f82b-119">上述將會建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞，以及在 VpnSiteLinks 中使用1的 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="6f82b-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="6f82b-120">在虛擬中樞之後，就會建立一個 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="6f82b-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="6f82b-121">建立閘道之後，就會使用 New-AzVpnConnection 命令將其連線至 VpnSite，並將 1 VpnSiteLinkConnections 至 VpnSite 的 VpnSiteLink。</span><span class="sxs-lookup"><span data-stu-id="6f82b-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="6f82b-122">參數</span><span class="sxs-lookup"><span data-stu-id="6f82b-122">PARAMETERS</span></span>

### <span data-ttu-id="6f82b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f82b-123">-AsJob</span></span>
<span data-ttu-id="6f82b-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6f82b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f82b-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="6f82b-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="6f82b-126">此連線所需處理的頻寬（以 mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="6f82b-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="6f82b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f82b-127">-DefaultProfile</span></span>
<span data-ttu-id="6f82b-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f82b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f82b-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6f82b-129">-EnableBgp</span></span>
<span data-ttu-id="6f82b-130">針對此連線啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="6f82b-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="6f82b-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6f82b-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="6f82b-132">針對此連線啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="6f82b-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="6f82b-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="6f82b-133">-IpSecPolicy</span></span>
<span data-ttu-id="6f82b-134">此連線所需處理的頻寬（以 mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="6f82b-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="6f82b-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f82b-135">-Name</span></span>
<span data-ttu-id="6f82b-136">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6f82b-136">The resource name.</span></span>

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

### <span data-ttu-id="6f82b-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6f82b-137">-ParentObject</span></span>
<span data-ttu-id="6f82b-138">此連接的父 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="6f82b-138">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="6f82b-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6f82b-139">-ParentResourceId</span></span>
<span data-ttu-id="6f82b-140">此連線之父 VpnGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f82b-140">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="6f82b-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6f82b-141">-ParentResourceName</span></span>
<span data-ttu-id="6f82b-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f82b-142">The resource group name.</span></span>

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

### <span data-ttu-id="6f82b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f82b-143">-ResourceGroupName</span></span>
<span data-ttu-id="6f82b-144">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f82b-144">The resource group name.</span></span>

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

### <span data-ttu-id="6f82b-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f82b-145">-RoutingConfiguration</span></span>
<span data-ttu-id="6f82b-146">此連線的路由設定</span><span class="sxs-lookup"><span data-stu-id="6f82b-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="6f82b-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6f82b-147">-SharedKey</span></span>
<span data-ttu-id="6f82b-148">設定此連線所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="6f82b-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="6f82b-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="6f82b-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="6f82b-150">啟動連線時，請使用本機 azure ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="6f82b-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="6f82b-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6f82b-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6f82b-152">針對這個連線使用原則的流量選取器。</span><span class="sxs-lookup"><span data-stu-id="6f82b-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="6f82b-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="6f82b-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="6f82b-154">閘道連線通訊協定： IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="6f82b-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="6f82b-155">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6f82b-155">-VpnSite</span></span>
<span data-ttu-id="6f82b-156">此中樞虛擬網路連線所連結的遠端 vpn 網站。</span><span class="sxs-lookup"><span data-stu-id="6f82b-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="6f82b-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="6f82b-157">-VpnSiteId</span></span>
<span data-ttu-id="6f82b-158">此中樞虛擬網路連線所連結的遠端 vpn 網站。</span><span class="sxs-lookup"><span data-stu-id="6f82b-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="6f82b-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6f82b-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="6f82b-160">此 VpnConnection 的 VpnSiteLinkConnections 清單。</span><span class="sxs-lookup"><span data-stu-id="6f82b-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

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

### <span data-ttu-id="6f82b-161">-確認</span><span class="sxs-lookup"><span data-stu-id="6f82b-161">-Confirm</span></span>
<span data-ttu-id="6f82b-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f82b-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f82b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f82b-163">-WhatIf</span></span>
<span data-ttu-id="6f82b-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f82b-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f82b-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f82b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f82b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f82b-166">CommonParameters</span></span>
<span data-ttu-id="6f82b-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f82b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f82b-168">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6f82b-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f82b-169">輸入</span><span class="sxs-lookup"><span data-stu-id="6f82b-169">INPUTS</span></span>

### <span data-ttu-id="6f82b-170">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6f82b-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="6f82b-171">System.object</span><span class="sxs-lookup"><span data-stu-id="6f82b-171">System.String</span></span>

## <span data-ttu-id="6f82b-172">輸出</span><span class="sxs-lookup"><span data-stu-id="6f82b-172">OUTPUTS</span></span>

### <span data-ttu-id="6f82b-173">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6f82b-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="6f82b-174">筆記</span><span class="sxs-lookup"><span data-stu-id="6f82b-174">NOTES</span></span>

## <span data-ttu-id="6f82b-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f82b-175">RELATED LINKS</span></span>

[<span data-ttu-id="6f82b-176">AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6f82b-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="6f82b-177">移除-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6f82b-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="6f82b-178">更新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6f82b-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="6f82b-179">新-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f82b-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
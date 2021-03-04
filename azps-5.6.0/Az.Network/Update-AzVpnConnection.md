---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 3de80ca92f86ab969b9d44ffc9f63871486d969a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901789"
---
# <span data-ttu-id="7e86b-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e86b-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="7e86b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e86b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e86b-103">更新 VPN 連接。</span><span class="sxs-lookup"><span data-stu-id="7e86b-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="7e86b-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e86b-104">SYNTAX</span></span>

### <span data-ttu-id="7e86b-105">By VpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="7e86b-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e86b-106">By VpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="7e86b-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e86b-107">By VpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="7e86b-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e86b-108">描述</span><span class="sxs-lookup"><span data-stu-id="7e86b-108">DESCRIPTION</span></span>
<span data-ttu-id="7e86b-109">**Update-Az VpnConnection** Cmdlet 會更新 VPN 連接。</span><span class="sxs-lookup"><span data-stu-id="7e86b-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="7e86b-110">VPN 連接會建立 IPsec 連接，將 VPN 閘道連接至 Azure 中以 VPN 網站表示的遠端客戶分支。</span><span class="sxs-lookup"><span data-stu-id="7e86b-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="7e86b-111">例子</span><span class="sxs-lookup"><span data-stu-id="7e86b-111">EXAMPLES</span></span>

### <span data-ttu-id="7e86b-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="7e86b-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="7e86b-113">上述步驟將在 Azure 的 「testRG」資源群組中，建立美國西部的資源群組、虛擬 WAN、虛擬網路、虛擬中樞和 VpnS 網站。</span><span class="sxs-lookup"><span data-stu-id="7e86b-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7e86b-114">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="7e86b-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7e86b-115">閘道建立完成後，即會使用 New-AzVpnConnection 命令連接到 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="7e86b-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="7e86b-116">接著，使用 Set-AzVpnConnection 命令更新該連接以擁有新的 IpSecPolicy。</span><span class="sxs-lookup"><span data-stu-id="7e86b-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="7e86b-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="7e86b-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="7e86b-118">上述步驟將在 Azure 的 「testRG」資源群組中，建立美國西部的資源群組、虛擬 WAN、虛擬網路、虛擬中樞和 VpnS 網站。</span><span class="sxs-lookup"><span data-stu-id="7e86b-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7e86b-119">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="7e86b-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7e86b-120">閘道建立完成後，即會使用 New-AzVpnConnection 命令連接到 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="7e86b-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="7e86b-121">接著，該連接會更新為使用安全字串結構的新共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="7e86b-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="7e86b-122">參數</span><span class="sxs-lookup"><span data-stu-id="7e86b-122">PARAMETERS</span></span>

### <span data-ttu-id="7e86b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e86b-123">-AsJob</span></span>
<span data-ttu-id="7e86b-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e86b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e86b-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="7e86b-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="7e86b-126">此連接需要處理的頻寬 ，以 mbps 表示。</span><span class="sxs-lookup"><span data-stu-id="7e86b-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="7e86b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e86b-127">-DefaultProfile</span></span>
<span data-ttu-id="7e86b-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e86b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e86b-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7e86b-129">-EnableBgp</span></span>
<span data-ttu-id="7e86b-130">為此連接啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="7e86b-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7e86b-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="7e86b-132">啟用此連接的網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="7e86b-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e86b-133">-InputObject</span></span>
<span data-ttu-id="7e86b-134">要更新的 VpnConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="7e86b-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="7e86b-135">-IpSecPolicy</span></span>
<span data-ttu-id="7e86b-136">此連接需要處理的頻寬 ，以 mbps 表示。</span><span class="sxs-lookup"><span data-stu-id="7e86b-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="7e86b-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e86b-137">-Name</span></span>
<span data-ttu-id="7e86b-138">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7e86b-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="7e86b-139">-ParentResourceName</span></span>
<span data-ttu-id="7e86b-140">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7e86b-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e86b-141">-ResourceGroupName</span></span>
<span data-ttu-id="7e86b-142">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7e86b-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e86b-143">-ResourceId</span></span>
<span data-ttu-id="7e86b-144">要刪除之 VpnConnection 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e86b-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e86b-145">-RoutingConfiguration</span></span>
<span data-ttu-id="7e86b-146">此連接的路由群組原則</span><span class="sxs-lookup"><span data-stu-id="7e86b-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="7e86b-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7e86b-147">-SharedKey</span></span>
<span data-ttu-id="7e86b-148">設定此連接所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="7e86b-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="7e86b-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e86b-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="7e86b-150">啟動連接時，請使用本地 azure ip 位址做為來源位址。</span><span class="sxs-lookup"><span data-stu-id="7e86b-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7e86b-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7e86b-152">針對此連接使用以策略為基礎的流量選取器。</span><span class="sxs-lookup"><span data-stu-id="7e86b-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e86b-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7e86b-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="7e86b-154">此 VpnConnection 所需的 VpnSiteLinkConnection 清單。</span><span class="sxs-lookup"><span data-stu-id="7e86b-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="7e86b-155">-確認</span><span class="sxs-lookup"><span data-stu-id="7e86b-155">-Confirm</span></span>
<span data-ttu-id="7e86b-156">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7e86b-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e86b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e86b-157">-WhatIf</span></span>
<span data-ttu-id="7e86b-158">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e86b-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e86b-159">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e86b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e86b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e86b-160">CommonParameters</span></span>
<span data-ttu-id="7e86b-161">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e86b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e86b-162">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e86b-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e86b-163">輸入</span><span class="sxs-lookup"><span data-stu-id="7e86b-163">INPUTS</span></span>

### <span data-ttu-id="7e86b-164">System.String</span><span class="sxs-lookup"><span data-stu-id="7e86b-164">System.String</span></span>

### <span data-ttu-id="7e86b-165">Microsoft.Azure.Commands.Network.models.PS VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e86b-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="7e86b-166">輸出</span><span class="sxs-lookup"><span data-stu-id="7e86b-166">OUTPUTS</span></span>

### <span data-ttu-id="7e86b-167">Microsoft.Azure.Commands.Network.models.PS VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e86b-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="7e86b-168">筆記</span><span class="sxs-lookup"><span data-stu-id="7e86b-168">NOTES</span></span>

## <span data-ttu-id="7e86b-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e86b-169">RELATED LINKS</span></span>

[<span data-ttu-id="7e86b-170">Get-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e86b-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="7e86b-171">New-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e86b-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="7e86b-172">Remove-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e86b-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="7e86b-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e86b-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137387"
---
# <span data-ttu-id="7bd7e-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7bd7e-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="7bd7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bd7e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd7e-103">更新 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="7bd7e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bd7e-104">SYNTAX</span></span>

### <span data-ttu-id="7bd7e-105">ByVpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="7bd7e-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd7e-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd7e-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bd7e-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="7bd7e-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bd7e-108">說明</span><span class="sxs-lookup"><span data-stu-id="7bd7e-108">DESCRIPTION</span></span>
<span data-ttu-id="7bd7e-109">**AzVpnConnection** Cmdlet 會更新 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="7bd7e-110">VPN 連線建立 IPsec 連線，該連線會將 VPN 閘道連線至 Azure 中代表 VPN 網站的遠端客戶分支。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="7bd7e-111">示例</span><span class="sxs-lookup"><span data-stu-id="7bd7e-111">EXAMPLES</span></span>

### <span data-ttu-id="7bd7e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7bd7e-112">Example 1</span></span>

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

<span data-ttu-id="7bd7e-113">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7bd7e-114">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7bd7e-115">建立閘道之後，就會使用 [New-AzVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="7bd7e-116">接著，您可以使用 Set-AzVpnConnection 命令來更新連接，以進行新的 IpSecPolicy。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="7bd7e-117">範例2</span><span class="sxs-lookup"><span data-stu-id="7bd7e-117">Example 2</span></span>

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

<span data-ttu-id="7bd7e-118">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7bd7e-119">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7bd7e-120">建立閘道之後，就會使用 [New-AzVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="7bd7e-121">接著，就會使用安全的字串構造來更新連接，以建立新的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="7bd7e-122">參數</span><span class="sxs-lookup"><span data-stu-id="7bd7e-122">PARAMETERS</span></span>

### <span data-ttu-id="7bd7e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bd7e-123">-AsJob</span></span>
<span data-ttu-id="7bd7e-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7bd7e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bd7e-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="7bd7e-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="7bd7e-126">此連線所需處理的頻寬（以 mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="7bd7e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd7e-127">-DefaultProfile</span></span>
<span data-ttu-id="7bd7e-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd7e-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7bd7e-129">-EnableBgp</span></span>
<span data-ttu-id="7bd7e-130">針對此連線啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="7bd7e-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="7bd7e-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7bd7e-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="7bd7e-132">針對此連線啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="7bd7e-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="7bd7e-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bd7e-133">-InputObject</span></span>
<span data-ttu-id="7bd7e-134">要更新的 VpnConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="7bd7e-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="7bd7e-135">-IpSecPolicy</span></span>
<span data-ttu-id="7bd7e-136">此連線所需處理的頻寬（以 mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="7bd7e-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bd7e-137">-Name</span></span>
<span data-ttu-id="7bd7e-138">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-138">The resource name.</span></span>

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

### <span data-ttu-id="7bd7e-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="7bd7e-139">-ParentResourceName</span></span>
<span data-ttu-id="7bd7e-140">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-140">The parent resource name.</span></span>

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

### <span data-ttu-id="7bd7e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd7e-141">-ResourceGroupName</span></span>
<span data-ttu-id="7bd7e-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-142">The resource group name.</span></span>

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

### <span data-ttu-id="7bd7e-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd7e-143">-ResourceId</span></span>
<span data-ttu-id="7bd7e-144">要刪除之 VpnConnection 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="7bd7e-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bd7e-145">-RoutingConfiguration</span></span>
<span data-ttu-id="7bd7e-146">此連線的路由設定</span><span class="sxs-lookup"><span data-stu-id="7bd7e-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="7bd7e-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7bd7e-147">-SharedKey</span></span>
<span data-ttu-id="7bd7e-148">設定此連線所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="7bd7e-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="7bd7e-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="7bd7e-150">啟動連線時，請使用本機 azure ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="7bd7e-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7bd7e-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7bd7e-152">針對這個連線使用原則的流量選取器。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="7bd7e-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7bd7e-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="7bd7e-154">此 VpnConnection 所需的 VpnSiteLinkConnections 清單。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="7bd7e-155">-確認</span><span class="sxs-lookup"><span data-stu-id="7bd7e-155">-Confirm</span></span>
<span data-ttu-id="7bd7e-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd7e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd7e-157">-WhatIf</span></span>
<span data-ttu-id="7bd7e-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd7e-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd7e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd7e-160">CommonParameters</span></span>
<span data-ttu-id="7bd7e-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd7e-162">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7bd7e-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd7e-163">輸入</span><span class="sxs-lookup"><span data-stu-id="7bd7e-163">INPUTS</span></span>

### <span data-ttu-id="7bd7e-164">System.object</span><span class="sxs-lookup"><span data-stu-id="7bd7e-164">System.String</span></span>

### <span data-ttu-id="7bd7e-165">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7bd7e-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="7bd7e-166">輸出</span><span class="sxs-lookup"><span data-stu-id="7bd7e-166">OUTPUTS</span></span>

### <span data-ttu-id="7bd7e-167">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7bd7e-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="7bd7e-168">筆記</span><span class="sxs-lookup"><span data-stu-id="7bd7e-168">NOTES</span></span>

## <span data-ttu-id="7bd7e-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bd7e-169">RELATED LINKS</span></span>

[<span data-ttu-id="7bd7e-170">AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7bd7e-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="7bd7e-171">新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7bd7e-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="7bd7e-172">移除-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7bd7e-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="7bd7e-173">新-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bd7e-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
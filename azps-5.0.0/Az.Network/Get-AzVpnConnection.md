---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 6ad7f5fcdaafed47d7292444370e332188f444b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286919"
---
# <span data-ttu-id="9fcee-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fcee-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="9fcee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9fcee-102">SYNOPSIS</span></span>
<span data-ttu-id="9fcee-103">透過名稱取得 vpn 連線，或列出連接至 VpnGateway 的所有 vpn 連線。</span><span class="sxs-lookup"><span data-stu-id="9fcee-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="9fcee-104">句法</span><span class="sxs-lookup"><span data-stu-id="9fcee-104">SYNTAX</span></span>

### <span data-ttu-id="9fcee-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="9fcee-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fcee-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9fcee-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fcee-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9fcee-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fcee-108">說明</span><span class="sxs-lookup"><span data-stu-id="9fcee-108">DESCRIPTION</span></span>
<span data-ttu-id="9fcee-109">透過名稱取得 vpn 連線，或列出連接至 VpnGateway 的所有 vpn 連線。</span><span class="sxs-lookup"><span data-stu-id="9fcee-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="9fcee-110">示例</span><span class="sxs-lookup"><span data-stu-id="9fcee-110">EXAMPLES</span></span>

### <span data-ttu-id="9fcee-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9fcee-111">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
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

<span data-ttu-id="9fcee-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="9fcee-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="9fcee-113">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="9fcee-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="9fcee-114">建立閘道之後，就會使用 [New-AzVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="9fcee-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="9fcee-115">然後它會使用連接名稱取得連線。</span><span class="sxs-lookup"><span data-stu-id="9fcee-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="9fcee-116">範例2</span><span class="sxs-lookup"><span data-stu-id="9fcee-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1
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

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
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

<span data-ttu-id="9fcee-117">這個 Cmdlet 會取得所有以「test」開頭的連線。</span><span class="sxs-lookup"><span data-stu-id="9fcee-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="9fcee-118">參數</span><span class="sxs-lookup"><span data-stu-id="9fcee-118">PARAMETERS</span></span>

### <span data-ttu-id="9fcee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fcee-119">-DefaultProfile</span></span>
<span data-ttu-id="9fcee-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fcee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fcee-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fcee-121">-Name</span></span>
<span data-ttu-id="9fcee-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcee-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fcee-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9fcee-123">-ParentObject</span></span>
<span data-ttu-id="9fcee-124">此連接的父 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="9fcee-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fcee-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9fcee-125">-ParentResourceId</span></span>
<span data-ttu-id="9fcee-126">此連線之父 VpnGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fcee-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fcee-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9fcee-127">-ParentResourceName</span></span>
<span data-ttu-id="9fcee-128">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcee-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fcee-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fcee-129">-ResourceGroupName</span></span>
<span data-ttu-id="9fcee-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcee-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fcee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fcee-131">CommonParameters</span></span>
<span data-ttu-id="9fcee-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9fcee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fcee-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9fcee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fcee-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9fcee-134">INPUTS</span></span>

### <span data-ttu-id="9fcee-135">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9fcee-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="9fcee-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9fcee-136">System.String</span></span>

## <span data-ttu-id="9fcee-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9fcee-137">OUTPUTS</span></span>

### <span data-ttu-id="9fcee-138">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9fcee-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="9fcee-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9fcee-139">NOTES</span></span>

## <span data-ttu-id="9fcee-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fcee-140">RELATED LINKS</span></span>

[<span data-ttu-id="9fcee-141">新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fcee-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="9fcee-142">移除-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fcee-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="9fcee-143">更新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fcee-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

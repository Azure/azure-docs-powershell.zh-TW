---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 4f61bce910a2dc0f2b177423a5dc199103da378d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909998"
---
# <span data-ttu-id="00e62-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="00e62-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="00e62-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00e62-102">SYNOPSIS</span></span>
<span data-ttu-id="00e62-103">建立 Azure VpnSiteLinkConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="00e62-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="00e62-104">語法</span><span class="sxs-lookup"><span data-stu-id="00e62-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-IngressNatRule <PSResourceId[]>] [-EgressNatRule <PSResourceId[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00e62-105">描述</span><span class="sxs-lookup"><span data-stu-id="00e62-105">DESCRIPTION</span></span>
<span data-ttu-id="00e62-106">建立 Azure VpnSiteLinkConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="00e62-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="00e62-107">例子</span><span class="sxs-lookup"><span data-stu-id="00e62-107">EXAMPLES</span></span>

### <span data-ttu-id="00e62-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="00e62-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="00e62-109">上述專案將在 Azure 的 「testRG」資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞，以及美國西部有 1 個 VpnSiteLink 的 VpnSite 網站。</span><span class="sxs-lookup"><span data-stu-id="00e62-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="00e62-110">在此之後，將在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="00e62-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="00e62-111">閘道建立之後，它會使用 New-AzVpnConnection 命令與 1 個 VpnSiteLinkConnections 連接至 VpnSiteLink VpnSiteLink。</span><span class="sxs-lookup"><span data-stu-id="00e62-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="00e62-112">參數</span><span class="sxs-lookup"><span data-stu-id="00e62-112">PARAMETERS</span></span>

### <span data-ttu-id="00e62-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="00e62-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="00e62-114">此連結連接需要處理的頻寬 ，以 mbps 表示。</span><span class="sxs-lookup"><span data-stu-id="00e62-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e62-115">-DefaultProfile</span></span>
<span data-ttu-id="00e62-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00e62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00e62-117">-EgressNatRule</span><span class="sxs-lookup"><span data-stu-id="00e62-117">-EgressNatRule</span></span>
<span data-ttu-id="00e62-118">與此連結連接關聯的出口 NAT 規則清單。</span><span class="sxs-lookup"><span data-stu-id="00e62-118">The list of egress  NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-119">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="00e62-119">-EnableBgp</span></span>
<span data-ttu-id="00e62-120">針對此連結連接啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="00e62-120">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="00e62-121">-IngressNatRule</span><span class="sxs-lookup"><span data-stu-id="00e62-121">-IngressNatRule</span></span>
<span data-ttu-id="00e62-122">與此連結連接關聯的入口 NAT 規則清單。</span><span class="sxs-lookup"><span data-stu-id="00e62-122">The list of ingress NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-123">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="00e62-123">-IpSecPolicy</span></span>
<span data-ttu-id="00e62-124">此連結連接要考慮的 IpSec 政策。</span><span class="sxs-lookup"><span data-stu-id="00e62-124">IpSec Policy to be considered for this link connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="00e62-125">-Name</span></span>
<span data-ttu-id="00e62-126">名字</span><span class="sxs-lookup"><span data-stu-id="00e62-126">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-127">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="00e62-127">-RoutingWeight</span></span>
<span data-ttu-id="00e62-128">路由粗細</span><span class="sxs-lookup"><span data-stu-id="00e62-128">Routing Weight</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-129">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="00e62-129">-SharedKey</span></span>
<span data-ttu-id="00e62-130">設定此連結連接所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="00e62-130">The shared key required to set this link connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="00e62-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="00e62-132">使用此連結連接時，請使用本地 azure ip 位址做為來源 IP。</span><span class="sxs-lookup"><span data-stu-id="00e62-132">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="00e62-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="00e62-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="00e62-134">針對此連結連接使用以策略為基礎的流量選取器。</span><span class="sxs-lookup"><span data-stu-id="00e62-134">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="00e62-135">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="00e62-135">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="00e62-136">閘道連接通訊協定：IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="00e62-136">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-137">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="00e62-137">-VpnSiteLink</span></span>
<span data-ttu-id="00e62-138">要連接的 vpn 網站連結化物件。</span><span class="sxs-lookup"><span data-stu-id="00e62-138">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00e62-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e62-139">CommonParameters</span></span>
<span data-ttu-id="00e62-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00e62-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e62-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00e62-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e62-142">輸入</span><span class="sxs-lookup"><span data-stu-id="00e62-142">INPUTS</span></span>

### <span data-ttu-id="00e62-143">Microsoft.Azure.Commands.Network.models.PS VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="00e62-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="00e62-144">輸出</span><span class="sxs-lookup"><span data-stu-id="00e62-144">OUTPUTS</span></span>

### <span data-ttu-id="00e62-145">Microsoft.Azure.Commands.Network.models.PS VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="00e62-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="00e62-146">筆記</span><span class="sxs-lookup"><span data-stu-id="00e62-146">NOTES</span></span>

## <span data-ttu-id="00e62-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="00e62-147">RELATED LINKS</span></span>

[<span data-ttu-id="00e62-148">New-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="00e62-148">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 31679702c1499ac91f41b14057e1bc13ef2dfc32
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286828"
---
# <span data-ttu-id="b5526-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="b5526-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="b5526-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5526-102">SYNOPSIS</span></span>
<span data-ttu-id="b5526-103">建立 Azure VpnSiteLinkConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="b5526-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="b5526-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5526-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5526-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5526-105">DESCRIPTION</span></span>
<span data-ttu-id="b5526-106">建立 Azure VpnSiteLinkConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="b5526-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="b5526-107">示例</span><span class="sxs-lookup"><span data-stu-id="b5526-107">EXAMPLES</span></span>

### <span data-ttu-id="b5526-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b5526-108">Example 1</span></span>
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

<span data-ttu-id="b5526-109">上述將會建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞，以及在 VpnSiteLinks 中使用1的 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="b5526-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="b5526-110">在虛擬中樞之後，就會建立一個 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="b5526-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="b5526-111">建立閘道之後，就會使用 New-AzVpnConnection 命令將其連線至 VpnSite，並將 1 VpnSiteLinkConnections 至 VpnSite 的 VpnSiteLink。</span><span class="sxs-lookup"><span data-stu-id="b5526-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="b5526-112">參數</span><span class="sxs-lookup"><span data-stu-id="b5526-112">PARAMETERS</span></span>

### <span data-ttu-id="b5526-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="b5526-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="b5526-114">需要由此連結連線處理的頻寬（以 mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="b5526-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="b5526-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5526-115">-DefaultProfile</span></span>
<span data-ttu-id="b5526-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5526-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5526-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="b5526-117">-EnableBgp</span></span>
<span data-ttu-id="b5526-118">針對此連結連線啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="b5526-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="b5526-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="b5526-119">-IpSecPolicy</span></span>
<span data-ttu-id="b5526-120">要針對此連結連線考慮的 IpSec 原則。</span><span class="sxs-lookup"><span data-stu-id="b5526-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="b5526-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5526-121">-Name</span></span>
<span data-ttu-id="b5526-122">列名</span><span class="sxs-lookup"><span data-stu-id="b5526-122">Name</span></span>

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

### <span data-ttu-id="b5526-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="b5526-123">-RoutingWeight</span></span>
<span data-ttu-id="b5526-124">佈線體重</span><span class="sxs-lookup"><span data-stu-id="b5526-124">Routing Weight</span></span>

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

### <span data-ttu-id="b5526-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b5526-125">-SharedKey</span></span>
<span data-ttu-id="b5526-126">需要將此連結連線設定為 [共用金鑰]。</span><span class="sxs-lookup"><span data-stu-id="b5526-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="b5526-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5526-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="b5526-128">使用本機 azure ip 位址作為此連結連線的來源 ip。</span><span class="sxs-lookup"><span data-stu-id="b5526-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="b5526-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="b5526-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="b5526-130">針對此連結連線使用 [以原則為基礎的流量選取器]。</span><span class="sxs-lookup"><span data-stu-id="b5526-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="b5526-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="b5526-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="b5526-132">閘道連線通訊協定： IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="b5526-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="b5526-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b5526-133">-VpnSiteLink</span></span>
<span data-ttu-id="b5526-134">要連接的 vpn 網站連結化物件。</span><span class="sxs-lookup"><span data-stu-id="b5526-134">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="b5526-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5526-135">CommonParameters</span></span>
<span data-ttu-id="b5526-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5526-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5526-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b5526-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5526-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b5526-138">INPUTS</span></span>

### <span data-ttu-id="b5526-139">PSVpnSiteLink 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b5526-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="b5526-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b5526-140">OUTPUTS</span></span>

### <span data-ttu-id="b5526-141">PSVpnSiteLinkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b5526-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="b5526-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b5526-142">NOTES</span></span>

## <span data-ttu-id="b5526-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5526-143">RELATED LINKS</span></span>

[<span data-ttu-id="b5526-144">新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b5526-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)
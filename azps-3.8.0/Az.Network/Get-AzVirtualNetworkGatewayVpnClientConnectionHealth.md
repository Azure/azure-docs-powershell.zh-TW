---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 9033d389990efb7bf17c568512becedaf475cc56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957322"
---
# <span data-ttu-id="e557c-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e557c-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="e557c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e557c-102">SYNOPSIS</span></span> 
<span data-ttu-id="e557c-103">取得每個 vpn 用戶端連線之 Azure 虛擬閘道的 vpn 用戶端連線健康情況清單</span><span class="sxs-lookup"><span data-stu-id="e557c-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="e557c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e557c-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="e557c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e557c-105">DESCRIPTION</span></span>
<span data-ttu-id="e557c-106">列出所有連線的 vpn 用戶端連線健康情況。</span><span class="sxs-lookup"><span data-stu-id="e557c-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="e557c-107">這包括： vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="e557c-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="e557c-108">示例</span><span class="sxs-lookup"><span data-stu-id="e557c-108">EXAMPLES</span></span>

### <span data-ttu-id="e557c-109">範例1</span><span class="sxs-lookup"><span data-stu-id="e557c-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName gatewayName -ResourceGroupName resourceGroup

VpnConnectionId           : OVPN_0085393D-B345-4846-0426-140616833F4C
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39672
PrivateIpAddress          : 10.1.1.131
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104084
EgressBytesTransferred    : 4059276
IngressPacketsTransferred : 1410
IngressBytesTransferred   : 67680
MaxPacketsPerSecond       : 1

VpnConnectionId           : OVPN_00F692AC-2D6F-DE7B-DCAF-07BE896233A0
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39692
PrivateIpAddress          : 10.1.1.79
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104623
EgressBytesTransferred    : 4080297
IngressPacketsTransferred : 1416
IngressBytesTransferred   : 67968
MaxPacketsPerSecond       : 1
```

<span data-ttu-id="e557c-110">針對資源群組 resourceGroup 中名為 gatewayname 的 Azure 虛擬網路閘道，請使用 OpenVpn 來檢索目前連線的 vpn 用戶端連線。</span><span class="sxs-lookup"><span data-stu-id="e557c-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

## <span data-ttu-id="e557c-111">參數</span><span class="sxs-lookup"><span data-stu-id="e557c-111">PARAMETERS</span></span>

### <span data-ttu-id="e557c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e557c-112">-ResourceGroupName</span></span>
<span data-ttu-id="e557c-113">虛擬網路閘道資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e557c-113">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e557c-114">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="e557c-114">-ResourceName</span></span>
<span data-ttu-id="e557c-115">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="e557c-115">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="e557c-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e557c-116">-ResourceId</span></span>
<span data-ttu-id="e557c-117">虛擬網路閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e557c-117">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e557c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e557c-118">-InputObject</span></span>
<span data-ttu-id="e557c-119">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="e557c-119">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e557c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e557c-120">-AsJob</span></span>
<span data-ttu-id="e557c-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e557c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e557c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e557c-122">CommonParameters</span></span>
<span data-ttu-id="e557c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e557c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e557c-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e557c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e557c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e557c-125">INPUTS</span></span>

### <span data-ttu-id="e557c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="e557c-126">System.String</span></span>

## <span data-ttu-id="e557c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e557c-127">OUTPUTS</span></span>

### <span data-ttu-id="e557c-128">PSGatewayRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e557c-128">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="e557c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e557c-129">NOTES</span></span>

## <span data-ttu-id="e557c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e557c-130">RELATED LINKS</span></span>

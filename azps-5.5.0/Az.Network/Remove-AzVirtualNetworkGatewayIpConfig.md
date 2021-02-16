---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 3287644b3f953c001490c7be207865a88b000e10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128750"
---
# <span data-ttu-id="884f9-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="884f9-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="884f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="884f9-102">SYNOPSIS</span></span>
<span data-ttu-id="884f9-103">從虛擬網路閘道移除 IP 配置</span><span class="sxs-lookup"><span data-stu-id="884f9-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="884f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="884f9-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="884f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="884f9-105">DESCRIPTION</span></span>
<span data-ttu-id="884f9-106">從虛擬網路閘道移除 IP 配置</span><span class="sxs-lookup"><span data-stu-id="884f9-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="884f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="884f9-107">EXAMPLES</span></span>

### <span data-ttu-id="884f9-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="884f9-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="884f9-109">參數</span><span class="sxs-lookup"><span data-stu-id="884f9-109">PARAMETERS</span></span>

### <span data-ttu-id="884f9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884f9-110">-DefaultProfile</span></span>
<span data-ttu-id="884f9-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="884f9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="884f9-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="884f9-112">-Name</span></span>
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

### <span data-ttu-id="884f9-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="884f9-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="884f9-114">-確認</span><span class="sxs-lookup"><span data-stu-id="884f9-114">-Confirm</span></span>
<span data-ttu-id="884f9-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="884f9-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f9-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="884f9-116">-WhatIf</span></span>
<span data-ttu-id="884f9-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="884f9-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="884f9-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="884f9-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884f9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884f9-119">CommonParameters</span></span>
<span data-ttu-id="884f9-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="884f9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884f9-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="884f9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884f9-122">輸入</span><span class="sxs-lookup"><span data-stu-id="884f9-122">INPUTS</span></span>

### <span data-ttu-id="884f9-123">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="884f9-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="884f9-124">輸出</span><span class="sxs-lookup"><span data-stu-id="884f9-124">OUTPUTS</span></span>

### <span data-ttu-id="884f9-125">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="884f9-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="884f9-126">筆記</span><span class="sxs-lookup"><span data-stu-id="884f9-126">NOTES</span></span>

## <span data-ttu-id="884f9-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="884f9-127">RELATED LINKS</span></span>

[<span data-ttu-id="884f9-128">附加 AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="884f9-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="884f9-129">新-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="884f9-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

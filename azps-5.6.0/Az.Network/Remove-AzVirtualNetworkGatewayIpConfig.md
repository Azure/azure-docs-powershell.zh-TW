---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: d8f77ffd6353ef55548e8ddc2a2cc4f823efe98d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915950"
---
# <span data-ttu-id="de3a2-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="de3a2-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="de3a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de3a2-102">SYNOPSIS</span></span>
<span data-ttu-id="de3a2-103">從虛擬網路閘道移除 IP 組</span><span class="sxs-lookup"><span data-stu-id="de3a2-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="de3a2-104">語法</span><span class="sxs-lookup"><span data-stu-id="de3a2-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3a2-105">描述</span><span class="sxs-lookup"><span data-stu-id="de3a2-105">DESCRIPTION</span></span>
<span data-ttu-id="de3a2-106">從虛擬網路閘道移除 IP 組</span><span class="sxs-lookup"><span data-stu-id="de3a2-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="de3a2-107">例子</span><span class="sxs-lookup"><span data-stu-id="de3a2-107">EXAMPLES</span></span>

### <span data-ttu-id="de3a2-108">範例 1：</span><span class="sxs-lookup"><span data-stu-id="de3a2-108">Example 1:</span></span>
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

## <span data-ttu-id="de3a2-109">參數</span><span class="sxs-lookup"><span data-stu-id="de3a2-109">PARAMETERS</span></span>

### <span data-ttu-id="de3a2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3a2-110">-DefaultProfile</span></span>
<span data-ttu-id="de3a2-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="de3a2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3a2-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="de3a2-112">-Name</span></span>
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

### <span data-ttu-id="de3a2-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="de3a2-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="de3a2-114">-確認</span><span class="sxs-lookup"><span data-stu-id="de3a2-114">-Confirm</span></span>
<span data-ttu-id="de3a2-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="de3a2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3a2-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3a2-116">-WhatIf</span></span>
<span data-ttu-id="de3a2-117">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de3a2-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de3a2-118">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de3a2-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3a2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3a2-119">CommonParameters</span></span>
<span data-ttu-id="de3a2-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de3a2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3a2-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="de3a2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3a2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="de3a2-122">INPUTS</span></span>

### <span data-ttu-id="de3a2-123">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="de3a2-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="de3a2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="de3a2-124">OUTPUTS</span></span>

### <span data-ttu-id="de3a2-125">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="de3a2-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="de3a2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="de3a2-126">NOTES</span></span>

## <span data-ttu-id="de3a2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="de3a2-127">RELATED LINKS</span></span>

[<span data-ttu-id="de3a2-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="de3a2-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="de3a2-129">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="de3a2-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

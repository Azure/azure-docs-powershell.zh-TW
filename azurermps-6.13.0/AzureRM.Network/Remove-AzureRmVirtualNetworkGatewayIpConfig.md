---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 09a3457127646c28c96007532f0e83d1dc1232f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448312"
---
# <span data-ttu-id="b57cc-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b57cc-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="b57cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b57cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b57cc-103">從虛擬網路閘道移除 IP 配置</span><span class="sxs-lookup"><span data-stu-id="b57cc-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b57cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b57cc-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b57cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="b57cc-105">DESCRIPTION</span></span>
<span data-ttu-id="b57cc-106">從虛擬網路閘道移除 IP 配置</span><span class="sxs-lookup"><span data-stu-id="b57cc-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="b57cc-107">示例</span><span class="sxs-lookup"><span data-stu-id="b57cc-107">EXAMPLES</span></span>

### <span data-ttu-id="b57cc-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="b57cc-108">Example 1:</span></span>
```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

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

## <span data-ttu-id="b57cc-109">參數</span><span class="sxs-lookup"><span data-stu-id="b57cc-109">PARAMETERS</span></span>

### <span data-ttu-id="b57cc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57cc-110">-DefaultProfile</span></span>
<span data-ttu-id="b57cc-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b57cc-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57cc-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="b57cc-112">-Name</span></span>
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

### <span data-ttu-id="b57cc-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b57cc-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="b57cc-114">-確認</span><span class="sxs-lookup"><span data-stu-id="b57cc-114">-Confirm</span></span>
<span data-ttu-id="b57cc-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b57cc-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b57cc-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b57cc-116">-WhatIf</span></span>
<span data-ttu-id="b57cc-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b57cc-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b57cc-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b57cc-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b57cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57cc-119">CommonParameters</span></span>
<span data-ttu-id="b57cc-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b57cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57cc-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b57cc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57cc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b57cc-122">INPUTS</span></span>

### <span data-ttu-id="b57cc-123">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b57cc-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="b57cc-124">參數： VirtualNetworkGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="b57cc-124">Parameters: VirtualNetworkGateway (ByValue)</span></span>

## <span data-ttu-id="b57cc-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b57cc-125">OUTPUTS</span></span>

### <span data-ttu-id="b57cc-126">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b57cc-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b57cc-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b57cc-127">NOTES</span></span>

## <span data-ttu-id="b57cc-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b57cc-128">RELATED LINKS</span></span>

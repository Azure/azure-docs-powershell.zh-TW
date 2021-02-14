---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128983"
---
# <span data-ttu-id="b21ba-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b21ba-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="b21ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b21ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b21ba-103">將 IP 配置新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="b21ba-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="b21ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="b21ba-104">SYNTAX</span></span>

### <span data-ttu-id="b21ba-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b21ba-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b21ba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b21ba-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b21ba-107">說明</span><span class="sxs-lookup"><span data-stu-id="b21ba-107">DESCRIPTION</span></span>
<span data-ttu-id="b21ba-108">**AzVirtualNetworkGatewayIpConfig** Cmdlet 會將 IP 配置新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="b21ba-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="b21ba-109">示例</span><span class="sxs-lookup"><span data-stu-id="b21ba-109">EXAMPLES</span></span>

### <span data-ttu-id="b21ba-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b21ba-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="b21ba-111">參數</span><span class="sxs-lookup"><span data-stu-id="b21ba-111">PARAMETERS</span></span>

### <span data-ttu-id="b21ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21ba-112">-DefaultProfile</span></span>
<span data-ttu-id="b21ba-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b21ba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b21ba-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="b21ba-114">-Name</span></span>
<span data-ttu-id="b21ba-115">指定要新增的閘道 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b21ba-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="b21ba-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b21ba-116">-PrivateIpAddress</span></span>
<span data-ttu-id="b21ba-117">指定私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b21ba-117">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ba-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b21ba-118">-PublicIpAddress</span></span>
<span data-ttu-id="b21ba-119">指定公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b21ba-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ba-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b21ba-120">-PublicIpAddressId</span></span>
<span data-ttu-id="b21ba-121">指定公用 IP 位址的 ID。</span><span class="sxs-lookup"><span data-stu-id="b21ba-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ba-122">-子網</span><span class="sxs-lookup"><span data-stu-id="b21ba-122">-Subnet</span></span>
<span data-ttu-id="b21ba-123">指定 **PSSubnet** 物件。</span><span class="sxs-lookup"><span data-stu-id="b21ba-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ba-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b21ba-124">-SubnetId</span></span>
<span data-ttu-id="b21ba-125">指定子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b21ba-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ba-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b21ba-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b21ba-127">指定 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="b21ba-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="b21ba-128">這個 Cmdlet 會修改您指定的 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="b21ba-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="b21ba-129">您可以使用 Get-AzVirtualNetworkGateway Cmdlet 來檢索 **PSVirtualNetworkGateway** 物件。</span><span class="sxs-lookup"><span data-stu-id="b21ba-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="b21ba-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b21ba-130">-Confirm</span></span>
<span data-ttu-id="b21ba-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b21ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b21ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21ba-132">-WhatIf</span></span>
<span data-ttu-id="b21ba-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b21ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b21ba-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b21ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b21ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21ba-135">CommonParameters</span></span>
<span data-ttu-id="b21ba-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b21ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21ba-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b21ba-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21ba-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b21ba-138">INPUTS</span></span>

### <span data-ttu-id="b21ba-139">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b21ba-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b21ba-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b21ba-140">OUTPUTS</span></span>

### <span data-ttu-id="b21ba-141">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b21ba-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b21ba-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b21ba-142">NOTES</span></span>

## <span data-ttu-id="b21ba-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b21ba-143">RELATED LINKS</span></span>

[<span data-ttu-id="b21ba-144">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b21ba-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b21ba-145">新-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b21ba-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="b21ba-146">移除-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b21ba-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)

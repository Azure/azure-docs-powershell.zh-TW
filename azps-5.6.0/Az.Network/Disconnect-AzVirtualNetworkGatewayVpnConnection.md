---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: 1cbbfcbc87ed1d9be869066f8ec6dd288ba3d4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915381"
---
# <span data-ttu-id="2102d-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2102d-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="2102d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2102d-102">SYNOPSIS</span></span> 
<span data-ttu-id="2102d-103">中斷與給定虛擬網路閘道的已連接 vpn 用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="2102d-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="2102d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2102d-104">SYNTAX</span></span>
### <span data-ttu-id="2102d-105">By VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="2102d-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="2102d-106">By VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2102d-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="2102d-107">By VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2102d-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="2102d-108">描述</span><span class="sxs-lookup"><span data-stu-id="2102d-108">DESCRIPTION</span></span>
<span data-ttu-id="2102d-109">**Disconnect-AzVirtualNetworkGateway VpnConnection** Cmdlet 可讓您中斷已連接的 vpn 用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="2102d-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="2102d-110">例子</span><span class="sxs-lookup"><span data-stu-id="2102d-110">EXAMPLES</span></span>

### <span data-ttu-id="2102d-111">例子</span><span class="sxs-lookup"><span data-stu-id="2102d-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="2102d-112">參數</span><span class="sxs-lookup"><span data-stu-id="2102d-112">PARAMETERS</span></span>

### <span data-ttu-id="2102d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2102d-113">-ResourceGroupName</span></span>
<span data-ttu-id="2102d-114">虛擬網路閘道資源組名</span><span class="sxs-lookup"><span data-stu-id="2102d-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2102d-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2102d-115">-ResourceName</span></span>
<span data-ttu-id="2102d-116">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="2102d-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2102d-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2102d-117">-ResourceId</span></span>
<span data-ttu-id="2102d-118">虛擬網路閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2102d-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2102d-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="2102d-119">-VpnConnectionId</span></span>
<span data-ttu-id="2102d-120">Vpn 連接識別碼</span><span class="sxs-lookup"><span data-stu-id="2102d-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2102d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2102d-121">-InputObject</span></span>
<span data-ttu-id="2102d-122">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="2102d-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2102d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2102d-123">-AsJob</span></span>
<span data-ttu-id="2102d-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2102d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2102d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2102d-125">CommonParameters</span></span>
<span data-ttu-id="2102d-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2102d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2102d-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2102d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2102d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2102d-128">INPUTS</span></span>

### <span data-ttu-id="2102d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2102d-129">System.String</span></span>

## <span data-ttu-id="2102d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2102d-130">OUTPUTS</span></span>

### <span data-ttu-id="2102d-131">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2102d-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2102d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2102d-132">NOTES</span></span>

## <span data-ttu-id="2102d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2102d-133">RELATED LINKS</span></span>

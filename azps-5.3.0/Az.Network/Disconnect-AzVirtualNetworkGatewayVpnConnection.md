---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288768"
---
# <span data-ttu-id="b5027-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b5027-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="b5027-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5027-102">SYNOPSIS</span></span> 
<span data-ttu-id="b5027-103">在已連接的 vpn 用戶端連線中，斷開與指定的虛擬閘道的連接。</span><span class="sxs-lookup"><span data-stu-id="b5027-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="b5027-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5027-104">SYNTAX</span></span>
### <span data-ttu-id="b5027-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="b5027-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="b5027-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b5027-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="b5027-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b5027-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="b5027-108">說明</span><span class="sxs-lookup"><span data-stu-id="b5027-108">DESCRIPTION</span></span>
<span data-ttu-id="b5027-109">**AzVirtualNetworkGatewayVpnConnection** Cmdlet 可讓您中斷已連接之 vpn 用戶端連線的連接。</span><span class="sxs-lookup"><span data-stu-id="b5027-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="b5027-110">示例</span><span class="sxs-lookup"><span data-stu-id="b5027-110">EXAMPLES</span></span>

### <span data-ttu-id="b5027-111">範例</span><span class="sxs-lookup"><span data-stu-id="b5027-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="b5027-112">參數</span><span class="sxs-lookup"><span data-stu-id="b5027-112">PARAMETERS</span></span>

### <span data-ttu-id="b5027-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5027-113">-ResourceGroupName</span></span>
<span data-ttu-id="b5027-114">虛擬網路閘道資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b5027-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="b5027-115">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="b5027-115">-ResourceName</span></span>
<span data-ttu-id="b5027-116">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="b5027-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="b5027-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5027-117">-ResourceId</span></span>
<span data-ttu-id="b5027-118">虛擬網路閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b5027-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="b5027-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="b5027-119">-VpnConnectionId</span></span>
<span data-ttu-id="b5027-120">Vpn 連線識別碼</span><span class="sxs-lookup"><span data-stu-id="b5027-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="b5027-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5027-121">-InputObject</span></span>
<span data-ttu-id="b5027-122">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="b5027-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="b5027-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5027-123">-AsJob</span></span>
<span data-ttu-id="b5027-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5027-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5027-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5027-125">CommonParameters</span></span>
<span data-ttu-id="b5027-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5027-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5027-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b5027-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5027-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b5027-128">INPUTS</span></span>

### <span data-ttu-id="b5027-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b5027-129">System.String</span></span>

## <span data-ttu-id="b5027-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b5027-130">OUTPUTS</span></span>

### <span data-ttu-id="b5027-131">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b5027-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b5027-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b5027-132">NOTES</span></span>

## <span data-ttu-id="b5027-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5027-133">RELATED LINKS</span></span>

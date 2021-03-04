---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: 511ff37071767c9e28164fcf93e985eb773297f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908102"
---
# <span data-ttu-id="120bd-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="120bd-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="120bd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="120bd-102">SYNOPSIS</span></span>
<span data-ttu-id="120bd-103">在兩個虛擬網路之間建立對等。</span><span class="sxs-lookup"><span data-stu-id="120bd-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="120bd-104">語法</span><span class="sxs-lookup"><span data-stu-id="120bd-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="120bd-105">描述</span><span class="sxs-lookup"><span data-stu-id="120bd-105">DESCRIPTION</span></span>
<span data-ttu-id="120bd-106">**Add-AzVirtualNetworkPeering** Cmdlet 會建立兩個虛擬網路之間的對等。</span><span class="sxs-lookup"><span data-stu-id="120bd-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="120bd-107">例子</span><span class="sxs-lookup"><span data-stu-id="120bd-107">EXAMPLES</span></span>

### <span data-ttu-id="120bd-108">範例 1：在同一區域建立兩個虛擬網路之間的對等</span><span class="sxs-lookup"><span data-stu-id="120bd-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="120bd-109">請注意，對等連結必須從 vnet1 建立到 vnet2，反之亦然，對等才能工作。</span><span class="sxs-lookup"><span data-stu-id="120bd-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="120bd-110">範例 2：在不同區域的兩個虛擬網路之間建立對等</span><span class="sxs-lookup"><span data-stu-id="120bd-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location canadacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="120bd-111">這裡位於美國中西部的 'myVnet1' 與加拿大中央的 'myVnet2' 對等。</span><span class="sxs-lookup"><span data-stu-id="120bd-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="120bd-112">參數</span><span class="sxs-lookup"><span data-stu-id="120bd-112">PARAMETERS</span></span>

### <span data-ttu-id="120bd-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="120bd-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="120bd-114">表示此 Cmdlet 允許遠端虛擬網路中虛擬機器的轉寄流量。</span><span class="sxs-lookup"><span data-stu-id="120bd-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="120bd-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="120bd-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="120bd-116">允許閘道連結用於遠端虛擬網路連結的標號</span><span class="sxs-lookup"><span data-stu-id="120bd-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="120bd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="120bd-117">-AsJob</span></span>
<span data-ttu-id="120bd-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="120bd-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="120bd-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="120bd-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="120bd-120">表示此 Cmdlet 會區塊連結的虛擬網路空間中的虛擬機器，以存取本地虛擬網路空間中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="120bd-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="120bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120bd-121">-DefaultProfile</span></span>
<span data-ttu-id="120bd-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="120bd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="120bd-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="120bd-123">-Name</span></span>
<span data-ttu-id="120bd-124">指定虛擬網路對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="120bd-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="120bd-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="120bd-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="120bd-126">指定遠端虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="120bd-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="120bd-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="120bd-127">-UseRemoteGateways</span></span>
<span data-ttu-id="120bd-128">表示此 Cmdlet 允許此虛擬網路上有遠端閘道。</span><span class="sxs-lookup"><span data-stu-id="120bd-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="120bd-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="120bd-129">-VirtualNetwork</span></span>
<span data-ttu-id="120bd-130">指定父虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="120bd-130">Specifies the parent virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="120bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120bd-131">CommonParameters</span></span>
<span data-ttu-id="120bd-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="120bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120bd-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="120bd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120bd-134">輸入</span><span class="sxs-lookup"><span data-stu-id="120bd-134">INPUTS</span></span>

### <span data-ttu-id="120bd-135">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="120bd-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="120bd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="120bd-136">System.String</span></span>

## <span data-ttu-id="120bd-137">輸出</span><span class="sxs-lookup"><span data-stu-id="120bd-137">OUTPUTS</span></span>

### <span data-ttu-id="120bd-138">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="120bd-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="120bd-139">筆記</span><span class="sxs-lookup"><span data-stu-id="120bd-139">NOTES</span></span>

## <span data-ttu-id="120bd-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="120bd-140">RELATED LINKS</span></span>

[<span data-ttu-id="120bd-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="120bd-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="120bd-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="120bd-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="120bd-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="120bd-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="120bd-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="120bd-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)

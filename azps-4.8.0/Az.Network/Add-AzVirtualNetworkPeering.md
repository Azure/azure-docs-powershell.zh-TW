---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: a63f6c2bc57bfc4d1a82861c6b25bd5c8a6e1383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128989"
---
# <span data-ttu-id="c29ae-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c29ae-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="c29ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c29ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c29ae-103">在兩個虛擬網路之間建立對等。</span><span class="sxs-lookup"><span data-stu-id="c29ae-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="c29ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="c29ae-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c29ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="c29ae-105">DESCRIPTION</span></span>
<span data-ttu-id="c29ae-106">**AzVirtualNetworkPeering** Cmdlet 會在兩個虛擬網路之間建立對等。</span><span class="sxs-lookup"><span data-stu-id="c29ae-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="c29ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="c29ae-107">EXAMPLES</span></span>

### <span data-ttu-id="c29ae-108">範例1：在同一個區域中建立兩個虛擬網路之間的對等專案</span><span class="sxs-lookup"><span data-stu-id="c29ae-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="c29ae-109">請注意，必須從 vnet1 到 vnet2 （反之亦然）建立對等連結，然後再按順序進行對等作業。</span><span class="sxs-lookup"><span data-stu-id="c29ae-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="c29ae-110">範例2：在不同地區的兩個虛擬網路之間建立對等</span><span class="sxs-lookup"><span data-stu-id="c29ae-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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

<span data-ttu-id="c29ae-111">這裡的「myVnet1」是位於加拿大中央的 [myVnet2] peered。</span><span class="sxs-lookup"><span data-stu-id="c29ae-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="c29ae-112">參數</span><span class="sxs-lookup"><span data-stu-id="c29ae-112">PARAMETERS</span></span>

### <span data-ttu-id="c29ae-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="c29ae-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="c29ae-114">表示此 Cmdlet 允許來自遠端虛擬網路中的虛擬機器的轉寄流量。</span><span class="sxs-lookup"><span data-stu-id="c29ae-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="c29ae-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="c29ae-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="c29ae-116">允許 gatewayLinks 在遠端虛擬網路的連結中用於此虛擬網路的標誌</span><span class="sxs-lookup"><span data-stu-id="c29ae-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="c29ae-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c29ae-117">-AsJob</span></span>
<span data-ttu-id="c29ae-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c29ae-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c29ae-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c29ae-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="c29ae-120">表示此 Cmdlet 會封鎖鏈接虛擬網路空間中的虛擬機器，以存取本機虛擬網路空間中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c29ae-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="c29ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c29ae-121">-DefaultProfile</span></span>
<span data-ttu-id="c29ae-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c29ae-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c29ae-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c29ae-123">-Name</span></span>
<span data-ttu-id="c29ae-124">指定虛擬網路對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="c29ae-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="c29ae-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c29ae-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="c29ae-126">指定遠端虛擬網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="c29ae-126">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="c29ae-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="c29ae-127">-UseRemoteGateways</span></span>
<span data-ttu-id="c29ae-128">表示此 Cmdlet 允許此虛擬網路上的遠端閘道。</span><span class="sxs-lookup"><span data-stu-id="c29ae-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="c29ae-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c29ae-129">-VirtualNetwork</span></span>
<span data-ttu-id="c29ae-130">指定父虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c29ae-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="c29ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c29ae-131">CommonParameters</span></span>
<span data-ttu-id="c29ae-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c29ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c29ae-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c29ae-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c29ae-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c29ae-134">INPUTS</span></span>

### <span data-ttu-id="c29ae-135">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c29ae-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="c29ae-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c29ae-136">System.String</span></span>

## <span data-ttu-id="c29ae-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c29ae-137">OUTPUTS</span></span>

### <span data-ttu-id="c29ae-138">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c29ae-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="c29ae-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c29ae-139">NOTES</span></span>

## <span data-ttu-id="c29ae-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c29ae-140">RELATED LINKS</span></span>

[<span data-ttu-id="c29ae-141">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c29ae-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="c29ae-142">AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c29ae-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="c29ae-143">移除-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c29ae-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="c29ae-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c29ae-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)

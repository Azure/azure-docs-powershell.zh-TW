---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 7a26e563c8416f31178855acb2d97f318001f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453399"
---
# <span data-ttu-id="fdf04-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fdf04-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="fdf04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdf04-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf04-103">在兩個虛擬網路之間建立對等。</span><span class="sxs-lookup"><span data-stu-id="fdf04-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf04-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdf04-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf04-105">說明</span><span class="sxs-lookup"><span data-stu-id="fdf04-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf04-106">**AzureRmVirtualNetworkPeering** Cmdlet 會在兩個虛擬網路之間建立對等。</span><span class="sxs-lookup"><span data-stu-id="fdf04-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="fdf04-107">示例</span><span class="sxs-lookup"><span data-stu-id="fdf04-107">EXAMPLES</span></span>

### <span data-ttu-id="fdf04-108">範例1：在同一個區域中建立兩個虛擬網路之間的對等專案</span><span class="sxs-lookup"><span data-stu-id="fdf04-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="fdf04-109">請注意，必須從 vnet1 到 vnet2 （反之亦然）建立對等連結，然後再按順序進行對等作業。</span><span class="sxs-lookup"><span data-stu-id="fdf04-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="fdf04-110">範例2：在不同地區的兩個虛擬網路之間建立對等</span><span class="sxs-lookup"><span data-stu-id="fdf04-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="fdf04-111">這裡的「myVnet1」是位於加拿大中央的 [myVnet2] peered。</span><span class="sxs-lookup"><span data-stu-id="fdf04-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="fdf04-112">參數</span><span class="sxs-lookup"><span data-stu-id="fdf04-112">PARAMETERS</span></span>

### <span data-ttu-id="fdf04-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="fdf04-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="fdf04-114">表示此 Cmdlet 允許來自遠端虛擬網路中的虛擬機器的轉寄流量。</span><span class="sxs-lookup"><span data-stu-id="fdf04-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="fdf04-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="fdf04-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="fdf04-116">允許 gatewayLinks 在遠端虛擬網路的連結中用於此虛擬網路的標誌</span><span class="sxs-lookup"><span data-stu-id="fdf04-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf04-117">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="fdf04-117">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="fdf04-118">表示此 Cmdlet 會封鎖鏈接虛擬網路空間中的虛擬機器，以存取本機虛擬網路空間中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fdf04-118">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="fdf04-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fdf04-119">-Name</span></span>
<span data-ttu-id="fdf04-120">指定虛擬網路對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdf04-120">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="fdf04-121">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fdf04-121">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="fdf04-122">指定遠端虛擬網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="fdf04-122">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="fdf04-123">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="fdf04-123">-UseRemoteGateways</span></span>
<span data-ttu-id="fdf04-124">表示此 Cmdlet 允許此虛擬網路上的遠端閘道。</span><span class="sxs-lookup"><span data-stu-id="fdf04-124">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="fdf04-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fdf04-125">-VirtualNetwork</span></span>
<span data-ttu-id="fdf04-126">指定父虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="fdf04-126">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="fdf04-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf04-127">-DefaultProfile</span></span>
<span data-ttu-id="fdf04-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fdf04-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdf04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf04-129">CommonParameters</span></span>
<span data-ttu-id="fdf04-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdf04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf04-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fdf04-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf04-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fdf04-132">INPUTS</span></span>

### <span data-ttu-id="fdf04-133">字串</span><span class="sxs-lookup"><span data-stu-id="fdf04-133">String</span></span>
<span data-ttu-id="fdf04-134">"RemoteVirtualNetworkId" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="fdf04-134">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="fdf04-135">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fdf04-135">PSVirtualNetwork</span></span>
<span data-ttu-id="fdf04-136">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="fdf04-136">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="fdf04-137">輸出</span><span class="sxs-lookup"><span data-stu-id="fdf04-137">OUTPUTS</span></span>

### <span data-ttu-id="fdf04-138">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fdf04-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="fdf04-139">筆記</span><span class="sxs-lookup"><span data-stu-id="fdf04-139">NOTES</span></span>

## <span data-ttu-id="fdf04-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdf04-140">RELATED LINKS</span></span>

[<span data-ttu-id="fdf04-141">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fdf04-141">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fdf04-142">AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fdf04-142">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="fdf04-143">移除-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fdf04-143">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="fdf04-144">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fdf04-144">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)



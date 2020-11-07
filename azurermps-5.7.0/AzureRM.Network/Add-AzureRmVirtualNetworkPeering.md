---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 1a27b43a7767fab6fee7cc89098ef045dde8529c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623706"
---
# <span data-ttu-id="5b1f7-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5b1f7-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="5b1f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1f7-103">在兩個虛擬網路之間建立對等。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b1f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b1f7-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b1f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b1f7-105">DESCRIPTION</span></span>
<span data-ttu-id="5b1f7-106">**AzureRmVirtualNetworkPeering** Cmdlet 會在兩個虛擬網路之間建立對等。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="5b1f7-107">示例</span><span class="sxs-lookup"><span data-stu-id="5b1f7-107">EXAMPLES</span></span>

### <span data-ttu-id="5b1f7-108">範例1：在同一個區域中建立兩個虛擬網路之間的對等專案</span><span class="sxs-lookup"><span data-stu-id="5b1f7-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="5b1f7-109">請注意，必須從 vnet1 到 vnet2 （反之亦然）建立對等連結，然後再按順序進行對等作業。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="5b1f7-110">範例2：在不同地區的兩個虛擬網路之間建立對等</span><span class="sxs-lookup"><span data-stu-id="5b1f7-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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

<span data-ttu-id="5b1f7-111">這裡的「myVnet1」是位於加拿大中央的 [myVnet2] peered。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="5b1f7-112">參數</span><span class="sxs-lookup"><span data-stu-id="5b1f7-112">PARAMETERS</span></span>

### <span data-ttu-id="5b1f7-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="5b1f7-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="5b1f7-114">表示此 Cmdlet 允許來自遠端虛擬網路中的虛擬機器的轉寄流量。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="5b1f7-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="5b1f7-116">允許 gatewayLinks 在遠端虛擬網路的連結中用於此虛擬網路的標誌</span><span class="sxs-lookup"><span data-stu-id="5b1f7-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b1f7-117">-AsJob</span></span>
<span data-ttu-id="5b1f7-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b1f7-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5b1f7-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="5b1f7-120">表示此 Cmdlet 會封鎖鏈接虛擬網路空間中的虛擬機器，以存取本機虛擬網路空間中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1f7-121">-DefaultProfile</span></span>
<span data-ttu-id="5b1f7-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b1f7-123">-Name</span></span>
<span data-ttu-id="5b1f7-124">指定虛擬網路對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5b1f7-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="5b1f7-126">指定遠端虛擬網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="5b1f7-127">-UseRemoteGateways</span></span>
<span data-ttu-id="5b1f7-128">表示此 Cmdlet 允許此虛擬網路上的遠端閘道。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b1f7-129">-VirtualNetwork</span></span>
<span data-ttu-id="5b1f7-130">指定父虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-130">Specifies the parent virtual network.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1f7-131">CommonParameters</span></span>
<span data-ttu-id="5b1f7-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1f7-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b1f7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1f7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5b1f7-134">INPUTS</span></span>

### <span data-ttu-id="5b1f7-135">字串</span><span class="sxs-lookup"><span data-stu-id="5b1f7-135">String</span></span>
<span data-ttu-id="5b1f7-136">"RemoteVirtualNetworkId" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="5b1f7-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="5b1f7-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b1f7-137">PSVirtualNetwork</span></span>
<span data-ttu-id="5b1f7-138">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5b1f7-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="5b1f7-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5b1f7-139">OUTPUTS</span></span>

### <span data-ttu-id="5b1f7-140">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5b1f7-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="5b1f7-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5b1f7-141">NOTES</span></span>

## <span data-ttu-id="5b1f7-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b1f7-142">RELATED LINKS</span></span>

[<span data-ttu-id="5b1f7-143">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b1f7-143">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="5b1f7-144">AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5b1f7-144">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="5b1f7-145">移除-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5b1f7-145">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="5b1f7-146">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5b1f7-146">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446712"
---
# <span data-ttu-id="7b458-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7b458-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="7b458-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b458-102">SYNOPSIS</span></span>
<span data-ttu-id="7b458-103">配置虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="7b458-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b458-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b458-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b458-105">說明</span><span class="sxs-lookup"><span data-stu-id="7b458-105">DESCRIPTION</span></span>
<span data-ttu-id="7b458-106">AzureRmVirtualNetworkPeering Cmdlet 會 **設定** 虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="7b458-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="7b458-107">示例</span><span class="sxs-lookup"><span data-stu-id="7b458-107">EXAMPLES</span></span>

### <span data-ttu-id="7b458-108">範例1：變更虛擬網路對等的轉寄流量設定</span><span class="sxs-lookup"><span data-stu-id="7b458-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="7b458-109">範例2：變更虛擬網路對等的虛擬網路存取權</span><span class="sxs-lookup"><span data-stu-id="7b458-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="7b458-110">範例3：變更虛擬網路對等的閘道中轉屬性設定</span><span class="sxs-lookup"><span data-stu-id="7b458-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="7b458-111">範例4：在虛擬網路對等中使用遠端閘道</span><span class="sxs-lookup"><span data-stu-id="7b458-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="7b458-112">透過將此屬性變更為 $True，就可以使用對等的 VNet 閘道。</span><span class="sxs-lookup"><span data-stu-id="7b458-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="7b458-113">不過，對等 VNet 必須已設定閘道，且 **AllowGatewayTransit** 必須具有 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="7b458-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="7b458-114">如果已設定閘道，則無法使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="7b458-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="7b458-115">參數</span><span class="sxs-lookup"><span data-stu-id="7b458-115">PARAMETERS</span></span>

### <span data-ttu-id="7b458-116">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7b458-116">-VirtualNetworkPeering</span></span>
<span data-ttu-id="7b458-117">指定虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="7b458-117">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b458-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b458-118">-DefaultProfile</span></span>
<span data-ttu-id="7b458-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b458-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b458-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b458-120">CommonParameters</span></span>
<span data-ttu-id="7b458-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b458-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b458-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7b458-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b458-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7b458-123">INPUTS</span></span>

### <span data-ttu-id="7b458-124">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7b458-124">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="7b458-125">形參 "VirtualNetworkPeering" 接受管線中 "PSVirtualNetworkPeering" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7b458-125">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="7b458-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7b458-126">OUTPUTS</span></span>

### <span data-ttu-id="7b458-127">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7b458-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="7b458-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7b458-128">NOTES</span></span>

## <span data-ttu-id="7b458-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b458-129">RELATED LINKS</span></span>

[<span data-ttu-id="7b458-130">附加 AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7b458-130">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="7b458-131">AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7b458-131">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="7b458-132">移除-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7b458-132">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)



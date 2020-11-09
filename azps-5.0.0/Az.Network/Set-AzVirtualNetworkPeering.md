---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 421358a9241fe41549898547c62404f6ba1162e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285854"
---
# <span data-ttu-id="0906c-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0906c-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="0906c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0906c-102">SYNOPSIS</span></span>
<span data-ttu-id="0906c-103">配置虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="0906c-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="0906c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0906c-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0906c-105">說明</span><span class="sxs-lookup"><span data-stu-id="0906c-105">DESCRIPTION</span></span>
<span data-ttu-id="0906c-106">AzVirtualNetworkPeering Cmdlet 會 **設定** 虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="0906c-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="0906c-107">示例</span><span class="sxs-lookup"><span data-stu-id="0906c-107">EXAMPLES</span></span>

### <span data-ttu-id="0906c-108">範例1：變更虛擬網路對等的轉寄流量設定</span><span class="sxs-lookup"><span data-stu-id="0906c-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="0906c-109">範例2：變更虛擬網路對等的虛擬網路存取權</span><span class="sxs-lookup"><span data-stu-id="0906c-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="0906c-110">範例3：變更虛擬網路對等的閘道中轉屬性設定</span><span class="sxs-lookup"><span data-stu-id="0906c-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="0906c-111">範例4：在虛擬網路對等中使用遠端閘道</span><span class="sxs-lookup"><span data-stu-id="0906c-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="0906c-112">透過將此屬性變更為 $True，就可以使用對等的 VNet 閘道。</span><span class="sxs-lookup"><span data-stu-id="0906c-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="0906c-113">不過，對等 VNet 必須已設定閘道，且 **AllowGatewayTransit** 必須具有 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="0906c-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="0906c-114">如果已設定閘道，則無法使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="0906c-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="0906c-115">參數</span><span class="sxs-lookup"><span data-stu-id="0906c-115">PARAMETERS</span></span>

### <span data-ttu-id="0906c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0906c-116">-AsJob</span></span>
<span data-ttu-id="0906c-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0906c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0906c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0906c-118">-DefaultProfile</span></span>
<span data-ttu-id="0906c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0906c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0906c-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0906c-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="0906c-121">指定虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="0906c-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="0906c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0906c-122">CommonParameters</span></span>
<span data-ttu-id="0906c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0906c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0906c-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0906c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0906c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0906c-125">INPUTS</span></span>

### <span data-ttu-id="0906c-126">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0906c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="0906c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0906c-127">OUTPUTS</span></span>

### <span data-ttu-id="0906c-128">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0906c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="0906c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0906c-129">NOTES</span></span>

## <span data-ttu-id="0906c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0906c-130">RELATED LINKS</span></span>

[<span data-ttu-id="0906c-131">附加 AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0906c-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0906c-132">AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0906c-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0906c-133">移除-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0906c-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

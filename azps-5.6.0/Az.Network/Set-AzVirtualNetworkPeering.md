---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 1f24dd8cff058b49c9661da1d2f5f2ae927e1a0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901930"
---
# <span data-ttu-id="2bc31-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2bc31-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="2bc31-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2bc31-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc31-103">設定虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="2bc31-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="2bc31-104">語法</span><span class="sxs-lookup"><span data-stu-id="2bc31-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc31-105">描述</span><span class="sxs-lookup"><span data-stu-id="2bc31-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc31-106">**Set-AzVirtualNetworkPeering** Cmdlet 會設定虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="2bc31-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="2bc31-107">例子</span><span class="sxs-lookup"><span data-stu-id="2bc31-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc31-108">範例 1：變更虛擬網路對等的轉轉流量組</span><span class="sxs-lookup"><span data-stu-id="2bc31-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="2bc31-109">範例 2：變更虛擬網路對等的虛擬機器存取權</span><span class="sxs-lookup"><span data-stu-id="2bc31-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="2bc31-110">範例 3：變更虛擬網路對等的閘道傳輸屬性組</span><span class="sxs-lookup"><span data-stu-id="2bc31-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="2bc31-111">範例 4：在虛擬網路對等使用遠端閘道</span><span class="sxs-lookup"><span data-stu-id="2bc31-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="2bc31-112">將此屬性變更為$True，就可以使用對等的 VNet 閘道。</span><span class="sxs-lookup"><span data-stu-id="2bc31-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="2bc31-113">不過，對等 VNet 必須擁有一個閘道， **而 AllowGatewayTransit** 必須有 $True。</span><span class="sxs-lookup"><span data-stu-id="2bc31-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="2bc31-114">如果已經設有閘道，就無法使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="2bc31-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="2bc31-115">參數</span><span class="sxs-lookup"><span data-stu-id="2bc31-115">PARAMETERS</span></span>

### <span data-ttu-id="2bc31-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bc31-116">-AsJob</span></span>
<span data-ttu-id="2bc31-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2bc31-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bc31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc31-118">-DefaultProfile</span></span>
<span data-ttu-id="2bc31-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bc31-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc31-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2bc31-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="2bc31-121">指定虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="2bc31-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="2bc31-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc31-122">CommonParameters</span></span>
<span data-ttu-id="2bc31-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2bc31-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc31-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2bc31-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc31-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2bc31-125">INPUTS</span></span>

### <span data-ttu-id="2bc31-126">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2bc31-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="2bc31-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2bc31-127">OUTPUTS</span></span>

### <span data-ttu-id="2bc31-128">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2bc31-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="2bc31-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2bc31-129">NOTES</span></span>

## <span data-ttu-id="2bc31-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bc31-130">RELATED LINKS</span></span>

[<span data-ttu-id="2bc31-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2bc31-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="2bc31-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2bc31-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="2bc31-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2bc31-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

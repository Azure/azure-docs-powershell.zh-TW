---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 40f84388caed0d332c36ee398e842ae00f2f353f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800346"
---
# <span data-ttu-id="903e6-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="903e6-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="903e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="903e6-102">SYNOPSIS</span></span>
<span data-ttu-id="903e6-103">設定虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="903e6-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="903e6-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="903e6-105">說明</span><span class="sxs-lookup"><span data-stu-id="903e6-105">DESCRIPTION</span></span>
<span data-ttu-id="903e6-106">**AzureRmVirtualNetwork** Cmdlet 設定 Azure 虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="903e6-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="903e6-107">示例</span><span class="sxs-lookup"><span data-stu-id="903e6-107">EXAMPLES</span></span>

### <span data-ttu-id="903e6-108">1：建立虛擬網路並移除其中一個子網</span><span class="sxs-lookup"><span data-stu-id="903e6-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="903e6-109">這個範例會建立具有兩個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="903e6-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="903e6-110">接著，它會從虛擬網路的記憶體內部表示形式移除一個子網。</span><span class="sxs-lookup"><span data-stu-id="903e6-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="903e6-111">然後使用 Set-AzureRmVirtualNetwork Cmdlet，在服務端寫入修改過的虛擬網路狀態。</span><span class="sxs-lookup"><span data-stu-id="903e6-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="903e6-112">參數</span><span class="sxs-lookup"><span data-stu-id="903e6-112">PARAMETERS</span></span>

### <span data-ttu-id="903e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="903e6-113">-AsJob</span></span>
<span data-ttu-id="903e6-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="903e6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="903e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903e6-115">-DefaultProfile</span></span>
<span data-ttu-id="903e6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="903e6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="903e6-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="903e6-117">-VirtualNetwork</span></span>
<span data-ttu-id="903e6-118">指定代表目標狀態的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="903e6-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="903e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903e6-119">CommonParameters</span></span>
<span data-ttu-id="903e6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="903e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903e6-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="903e6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903e6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="903e6-122">INPUTS</span></span>

### <span data-ttu-id="903e6-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="903e6-123">PSVirtualNetwork</span></span>
<span data-ttu-id="903e6-124">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="903e6-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="903e6-125">輸出</span><span class="sxs-lookup"><span data-stu-id="903e6-125">OUTPUTS</span></span>

### <span data-ttu-id="903e6-126">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="903e6-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="903e6-127">筆記</span><span class="sxs-lookup"><span data-stu-id="903e6-127">NOTES</span></span>

## <span data-ttu-id="903e6-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="903e6-128">RELATED LINKS</span></span>

[<span data-ttu-id="903e6-129">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="903e6-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="903e6-130">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="903e6-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="903e6-131">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="903e6-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="903e6-132">移除-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="903e6-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


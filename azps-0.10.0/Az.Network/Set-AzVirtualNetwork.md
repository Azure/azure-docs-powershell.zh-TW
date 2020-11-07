---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795385"
---
# <span data-ttu-id="b06ae-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b06ae-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="b06ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b06ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b06ae-103">設定虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="b06ae-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="b06ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="b06ae-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b06ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="b06ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b06ae-106">**AzVirtualNetwork** Cmdlet 設定 Azure 虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="b06ae-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="b06ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="b06ae-107">EXAMPLES</span></span>

### <span data-ttu-id="b06ae-108">1：建立虛擬網路並移除其中一個子網</span><span class="sxs-lookup"><span data-stu-id="b06ae-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="b06ae-109">這個範例會建立具有兩個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b06ae-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="b06ae-110">接著，它會從虛擬網路的記憶體內部表示形式移除一個子網。</span><span class="sxs-lookup"><span data-stu-id="b06ae-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="b06ae-111">然後使用 Set-AzVirtualNetwork Cmdlet，在服務端寫入修改過的虛擬網路狀態。</span><span class="sxs-lookup"><span data-stu-id="b06ae-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="b06ae-112">參數</span><span class="sxs-lookup"><span data-stu-id="b06ae-112">PARAMETERS</span></span>

### <span data-ttu-id="b06ae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b06ae-113">-AsJob</span></span>
<span data-ttu-id="b06ae-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b06ae-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b06ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06ae-115">-DefaultProfile</span></span>
<span data-ttu-id="b06ae-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b06ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b06ae-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b06ae-117">-VirtualNetwork</span></span>
<span data-ttu-id="b06ae-118">指定代表目標狀態的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="b06ae-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="b06ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06ae-119">CommonParameters</span></span>
<span data-ttu-id="b06ae-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b06ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06ae-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b06ae-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06ae-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b06ae-122">INPUTS</span></span>

### <span data-ttu-id="b06ae-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b06ae-123">PSVirtualNetwork</span></span>
<span data-ttu-id="b06ae-124">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b06ae-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="b06ae-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b06ae-125">OUTPUTS</span></span>

### <span data-ttu-id="b06ae-126">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b06ae-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b06ae-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b06ae-127">NOTES</span></span>

## <span data-ttu-id="b06ae-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b06ae-128">RELATED LINKS</span></span>

[<span data-ttu-id="b06ae-129">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b06ae-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b06ae-130">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b06ae-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b06ae-131">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b06ae-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="b06ae-132">移除-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b06ae-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799110"
---
# <span data-ttu-id="df09e-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df09e-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="df09e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df09e-102">SYNOPSIS</span></span>
<span data-ttu-id="df09e-103">更新虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="df09e-103">Updates a virtual network.</span></span>

## <span data-ttu-id="df09e-104">句法</span><span class="sxs-lookup"><span data-stu-id="df09e-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df09e-105">說明</span><span class="sxs-lookup"><span data-stu-id="df09e-105">DESCRIPTION</span></span>
<span data-ttu-id="df09e-106">**AzVirtualNetwork** Cmdlet 會更新虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="df09e-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="df09e-107">示例</span><span class="sxs-lookup"><span data-stu-id="df09e-107">EXAMPLES</span></span>

### <span data-ttu-id="df09e-108">1：建立虛擬網路並移除其中一個子網</span><span class="sxs-lookup"><span data-stu-id="df09e-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="df09e-109">這個範例會建立名為 TestResourceGroup 的虛擬網路，其中包含兩個子網： frontendSubnet 和 backendSubnet。</span><span class="sxs-lookup"><span data-stu-id="df09e-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="df09e-110">然後它會將 backendSubnet 子網從虛擬網路的記憶體內部表示形式中移除。</span><span class="sxs-lookup"><span data-stu-id="df09e-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="df09e-111">然後使用 Set-AzVirtualNetwork Cmdlet，在服務端寫入修改過的虛擬網路狀態。</span><span class="sxs-lookup"><span data-stu-id="df09e-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="df09e-112">執行 Set-AzVirtualNetwork Cmdlet 時，會移除 backendSubnet。</span><span class="sxs-lookup"><span data-stu-id="df09e-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="df09e-113">參數</span><span class="sxs-lookup"><span data-stu-id="df09e-113">PARAMETERS</span></span>

### <span data-ttu-id="df09e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df09e-114">-AsJob</span></span>
<span data-ttu-id="df09e-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="df09e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df09e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df09e-116">-DefaultProfile</span></span>
<span data-ttu-id="df09e-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df09e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df09e-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df09e-118">-VirtualNetwork</span></span>
<span data-ttu-id="df09e-119">指定代表虛擬網路應設定之狀態的虛擬網路物件。</span><span class="sxs-lookup"><span data-stu-id="df09e-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="df09e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df09e-120">CommonParameters</span></span>
<span data-ttu-id="df09e-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df09e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df09e-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df09e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df09e-123">輸入</span><span class="sxs-lookup"><span data-stu-id="df09e-123">INPUTS</span></span>

### <span data-ttu-id="df09e-124">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="df09e-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="df09e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="df09e-125">OUTPUTS</span></span>

### <span data-ttu-id="df09e-126">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="df09e-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="df09e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="df09e-127">NOTES</span></span>

## <span data-ttu-id="df09e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="df09e-128">RELATED LINKS</span></span>

[<span data-ttu-id="df09e-129">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df09e-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="df09e-130">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df09e-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="df09e-131">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df09e-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="df09e-132">移除-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df09e-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)



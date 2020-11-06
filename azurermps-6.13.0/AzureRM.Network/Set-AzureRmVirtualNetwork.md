---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448295"
---
# <span data-ttu-id="a1232-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1232-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="a1232-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1232-102">SYNOPSIS</span></span>
<span data-ttu-id="a1232-103">設定虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a1232-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1232-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1232-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1232-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1232-105">DESCRIPTION</span></span>
<span data-ttu-id="a1232-106">**AzureRmVirtualNetwork** Cmdlet 設定 Azure 虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a1232-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="a1232-107">示例</span><span class="sxs-lookup"><span data-stu-id="a1232-107">EXAMPLES</span></span>

### <span data-ttu-id="a1232-108">1：建立虛擬網路並移除其中一個子網</span><span class="sxs-lookup"><span data-stu-id="a1232-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="a1232-109">這個範例會建立名為 TestResourceGroup 的虛擬網路，其中包含兩個子網： frontendSubnet 和 backendSubnet。</span><span class="sxs-lookup"><span data-stu-id="a1232-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="a1232-110">然後它會將 backendSubnet 子網從虛擬網路的記憶體內部表示形式中移除。</span><span class="sxs-lookup"><span data-stu-id="a1232-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a1232-111">然後使用 Set-AzureRmVirtualNetwork Cmdlet，在服務端寫入修改過的虛擬網路狀態。</span><span class="sxs-lookup"><span data-stu-id="a1232-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="a1232-112">執行 Set-AzureRmVirtualNetwork Cmdlet 時，會移除 backendSubnet。</span><span class="sxs-lookup"><span data-stu-id="a1232-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="a1232-113">參數</span><span class="sxs-lookup"><span data-stu-id="a1232-113">PARAMETERS</span></span>

### <span data-ttu-id="a1232-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1232-114">-AsJob</span></span>
<span data-ttu-id="a1232-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a1232-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1232-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1232-116">-DefaultProfile</span></span>
<span data-ttu-id="a1232-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1232-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1232-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1232-118">-VirtualNetwork</span></span>
<span data-ttu-id="a1232-119">指定代表目標狀態的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="a1232-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="a1232-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1232-120">CommonParameters</span></span>
<span data-ttu-id="a1232-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1232-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1232-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1232-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1232-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a1232-123">INPUTS</span></span>

### <span data-ttu-id="a1232-124">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1232-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="a1232-125">參數： VirtualNetwork (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a1232-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="a1232-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a1232-126">OUTPUTS</span></span>

### <span data-ttu-id="a1232-127">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1232-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a1232-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a1232-128">NOTES</span></span>

## <span data-ttu-id="a1232-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1232-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1232-130">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1232-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="a1232-131">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1232-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="a1232-132">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1232-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="a1232-133">移除-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1232-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


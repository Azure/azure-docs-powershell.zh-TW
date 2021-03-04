---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 1c5a5bc119c481c47c865ca72896b832f3a82b2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913814"
---
# <span data-ttu-id="14c80-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14c80-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="14c80-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14c80-102">SYNOPSIS</span></span>
<span data-ttu-id="14c80-103">更新虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="14c80-103">Updates a virtual network.</span></span>

## <span data-ttu-id="14c80-104">語法</span><span class="sxs-lookup"><span data-stu-id="14c80-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14c80-105">描述</span><span class="sxs-lookup"><span data-stu-id="14c80-105">DESCRIPTION</span></span>
<span data-ttu-id="14c80-106">**Set-AzVirtualNetwork** Cmdlet 會更新虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="14c80-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="14c80-107">例子</span><span class="sxs-lookup"><span data-stu-id="14c80-107">EXAMPLES</span></span>

### <span data-ttu-id="14c80-108">1：建立虛擬網路並移除其中一個子網</span><span class="sxs-lookup"><span data-stu-id="14c80-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="14c80-109">此範例會建立一個稱為 TestResourceGroup 的虛擬網路，具有兩個子網：frontendSubnet 和後端Subnet。</span><span class="sxs-lookup"><span data-stu-id="14c80-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="14c80-110">接著，它會從虛擬網路的記憶體中標記法移除後端Subnet 子網。</span><span class="sxs-lookup"><span data-stu-id="14c80-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="14c80-111">然後Set-AzVirtualNetwork Cmdlet 在服務端寫入修改後的虛擬網路狀態。</span><span class="sxs-lookup"><span data-stu-id="14c80-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="14c80-112">執行 Set-AzVirtualNetwork Cmdlet 時，會移除後端Subnet。</span><span class="sxs-lookup"><span data-stu-id="14c80-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="14c80-113">參數</span><span class="sxs-lookup"><span data-stu-id="14c80-113">PARAMETERS</span></span>

### <span data-ttu-id="14c80-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14c80-114">-AsJob</span></span>
<span data-ttu-id="14c80-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="14c80-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14c80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c80-116">-DefaultProfile</span></span>
<span data-ttu-id="14c80-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="14c80-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14c80-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14c80-118">-VirtualNetwork</span></span>
<span data-ttu-id="14c80-119">指定一個虛擬網路物件，代表應設定該虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="14c80-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="14c80-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c80-120">CommonParameters</span></span>
<span data-ttu-id="14c80-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14c80-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c80-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="14c80-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c80-123">輸入</span><span class="sxs-lookup"><span data-stu-id="14c80-123">INPUTS</span></span>

### <span data-ttu-id="14c80-124">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14c80-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="14c80-125">輸出</span><span class="sxs-lookup"><span data-stu-id="14c80-125">OUTPUTS</span></span>

### <span data-ttu-id="14c80-126">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14c80-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="14c80-127">筆記</span><span class="sxs-lookup"><span data-stu-id="14c80-127">NOTES</span></span>

## <span data-ttu-id="14c80-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="14c80-128">RELATED LINKS</span></span>

[<span data-ttu-id="14c80-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14c80-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="14c80-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14c80-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="14c80-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14c80-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="14c80-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14c80-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)



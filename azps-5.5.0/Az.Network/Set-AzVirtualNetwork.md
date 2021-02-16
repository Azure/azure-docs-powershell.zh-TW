---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 023d50aaf32d894722e2167737703d24776a1fd5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135683"
---
# <span data-ttu-id="006df-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="006df-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="006df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="006df-102">SYNOPSIS</span></span>
<span data-ttu-id="006df-103">更新虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="006df-103">Updates a virtual network.</span></span>

## <span data-ttu-id="006df-104">句法</span><span class="sxs-lookup"><span data-stu-id="006df-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="006df-105">說明</span><span class="sxs-lookup"><span data-stu-id="006df-105">DESCRIPTION</span></span>
<span data-ttu-id="006df-106">**AzVirtualNetwork** Cmdlet 會更新虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="006df-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="006df-107">示例</span><span class="sxs-lookup"><span data-stu-id="006df-107">EXAMPLES</span></span>

### <span data-ttu-id="006df-108">1：建立虛擬網路並移除其中一個子網</span><span class="sxs-lookup"><span data-stu-id="006df-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="006df-109">這個範例會建立名為 TestResourceGroup 的虛擬網路，其中包含兩個子網： frontendSubnet 和 backendSubnet。</span><span class="sxs-lookup"><span data-stu-id="006df-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="006df-110">然後它會將 backendSubnet 子網從虛擬網路的記憶體內部表示形式中移除。</span><span class="sxs-lookup"><span data-stu-id="006df-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="006df-111">然後使用 Set-AzVirtualNetwork Cmdlet，在服務端寫入修改過的虛擬網路狀態。</span><span class="sxs-lookup"><span data-stu-id="006df-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="006df-112">執行 Set-AzVirtualNetwork Cmdlet 時，會移除 backendSubnet。</span><span class="sxs-lookup"><span data-stu-id="006df-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="006df-113">參數</span><span class="sxs-lookup"><span data-stu-id="006df-113">PARAMETERS</span></span>

### <span data-ttu-id="006df-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="006df-114">-AsJob</span></span>
<span data-ttu-id="006df-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="006df-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="006df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006df-116">-DefaultProfile</span></span>
<span data-ttu-id="006df-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="006df-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="006df-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="006df-118">-VirtualNetwork</span></span>
<span data-ttu-id="006df-119">指定代表虛擬網路應設定之狀態的虛擬網路物件。</span><span class="sxs-lookup"><span data-stu-id="006df-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="006df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006df-120">CommonParameters</span></span>
<span data-ttu-id="006df-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="006df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006df-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="006df-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006df-123">輸入</span><span class="sxs-lookup"><span data-stu-id="006df-123">INPUTS</span></span>

### <span data-ttu-id="006df-124">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="006df-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="006df-125">輸出</span><span class="sxs-lookup"><span data-stu-id="006df-125">OUTPUTS</span></span>

### <span data-ttu-id="006df-126">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="006df-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="006df-127">筆記</span><span class="sxs-lookup"><span data-stu-id="006df-127">NOTES</span></span>

## <span data-ttu-id="006df-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="006df-128">RELATED LINKS</span></span>

[<span data-ttu-id="006df-129">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="006df-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="006df-130">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="006df-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="006df-131">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="006df-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="006df-132">移除-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="006df-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)



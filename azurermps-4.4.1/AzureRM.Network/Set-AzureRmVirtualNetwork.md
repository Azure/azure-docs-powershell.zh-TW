---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456475"
---
# <span data-ttu-id="40005-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40005-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="40005-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40005-102">SYNOPSIS</span></span>
<span data-ttu-id="40005-103">設定虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="40005-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40005-104">句法</span><span class="sxs-lookup"><span data-stu-id="40005-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40005-105">說明</span><span class="sxs-lookup"><span data-stu-id="40005-105">DESCRIPTION</span></span>
<span data-ttu-id="40005-106">**AzureRmVirtualNetwork** Cmdlet 設定 Azure 虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="40005-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="40005-107">示例</span><span class="sxs-lookup"><span data-stu-id="40005-107">EXAMPLES</span></span>

### <span data-ttu-id="40005-108">1：建立虛擬網路並移除其中一個子網</span><span class="sxs-lookup"><span data-stu-id="40005-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="40005-109">這個範例會建立具有兩個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="40005-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="40005-110">接著，它會從虛擬網路的記憶體內部表示形式移除一個子網。</span><span class="sxs-lookup"><span data-stu-id="40005-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="40005-111">然後使用 Set-AzureRmVirtualNetwork Cmdlet，在服務端寫入修改過的虛擬網路狀態。</span><span class="sxs-lookup"><span data-stu-id="40005-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="40005-112">參數</span><span class="sxs-lookup"><span data-stu-id="40005-112">PARAMETERS</span></span>

### <span data-ttu-id="40005-113">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40005-113">-VirtualNetwork</span></span>
<span data-ttu-id="40005-114">指定代表目標狀態的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="40005-114">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="40005-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40005-115">-DefaultProfile</span></span>
<span data-ttu-id="40005-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40005-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40005-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40005-117">CommonParameters</span></span>
<span data-ttu-id="40005-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40005-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40005-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40005-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40005-120">輸入</span><span class="sxs-lookup"><span data-stu-id="40005-120">INPUTS</span></span>

### <span data-ttu-id="40005-121">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40005-121">PSVirtualNetwork</span></span>
<span data-ttu-id="40005-122">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="40005-122">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="40005-123">輸出</span><span class="sxs-lookup"><span data-stu-id="40005-123">OUTPUTS</span></span>

### <span data-ttu-id="40005-124">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="40005-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="40005-125">筆記</span><span class="sxs-lookup"><span data-stu-id="40005-125">NOTES</span></span>

## <span data-ttu-id="40005-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="40005-126">RELATED LINKS</span></span>

[<span data-ttu-id="40005-127">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40005-127">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="40005-128">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40005-128">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="40005-129">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40005-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="40005-130">移除-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="40005-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)



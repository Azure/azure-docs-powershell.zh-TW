---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970932"
---
# <span data-ttu-id="6a349-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6a349-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="6a349-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a349-102">SYNOPSIS</span></span>
<span data-ttu-id="6a349-103">取得虛擬網路中的子網。</span><span class="sxs-lookup"><span data-stu-id="6a349-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="6a349-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a349-104">SYNTAX</span></span>

### <span data-ttu-id="6a349-105">GetByVirtualNetwork (預設) </span><span class="sxs-lookup"><span data-stu-id="6a349-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a349-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a349-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a349-107">說明</span><span class="sxs-lookup"><span data-stu-id="6a349-107">DESCRIPTION</span></span>
<span data-ttu-id="6a349-108">**AzVirtualNetworkSubnetConfig** Cmdlet 可取得 Azure 虛擬網路中的一或多個子網配置。</span><span class="sxs-lookup"><span data-stu-id="6a349-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="6a349-109">示例</span><span class="sxs-lookup"><span data-stu-id="6a349-109">EXAMPLES</span></span>

### <span data-ttu-id="6a349-110">1：在虛擬網路中取得子網</span><span class="sxs-lookup"><span data-stu-id="6a349-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="6a349-111">這個範例會建立一個資源群組，以及該資源群組中有單一子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="6a349-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="6a349-112">接著，它會檢索該子網上的相關資料。</span><span class="sxs-lookup"><span data-stu-id="6a349-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="6a349-113">參數</span><span class="sxs-lookup"><span data-stu-id="6a349-113">PARAMETERS</span></span>

### <span data-ttu-id="6a349-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a349-114">-DefaultProfile</span></span>
<span data-ttu-id="6a349-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a349-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a349-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a349-116">-Name</span></span>
<span data-ttu-id="6a349-117">指定此 Cmdlet 所取得之子網設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a349-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a349-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a349-118">-ResourceId</span></span>
<span data-ttu-id="6a349-119">指定此 Cmdlet 取得之子網的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a349-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a349-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6a349-120">-VirtualNetwork</span></span>
<span data-ttu-id="6a349-121">指定包含此 Cmdlet 所取得之子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="6a349-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a349-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a349-122">CommonParameters</span></span>
<span data-ttu-id="6a349-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a349-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a349-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6a349-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a349-125">輸入</span><span class="sxs-lookup"><span data-stu-id="6a349-125">INPUTS</span></span>

### <span data-ttu-id="6a349-126">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6a349-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="6a349-127">System.object</span><span class="sxs-lookup"><span data-stu-id="6a349-127">System.String</span></span>

## <span data-ttu-id="6a349-128">輸出</span><span class="sxs-lookup"><span data-stu-id="6a349-128">OUTPUTS</span></span>

### <span data-ttu-id="6a349-129">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6a349-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="6a349-130">筆記</span><span class="sxs-lookup"><span data-stu-id="6a349-130">NOTES</span></span>

## <span data-ttu-id="6a349-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a349-131">RELATED LINKS</span></span>

[<span data-ttu-id="6a349-132">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6a349-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6a349-133">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6a349-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6a349-134">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6a349-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6a349-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6a349-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
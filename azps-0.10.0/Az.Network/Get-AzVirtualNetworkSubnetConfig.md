---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794342"
---
# <span data-ttu-id="5d752-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5d752-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5d752-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d752-102">SYNOPSIS</span></span>
<span data-ttu-id="5d752-103">取得虛擬網路中的子網。</span><span class="sxs-lookup"><span data-stu-id="5d752-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="5d752-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d752-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d752-105">說明</span><span class="sxs-lookup"><span data-stu-id="5d752-105">DESCRIPTION</span></span>
<span data-ttu-id="5d752-106">**AzVirtualNetworkSubnetConfig** Cmdlet 可取得 Azure 虛擬網路中的一或多個子網配置。</span><span class="sxs-lookup"><span data-stu-id="5d752-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="5d752-107">示例</span><span class="sxs-lookup"><span data-stu-id="5d752-107">EXAMPLES</span></span>

### <span data-ttu-id="5d752-108">1：在虛擬網路中取得子網</span><span class="sxs-lookup"><span data-stu-id="5d752-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="5d752-109">這個範例會建立一個資源群組，以及該資源群組中有單一子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="5d752-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="5d752-110">接著，它會檢索該子網上的相關資料。</span><span class="sxs-lookup"><span data-stu-id="5d752-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="5d752-111">參數</span><span class="sxs-lookup"><span data-stu-id="5d752-111">PARAMETERS</span></span>

### <span data-ttu-id="5d752-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d752-112">-DefaultProfile</span></span>
<span data-ttu-id="5d752-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d752-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d752-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d752-114">-Name</span></span>
<span data-ttu-id="5d752-115">指定此 Cmdlet 所取得之子網設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d752-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d752-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5d752-116">-VirtualNetwork</span></span>
<span data-ttu-id="5d752-117">指定包含此 Cmdlet 所取得之子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="5d752-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5d752-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d752-118">CommonParameters</span></span>
<span data-ttu-id="5d752-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d752-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d752-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d752-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d752-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5d752-121">INPUTS</span></span>

### <span data-ttu-id="5d752-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5d752-122">PSVirtualNetwork</span></span>
<span data-ttu-id="5d752-123">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5d752-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="5d752-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5d752-124">OUTPUTS</span></span>

### <span data-ttu-id="5d752-125">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5d752-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5d752-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5d752-126">NOTES</span></span>

## <span data-ttu-id="5d752-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d752-127">RELATED LINKS</span></span>

[<span data-ttu-id="5d752-128">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5d752-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5d752-129">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5d752-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5d752-130">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5d752-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5d752-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5d752-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)



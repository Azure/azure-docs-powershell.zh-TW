---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 531eab9d8b1405b34a4676cd3e06430cfeda0680
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449291"
---
# <span data-ttu-id="25704-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="25704-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="25704-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25704-102">SYNOPSIS</span></span>
<span data-ttu-id="25704-103">取得虛擬網路中的子網。</span><span class="sxs-lookup"><span data-stu-id="25704-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25704-104">句法</span><span class="sxs-lookup"><span data-stu-id="25704-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25704-105">說明</span><span class="sxs-lookup"><span data-stu-id="25704-105">DESCRIPTION</span></span>
<span data-ttu-id="25704-106">**AzureRmVirtualNetworkSubnetConfig** Cmdlet 可取得 Azure 虛擬網路中的一或多個子網配置。</span><span class="sxs-lookup"><span data-stu-id="25704-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="25704-107">示例</span><span class="sxs-lookup"><span data-stu-id="25704-107">EXAMPLES</span></span>

### <span data-ttu-id="25704-108">1：在虛擬網路中取得子網</span><span class="sxs-lookup"><span data-stu-id="25704-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="25704-109">這個範例會建立一個資源群組，以及該資源群組中有單一子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="25704-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="25704-110">接著，它會檢索該子網上的相關資料。</span><span class="sxs-lookup"><span data-stu-id="25704-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="25704-111">參數</span><span class="sxs-lookup"><span data-stu-id="25704-111">PARAMETERS</span></span>

### <span data-ttu-id="25704-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25704-112">-DefaultProfile</span></span>
<span data-ttu-id="25704-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25704-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25704-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="25704-114">-Name</span></span>
<span data-ttu-id="25704-115">指定此 Cmdlet 所取得之子網設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="25704-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="25704-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="25704-116">-VirtualNetwork</span></span>
<span data-ttu-id="25704-117">指定包含此 Cmdlet 所取得之子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="25704-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="25704-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25704-118">CommonParameters</span></span>
<span data-ttu-id="25704-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25704-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25704-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25704-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25704-121">輸入</span><span class="sxs-lookup"><span data-stu-id="25704-121">INPUTS</span></span>

### <span data-ttu-id="25704-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="25704-122">PSVirtualNetwork</span></span>
<span data-ttu-id="25704-123">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="25704-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="25704-124">輸出</span><span class="sxs-lookup"><span data-stu-id="25704-124">OUTPUTS</span></span>

### <span data-ttu-id="25704-125">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="25704-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="25704-126">筆記</span><span class="sxs-lookup"><span data-stu-id="25704-126">NOTES</span></span>

## <span data-ttu-id="25704-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="25704-127">RELATED LINKS</span></span>

[<span data-ttu-id="25704-128">附加 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="25704-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="25704-129">新-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="25704-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="25704-130">移除-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="25704-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="25704-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="25704-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)



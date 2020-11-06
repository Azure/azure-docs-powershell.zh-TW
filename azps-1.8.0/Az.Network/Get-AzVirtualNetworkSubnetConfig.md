---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: e5b881547f84714e238f541948602569c773c9c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621912"
---
# <span data-ttu-id="cdbf6-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdbf6-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="cdbf6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="cdbf6-103">取得虛擬網路中的子網。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="cdbf6-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdbf6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdbf6-105">說明</span><span class="sxs-lookup"><span data-stu-id="cdbf6-105">DESCRIPTION</span></span>
<span data-ttu-id="cdbf6-106">**AzVirtualNetworkSubnetConfig** Cmdlet 可取得 Azure 虛擬網路中的一或多個子網配置。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="cdbf6-107">示例</span><span class="sxs-lookup"><span data-stu-id="cdbf6-107">EXAMPLES</span></span>

### <span data-ttu-id="cdbf6-108">1：在虛擬網路中取得子網</span><span class="sxs-lookup"><span data-stu-id="cdbf6-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="cdbf6-109">這個範例會建立一個資源群組，以及該資源群組中有單一子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="cdbf6-110">接著，它會檢索該子網上的相關資料。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="cdbf6-111">參數</span><span class="sxs-lookup"><span data-stu-id="cdbf6-111">PARAMETERS</span></span>

### <span data-ttu-id="cdbf6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdbf6-112">-DefaultProfile</span></span>
<span data-ttu-id="cdbf6-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdbf6-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="cdbf6-114">-Name</span></span>
<span data-ttu-id="cdbf6-115">指定此 Cmdlet 所取得之子網設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbf6-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdbf6-116">-VirtualNetwork</span></span>
<span data-ttu-id="cdbf6-117">指定包含此 Cmdlet 所取得之子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cdbf6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdbf6-118">CommonParameters</span></span>
<span data-ttu-id="cdbf6-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdbf6-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cdbf6-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdbf6-121">輸入</span><span class="sxs-lookup"><span data-stu-id="cdbf6-121">INPUTS</span></span>

### <span data-ttu-id="cdbf6-122">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cdbf6-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cdbf6-123">輸出</span><span class="sxs-lookup"><span data-stu-id="cdbf6-123">OUTPUTS</span></span>

### <span data-ttu-id="cdbf6-124">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cdbf6-124">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="cdbf6-125">筆記</span><span class="sxs-lookup"><span data-stu-id="cdbf6-125">NOTES</span></span>

## <span data-ttu-id="cdbf6-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdbf6-126">RELATED LINKS</span></span>

[<span data-ttu-id="cdbf6-127">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdbf6-127">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="cdbf6-128">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdbf6-128">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="cdbf6-129">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdbf6-129">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="cdbf6-130">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cdbf6-130">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)



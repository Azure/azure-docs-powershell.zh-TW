---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: bee7857751b9553314085ab3fee4f5edbadce1b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908490"
---
# <span data-ttu-id="b408e-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b408e-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b408e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b408e-102">SYNOPSIS</span></span>
<span data-ttu-id="b408e-103">在虛擬網路中建立子網。</span><span class="sxs-lookup"><span data-stu-id="b408e-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="b408e-104">語法</span><span class="sxs-lookup"><span data-stu-id="b408e-104">SYNTAX</span></span>

### <span data-ttu-id="b408e-105">GetByVirtualNetwork (預設) </span><span class="sxs-lookup"><span data-stu-id="b408e-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b408e-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b408e-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b408e-107">描述</span><span class="sxs-lookup"><span data-stu-id="b408e-107">DESCRIPTION</span></span>
<span data-ttu-id="b408e-108">**Get-AzVirtualNetworkSubnetConfig** Cmdlet 在 Azure 虛擬網路中取得一或多個子網組配置。</span><span class="sxs-lookup"><span data-stu-id="b408e-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="b408e-109">例子</span><span class="sxs-lookup"><span data-stu-id="b408e-109">EXAMPLES</span></span>

### <span data-ttu-id="b408e-110">1：在虛擬網路中取得子網</span><span class="sxs-lookup"><span data-stu-id="b408e-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="b408e-111">此範例會建立資源群組，以及該資源群組中單一子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b408e-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="b408e-112">然後，它會從該子網中取回資料。</span><span class="sxs-lookup"><span data-stu-id="b408e-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="b408e-113">參數</span><span class="sxs-lookup"><span data-stu-id="b408e-113">PARAMETERS</span></span>

### <span data-ttu-id="b408e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b408e-114">-DefaultProfile</span></span>
<span data-ttu-id="b408e-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b408e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b408e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b408e-116">-Name</span></span>
<span data-ttu-id="b408e-117">指定此 Cmdlet 所獲得之子網組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b408e-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b408e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b408e-118">-ResourceId</span></span>
<span data-ttu-id="b408e-119">指定此 Cmdlet 所獲得子網的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b408e-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b408e-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b408e-120">-VirtualNetwork</span></span>
<span data-ttu-id="b408e-121">指定 **包含此 Cmdlet** 所獲得子網配置的 VirtualNetwork 物件。</span><span class="sxs-lookup"><span data-stu-id="b408e-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b408e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b408e-122">CommonParameters</span></span>
<span data-ttu-id="b408e-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b408e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b408e-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b408e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b408e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b408e-125">INPUTS</span></span>

### <span data-ttu-id="b408e-126">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b408e-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="b408e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b408e-127">System.String</span></span>

## <span data-ttu-id="b408e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b408e-128">OUTPUTS</span></span>

### <span data-ttu-id="b408e-129">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b408e-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b408e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b408e-130">NOTES</span></span>

## <span data-ttu-id="b408e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b408e-131">RELATED LINKS</span></span>

[<span data-ttu-id="b408e-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b408e-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b408e-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b408e-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b408e-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b408e-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b408e-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b408e-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 92550eb08fb6abf704d450f323e3fd0b724d9942
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621542"
---
# <span data-ttu-id="43622-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="43622-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="43622-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43622-102">SYNOPSIS</span></span>
<span data-ttu-id="43622-103">從虛擬網路移除子網配置。</span><span class="sxs-lookup"><span data-stu-id="43622-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="43622-104">句法</span><span class="sxs-lookup"><span data-stu-id="43622-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43622-105">說明</span><span class="sxs-lookup"><span data-stu-id="43622-105">DESCRIPTION</span></span>
<span data-ttu-id="43622-106">**AzVirtualNetworkSubnetConfig** Cmdlet 會從 Azure 虛擬網路中移除子網。</span><span class="sxs-lookup"><span data-stu-id="43622-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="43622-107">示例</span><span class="sxs-lookup"><span data-stu-id="43622-107">EXAMPLES</span></span>

### <span data-ttu-id="43622-108">1：從虛擬網路移除子網並更新虛擬網路</span><span class="sxs-lookup"><span data-stu-id="43622-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="43622-109">這個範例會建立一個含有兩個子網的資源群組和虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="43622-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="43622-110">接著，它會使用 Remove-AzVirtualNetworkSubnetConfig 命令來從虛擬網路的記憶體內部表示形式中移除後端子網。</span><span class="sxs-lookup"><span data-stu-id="43622-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="43622-111">接著，就會呼叫 Set-AzVirtualNetwork 來修改伺服器端的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="43622-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="43622-112">參數</span><span class="sxs-lookup"><span data-stu-id="43622-112">PARAMETERS</span></span>

### <span data-ttu-id="43622-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43622-113">-DefaultProfile</span></span>
<span data-ttu-id="43622-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43622-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43622-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="43622-115">-Name</span></span>
<span data-ttu-id="43622-116">指定要移除的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="43622-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="43622-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="43622-117">-VirtualNetwork</span></span>
<span data-ttu-id="43622-118">指定包含要移除之子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="43622-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="43622-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43622-119">CommonParameters</span></span>
<span data-ttu-id="43622-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43622-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43622-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43622-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43622-122">輸入</span><span class="sxs-lookup"><span data-stu-id="43622-122">INPUTS</span></span>

### <span data-ttu-id="43622-123">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43622-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="43622-124">輸出</span><span class="sxs-lookup"><span data-stu-id="43622-124">OUTPUTS</span></span>

### <span data-ttu-id="43622-125">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43622-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="43622-126">筆記</span><span class="sxs-lookup"><span data-stu-id="43622-126">NOTES</span></span>

## <span data-ttu-id="43622-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="43622-127">RELATED LINKS</span></span>

[<span data-ttu-id="43622-128">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="43622-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="43622-129">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="43622-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="43622-130">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="43622-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="43622-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="43622-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)



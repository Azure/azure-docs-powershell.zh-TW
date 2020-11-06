---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: f2e0bb88df867da0a110422debea4d6688ad3af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453375"
---
# <span data-ttu-id="58da2-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58da2-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="58da2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58da2-102">SYNOPSIS</span></span>
<span data-ttu-id="58da2-103">從虛擬網路移除子網配置。</span><span class="sxs-lookup"><span data-stu-id="58da2-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58da2-104">句法</span><span class="sxs-lookup"><span data-stu-id="58da2-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58da2-105">說明</span><span class="sxs-lookup"><span data-stu-id="58da2-105">DESCRIPTION</span></span>
<span data-ttu-id="58da2-106">**AzureRmVirtualNetworkSubnetConfig** Cmdlet 會從 Azure 虛擬網路中移除子網。</span><span class="sxs-lookup"><span data-stu-id="58da2-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="58da2-107">示例</span><span class="sxs-lookup"><span data-stu-id="58da2-107">EXAMPLES</span></span>

### <span data-ttu-id="58da2-108">1：從虛擬網路移除子網並更新虛擬網路</span><span class="sxs-lookup"><span data-stu-id="58da2-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="58da2-109">這個範例會建立一個含有兩個子網的資源群組和虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="58da2-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="58da2-110">接著，它會使用 Remove-AzureRmVirtualNetworkSubnetConfig 命令來從虛擬網路的記憶體內部表示形式中移除後端子網。</span><span class="sxs-lookup"><span data-stu-id="58da2-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="58da2-111">接著，就會呼叫 Set-AzureRmVirtualNetwork 來修改伺服器端的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="58da2-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="58da2-112">參數</span><span class="sxs-lookup"><span data-stu-id="58da2-112">PARAMETERS</span></span>

### <span data-ttu-id="58da2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="58da2-113">-Name</span></span>
<span data-ttu-id="58da2-114">指定要移除的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="58da2-114">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="58da2-115">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="58da2-115">-VirtualNetwork</span></span>
<span data-ttu-id="58da2-116">指定包含要移除之子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="58da2-116">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="58da2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58da2-117">-DefaultProfile</span></span>
<span data-ttu-id="58da2-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58da2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58da2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58da2-119">CommonParameters</span></span>
<span data-ttu-id="58da2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58da2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58da2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58da2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58da2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="58da2-122">INPUTS</span></span>

### <span data-ttu-id="58da2-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="58da2-123">PSVirtualNetwork</span></span>
<span data-ttu-id="58da2-124">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="58da2-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="58da2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="58da2-125">OUTPUTS</span></span>

### <span data-ttu-id="58da2-126">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="58da2-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="58da2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="58da2-127">NOTES</span></span>

## <span data-ttu-id="58da2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="58da2-128">RELATED LINKS</span></span>

[<span data-ttu-id="58da2-129">附加 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58da2-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58da2-130">AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58da2-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58da2-131">新-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58da2-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58da2-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58da2-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)



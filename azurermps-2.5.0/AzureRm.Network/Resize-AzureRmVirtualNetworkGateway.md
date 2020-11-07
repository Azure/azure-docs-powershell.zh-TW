---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 0a3dea2b706f7efcdc76b48175df225e2974728c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802249"
---
# <span data-ttu-id="a2eea-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2eea-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="a2eea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2eea-102">SYNOPSIS</span></span>
<span data-ttu-id="a2eea-103">重新調整現有虛擬網路閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="a2eea-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2eea-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2eea-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2eea-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2eea-105">DESCRIPTION</span></span>
<span data-ttu-id="a2eea-106">重 **設大小 AzureRmVirtualNetworkGateway** Cmdlet 能讓您變更虛擬閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="a2eea-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="a2eea-107">Sku 決定閘道的功能，包括輸送量與允許的 IP 隧道數目上限等。</span><span class="sxs-lookup"><span data-stu-id="a2eea-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="a2eea-108">Azure 支援基本、標準、高效能、VpnGw1、VpnGw2 和 VpnGw3 Sku， (有時稱為小型、中型及大型 Sku) 。</span><span class="sxs-lookup"><span data-stu-id="a2eea-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="a2eea-109">如需有關每個 SKU 類型之功能的詳細資訊，請參閱 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 。</span><span class="sxs-lookup"><span data-stu-id="a2eea-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="a2eea-110">請記住，Sku 與定價及功能有不同。</span><span class="sxs-lookup"><span data-stu-id="a2eea-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="a2eea-111">如需詳細資訊，請參閱 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 。</span><span class="sxs-lookup"><span data-stu-id="a2eea-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="a2eea-112">示例</span><span class="sxs-lookup"><span data-stu-id="a2eea-112">EXAMPLES</span></span>

### <span data-ttu-id="a2eea-113">範例1：變更虛擬閘道的大小</span><span class="sxs-lookup"><span data-stu-id="a2eea-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="a2eea-114">這個範例會變更名為 ContosoVirtualGateway 的虛擬網路閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="a2eea-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="a2eea-115">第一個命令會建立 ContosoVirtualGateway 的物件參照;這個物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="a2eea-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="a2eea-116">然後，第二個命令會使用 **AzureRmVirtualNetworkGateway** Cmdlet，將 *GatewaySku* 屬性設為 Basic。</span><span class="sxs-lookup"><span data-stu-id="a2eea-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="a2eea-117">參數</span><span class="sxs-lookup"><span data-stu-id="a2eea-117">PARAMETERS</span></span>

### <span data-ttu-id="a2eea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2eea-118">-DefaultProfile</span></span>
<span data-ttu-id="a2eea-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2eea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2eea-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="a2eea-120">-GatewaySku</span></span>
<span data-ttu-id="a2eea-121">指定新的閘道 SKU 類型。</span><span class="sxs-lookup"><span data-stu-id="a2eea-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="a2eea-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a2eea-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2eea-123">空白</span><span class="sxs-lookup"><span data-stu-id="a2eea-123">Basic</span></span>
- <span data-ttu-id="a2eea-124">標準</span><span class="sxs-lookup"><span data-stu-id="a2eea-124">Standard</span></span>
- <span data-ttu-id="a2eea-125">高效能</span><span class="sxs-lookup"><span data-stu-id="a2eea-125">High Performance</span></span>
- <span data-ttu-id="a2eea-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="a2eea-126">VpnGw1</span></span>
- <span data-ttu-id="a2eea-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="a2eea-127">VpnGw2</span></span>
- <span data-ttu-id="a2eea-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="a2eea-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2eea-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2eea-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a2eea-130">指定要調整其大小的虛擬網路閘道物件參照。</span><span class="sxs-lookup"><span data-stu-id="a2eea-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="a2eea-131">您可以使用 Get-AzureRmVirtualNetworkGateway 並指定閘道的名稱來建立此物件參照。</span><span class="sxs-lookup"><span data-stu-id="a2eea-131">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2eea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2eea-132">CommonParameters</span></span>
<span data-ttu-id="a2eea-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2eea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2eea-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2eea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2eea-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a2eea-135">INPUTS</span></span>

###  
<span data-ttu-id="a2eea-136">這個 Cmdlet 會接受 PSVirtualNetworkGateway 物件的流水線實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。</span><span class="sxs-lookup"><span data-stu-id="a2eea-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="a2eea-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a2eea-137">OUTPUTS</span></span>

###  
<span data-ttu-id="a2eea-138">這個 Cmdlet 會修改 PSVirtualNetworkGateway 物件的現有實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。</span><span class="sxs-lookup"><span data-stu-id="a2eea-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="a2eea-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a2eea-139">NOTES</span></span>
<span data-ttu-id="a2eea-140">您無法將基本/標準/HighPerformance Sku 的大小調整成新的 VpnGw1/VpnGw2/VpnGw3 Sku。</span><span class="sxs-lookup"><span data-stu-id="a2eea-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="a2eea-141"> https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways如需相關指示，請參閱。</span><span class="sxs-lookup"><span data-stu-id="a2eea-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="a2eea-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2eea-142">RELATED LINKS</span></span>

[<span data-ttu-id="a2eea-143">AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="a2eea-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="a2eea-144">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2eea-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a2eea-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="a2eea-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)



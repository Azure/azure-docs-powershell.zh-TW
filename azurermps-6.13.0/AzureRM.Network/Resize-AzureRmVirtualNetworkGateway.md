---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455132"
---
# <span data-ttu-id="d9c36-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d9c36-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="d9c36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9c36-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c36-103">重新調整現有虛擬網路閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="d9c36-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9c36-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9c36-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9c36-105">說明</span><span class="sxs-lookup"><span data-stu-id="d9c36-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c36-106">重 **設大小 AzureRmVirtualNetworkGateway** Cmdlet 能讓您變更虛擬閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="d9c36-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="d9c36-107">Sku 決定閘道的功能，包括輸送量與允許的 IP 隧道數目上限等。</span><span class="sxs-lookup"><span data-stu-id="d9c36-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="d9c36-108">Azure 支援基本、標準、高效能、VpnGw1、VpnGw2、VpnGw3、VpnGw1AZ、VpnGw2AZ、VpnGw3AZ、ErGw1AZ、ErGw2AZ、ErGw3AZ Sku (有時稱為中小型、中型及大型 Sku) 。</span><span class="sxs-lookup"><span data-stu-id="d9c36-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="d9c36-109">如需有關每個 SKU 類型之功能的詳細資訊，請參閱 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 。</span><span class="sxs-lookup"><span data-stu-id="d9c36-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="d9c36-110">請記住，Sku 與定價及功能有不同。</span><span class="sxs-lookup"><span data-stu-id="d9c36-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="d9c36-111">如需詳細資訊，請參閱 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 。</span><span class="sxs-lookup"><span data-stu-id="d9c36-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="d9c36-112">示例</span><span class="sxs-lookup"><span data-stu-id="d9c36-112">EXAMPLES</span></span>

### <span data-ttu-id="d9c36-113">範例1：變更虛擬閘道的大小</span><span class="sxs-lookup"><span data-stu-id="d9c36-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="d9c36-114">這個範例會變更名為 ContosoVirtualGateway 的虛擬網路閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="d9c36-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="d9c36-115">第一個命令會建立 ContosoVirtualGateway 的物件參照;這個物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d9c36-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="d9c36-116">然後，第二個命令會使用 **AzureRmVirtualNetworkGateway** Cmdlet，將 *GatewaySku* 屬性設為 Basic。</span><span class="sxs-lookup"><span data-stu-id="d9c36-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="d9c36-117">參數</span><span class="sxs-lookup"><span data-stu-id="d9c36-117">PARAMETERS</span></span>

### <span data-ttu-id="d9c36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c36-118">-DefaultProfile</span></span>
<span data-ttu-id="d9c36-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9c36-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9c36-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="d9c36-120">-GatewaySku</span></span>
<span data-ttu-id="d9c36-121">指定新的閘道 SKU 類型。</span><span class="sxs-lookup"><span data-stu-id="d9c36-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="d9c36-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d9c36-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9c36-123">空白</span><span class="sxs-lookup"><span data-stu-id="d9c36-123">Basic</span></span>
- <span data-ttu-id="d9c36-124">標準</span><span class="sxs-lookup"><span data-stu-id="d9c36-124">Standard</span></span>
- <span data-ttu-id="d9c36-125">高效能</span><span class="sxs-lookup"><span data-stu-id="d9c36-125">High Performance</span></span>
- <span data-ttu-id="d9c36-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="d9c36-126">VpnGw1</span></span>
- <span data-ttu-id="d9c36-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="d9c36-127">VpnGw2</span></span>
- <span data-ttu-id="d9c36-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="d9c36-128">VpnGw3</span></span>
- <span data-ttu-id="d9c36-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d9c36-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="d9c36-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d9c36-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="d9c36-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d9c36-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="d9c36-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d9c36-132">ErGw1AZ</span></span> 
- <span data-ttu-id="d9c36-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d9c36-133">ErGw2AZ</span></span> 
- <span data-ttu-id="d9c36-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d9c36-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c36-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d9c36-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d9c36-136">指定要調整其大小的虛擬網路閘道物件參照。</span><span class="sxs-lookup"><span data-stu-id="d9c36-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="d9c36-137">您可以使用 Get-AzureRmVirtualNetworkGateway 並指定閘道的名稱來建立此物件參照。</span><span class="sxs-lookup"><span data-stu-id="d9c36-137">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c36-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c36-138">CommonParameters</span></span>
<span data-ttu-id="d9c36-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9c36-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c36-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9c36-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c36-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d9c36-141">INPUTS</span></span>

### <span data-ttu-id="d9c36-142">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d9c36-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="d9c36-143">參數： VirtualNetworkGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d9c36-143">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="d9c36-144">System.object</span><span class="sxs-lookup"><span data-stu-id="d9c36-144">System.String</span></span>

## <span data-ttu-id="d9c36-145">輸出</span><span class="sxs-lookup"><span data-stu-id="d9c36-145">OUTPUTS</span></span>

### <span data-ttu-id="d9c36-146">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d9c36-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d9c36-147">筆記</span><span class="sxs-lookup"><span data-stu-id="d9c36-147">NOTES</span></span>
<span data-ttu-id="d9c36-148">您無法將基本/標準/HighPerformance Sku 的大小調整成新的 VpnGw1/VpnGw2/VpnGw3 Sku。</span><span class="sxs-lookup"><span data-stu-id="d9c36-148">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="d9c36-149">不允許從/至 VpnGw1AZ/VpnGw2AZ/VpnGw3AZ 或 ErGw1AZ/ErGw2AZ/ErGw3AZ 進行進一步的調整大小。</span><span class="sxs-lookup"><span data-stu-id="d9c36-149">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="d9c36-150">只允許在 SKU "series" 中使用調整大小（例如，可以從 VpnGw2AZ/VpnGw3AZ 調整 VpnGw1AZ 大小），也可以從 ErGw2AZ/ErGw3AZ 調整 ErGw1AZ 的大小。</span><span class="sxs-lookup"><span data-stu-id="d9c36-150">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="d9c36-151"> https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways如需相關指示，請參閱。</span><span class="sxs-lookup"><span data-stu-id="d9c36-151">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="d9c36-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9c36-152">RELATED LINKS</span></span>

[<span data-ttu-id="d9c36-153">AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="d9c36-153">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="d9c36-154">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d9c36-154">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d9c36-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="d9c36-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)



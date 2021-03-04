---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4b2963d77d2182821bb4950907ef278950e410f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903461"
---
# <span data-ttu-id="77d98-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="77d98-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77d98-102">SYNOPSIS</span></span>
<span data-ttu-id="77d98-103">調整現有虛擬網路閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="77d98-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="77d98-104">語法</span><span class="sxs-lookup"><span data-stu-id="77d98-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77d98-105">描述</span><span class="sxs-lookup"><span data-stu-id="77d98-105">DESCRIPTION</span></span>
<span data-ttu-id="77d98-106">**Resize-AzVirtualNetworkGateway** Cmdlet 可讓您變更 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="77d98-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="77d98-107">SKUS 會決定閘道的功能，包括輸送量和允許的最大 IP 數量等。</span><span class="sxs-lookup"><span data-stu-id="77d98-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="77d98-108">Azure 支援基本、標準、高績效、VpnGw1、VpnGw2、VpnGw3、VpnGw1AZ、VpnGw2AZ、VpnGw3AZ、ErGw1AZ、ErGw2AZ、ErGw3AZ SKUS (有時稱為小型、中型和大型 SKUS) 。</span><span class="sxs-lookup"><span data-stu-id="77d98-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="77d98-109">有關每個 SKU 類型功能的詳細資訊，請參閱 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 。</span><span class="sxs-lookup"><span data-stu-id="77d98-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="77d98-110">請記住，SKUS 在定價和功能上有所不同。</span><span class="sxs-lookup"><span data-stu-id="77d98-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="77d98-111">詳細資訊請參閱 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 。</span><span class="sxs-lookup"><span data-stu-id="77d98-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="77d98-112">例子</span><span class="sxs-lookup"><span data-stu-id="77d98-112">EXAMPLES</span></span>

### <span data-ttu-id="77d98-113">範例 1：變更虛擬網路閘道的大小</span><span class="sxs-lookup"><span data-stu-id="77d98-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="77d98-114">此範例會變更名為 ContosoVirtualGateway 的虛擬網路閘道大小。</span><span class="sxs-lookup"><span data-stu-id="77d98-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="77d98-115">第一個命令會建立 ContosoVirtualGateway 的物件參照;此物件參照會儲存在名為 $Gateway 的$Gateway。</span><span class="sxs-lookup"><span data-stu-id="77d98-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="77d98-116">接著，第二個命令會使用 **Resize-AzVirtualNetworkGateway** Cmdlet 將 *GatewaySku* 屬性設為 Basic。</span><span class="sxs-lookup"><span data-stu-id="77d98-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="77d98-117">參數</span><span class="sxs-lookup"><span data-stu-id="77d98-117">PARAMETERS</span></span>

### <span data-ttu-id="77d98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d98-118">-DefaultProfile</span></span>
<span data-ttu-id="77d98-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="77d98-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77d98-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="77d98-120">-GatewaySku</span></span>
<span data-ttu-id="77d98-121">指定新類型的閘道 SKU。</span><span class="sxs-lookup"><span data-stu-id="77d98-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="77d98-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="77d98-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77d98-123">基本</span><span class="sxs-lookup"><span data-stu-id="77d98-123">Basic</span></span>
- <span data-ttu-id="77d98-124">標準</span><span class="sxs-lookup"><span data-stu-id="77d98-124">Standard</span></span>
- <span data-ttu-id="77d98-125">高績效</span><span class="sxs-lookup"><span data-stu-id="77d98-125">High Performance</span></span>
- <span data-ttu-id="77d98-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="77d98-126">VpnGw1</span></span>
- <span data-ttu-id="77d98-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="77d98-127">VpnGw2</span></span>
- <span data-ttu-id="77d98-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="77d98-128">VpnGw3</span></span>
- <span data-ttu-id="77d98-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="77d98-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="77d98-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="77d98-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="77d98-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="77d98-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="77d98-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="77d98-132">ErGw1AZ</span></span> 
- <span data-ttu-id="77d98-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="77d98-133">ErGw2AZ</span></span> 
- <span data-ttu-id="77d98-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="77d98-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="77d98-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="77d98-136">指定要調整大小之虛擬網路閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="77d98-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="77d98-137">您可以使用資料Get-AzVirtualNetworkGateway指定閘道名稱，以建立此物件參照。</span><span class="sxs-lookup"><span data-stu-id="77d98-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="77d98-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d98-138">CommonParameters</span></span>
<span data-ttu-id="77d98-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77d98-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d98-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="77d98-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d98-141">輸入</span><span class="sxs-lookup"><span data-stu-id="77d98-141">INPUTS</span></span>

### <span data-ttu-id="77d98-142">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="77d98-143">System.String</span><span class="sxs-lookup"><span data-stu-id="77d98-143">System.String</span></span>

## <span data-ttu-id="77d98-144">輸出</span><span class="sxs-lookup"><span data-stu-id="77d98-144">OUTPUTS</span></span>

### <span data-ttu-id="77d98-145">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="77d98-146">筆記</span><span class="sxs-lookup"><span data-stu-id="77d98-146">NOTES</span></span>
<span data-ttu-id="77d98-147">您無法將基本/標準/HighPerformance SKUS 的大小調整為新的 VpnGw1/VpnGw2/VpnGw3 SKUS。</span><span class="sxs-lookup"><span data-stu-id="77d98-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="77d98-148">不允許進一步調整大小，從/到 VpnGw1AZ/VpnGw2AZ/VpnGw3AZ 或 ErGw1AZ/ErGw2AZ/ErGw3AZ。</span><span class="sxs-lookup"><span data-stu-id="77d98-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="77d98-149">只有在 SKU 'series' 內允許調整大小，例如 VpnGw1AZ 可以調整大小至/從 VpnGw2AZ/VpnGw3AZ 和 ErGw1AZ 可以調整大小至/從 ErGw2AZ/ErGw3AZ。</span><span class="sxs-lookup"><span data-stu-id="77d98-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="77d98-150">請參閱 https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways 指示。</span><span class="sxs-lookup"><span data-stu-id="77d98-150">See https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="77d98-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="77d98-151">RELATED LINKS</span></span>

[<span data-ttu-id="77d98-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="77d98-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="77d98-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="77d98-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="77d98-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="77d98-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="77d98-157">Get-Az VpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="77d98-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="77d98-158">Set-AzVirtualNetworkGateway VpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="77d98-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)

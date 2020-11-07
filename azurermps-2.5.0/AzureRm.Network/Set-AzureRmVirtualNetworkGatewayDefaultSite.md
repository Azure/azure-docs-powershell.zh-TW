---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: 463951ca6b6679671f330a3ddb0f9460a878a3d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801578"
---
# <span data-ttu-id="6288c-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="6288c-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="6288c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6288c-102">SYNOPSIS</span></span>
<span data-ttu-id="6288c-103">設定虛擬網路閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="6288c-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6288c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6288c-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6288c-105">說明</span><span class="sxs-lookup"><span data-stu-id="6288c-105">DESCRIPTION</span></span>
<span data-ttu-id="6288c-106">**AzureRmVirtualNetworkGatewayDefaultSite** Cmdlet 會將強制隧道預設網站指派給虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6288c-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="6288c-107">強制隧道提供一種將網際網路系結流量從 Azure 虛擬機器重新導向到您的內部部署網路的方式;這可讓您在釋放流量前先檢查並進行審核。</span><span class="sxs-lookup"><span data-stu-id="6288c-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="6288c-108">強制隧道是使用虛擬私人網路絡 (VPN) 隧道來執行;這個隧道需要一個預設的網站，即會重新導向所有 Azure 網際網路系結流量的本機閘道。</span><span class="sxs-lookup"><span data-stu-id="6288c-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="6288c-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** 提供一種變更指派給閘道之預設網站的方法。</span><span class="sxs-lookup"><span data-stu-id="6288c-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="6288c-110">示例</span><span class="sxs-lookup"><span data-stu-id="6288c-110">EXAMPLES</span></span>

### <span data-ttu-id="6288c-111">範例1：指派預設網站至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6288c-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="6288c-112">這個範例會將預設網站指派給名為 ContosoVirtualGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6288c-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="6288c-113">第一個命令會建立名為 ContosoLocalGateway 的本機閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="6288c-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="6288c-114">儲存在名為 $LocalGateway 的變數中的物件參照代表要設定為預設網站的閘道</span><span class="sxs-lookup"><span data-stu-id="6288c-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="6288c-115">.</span><span class="sxs-lookup"><span data-stu-id="6288c-115">.</span></span>
<span data-ttu-id="6288c-116">然後，第二個命令會建立虛擬網路閘道的物件參照，並將結果儲存在名為 $VirtualGateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6288c-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="6288c-117">第三個命令使用 **AzureRmVirtualNetworkGatewayDefaultSite** Cmdlet 將預設的網站指派給 ContosoVirtualGateway。</span><span class="sxs-lookup"><span data-stu-id="6288c-117">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="6288c-118">參數</span><span class="sxs-lookup"><span data-stu-id="6288c-118">PARAMETERS</span></span>

### <span data-ttu-id="6288c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6288c-119">-DefaultProfile</span></span>
<span data-ttu-id="6288c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6288c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6288c-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="6288c-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="6288c-122">指定要指派為指定虛擬網路預設網站之本機網路閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="6288c-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="6288c-123">您可以使用 Get-AzureRmLocalNetworkGateway Cmdlet 來建立本機閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="6288c-123">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6288c-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6288c-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="6288c-125">指定將指派預設網站之虛擬網路閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="6288c-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="6288c-126">您可以使用 **AzureRmVirtualNetworkGateway** ，並指定閘道的名稱，來建立虛擬閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="6288c-126">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="6288c-127">變數 $VirtualGateway 可以用來做為 *VirtualNetworkGateway* 參數的參數值：</span><span class="sxs-lookup"><span data-stu-id="6288c-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="6288c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6288c-128">CommonParameters</span></span>
<span data-ttu-id="6288c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6288c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6288c-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6288c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6288c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6288c-131">INPUTS</span></span>

###  
<span data-ttu-id="6288c-132">這個 Cmdlet 會接受 PSVirtualNetworkGateway 物件的流水線實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。</span><span class="sxs-lookup"><span data-stu-id="6288c-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="6288c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6288c-133">OUTPUTS</span></span>

###  
<span data-ttu-id="6288c-134">這個 Cmdlet 會修改 PSVirtualNetworkGateway 物件的現有實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。</span><span class="sxs-lookup"><span data-stu-id="6288c-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="6288c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6288c-135">NOTES</span></span>

## <span data-ttu-id="6288c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6288c-136">RELATED LINKS</span></span>

[<span data-ttu-id="6288c-137">AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6288c-137">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="6288c-138">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6288c-138">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6288c-139">移除-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="6288c-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)



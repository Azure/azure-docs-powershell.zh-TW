---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970866"
---
# <span data-ttu-id="f3363-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f3363-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="f3363-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3363-102">SYNOPSIS</span></span>
<span data-ttu-id="f3363-103">設定虛擬網路閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="f3363-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="f3363-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3363-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3363-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3363-105">DESCRIPTION</span></span>
<span data-ttu-id="f3363-106">**AzVirtualNetworkGatewayDefaultSite** Cmdlet 會將強制隧道預設網站指派給虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f3363-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="f3363-107">強制隧道提供一種將網際網路系結流量從 Azure 虛擬機器重新導向到您的內部部署網路的方式;這可讓您在釋放流量前先檢查並進行審核。</span><span class="sxs-lookup"><span data-stu-id="f3363-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="f3363-108">強制隧道是使用虛擬私人網路絡 (VPN) 隧道來執行;這個隧道需要一個預設的網站，即會重新導向所有 Azure 網際網路系結流量的本機閘道。</span><span class="sxs-lookup"><span data-stu-id="f3363-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="f3363-109">**Set-AzVirtualNetworkGatewayDefaultSite** 提供一種變更指派給閘道之預設網站的方法。</span><span class="sxs-lookup"><span data-stu-id="f3363-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="f3363-110">示例</span><span class="sxs-lookup"><span data-stu-id="f3363-110">EXAMPLES</span></span>

### <span data-ttu-id="f3363-111">範例1：指派預設網站至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="f3363-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="f3363-112">這個範例會將預設網站指派給名為 ContosoVirtualGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f3363-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="f3363-113">第一個命令會建立名為 ContosoLocalGateway 的本機閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="f3363-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="f3363-114">儲存在名為 $LocalGateway 的變數中的物件參照代表要設定為預設網站的閘道。</span><span class="sxs-lookup"><span data-stu-id="f3363-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="f3363-115">然後，第二個命令會建立虛擬網路閘道的物件參照，並將結果儲存在名為 $VirtualGateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f3363-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="f3363-116">第三個命令使用 **AzVirtualNetworkGatewayDefaultSite** Cmdlet 將預設的網站指派給 ContosoVirtualGateway。</span><span class="sxs-lookup"><span data-stu-id="f3363-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="f3363-117">參數</span><span class="sxs-lookup"><span data-stu-id="f3363-117">PARAMETERS</span></span>

### <span data-ttu-id="f3363-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3363-118">-DefaultProfile</span></span>
<span data-ttu-id="f3363-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3363-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3363-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f3363-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="f3363-121">指定要指派為指定虛擬網路預設網站之本機網路閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="f3363-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="f3363-122">您可以使用 Get-AzLocalNetworkGateway Cmdlet 來建立本機閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="f3363-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3363-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3363-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f3363-124">指定將指派預設網站之虛擬網路閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="f3363-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="f3363-125">您可以使用 **AzVirtualNetworkGateway** ，並指定閘道的名稱，來建立虛擬閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="f3363-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="f3363-126">變數 $VirtualGateway 可以用來做為 *VirtualNetworkGateway* 參數的參數值：</span><span class="sxs-lookup"><span data-stu-id="f3363-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="f3363-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3363-127">CommonParameters</span></span>
<span data-ttu-id="f3363-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3363-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3363-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3363-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3363-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f3363-130">INPUTS</span></span>

### <span data-ttu-id="f3363-131">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3363-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f3363-132">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3363-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f3363-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f3363-133">OUTPUTS</span></span>

### <span data-ttu-id="f3363-134">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3363-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f3363-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f3363-135">NOTES</span></span>

## <span data-ttu-id="f3363-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3363-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3363-137">AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3363-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="f3363-138">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3363-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f3363-139">移除-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f3363-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)



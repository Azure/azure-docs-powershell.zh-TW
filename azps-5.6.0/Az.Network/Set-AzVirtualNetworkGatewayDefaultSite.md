---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908782"
---
# <span data-ttu-id="33302-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="33302-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="33302-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33302-102">SYNOPSIS</span></span>
<span data-ttu-id="33302-103">設定虛擬網路閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="33302-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="33302-104">語法</span><span class="sxs-lookup"><span data-stu-id="33302-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33302-105">描述</span><span class="sxs-lookup"><span data-stu-id="33302-105">DESCRIPTION</span></span>
<span data-ttu-id="33302-106">**Set-AzVirtualNetworkGatewayDefaultSite** Cmdlet 會指派強制設定預設網站至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="33302-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="33302-107">強制導向提供一種將受網際網路限制的流量從 Azure 虛擬機器重新導向到內部部署網路的方法;這可讓您在發行之前檢查和稽核流量。</span><span class="sxs-lookup"><span data-stu-id="33302-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="33302-108">使用虛擬私人網路或 VPN (進行強制) 部署;此管道需要預設網站，即重新導向所有 Azure 網際網路流量的一個本地閘道。</span><span class="sxs-lookup"><span data-stu-id="33302-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="33302-109">**Set-AzVirtualNetworkGatewayDefaultSite** 提供變更指派給閘道的預設網站的方法。</span><span class="sxs-lookup"><span data-stu-id="33302-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="33302-110">例子</span><span class="sxs-lookup"><span data-stu-id="33302-110">EXAMPLES</span></span>

### <span data-ttu-id="33302-111">範例 1：將預設網站指派給虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="33302-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="33302-112">此範例會指派預設網站給名為 ContosoVirtualGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="33302-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="33302-113">第一個命令會建立名為 ContosoLocalGateway 之本地閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="33302-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="33302-114">儲存在名為 $LocalGateway 的變數中的這個物件參照代表要當做預設網站的閘道。</span><span class="sxs-lookup"><span data-stu-id="33302-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="33302-115">接著，第二個命令會建立虛擬網路閘道的物件參照，然後將結果儲存在名為 $VirtualGateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="33302-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="33302-116">第三個命令使用 **Set-AzVirtualNetworkGatewayDefaultSite** Cmdlet 將預設網站指派給 ContosoVirtualGateway。</span><span class="sxs-lookup"><span data-stu-id="33302-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="33302-117">參數</span><span class="sxs-lookup"><span data-stu-id="33302-117">PARAMETERS</span></span>

### <span data-ttu-id="33302-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33302-118">-DefaultProfile</span></span>
<span data-ttu-id="33302-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33302-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33302-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="33302-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="33302-121">指定要指派為指定之虛擬網路預設網站之本地網路閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="33302-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="33302-122">您可以使用 Get-AzLocalNetworkGateway Cmdlet 建立本地閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="33302-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="33302-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33302-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="33302-124">指定將指派預設網站之虛擬網路閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="33302-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="33302-125">您可以使用 **Get-AzVirtualNetworkGateway** 並指定閘道名稱，來建立虛擬網路閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="33302-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="33302-126">然後$VirtualGateway變數做為 *VirtualNetworkGateway* 參數的參數值：</span><span class="sxs-lookup"><span data-stu-id="33302-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="33302-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33302-127">CommonParameters</span></span>
<span data-ttu-id="33302-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33302-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33302-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="33302-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33302-130">輸入</span><span class="sxs-lookup"><span data-stu-id="33302-130">INPUTS</span></span>

### <span data-ttu-id="33302-131">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33302-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="33302-132">Microsoft.Azure.Commands.Network.models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33302-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="33302-133">輸出</span><span class="sxs-lookup"><span data-stu-id="33302-133">OUTPUTS</span></span>

### <span data-ttu-id="33302-134">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33302-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="33302-135">筆記</span><span class="sxs-lookup"><span data-stu-id="33302-135">NOTES</span></span>

## <span data-ttu-id="33302-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="33302-136">RELATED LINKS</span></span>

[<span data-ttu-id="33302-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33302-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="33302-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33302-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="33302-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="33302-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128751"
---
# <span data-ttu-id="75a42-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="75a42-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="75a42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75a42-102">SYNOPSIS</span></span>
<span data-ttu-id="75a42-103">從虛擬網路閘道移除預設網站。</span><span class="sxs-lookup"><span data-stu-id="75a42-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="75a42-104">句法</span><span class="sxs-lookup"><span data-stu-id="75a42-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a42-105">說明</span><span class="sxs-lookup"><span data-stu-id="75a42-105">DESCRIPTION</span></span>
<span data-ttu-id="75a42-106">**AzVirtualNetworkGatewayDefaultSite** Cmdlet 會從虛擬網路閘道中移除強制隧道預設網站。</span><span class="sxs-lookup"><span data-stu-id="75a42-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="75a42-107">強制隧道提供一種將網際網路系結流量從 Azure 虛擬機器重新導向到您的內部部署網路的方式;這可讓您在釋放流量前先檢查並進行審核。</span><span class="sxs-lookup"><span data-stu-id="75a42-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="75a42-108">強制隧道是使用虛擬私人網路絡 (VPN) 隧道來執行;這個隧道需要一個預設的網站，即會重新導向所有 Azure 網際網路系結流量的本機閘道。</span><span class="sxs-lookup"><span data-stu-id="75a42-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="75a42-109">**移除-AzVirtualNetworkGatewayDefaultSite** 會移除指派給閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="75a42-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="75a42-110">如果您這麼做，您將需要使用 Set-AzVirtualNetworkGatewayDefaultSite 來指派新的預設網站，然後才能將閘道用於強制性隧道。</span><span class="sxs-lookup"><span data-stu-id="75a42-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="75a42-111">示例</span><span class="sxs-lookup"><span data-stu-id="75a42-111">EXAMPLES</span></span>

### <span data-ttu-id="75a42-112">範例1：移除指派給虛擬網路閘道的預設網站</span><span class="sxs-lookup"><span data-stu-id="75a42-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="75a42-113">這個範例會移除目前指派給名為 ContosoVirtualGateway 的虛擬網路閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="75a42-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="75a42-114">第一個命令使用 **AzVirtualNetworkGateway** 來建立閘道的物件參照;這個物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="75a42-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="75a42-115">然後，第二個命令會使用 **移除 AzVirtualNetworkGatewayDefaultSite** 來移除指派給該閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="75a42-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="75a42-116">參數</span><span class="sxs-lookup"><span data-stu-id="75a42-116">PARAMETERS</span></span>

### <span data-ttu-id="75a42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a42-117">-DefaultProfile</span></span>
<span data-ttu-id="75a42-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75a42-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75a42-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="75a42-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="75a42-120">指定包含要移除之預設網站之虛擬網路閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="75a42-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="75a42-121">您可以使用 Get-AzVirtualNetworkGateway 並指定閘道的名稱，以建立虛擬閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="75a42-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="75a42-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a42-122">CommonParameters</span></span>
<span data-ttu-id="75a42-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75a42-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a42-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75a42-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a42-125">輸入</span><span class="sxs-lookup"><span data-stu-id="75a42-125">INPUTS</span></span>

### <span data-ttu-id="75a42-126">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="75a42-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="75a42-127">輸出</span><span class="sxs-lookup"><span data-stu-id="75a42-127">OUTPUTS</span></span>

### <span data-ttu-id="75a42-128">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="75a42-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="75a42-129">筆記</span><span class="sxs-lookup"><span data-stu-id="75a42-129">NOTES</span></span>

## <span data-ttu-id="75a42-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="75a42-130">RELATED LINKS</span></span>

[<span data-ttu-id="75a42-131">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="75a42-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="75a42-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="75a42-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)



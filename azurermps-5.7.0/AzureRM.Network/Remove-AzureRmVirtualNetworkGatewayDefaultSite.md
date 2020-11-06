---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 6ea456ca5e8d06c1ff732664127ca2e7a62abb2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454711"
---
# <span data-ttu-id="bd7de-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="bd7de-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="bd7de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd7de-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7de-103">從虛擬網路閘道移除預設網站。</span><span class="sxs-lookup"><span data-stu-id="bd7de-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd7de-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd7de-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd7de-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd7de-105">DESCRIPTION</span></span>
<span data-ttu-id="bd7de-106">**AzureRmVirtualNetworkGatewayDefaultSite** Cmdlet 會從虛擬網路閘道中移除強制隧道預設網站。</span><span class="sxs-lookup"><span data-stu-id="bd7de-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="bd7de-107">強制隧道提供一種將網際網路系結流量從 Azure 虛擬機器重新導向到您的內部部署網路的方式;這可讓您在釋放流量前先檢查並進行審核。</span><span class="sxs-lookup"><span data-stu-id="bd7de-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="bd7de-108">強制隧道是使用虛擬私人網路絡 (VPN) 隧道來執行;這個隧道需要一個預設的網站，即會重新導向所有 Azure 網際網路系結流量的本機閘道。</span><span class="sxs-lookup"><span data-stu-id="bd7de-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="bd7de-109">**移除-AzureRmVirtualNetworkGatewayDefaultSite** 會移除指派給閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="bd7de-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="bd7de-110">如果您這麼做，您將需要使用 Set-AzureRmVirtualNetworkGatewayDefaultSite 來指派新的預設網站，然後才能將閘道用於強制性隧道。</span><span class="sxs-lookup"><span data-stu-id="bd7de-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="bd7de-111">示例</span><span class="sxs-lookup"><span data-stu-id="bd7de-111">EXAMPLES</span></span>

### <span data-ttu-id="bd7de-112">範例1：移除指派給虛擬網路閘道的預設網站</span><span class="sxs-lookup"><span data-stu-id="bd7de-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="bd7de-113">這個範例會移除目前指派給名為 ContosoVirtualGateway 的虛擬網路閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="bd7de-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="bd7de-114">第一個命令使用 **AzureRmVirtualNetworkGateway** 來建立閘道的物件參照;這個物件參照會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bd7de-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="bd7de-115">然後，第二個命令會使用 **移除 AzureRmVirtualNetworkGatewayDefaultSite** 來移除指派給該閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="bd7de-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="bd7de-116">參數</span><span class="sxs-lookup"><span data-stu-id="bd7de-116">PARAMETERS</span></span>

### <span data-ttu-id="bd7de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7de-117">-DefaultProfile</span></span>
<span data-ttu-id="bd7de-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd7de-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd7de-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd7de-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="bd7de-120">指定包含要移除之預設網站之虛擬網路閘道的物件參照。</span><span class="sxs-lookup"><span data-stu-id="bd7de-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="bd7de-121">您可以使用 Get-AzureRmVirtualNetworkGateway 並指定閘道的名稱，以建立虛擬閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="bd7de-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="bd7de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7de-122">CommonParameters</span></span>
<span data-ttu-id="bd7de-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd7de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7de-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd7de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7de-125">輸入</span><span class="sxs-lookup"><span data-stu-id="bd7de-125">INPUTS</span></span>

###  
<span data-ttu-id="bd7de-126">這個 Cmdlet 會接受 PSVirtualNetworkGateway 物件的流水線實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。</span><span class="sxs-lookup"><span data-stu-id="bd7de-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="bd7de-127">輸出</span><span class="sxs-lookup"><span data-stu-id="bd7de-127">OUTPUTS</span></span>

###  
<span data-ttu-id="bd7de-128">這個 Cmdlet 會修改 PSVirtualNetworkGateway 物件的現有實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。</span><span class="sxs-lookup"><span data-stu-id="bd7de-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="bd7de-129">筆記</span><span class="sxs-lookup"><span data-stu-id="bd7de-129">NOTES</span></span>

## <span data-ttu-id="bd7de-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd7de-130">RELATED LINKS</span></span>

[<span data-ttu-id="bd7de-131">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd7de-131">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bd7de-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="bd7de-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)



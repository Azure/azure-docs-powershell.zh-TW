---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: ddf0f6687550e544aa22efbce772c0751a7b810e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915954"
---
# <span data-ttu-id="ee65b-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ee65b-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="ee65b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee65b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee65b-103">從虛擬網路閘道移除預設網站。</span><span class="sxs-lookup"><span data-stu-id="ee65b-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="ee65b-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee65b-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee65b-105">描述</span><span class="sxs-lookup"><span data-stu-id="ee65b-105">DESCRIPTION</span></span>
<span data-ttu-id="ee65b-106">**Remove-AzVirtualNetworkGatewayDefaultSite** Cmdlet 會從虛擬網路閘道移除強制設置預設網站。</span><span class="sxs-lookup"><span data-stu-id="ee65b-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="ee65b-107">強制導向提供一種將受網際網路限制的流量從 Azure 虛擬機器重新導向到內部部署網路的方法;這可讓您在發行之前檢查和稽核流量。</span><span class="sxs-lookup"><span data-stu-id="ee65b-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="ee65b-108">使用虛擬私人網路或 VPN (進行強制) 部署;此管道需要預設網站，即重新導向所有 Azure 網際網路流量的一個本地閘道。</span><span class="sxs-lookup"><span data-stu-id="ee65b-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="ee65b-109">**Remove-AzVirtualNetworkGatewayDefaultSite** 會移除指派給閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="ee65b-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="ee65b-110">如果您這麼做，您必須使用 Set-AzVirtualNetworkGatewayDefaultSite 指派新的預設網站，閘道才能用於強制呼叫。</span><span class="sxs-lookup"><span data-stu-id="ee65b-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="ee65b-111">例子</span><span class="sxs-lookup"><span data-stu-id="ee65b-111">EXAMPLES</span></span>

### <span data-ttu-id="ee65b-112">範例 1：移除指派給虛擬網路閘道的預設網站</span><span class="sxs-lookup"><span data-stu-id="ee65b-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="ee65b-113">此範例會移除目前指派給名為 ContosoVirtualGateway 之虛擬網路閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="ee65b-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ee65b-114">第一個命令 **使用 Get-AzVirtualNetworkGateway** 建立閘道的物件參照;此物件參照會儲存在名為 $Gateway 的$Gateway。</span><span class="sxs-lookup"><span data-stu-id="ee65b-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="ee65b-115">接著，第二個命令會使用 **Remove-AzVirtualNetworkGatewayDefaultSite** 來移除指派給該閘道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="ee65b-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="ee65b-116">參數</span><span class="sxs-lookup"><span data-stu-id="ee65b-116">PARAMETERS</span></span>

### <span data-ttu-id="ee65b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee65b-117">-DefaultProfile</span></span>
<span data-ttu-id="ee65b-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee65b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee65b-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee65b-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ee65b-120">指定虛擬網路閘道的物件參照，其中包含要移除的預設網站。</span><span class="sxs-lookup"><span data-stu-id="ee65b-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="ee65b-121">您可以使用虛擬網路閘道建立物件參照Get-AzVirtualNetworkGateway指定閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee65b-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="ee65b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee65b-122">CommonParameters</span></span>
<span data-ttu-id="ee65b-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee65b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee65b-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ee65b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee65b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ee65b-125">INPUTS</span></span>

### <span data-ttu-id="ee65b-126">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee65b-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ee65b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ee65b-127">OUTPUTS</span></span>

### <span data-ttu-id="ee65b-128">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee65b-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ee65b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ee65b-129">NOTES</span></span>

## <span data-ttu-id="ee65b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee65b-130">RELATED LINKS</span></span>

[<span data-ttu-id="ee65b-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee65b-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ee65b-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ee65b-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)



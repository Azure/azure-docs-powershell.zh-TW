---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448138"
---
# <span data-ttu-id="db4a3-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="db4a3-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="db4a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="db4a3-103">建立路由表的路線。</span><span class="sxs-lookup"><span data-stu-id="db4a3-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db4a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="db4a3-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db4a3-105">說明</span><span class="sxs-lookup"><span data-stu-id="db4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="db4a3-106">**AzureRmRouteConfig** Cmdlet 會建立 Azure 路由表的路由。</span><span class="sxs-lookup"><span data-stu-id="db4a3-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="db4a3-107">示例</span><span class="sxs-lookup"><span data-stu-id="db4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="db4a3-108">範例1：建立路線</span><span class="sxs-lookup"><span data-stu-id="db4a3-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="db4a3-109">第一個命令會建立名為 Route07 的路由，然後將它儲存在 $Route 變數中。</span><span class="sxs-lookup"><span data-stu-id="db4a3-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="db4a3-110">此路由會將資料包轉寄到本機虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="db4a3-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="db4a3-111">第二個命令會顯示路線的屬性。</span><span class="sxs-lookup"><span data-stu-id="db4a3-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="db4a3-112">參數</span><span class="sxs-lookup"><span data-stu-id="db4a3-112">PARAMETERS</span></span>

### <span data-ttu-id="db4a3-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="db4a3-113">-AddressPrefix</span></span>
<span data-ttu-id="db4a3-114">在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。</span><span class="sxs-lookup"><span data-stu-id="db4a3-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="db4a3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="db4a3-115">-Name</span></span>
<span data-ttu-id="db4a3-116">指定路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="db4a3-116">Specifies a name for the route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4a3-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="db4a3-117">-NextHopIpAddress</span></span>
<span data-ttu-id="db4a3-118">指定您新增至 Azurevirtual 網路之虛擬裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="db4a3-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="db4a3-119">此路由會將資料包轉寄到該位址。</span><span class="sxs-lookup"><span data-stu-id="db4a3-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="db4a3-120">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="db4a3-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="db4a3-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="db4a3-121">-NextHopType</span></span>
<span data-ttu-id="db4a3-122">指定此路由轉寄資料包的方式。</span><span class="sxs-lookup"><span data-stu-id="db4a3-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="db4a3-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="db4a3-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db4a3-124">互聯.</span><span class="sxs-lookup"><span data-stu-id="db4a3-124">Internet.</span></span>
<span data-ttu-id="db4a3-125">由 Azure 提供的預設 Internet 閘道。</span><span class="sxs-lookup"><span data-stu-id="db4a3-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="db4a3-126">所有.</span><span class="sxs-lookup"><span data-stu-id="db4a3-126">None.</span></span>
<span data-ttu-id="db4a3-127">如果您指定這個值，路由就不會轉寄資料包。</span><span class="sxs-lookup"><span data-stu-id="db4a3-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="db4a3-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="db4a3-128">VirtualAppliance.</span></span>
<span data-ttu-id="db4a3-129">您新增至 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="db4a3-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="db4a3-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="db4a3-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="db4a3-131">Azure 伺服器對伺服器虛擬私人網路關。</span><span class="sxs-lookup"><span data-stu-id="db4a3-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="db4a3-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="db4a3-132">VnetLocal.</span></span>
<span data-ttu-id="db4a3-133">[本機虛擬網路]。</span><span class="sxs-lookup"><span data-stu-id="db4a3-133">The local virtual network.</span></span>
<span data-ttu-id="db4a3-134">如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。</span><span class="sxs-lookup"><span data-stu-id="db4a3-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4a3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4a3-135">-DefaultProfile</span></span>
<span data-ttu-id="db4a3-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db4a3-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db4a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4a3-137">CommonParameters</span></span>
<span data-ttu-id="db4a3-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db4a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4a3-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db4a3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4a3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="db4a3-140">INPUTS</span></span>

## <span data-ttu-id="db4a3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="db4a3-141">OUTPUTS</span></span>

### <span data-ttu-id="db4a3-142">PSRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="db4a3-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="db4a3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="db4a3-143">NOTES</span></span>

## <span data-ttu-id="db4a3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="db4a3-144">RELATED LINKS</span></span>

[<span data-ttu-id="db4a3-145">附加 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="db4a3-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="db4a3-146">AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="db4a3-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="db4a3-147">移除-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="db4a3-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="db4a3-148">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="db4a3-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)



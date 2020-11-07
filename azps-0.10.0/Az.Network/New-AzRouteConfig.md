---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 1311c229b670af3ffd049f3f13b3460fb0631628
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794244"
---
# <span data-ttu-id="88ad7-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="88ad7-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="88ad7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="88ad7-103">建立路由表的路線。</span><span class="sxs-lookup"><span data-stu-id="88ad7-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="88ad7-104">句法</span><span class="sxs-lookup"><span data-stu-id="88ad7-104">SYNTAX</span></span>

```
New-AzRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88ad7-105">說明</span><span class="sxs-lookup"><span data-stu-id="88ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="88ad7-106">**AzRouteConfig** Cmdlet 會建立 Azure 路由表的路由。</span><span class="sxs-lookup"><span data-stu-id="88ad7-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="88ad7-107">示例</span><span class="sxs-lookup"><span data-stu-id="88ad7-107">EXAMPLES</span></span>

### <span data-ttu-id="88ad7-108">範例1：建立路線</span><span class="sxs-lookup"><span data-stu-id="88ad7-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="88ad7-109">第一個命令會建立名為 Route07 的路由，然後將它儲存在 $Route 變數中。</span><span class="sxs-lookup"><span data-stu-id="88ad7-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="88ad7-110">此路由會將資料包轉寄到本機虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="88ad7-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="88ad7-111">第二個命令會顯示路線的屬性。</span><span class="sxs-lookup"><span data-stu-id="88ad7-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="88ad7-112">參數</span><span class="sxs-lookup"><span data-stu-id="88ad7-112">PARAMETERS</span></span>

### <span data-ttu-id="88ad7-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="88ad7-113">-AddressPrefix</span></span>
<span data-ttu-id="88ad7-114">在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。</span><span class="sxs-lookup"><span data-stu-id="88ad7-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ad7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ad7-115">-DefaultProfile</span></span>
<span data-ttu-id="88ad7-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88ad7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ad7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="88ad7-117">-Name</span></span>
<span data-ttu-id="88ad7-118">指定路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="88ad7-118">Specifies a name for the route.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ad7-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="88ad7-119">-NextHopIpAddress</span></span>
<span data-ttu-id="88ad7-120">指定您新增至 Azurevirtual 網路之虛擬裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="88ad7-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="88ad7-121">此路由會將資料包轉寄到該位址。</span><span class="sxs-lookup"><span data-stu-id="88ad7-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="88ad7-122">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="88ad7-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ad7-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="88ad7-123">-NextHopType</span></span>
<span data-ttu-id="88ad7-124">指定此路由轉寄資料包的方式。</span><span class="sxs-lookup"><span data-stu-id="88ad7-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="88ad7-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="88ad7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88ad7-126">互聯.</span><span class="sxs-lookup"><span data-stu-id="88ad7-126">Internet.</span></span>
<span data-ttu-id="88ad7-127">由 Azure 提供的預設 Internet 閘道。</span><span class="sxs-lookup"><span data-stu-id="88ad7-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="88ad7-128">所有.</span><span class="sxs-lookup"><span data-stu-id="88ad7-128">None.</span></span>
<span data-ttu-id="88ad7-129">如果您指定這個值，路由就不會轉寄資料包。</span><span class="sxs-lookup"><span data-stu-id="88ad7-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="88ad7-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="88ad7-130">VirtualAppliance.</span></span>
<span data-ttu-id="88ad7-131">您新增至 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="88ad7-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="88ad7-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="88ad7-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="88ad7-133">Azure 伺服器對伺服器虛擬私人網路關。</span><span class="sxs-lookup"><span data-stu-id="88ad7-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="88ad7-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="88ad7-134">VnetLocal.</span></span>
<span data-ttu-id="88ad7-135">[本機虛擬網路]。</span><span class="sxs-lookup"><span data-stu-id="88ad7-135">The local virtual network.</span></span>
<span data-ttu-id="88ad7-136">如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。</span><span class="sxs-lookup"><span data-stu-id="88ad7-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ad7-137">-確認</span><span class="sxs-lookup"><span data-stu-id="88ad7-137">-Confirm</span></span>
<span data-ttu-id="88ad7-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88ad7-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ad7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ad7-139">-WhatIf</span></span>
<span data-ttu-id="88ad7-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88ad7-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88ad7-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88ad7-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ad7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ad7-142">CommonParameters</span></span>
<span data-ttu-id="88ad7-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88ad7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ad7-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88ad7-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ad7-145">輸入</span><span class="sxs-lookup"><span data-stu-id="88ad7-145">INPUTS</span></span>

## <span data-ttu-id="88ad7-146">輸出</span><span class="sxs-lookup"><span data-stu-id="88ad7-146">OUTPUTS</span></span>

### <span data-ttu-id="88ad7-147">PSRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="88ad7-147">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="88ad7-148">筆記</span><span class="sxs-lookup"><span data-stu-id="88ad7-148">NOTES</span></span>

## <span data-ttu-id="88ad7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="88ad7-149">RELATED LINKS</span></span>

[<span data-ttu-id="88ad7-150">附加 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="88ad7-150">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="88ad7-151">AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="88ad7-151">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="88ad7-152">移除-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="88ad7-152">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="88ad7-153">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="88ad7-153">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


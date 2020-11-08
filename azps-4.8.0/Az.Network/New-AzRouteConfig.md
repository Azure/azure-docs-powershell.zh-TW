---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 54a12f4485e56b592b2e42d7b9515af595d4b6c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128927"
---
# <span data-ttu-id="bcd44-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bcd44-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="bcd44-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcd44-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd44-103">建立路由表的路線。</span><span class="sxs-lookup"><span data-stu-id="bcd44-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="bcd44-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcd44-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcd44-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcd44-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd44-106">**AzRouteConfig** Cmdlet 會建立 Azure 路由表的路由。</span><span class="sxs-lookup"><span data-stu-id="bcd44-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="bcd44-107">示例</span><span class="sxs-lookup"><span data-stu-id="bcd44-107">EXAMPLES</span></span>

### <span data-ttu-id="bcd44-108">範例1：建立路線</span><span class="sxs-lookup"><span data-stu-id="bcd44-108">Example 1: Create a route</span></span>
```powershell
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

<span data-ttu-id="bcd44-109">第一個命令會建立名為 Route07 的路由，然後將它儲存在 $Route 變數中。</span><span class="sxs-lookup"><span data-stu-id="bcd44-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="bcd44-110">此路由會將資料包轉寄到本機虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="bcd44-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="bcd44-111">第二個命令會顯示路線的屬性。</span><span class="sxs-lookup"><span data-stu-id="bcd44-111">The second command displays the properties of the route.</span></span>

### <span data-ttu-id="bcd44-112">範例2</span><span class="sxs-lookup"><span data-stu-id="bcd44-112">Example 2</span></span>

<span data-ttu-id="bcd44-113">建立路由表的路線。</span><span class="sxs-lookup"><span data-stu-id="bcd44-113">Creates a route for a route table.</span></span> <span data-ttu-id="bcd44-114"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="bcd44-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzRouteConfig -AddressPrefix 10.1.0.0/16 -Name 'Route07' -NextHopIpAddress '12.0.0.5' -NextHopType 'VnetLocal'
```

## <span data-ttu-id="bcd44-115">參數</span><span class="sxs-lookup"><span data-stu-id="bcd44-115">PARAMETERS</span></span>

### <span data-ttu-id="bcd44-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bcd44-116">-AddressPrefix</span></span>
<span data-ttu-id="bcd44-117">在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。</span><span class="sxs-lookup"><span data-stu-id="bcd44-117">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd44-118">-DefaultProfile</span></span>
<span data-ttu-id="bcd44-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcd44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd44-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcd44-120">-Name</span></span>
<span data-ttu-id="bcd44-121">指定路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcd44-121">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="bcd44-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="bcd44-122">-NextHopIpAddress</span></span>
<span data-ttu-id="bcd44-123">指定您新增至 Azurevirtual 網路之虛擬裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bcd44-123">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="bcd44-124">此路由會將資料包轉寄到該位址。</span><span class="sxs-lookup"><span data-stu-id="bcd44-124">This route forwards packets to that address.</span></span>
<span data-ttu-id="bcd44-125">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="bcd44-125">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd44-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="bcd44-126">-NextHopType</span></span>
<span data-ttu-id="bcd44-127">指定此路由轉寄資料包的方式。</span><span class="sxs-lookup"><span data-stu-id="bcd44-127">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="bcd44-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bcd44-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bcd44-129">互聯.</span><span class="sxs-lookup"><span data-stu-id="bcd44-129">Internet.</span></span>
<span data-ttu-id="bcd44-130">由 Azure 提供的預設 Internet 閘道。</span><span class="sxs-lookup"><span data-stu-id="bcd44-130">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="bcd44-131">所有.</span><span class="sxs-lookup"><span data-stu-id="bcd44-131">None.</span></span>
<span data-ttu-id="bcd44-132">如果您指定這個值，路由就不會轉寄資料包。</span><span class="sxs-lookup"><span data-stu-id="bcd44-132">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="bcd44-133">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="bcd44-133">VirtualAppliance.</span></span>
<span data-ttu-id="bcd44-134">您新增至 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="bcd44-134">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="bcd44-135">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="bcd44-135">VirtualNetworkGateway.</span></span>
<span data-ttu-id="bcd44-136">Azure 伺服器對伺服器虛擬私人網路關。</span><span class="sxs-lookup"><span data-stu-id="bcd44-136">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="bcd44-137">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="bcd44-137">VnetLocal.</span></span>
<span data-ttu-id="bcd44-138">[本機虛擬網路]。</span><span class="sxs-lookup"><span data-stu-id="bcd44-138">The local virtual network.</span></span>
<span data-ttu-id="bcd44-139">如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。</span><span class="sxs-lookup"><span data-stu-id="bcd44-139">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd44-140">-確認</span><span class="sxs-lookup"><span data-stu-id="bcd44-140">-Confirm</span></span>
<span data-ttu-id="bcd44-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bcd44-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcd44-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd44-142">-WhatIf</span></span>
<span data-ttu-id="bcd44-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcd44-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcd44-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcd44-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcd44-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd44-145">CommonParameters</span></span>
<span data-ttu-id="bcd44-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcd44-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd44-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcd44-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd44-148">輸入</span><span class="sxs-lookup"><span data-stu-id="bcd44-148">INPUTS</span></span>

### <span data-ttu-id="bcd44-149">System.object</span><span class="sxs-lookup"><span data-stu-id="bcd44-149">System.String</span></span>

## <span data-ttu-id="bcd44-150">輸出</span><span class="sxs-lookup"><span data-stu-id="bcd44-150">OUTPUTS</span></span>

### <span data-ttu-id="bcd44-151">PSRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bcd44-151">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="bcd44-152">筆記</span><span class="sxs-lookup"><span data-stu-id="bcd44-152">NOTES</span></span>

## <span data-ttu-id="bcd44-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcd44-153">RELATED LINKS</span></span>

[<span data-ttu-id="bcd44-154">附加 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bcd44-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="bcd44-155">AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bcd44-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="bcd44-156">移除-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bcd44-156">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="bcd44-157">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bcd44-157">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ca7335abfd8fe2dc9591dcb7d96fb6ca71dda4fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126360"
---
# <span data-ttu-id="c6599-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c6599-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="c6599-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6599-102">SYNOPSIS</span></span>
<span data-ttu-id="c6599-103">更新路由表的路線設定。</span><span class="sxs-lookup"><span data-stu-id="c6599-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="c6599-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6599-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6599-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6599-105">DESCRIPTION</span></span>
<span data-ttu-id="c6599-106">**AzRouteConfig** Cmdlet 會更新路由表的路由設定。</span><span class="sxs-lookup"><span data-stu-id="c6599-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="c6599-107">示例</span><span class="sxs-lookup"><span data-stu-id="c6599-107">EXAMPLES</span></span>

### <span data-ttu-id="c6599-108">範例1：修改路線</span><span class="sxs-lookup"><span data-stu-id="c6599-108">Example 1: Modify a route</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="c6599-109">這個命令會透過使用 Get-AzRouteTable Cmdlet 來取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="c6599-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="c6599-110">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6599-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c6599-111">目前的 Cmdlet 會修改名為 Route02 的路由，然後將結果傳遞到 **AzRouteTable** Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="c6599-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="c6599-112">參數</span><span class="sxs-lookup"><span data-stu-id="c6599-112">PARAMETERS</span></span>

### <span data-ttu-id="c6599-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c6599-113">-AddressPrefix</span></span>
<span data-ttu-id="c6599-114">在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。</span><span class="sxs-lookup"><span data-stu-id="c6599-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="c6599-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6599-115">-DefaultProfile</span></span>
<span data-ttu-id="c6599-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6599-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6599-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6599-117">-Name</span></span>
<span data-ttu-id="c6599-118">指定此 Cmdlet 所修改之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6599-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c6599-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="c6599-119">-NextHopIpAddress</span></span>
<span data-ttu-id="c6599-120">指定您新增至 Azure 虛擬網路的虛擬裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c6599-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="c6599-121">此路由會將資料包轉寄到該位址。</span><span class="sxs-lookup"><span data-stu-id="c6599-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="c6599-122">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="c6599-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="c6599-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="c6599-123">-NextHopType</span></span>
<span data-ttu-id="c6599-124">指定此路由轉寄資料包的方式。</span><span class="sxs-lookup"><span data-stu-id="c6599-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="c6599-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c6599-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6599-126">互聯.</span><span class="sxs-lookup"><span data-stu-id="c6599-126">Internet.</span></span>
<span data-ttu-id="c6599-127">由 Azure 提供的預設 Internet 閘道。</span><span class="sxs-lookup"><span data-stu-id="c6599-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="c6599-128">所有.</span><span class="sxs-lookup"><span data-stu-id="c6599-128">None.</span></span>
<span data-ttu-id="c6599-129">如果您指定這個值，路由就不會轉寄資料包。</span><span class="sxs-lookup"><span data-stu-id="c6599-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="c6599-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="c6599-130">VirtualAppliance.</span></span>
<span data-ttu-id="c6599-131">您新增至 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="c6599-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="c6599-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c6599-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="c6599-133">Azureserver 到伺服器虛擬私人網路關。</span><span class="sxs-lookup"><span data-stu-id="c6599-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="c6599-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="c6599-134">VnetLocal.</span></span>
<span data-ttu-id="c6599-135">[本機虛擬網路]。</span><span class="sxs-lookup"><span data-stu-id="c6599-135">The local virtual network.</span></span>
<span data-ttu-id="c6599-136">如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。</span><span class="sxs-lookup"><span data-stu-id="c6599-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="c6599-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c6599-137">-RouteTable</span></span>
<span data-ttu-id="c6599-138">指定與此路線相關聯的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="c6599-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6599-139">-確認</span><span class="sxs-lookup"><span data-stu-id="c6599-139">-Confirm</span></span>
<span data-ttu-id="c6599-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6599-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6599-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6599-141">-WhatIf</span></span>
<span data-ttu-id="c6599-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6599-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6599-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6599-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6599-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6599-144">CommonParameters</span></span>
<span data-ttu-id="c6599-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6599-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6599-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6599-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6599-147">輸入</span><span class="sxs-lookup"><span data-stu-id="c6599-147">INPUTS</span></span>

### <span data-ttu-id="c6599-148">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c6599-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="c6599-149">System.object</span><span class="sxs-lookup"><span data-stu-id="c6599-149">System.String</span></span>

## <span data-ttu-id="c6599-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c6599-150">OUTPUTS</span></span>

### <span data-ttu-id="c6599-151">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c6599-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c6599-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c6599-152">NOTES</span></span>

## <span data-ttu-id="c6599-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6599-153">RELATED LINKS</span></span>

[<span data-ttu-id="c6599-154">附加 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c6599-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="c6599-155">AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c6599-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="c6599-156">新-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c6599-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="c6599-157">移除-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c6599-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


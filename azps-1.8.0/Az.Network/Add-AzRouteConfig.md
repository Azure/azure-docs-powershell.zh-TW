---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 567796aaca3ac9d932319211f2b8ad1abbfdf161
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622141"
---
# <span data-ttu-id="6511c-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6511c-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="6511c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6511c-102">SYNOPSIS</span></span>
<span data-ttu-id="6511c-103">新增路由至路由表。</span><span class="sxs-lookup"><span data-stu-id="6511c-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="6511c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6511c-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6511c-105">說明</span><span class="sxs-lookup"><span data-stu-id="6511c-105">DESCRIPTION</span></span>
<span data-ttu-id="6511c-106">**AzRouteConfig** Cmdlet 會將路由新增到 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="6511c-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="6511c-107">示例</span><span class="sxs-lookup"><span data-stu-id="6511c-107">EXAMPLES</span></span>

### <span data-ttu-id="6511c-108">範例1：在路由表中新增路由</span><span class="sxs-lookup"><span data-stu-id="6511c-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="6511c-109">第一個命令會使用 Get-AzRouteTable Cmdlet 來取得名為 RouteTable01 的路由表。</span><span class="sxs-lookup"><span data-stu-id="6511c-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="6511c-110">該命令會將資料表儲存在 $RouteTable 變數中。</span><span class="sxs-lookup"><span data-stu-id="6511c-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="6511c-111">第二個命令會將一個名為 Route13 的路由新增到儲存在 $RouteTable 的路由表中。</span><span class="sxs-lookup"><span data-stu-id="6511c-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="6511c-112">此路由會將資料包轉寄到本機虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="6511c-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="6511c-113">範例2：使用管線將路由新增至路由資料表</span><span class="sxs-lookup"><span data-stu-id="6511c-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="6511c-114">這個命令會使用 **AzRouteTable 取得** 名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="6511c-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="6511c-115">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6511c-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6511c-116">目前的 Cmdlet 會新增名為 Route02 的路由，然後將結果傳遞到 **AzRouteTable** Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="6511c-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="6511c-117">參數</span><span class="sxs-lookup"><span data-stu-id="6511c-117">PARAMETERS</span></span>

### <span data-ttu-id="6511c-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6511c-118">-AddressPrefix</span></span>
<span data-ttu-id="6511c-119">在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。</span><span class="sxs-lookup"><span data-stu-id="6511c-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="6511c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6511c-120">-DefaultProfile</span></span>
<span data-ttu-id="6511c-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6511c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6511c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6511c-122">-Name</span></span>
<span data-ttu-id="6511c-123">指定要新增至路由資料表的路由名稱。</span><span class="sxs-lookup"><span data-stu-id="6511c-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="6511c-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="6511c-124">-NextHopIpAddress</span></span>
<span data-ttu-id="6511c-125">指定您新增至 Azure 虛擬網路的虛擬裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6511c-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="6511c-126">此路由會將資料包轉寄到該位址。</span><span class="sxs-lookup"><span data-stu-id="6511c-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="6511c-127">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="6511c-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="6511c-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="6511c-128">-NextHopType</span></span>
<span data-ttu-id="6511c-129">指定此路由轉寄資料包的方式。</span><span class="sxs-lookup"><span data-stu-id="6511c-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="6511c-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6511c-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6511c-131">互聯.</span><span class="sxs-lookup"><span data-stu-id="6511c-131">Internet.</span></span>
<span data-ttu-id="6511c-132">由 Azure 提供的預設 Internet 閘道。</span><span class="sxs-lookup"><span data-stu-id="6511c-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="6511c-133">所有.</span><span class="sxs-lookup"><span data-stu-id="6511c-133">None.</span></span>
<span data-ttu-id="6511c-134">如果您指定這個值，路由就不會轉寄資料包。</span><span class="sxs-lookup"><span data-stu-id="6511c-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="6511c-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="6511c-135">VirtualAppliance.</span></span>
<span data-ttu-id="6511c-136">您新增至 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="6511c-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="6511c-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="6511c-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="6511c-138">Azure 伺服器對伺服器虛擬私人網路關。</span><span class="sxs-lookup"><span data-stu-id="6511c-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="6511c-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="6511c-139">VnetLocal.</span></span>
<span data-ttu-id="6511c-140">[本機虛擬網路]。</span><span class="sxs-lookup"><span data-stu-id="6511c-140">The local virtual network.</span></span>
<span data-ttu-id="6511c-141">如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。</span><span class="sxs-lookup"><span data-stu-id="6511c-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="6511c-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="6511c-142">-RouteTable</span></span>
<span data-ttu-id="6511c-143">指定此 Cmdlet 將路由新增到哪個路由表。</span><span class="sxs-lookup"><span data-stu-id="6511c-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="6511c-144">-確認</span><span class="sxs-lookup"><span data-stu-id="6511c-144">-Confirm</span></span>
<span data-ttu-id="6511c-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6511c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6511c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6511c-146">-WhatIf</span></span>
<span data-ttu-id="6511c-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6511c-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6511c-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6511c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6511c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6511c-149">CommonParameters</span></span>
<span data-ttu-id="6511c-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6511c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6511c-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6511c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6511c-152">輸入</span><span class="sxs-lookup"><span data-stu-id="6511c-152">INPUTS</span></span>

### <span data-ttu-id="6511c-153">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6511c-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="6511c-154">System.object</span><span class="sxs-lookup"><span data-stu-id="6511c-154">System.String</span></span>

## <span data-ttu-id="6511c-155">輸出</span><span class="sxs-lookup"><span data-stu-id="6511c-155">OUTPUTS</span></span>

### <span data-ttu-id="6511c-156">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6511c-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="6511c-157">筆記</span><span class="sxs-lookup"><span data-stu-id="6511c-157">NOTES</span></span>

## <span data-ttu-id="6511c-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="6511c-158">RELATED LINKS</span></span>

[<span data-ttu-id="6511c-159">AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6511c-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="6511c-160">AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="6511c-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="6511c-161">新-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6511c-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="6511c-162">移除-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6511c-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="6511c-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6511c-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="6511c-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="6511c-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)



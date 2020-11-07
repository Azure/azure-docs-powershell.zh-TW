---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 10018ad3a58de005ecf5798aafaa610c4899d4d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626387"
---
# <span data-ttu-id="c2ea9-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c2ea9-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="c2ea9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ea9-103">新增路由至路由表。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2ea9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2ea9-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>]
 [-NextHopType <String>] [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ea9-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ea9-106">**AzureRmRouteConfig** Cmdlet 會將路由新增到 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="c2ea9-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2ea9-107">EXAMPLES</span></span>

### <span data-ttu-id="c2ea9-108">範例1：在路由表中新增路由</span><span class="sxs-lookup"><span data-stu-id="c2ea9-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="c2ea9-109">第一個命令會使用 Get-AzureRmRouteTable Cmdlet 來取得名為 RouteTable01 的路由表。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="c2ea9-110">該命令會將資料表儲存在 $RouteTable 變數中。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="c2ea9-111">第二個命令會將一個名為 Route13 的路由新增到儲存在 $RouteTable 的路由表中。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="c2ea9-112">此路由會將資料包轉寄到本機虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="c2ea9-113">範例2：使用管線將路由新增至路由資料表</span><span class="sxs-lookup"><span data-stu-id="c2ea9-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="c2ea9-114">這個命令會使用 **AzureRmRouteTable 取得** 名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="c2ea9-115">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c2ea9-116">目前的 Cmdlet 會新增名為 Route02 的路由，然後將結果傳遞到 **AzureRmRouteTable** Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="c2ea9-117">參數</span><span class="sxs-lookup"><span data-stu-id="c2ea9-117">PARAMETERS</span></span>

### <span data-ttu-id="c2ea9-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c2ea9-118">-AddressPrefix</span></span>
<span data-ttu-id="c2ea9-119">在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="c2ea9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ea9-120">-DefaultProfile</span></span>
<span data-ttu-id="c2ea9-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2ea9-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2ea9-122">-Name</span></span>
<span data-ttu-id="c2ea9-123">指定要新增至路由資料表的路由名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="c2ea9-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2ea9-124">-NextHopIpAddress</span></span>
<span data-ttu-id="c2ea9-125">指定您新增至 Azure 虛擬網路的虛擬裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="c2ea9-126">此路由會將資料包轉寄到該位址。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="c2ea9-127">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="c2ea9-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="c2ea9-128">-NextHopType</span></span>
<span data-ttu-id="c2ea9-129">指定此路由轉寄資料包的方式。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="c2ea9-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c2ea9-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2ea9-131">互聯.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-131">Internet.</span></span>
<span data-ttu-id="c2ea9-132">由 Azure 提供的預設 Internet 閘道。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="c2ea9-133">所有.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-133">None.</span></span>
<span data-ttu-id="c2ea9-134">如果您指定這個值，路由就不會轉寄資料包。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="c2ea9-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-135">VirtualAppliance.</span></span>
<span data-ttu-id="c2ea9-136">您新增至 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="c2ea9-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="c2ea9-138">Azure 伺服器對伺服器虛擬私人網路關。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="c2ea9-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="c2ea9-139">VnetLocal.</span></span>
<span data-ttu-id="c2ea9-140">[本機虛擬網路]。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-140">The local virtual network.</span></span>
<span data-ttu-id="c2ea9-141">如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="c2ea9-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c2ea9-142">-RouteTable</span></span>
<span data-ttu-id="c2ea9-143">指定此 Cmdlet 將路由新增到哪個路由表。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="c2ea9-144">-確認</span><span class="sxs-lookup"><span data-stu-id="c2ea9-144">-Confirm</span></span>
<span data-ttu-id="c2ea9-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ea9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ea9-146">-WhatIf</span></span>
<span data-ttu-id="c2ea9-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2ea9-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ea9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ea9-149">CommonParameters</span></span>
<span data-ttu-id="c2ea9-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ea9-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2ea9-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ea9-152">輸入</span><span class="sxs-lookup"><span data-stu-id="c2ea9-152">INPUTS</span></span>

### <span data-ttu-id="c2ea9-153">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2ea9-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="c2ea9-154">System.object</span><span class="sxs-lookup"><span data-stu-id="c2ea9-154">System.String</span></span>

## <span data-ttu-id="c2ea9-155">輸出</span><span class="sxs-lookup"><span data-stu-id="c2ea9-155">OUTPUTS</span></span>

### <span data-ttu-id="c2ea9-156">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2ea9-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c2ea9-157">筆記</span><span class="sxs-lookup"><span data-stu-id="c2ea9-157">NOTES</span></span>

## <span data-ttu-id="c2ea9-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2ea9-158">RELATED LINKS</span></span>

[<span data-ttu-id="c2ea9-159">AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c2ea9-159">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="c2ea9-160">AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c2ea9-160">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="c2ea9-161">新-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c2ea9-161">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="c2ea9-162">移除-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c2ea9-162">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="c2ea9-163">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c2ea9-163">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="c2ea9-164">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c2ea9-164">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)



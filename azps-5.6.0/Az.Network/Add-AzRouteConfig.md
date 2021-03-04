---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 8b0e50bfd335fd8efecef44d4f40e540da8afe09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907097"
---
# <span data-ttu-id="196f4-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="196f4-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="196f4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="196f4-102">SYNOPSIS</span></span>
<span data-ttu-id="196f4-103">新增路由至路由資料表。</span><span class="sxs-lookup"><span data-stu-id="196f4-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="196f4-104">語法</span><span class="sxs-lookup"><span data-stu-id="196f4-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="196f4-105">描述</span><span class="sxs-lookup"><span data-stu-id="196f4-105">DESCRIPTION</span></span>
<span data-ttu-id="196f4-106">**Add-AzRouteConfig** Cmdlet 會新增路由至 Azure 路由資料表。</span><span class="sxs-lookup"><span data-stu-id="196f4-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="196f4-107">例子</span><span class="sxs-lookup"><span data-stu-id="196f4-107">EXAMPLES</span></span>

### <span data-ttu-id="196f4-108">範例 1：新增路由至路由資料表</span><span class="sxs-lookup"><span data-stu-id="196f4-108">Example 1: Add a route to a route table</span></span>
```powershell
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="196f4-109">第一個命令會使用 Get-AzRouteTable Cmdlet，獲得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="196f4-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="196f4-110">命令會儲存資料表$RouteTable變數。</span><span class="sxs-lookup"><span data-stu-id="196f4-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="196f4-111">第二個命令會將名為 Route13 的路由新增到儲存在 $RouteTable 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="196f4-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="196f4-112">此路由會轉送封包到本地虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="196f4-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="196f4-113">範例 2：使用管線新增路由至路由資料表</span><span class="sxs-lookup"><span data-stu-id="196f4-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```powershell
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

<span data-ttu-id="196f4-114">此命令會使用 **Get-AzRouteTable** 取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="196f4-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="196f4-115">該命令會使用管線運算子，將表格傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="196f4-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="196f4-116">目前的 Cmdlet 會新增名為 Route02 的路由，然後將結果傳遞至 **Set-AzRouteTable** Cmdlet，此 Cmdlet 會更新資料表以反映您的變更。</span><span class="sxs-lookup"><span data-stu-id="196f4-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="196f4-117">參數</span><span class="sxs-lookup"><span data-stu-id="196f4-117">PARAMETERS</span></span>

### <span data-ttu-id="196f4-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="196f4-118">-AddressPrefix</span></span>
<span data-ttu-id="196f4-119">以 CIDR 的類別間路由 (CIDR) 指定路由適用的目的地。</span><span class="sxs-lookup"><span data-stu-id="196f4-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="196f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196f4-120">-DefaultProfile</span></span>
<span data-ttu-id="196f4-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="196f4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="196f4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="196f4-122">-Name</span></span>
<span data-ttu-id="196f4-123">指定要新加入路由資料表的路由名稱。</span><span class="sxs-lookup"><span data-stu-id="196f4-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="196f4-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="196f4-124">-NextHopIpAddress</span></span>
<span data-ttu-id="196f4-125">指定您新加入 Azure 虛擬網路之虛擬裝置之 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="196f4-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="196f4-126">此路由會轉送封包至該位址。</span><span class="sxs-lookup"><span data-stu-id="196f4-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="196f4-127">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="196f4-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="196f4-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="196f4-128">-NextHopType</span></span>
<span data-ttu-id="196f4-129">指定此路由如何轉送封包。</span><span class="sxs-lookup"><span data-stu-id="196f4-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="196f4-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="196f4-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="196f4-131">互聯網。</span><span class="sxs-lookup"><span data-stu-id="196f4-131">Internet.</span></span>
<span data-ttu-id="196f4-132">Azure 提供的預設網際網路閘道。</span><span class="sxs-lookup"><span data-stu-id="196f4-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="196f4-133">沒有。</span><span class="sxs-lookup"><span data-stu-id="196f4-133">None.</span></span>
<span data-ttu-id="196f4-134">如果您指定此值，路由不會轉送封包。</span><span class="sxs-lookup"><span data-stu-id="196f4-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="196f4-135">VirtualAppliance。</span><span class="sxs-lookup"><span data-stu-id="196f4-135">VirtualAppliance.</span></span>
<span data-ttu-id="196f4-136">您新加入 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="196f4-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="196f4-137">VirtualNetworkGateway。</span><span class="sxs-lookup"><span data-stu-id="196f4-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="196f4-138">Azure 伺服器對伺服器虛擬專用網路閘道。</span><span class="sxs-lookup"><span data-stu-id="196f4-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="196f4-139">VnetLocal。</span><span class="sxs-lookup"><span data-stu-id="196f4-139">VnetLocal.</span></span>
<span data-ttu-id="196f4-140">本地虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="196f4-140">The local virtual network.</span></span>
<span data-ttu-id="196f4-141">如果您在同一個虛擬網路中有兩個子網，10.1.0.0/0/16 和 10.2.0.0/16，請選取每個子網的 VnetLocal 值以轉往另一個子網。</span><span class="sxs-lookup"><span data-stu-id="196f4-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="196f4-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="196f4-142">-RouteTable</span></span>
<span data-ttu-id="196f4-143">指定此 Cmdlet 新增路由的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="196f4-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="196f4-144">-確認</span><span class="sxs-lookup"><span data-stu-id="196f4-144">-Confirm</span></span>
<span data-ttu-id="196f4-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="196f4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196f4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196f4-146">-WhatIf</span></span>
<span data-ttu-id="196f4-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="196f4-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="196f4-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="196f4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196f4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196f4-149">CommonParameters</span></span>
<span data-ttu-id="196f4-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="196f4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196f4-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="196f4-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196f4-152">輸入</span><span class="sxs-lookup"><span data-stu-id="196f4-152">INPUTS</span></span>

### <span data-ttu-id="196f4-153">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="196f4-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="196f4-154">System.String</span><span class="sxs-lookup"><span data-stu-id="196f4-154">System.String</span></span>

## <span data-ttu-id="196f4-155">輸出</span><span class="sxs-lookup"><span data-stu-id="196f4-155">OUTPUTS</span></span>

### <span data-ttu-id="196f4-156">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="196f4-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="196f4-157">筆記</span><span class="sxs-lookup"><span data-stu-id="196f4-157">NOTES</span></span>

## <span data-ttu-id="196f4-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="196f4-158">RELATED LINKS</span></span>

[<span data-ttu-id="196f4-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="196f4-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="196f4-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="196f4-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="196f4-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="196f4-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="196f4-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="196f4-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="196f4-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="196f4-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="196f4-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="196f4-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)



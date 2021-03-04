---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: a4cdcbf52dfb20f0282347d5dc1ce9a5aec14da0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911886"
---
# <span data-ttu-id="9107d-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9107d-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="9107d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9107d-102">SYNOPSIS</span></span>
<span data-ttu-id="9107d-103">更新路由資料表的路由組配置。</span><span class="sxs-lookup"><span data-stu-id="9107d-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="9107d-104">語法</span><span class="sxs-lookup"><span data-stu-id="9107d-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9107d-105">描述</span><span class="sxs-lookup"><span data-stu-id="9107d-105">DESCRIPTION</span></span>
<span data-ttu-id="9107d-106">**Set-AzRouteConfig** Cmdlet 會更新路由資料表的路由設定。</span><span class="sxs-lookup"><span data-stu-id="9107d-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="9107d-107">例子</span><span class="sxs-lookup"><span data-stu-id="9107d-107">EXAMPLES</span></span>

### <span data-ttu-id="9107d-108">範例 1：修改路由</span><span class="sxs-lookup"><span data-stu-id="9107d-108">Example 1: Modify a route</span></span>
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

<span data-ttu-id="9107d-109">此命令會使用 Cmdlet 的路由資料表，Get-AzRouteTable路由資料表。</span><span class="sxs-lookup"><span data-stu-id="9107d-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="9107d-110">該命令會使用管線運算子，將表格傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9107d-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9107d-111">目前的 Cmdlet 會修改名為 Route02 的路由，然後將結果傳遞至 **Set-AzRouteTable** Cmdlet，此 Cmdlet 會更新資料表以反映您的變更。</span><span class="sxs-lookup"><span data-stu-id="9107d-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="9107d-112">參數</span><span class="sxs-lookup"><span data-stu-id="9107d-112">PARAMETERS</span></span>

### <span data-ttu-id="9107d-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9107d-113">-AddressPrefix</span></span>
<span data-ttu-id="9107d-114">以 CIDR 的類別間路由 (CIDR) 指定路由適用的目的地。</span><span class="sxs-lookup"><span data-stu-id="9107d-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="9107d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9107d-115">-DefaultProfile</span></span>
<span data-ttu-id="9107d-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9107d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9107d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9107d-117">-Name</span></span>
<span data-ttu-id="9107d-118">指定此 Cmdlet 修改的路由名稱。</span><span class="sxs-lookup"><span data-stu-id="9107d-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9107d-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="9107d-119">-NextHopIpAddress</span></span>
<span data-ttu-id="9107d-120">指定您新加入 Azure 虛擬網路之虛擬裝置之 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9107d-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="9107d-121">此路由會轉送封包至該位址。</span><span class="sxs-lookup"><span data-stu-id="9107d-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="9107d-122">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="9107d-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="9107d-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="9107d-123">-NextHopType</span></span>
<span data-ttu-id="9107d-124">指定此路由如何轉送封包。</span><span class="sxs-lookup"><span data-stu-id="9107d-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="9107d-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9107d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9107d-126">互聯網。</span><span class="sxs-lookup"><span data-stu-id="9107d-126">Internet.</span></span>
<span data-ttu-id="9107d-127">Azure 提供的預設網際網路閘道。</span><span class="sxs-lookup"><span data-stu-id="9107d-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="9107d-128">沒有。</span><span class="sxs-lookup"><span data-stu-id="9107d-128">None.</span></span>
<span data-ttu-id="9107d-129">如果您指定此值，路由不會轉送封包。</span><span class="sxs-lookup"><span data-stu-id="9107d-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="9107d-130">VirtualAppliance。</span><span class="sxs-lookup"><span data-stu-id="9107d-130">VirtualAppliance.</span></span>
<span data-ttu-id="9107d-131">您新加入 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="9107d-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="9107d-132">VirtualNetworkGateway。</span><span class="sxs-lookup"><span data-stu-id="9107d-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="9107d-133">Azureserver-to-server 虛擬專用網路閘道。</span><span class="sxs-lookup"><span data-stu-id="9107d-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="9107d-134">VnetLocal。</span><span class="sxs-lookup"><span data-stu-id="9107d-134">VnetLocal.</span></span>
<span data-ttu-id="9107d-135">本地虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="9107d-135">The local virtual network.</span></span>
<span data-ttu-id="9107d-136">如果您在同一個虛擬網路中有兩個子網，10.1.0.0/0/16 和 10.2.0.0/16，請選取每個子網的 VnetLocal 值以轉往另一個子網。</span><span class="sxs-lookup"><span data-stu-id="9107d-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="9107d-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="9107d-137">-RouteTable</span></span>
<span data-ttu-id="9107d-138">指定與此路由相關聯的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="9107d-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="9107d-139">-確認</span><span class="sxs-lookup"><span data-stu-id="9107d-139">-Confirm</span></span>
<span data-ttu-id="9107d-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9107d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9107d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9107d-141">-WhatIf</span></span>
<span data-ttu-id="9107d-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9107d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9107d-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9107d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9107d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9107d-144">CommonParameters</span></span>
<span data-ttu-id="9107d-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9107d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9107d-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9107d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9107d-147">輸入</span><span class="sxs-lookup"><span data-stu-id="9107d-147">INPUTS</span></span>

### <span data-ttu-id="9107d-148">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9107d-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="9107d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9107d-149">System.String</span></span>

## <span data-ttu-id="9107d-150">輸出</span><span class="sxs-lookup"><span data-stu-id="9107d-150">OUTPUTS</span></span>

### <span data-ttu-id="9107d-151">Microsoft.Azure.Commands.Network.models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9107d-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="9107d-152">筆記</span><span class="sxs-lookup"><span data-stu-id="9107d-152">NOTES</span></span>

## <span data-ttu-id="9107d-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="9107d-153">RELATED LINKS</span></span>

[<span data-ttu-id="9107d-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9107d-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="9107d-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9107d-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="9107d-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9107d-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="9107d-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9107d-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)



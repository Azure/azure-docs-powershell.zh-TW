---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 5aa84098c19595ac1c7d6b33c56dca20d08a475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800714"
---
# <span data-ttu-id="f0741-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f0741-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="f0741-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0741-102">SYNOPSIS</span></span>
<span data-ttu-id="f0741-103">設定路線的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f0741-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0741-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0741-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0741-105">說明</span><span class="sxs-lookup"><span data-stu-id="f0741-105">DESCRIPTION</span></span>
<span data-ttu-id="f0741-106">**AzureRmRouteConfig** Cmdlet 設定 Azure 路由的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f0741-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="f0741-107">示例</span><span class="sxs-lookup"><span data-stu-id="f0741-107">EXAMPLES</span></span>

### <span data-ttu-id="f0741-108">範例1：修改路線</span><span class="sxs-lookup"><span data-stu-id="f0741-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="f0741-109">這個命令會透過使用 Get-AzureRmRouteTable Cmdlet 來取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="f0741-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="f0741-110">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0741-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f0741-111">目前的 Cmdlet 會修改名為 Route02 的路由，然後將結果傳遞到 **AzureRmRouteTable** Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="f0741-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="f0741-112">參數</span><span class="sxs-lookup"><span data-stu-id="f0741-112">PARAMETERS</span></span>

### <span data-ttu-id="f0741-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f0741-113">-AddressPrefix</span></span>
<span data-ttu-id="f0741-114">在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。</span><span class="sxs-lookup"><span data-stu-id="f0741-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="f0741-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0741-115">-DefaultProfile</span></span>
<span data-ttu-id="f0741-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0741-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0741-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0741-117">-Name</span></span>
<span data-ttu-id="f0741-118">指定此 Cmdlet 所修改之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0741-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f0741-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0741-119">-NextHopIpAddress</span></span>
<span data-ttu-id="f0741-120">指定您新增至 Azure 虛擬網路的虛擬裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f0741-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="f0741-121">此路由會將資料包轉寄到該位址。</span><span class="sxs-lookup"><span data-stu-id="f0741-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="f0741-122">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f0741-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="f0741-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="f0741-123">-NextHopType</span></span>
<span data-ttu-id="f0741-124">指定此路由轉寄資料包的方式。</span><span class="sxs-lookup"><span data-stu-id="f0741-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="f0741-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f0741-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f0741-126">互聯.</span><span class="sxs-lookup"><span data-stu-id="f0741-126">Internet.</span></span>
<span data-ttu-id="f0741-127">由 Azure 提供的預設 Internet 閘道。</span><span class="sxs-lookup"><span data-stu-id="f0741-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="f0741-128">所有.</span><span class="sxs-lookup"><span data-stu-id="f0741-128">None.</span></span>
<span data-ttu-id="f0741-129">如果您指定這個值，路由就不會轉寄資料包。</span><span class="sxs-lookup"><span data-stu-id="f0741-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="f0741-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="f0741-130">VirtualAppliance.</span></span>
<span data-ttu-id="f0741-131">您新增至 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="f0741-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="f0741-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="f0741-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="f0741-133">Azureserver 到伺服器虛擬私人網路關。</span><span class="sxs-lookup"><span data-stu-id="f0741-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="f0741-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="f0741-134">VnetLocal.</span></span>
<span data-ttu-id="f0741-135">[本機虛擬網路]。</span><span class="sxs-lookup"><span data-stu-id="f0741-135">The local virtual network.</span></span>
<span data-ttu-id="f0741-136">如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。</span><span class="sxs-lookup"><span data-stu-id="f0741-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="f0741-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f0741-137">-RouteTable</span></span>
<span data-ttu-id="f0741-138">指定與此路線相關聯的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="f0741-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0741-139">-確認</span><span class="sxs-lookup"><span data-stu-id="f0741-139">-Confirm</span></span>
<span data-ttu-id="f0741-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0741-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0741-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0741-141">-WhatIf</span></span>
<span data-ttu-id="f0741-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0741-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0741-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0741-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0741-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0741-144">CommonParameters</span></span>
<span data-ttu-id="f0741-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0741-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0741-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0741-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0741-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f0741-147">INPUTS</span></span>

### <span data-ttu-id="f0741-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f0741-148">PSRouteTable</span></span>
<span data-ttu-id="f0741-149">形參 "RouteTable" 接受管線中 "PSRouteTable" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f0741-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="f0741-150">輸出</span><span class="sxs-lookup"><span data-stu-id="f0741-150">OUTPUTS</span></span>

### <span data-ttu-id="f0741-151">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f0741-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f0741-152">筆記</span><span class="sxs-lookup"><span data-stu-id="f0741-152">NOTES</span></span>

## <span data-ttu-id="f0741-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0741-153">RELATED LINKS</span></span>

[<span data-ttu-id="f0741-154">附加 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f0741-154">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="f0741-155">AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f0741-155">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="f0741-156">新-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f0741-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="f0741-157">移除-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f0741-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)



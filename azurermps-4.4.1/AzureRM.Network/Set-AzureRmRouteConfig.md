---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: a86e5346078bd1a8c9be924cdeac3b94fab907dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448107"
---
# <span data-ttu-id="a251b-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a251b-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="a251b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a251b-102">SYNOPSIS</span></span>
<span data-ttu-id="a251b-103">設定路線的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a251b-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a251b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a251b-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a251b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a251b-105">DESCRIPTION</span></span>
<span data-ttu-id="a251b-106">**AzureRmRouteConfig** Cmdlet 設定 Azure 路由的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a251b-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="a251b-107">示例</span><span class="sxs-lookup"><span data-stu-id="a251b-107">EXAMPLES</span></span>

### <span data-ttu-id="a251b-108">範例1：修改路線</span><span class="sxs-lookup"><span data-stu-id="a251b-108">Example 1: Modify a route</span></span>
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

<span data-ttu-id="a251b-109">這個命令會透過使用 Get-AzureRmRouteTable Cmdlet 來取得名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="a251b-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="a251b-110">命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a251b-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a251b-111">目前的 Cmdlet 會修改名為 Route02 的路由，然後將結果傳遞到 **AzureRmRouteTable** Cmdlet，這會更新資料表以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="a251b-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="a251b-112">參數</span><span class="sxs-lookup"><span data-stu-id="a251b-112">PARAMETERS</span></span>

### <span data-ttu-id="a251b-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a251b-113">-AddressPrefix</span></span>
<span data-ttu-id="a251b-114">在 [無類別域間路由 (CIDR) 格式] 中指定目的地，傳送路線適用的位置。</span><span class="sxs-lookup"><span data-stu-id="a251b-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="a251b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a251b-115">-Name</span></span>
<span data-ttu-id="a251b-116">指定此 Cmdlet 所修改之路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="a251b-116">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a251b-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="a251b-117">-NextHopIpAddress</span></span>
<span data-ttu-id="a251b-118">指定您新增至 Azure 虛擬網路的虛擬裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a251b-118">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="a251b-119">此路由會將資料包轉寄到該位址。</span><span class="sxs-lookup"><span data-stu-id="a251b-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="a251b-120">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="a251b-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="a251b-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="a251b-121">-NextHopType</span></span>
<span data-ttu-id="a251b-122">指定此路由轉寄資料包的方式。</span><span class="sxs-lookup"><span data-stu-id="a251b-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="a251b-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a251b-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a251b-124">互聯.</span><span class="sxs-lookup"><span data-stu-id="a251b-124">Internet.</span></span>
<span data-ttu-id="a251b-125">由 Azure 提供的預設 Internet 閘道。</span><span class="sxs-lookup"><span data-stu-id="a251b-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="a251b-126">所有.</span><span class="sxs-lookup"><span data-stu-id="a251b-126">None.</span></span>
<span data-ttu-id="a251b-127">如果您指定這個值，路由就不會轉寄資料包。</span><span class="sxs-lookup"><span data-stu-id="a251b-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="a251b-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="a251b-128">VirtualAppliance.</span></span>
<span data-ttu-id="a251b-129">您新增至 Azure 虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="a251b-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="a251b-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a251b-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="a251b-131">Azureserver 到伺服器虛擬私人網路關。</span><span class="sxs-lookup"><span data-stu-id="a251b-131">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="a251b-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="a251b-132">VnetLocal.</span></span>
<span data-ttu-id="a251b-133">[本機虛擬網路]。</span><span class="sxs-lookup"><span data-stu-id="a251b-133">The local virtual network.</span></span>
<span data-ttu-id="a251b-134">如果您在同一個虛擬網路中有兩個子網，請 10.1.0.0/16 和 10.2.0.0/16，請針對每個子網選取一個 VnetLocal，將其轉寄到其他子網。</span><span class="sxs-lookup"><span data-stu-id="a251b-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="a251b-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a251b-135">-RouteTable</span></span>
<span data-ttu-id="a251b-136">指定與此路線相關聯的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="a251b-136">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a251b-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a251b-137">-DefaultProfile</span></span>
<span data-ttu-id="a251b-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a251b-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a251b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a251b-139">CommonParameters</span></span>
<span data-ttu-id="a251b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a251b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a251b-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a251b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a251b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a251b-142">INPUTS</span></span>

### <span data-ttu-id="a251b-143">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a251b-143">PSRouteTable</span></span>
<span data-ttu-id="a251b-144">形參 "RouteTable" 接受管線中 "PSRouteTable" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a251b-144">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="a251b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a251b-145">OUTPUTS</span></span>

### <span data-ttu-id="a251b-146">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a251b-146">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a251b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a251b-147">NOTES</span></span>

## <span data-ttu-id="a251b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a251b-148">RELATED LINKS</span></span>

[<span data-ttu-id="a251b-149">附加 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a251b-149">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="a251b-150">AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a251b-150">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="a251b-151">新-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a251b-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="a251b-152">移除-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a251b-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: b67b37f66e9b13c692b10dbdca54230bc1b0a529
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902393"
---
# <span data-ttu-id="19649-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="19649-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="19649-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19649-102">SYNOPSIS</span></span>
<span data-ttu-id="19649-103">建立 RoutingConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="19649-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="19649-104">語法</span><span class="sxs-lookup"><span data-stu-id="19649-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19649-105">描述</span><span class="sxs-lookup"><span data-stu-id="19649-105">DESCRIPTION</span></span>
<span data-ttu-id="19649-106">建立 RoutingConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="19649-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="19649-107">例子</span><span class="sxs-lookup"><span data-stu-id="19649-107">EXAMPLES</span></span>

### <span data-ttu-id="19649-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="19649-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="19649-109">上述命令會建立一個 RoutingConfiguration 物件，然後可以新加入到連接資源中。</span><span class="sxs-lookup"><span data-stu-id="19649-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="19649-110">靜態路由只能與 HubVirtualNetworkConnection 物件一起允許。</span><span class="sxs-lookup"><span data-stu-id="19649-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="19649-111">參數</span><span class="sxs-lookup"><span data-stu-id="19649-111">PARAMETERS</span></span>

### <span data-ttu-id="19649-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19649-112">-DefaultProfile</span></span>
<span data-ttu-id="19649-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="19649-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19649-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="19649-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="19649-115">與此路由群組原則相關聯的中樞路由資料表。</span><span class="sxs-lookup"><span data-stu-id="19649-115">The hub route table associated with this routing configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19649-116">-Id</span><span class="sxs-lookup"><span data-stu-id="19649-116">-Id</span></span>
<span data-ttu-id="19649-117">所有中樞路由資料表的資源識別碼清單，以將路由宣告給傳播資料表屬性。</span><span class="sxs-lookup"><span data-stu-id="19649-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19649-118">-標籤</span><span class="sxs-lookup"><span data-stu-id="19649-118">-Label</span></span>
<span data-ttu-id="19649-119">PropagatedRouteTables 屬性的標籤清單。</span><span class="sxs-lookup"><span data-stu-id="19649-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19649-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="19649-120">-StaticRoute</span></span>
<span data-ttu-id="19649-121">控制從 VirtualHub 路由到虛擬網路連接的路由清單。</span><span class="sxs-lookup"><span data-stu-id="19649-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19649-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19649-122">CommonParameters</span></span>
<span data-ttu-id="19649-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19649-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19649-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19649-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19649-125">輸入</span><span class="sxs-lookup"><span data-stu-id="19649-125">INPUTS</span></span>

### <span data-ttu-id="19649-126">System.String</span><span class="sxs-lookup"><span data-stu-id="19649-126">System.String</span></span>

### <span data-ttu-id="19649-127">Microsoft.Azure.Commands.Network.models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="19649-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="19649-128">輸出</span><span class="sxs-lookup"><span data-stu-id="19649-128">OUTPUTS</span></span>

### <span data-ttu-id="19649-129">Microsoft.Azure.Commands.Network.models.PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="19649-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="19649-130">筆記</span><span class="sxs-lookup"><span data-stu-id="19649-130">NOTES</span></span>

## <span data-ttu-id="19649-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="19649-131">RELATED LINKS</span></span>

[<span data-ttu-id="19649-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="19649-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="19649-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="19649-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="19649-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="19649-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="19649-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="19649-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="19649-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="19649-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="19649-137">New-AzP2s VpnGateway</span><span class="sxs-lookup"><span data-stu-id="19649-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="19649-138">Update-AzP2s VpnGateway</span><span class="sxs-lookup"><span data-stu-id="19649-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="19649-139">New-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="19649-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="19649-140">Update-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="19649-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
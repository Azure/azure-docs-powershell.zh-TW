---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286863"
---
# <span data-ttu-id="25869-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="25869-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="25869-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25869-102">SYNOPSIS</span></span>
<span data-ttu-id="25869-103">建立 RoutingConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="25869-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="25869-104">句法</span><span class="sxs-lookup"><span data-stu-id="25869-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25869-105">說明</span><span class="sxs-lookup"><span data-stu-id="25869-105">DESCRIPTION</span></span>
<span data-ttu-id="25869-106">建立 RoutingConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="25869-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="25869-107">示例</span><span class="sxs-lookup"><span data-stu-id="25869-107">EXAMPLES</span></span>

### <span data-ttu-id="25869-108">範例1</span><span class="sxs-lookup"><span data-stu-id="25869-108">Example 1</span></span>
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

<span data-ttu-id="25869-109">上述命令會建立 RoutingConfiguration 物件，然後可以將該物件新增至連線資源。</span><span class="sxs-lookup"><span data-stu-id="25869-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="25869-110">只允許對 HubVirtualNetworkConnection 物件使用靜態路由。</span><span class="sxs-lookup"><span data-stu-id="25869-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="25869-111">參數</span><span class="sxs-lookup"><span data-stu-id="25869-111">PARAMETERS</span></span>

### <span data-ttu-id="25869-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25869-112">-DefaultProfile</span></span>
<span data-ttu-id="25869-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25869-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25869-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="25869-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="25869-115">與此路由設定相關聯的中心路由表。</span><span class="sxs-lookup"><span data-stu-id="25869-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="25869-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="25869-116">-Id</span></span>
<span data-ttu-id="25869-117">要為 PropagatedRouteTables 屬性宣告路由的所有中心路由資料表的資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="25869-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="25869-118">-標籤</span><span class="sxs-lookup"><span data-stu-id="25869-118">-Label</span></span>
<span data-ttu-id="25869-119">PropagatedRouteTables 屬性的標籤清單。</span><span class="sxs-lookup"><span data-stu-id="25869-119">The list of labels for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="25869-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="25869-120">-StaticRoute</span></span>
<span data-ttu-id="25869-121">控制從 VirtualHub 路由到虛擬網路連線的路由清單。</span><span class="sxs-lookup"><span data-stu-id="25869-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

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

### <span data-ttu-id="25869-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25869-122">CommonParameters</span></span>
<span data-ttu-id="25869-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25869-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25869-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="25869-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25869-125">輸入</span><span class="sxs-lookup"><span data-stu-id="25869-125">INPUTS</span></span>

### <span data-ttu-id="25869-126">System.object</span><span class="sxs-lookup"><span data-stu-id="25869-126">System.String</span></span>

### <span data-ttu-id="25869-127">PSStaticRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="25869-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="25869-128">輸出</span><span class="sxs-lookup"><span data-stu-id="25869-128">OUTPUTS</span></span>

### <span data-ttu-id="25869-129">PSRoutingConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="25869-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="25869-130">筆記</span><span class="sxs-lookup"><span data-stu-id="25869-130">NOTES</span></span>

## <span data-ttu-id="25869-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="25869-131">RELATED LINKS</span></span>

[<span data-ttu-id="25869-132">新-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="25869-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="25869-133">新-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="25869-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="25869-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="25869-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="25869-135">新-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="25869-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="25869-136">更新-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="25869-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="25869-137">新-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25869-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="25869-138">更新-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25869-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="25869-139">新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="25869-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="25869-140">更新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="25869-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
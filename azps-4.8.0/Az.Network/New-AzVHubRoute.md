---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126446"
---
# <span data-ttu-id="da90f-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="da90f-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="da90f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da90f-102">SYNOPSIS</span></span>
<span data-ttu-id="da90f-103">建立 VHubRoute 物件，該物件可以作為參數傳遞到 New-AzVHubRouteTable 命令。</span><span class="sxs-lookup"><span data-stu-id="da90f-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="da90f-104">句法</span><span class="sxs-lookup"><span data-stu-id="da90f-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da90f-105">說明</span><span class="sxs-lookup"><span data-stu-id="da90f-105">DESCRIPTION</span></span>

<span data-ttu-id="da90f-106">建立 VHubRoute 物件。</span><span class="sxs-lookup"><span data-stu-id="da90f-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="da90f-107">示例</span><span class="sxs-lookup"><span data-stu-id="da90f-107">EXAMPLES</span></span>

### <span data-ttu-id="da90f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="da90f-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="da90f-109">上述命令會建立一個 VHubRoute 物件，並以 nextHop 作為指定的防火牆，然後再將它新增到 VHubRouteTable 資源。</span><span class="sxs-lookup"><span data-stu-id="da90f-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="da90f-110">範例2</span><span class="sxs-lookup"><span data-stu-id="da90f-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="da90f-111">上述命令會建立一個 VHubRoute 物件，並以 nextHop 作為指定 hubVnetConnection，然後再將它新增至 VHubRouteTable 資源。</span><span class="sxs-lookup"><span data-stu-id="da90f-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="da90f-112">參數</span><span class="sxs-lookup"><span data-stu-id="da90f-112">PARAMETERS</span></span>

### <span data-ttu-id="da90f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da90f-113">-DefaultProfile</span></span>
<span data-ttu-id="da90f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da90f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da90f-115">-目的地</span><span class="sxs-lookup"><span data-stu-id="da90f-115">-Destination</span></span>
<span data-ttu-id="da90f-116">目的地清單。</span><span class="sxs-lookup"><span data-stu-id="da90f-116">List of Destinations.</span></span>

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

### <span data-ttu-id="da90f-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="da90f-117">-DestinationType</span></span>
<span data-ttu-id="da90f-118">目的地類型。</span><span class="sxs-lookup"><span data-stu-id="da90f-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="da90f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="da90f-119">-Name</span></span>
<span data-ttu-id="da90f-120">路由名稱。</span><span class="sxs-lookup"><span data-stu-id="da90f-120">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da90f-121">-NextHop</span><span class="sxs-lookup"><span data-stu-id="da90f-121">-NextHop</span></span>
<span data-ttu-id="da90f-122">下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="da90f-122">The next hop.</span></span>

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

### <span data-ttu-id="da90f-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="da90f-123">-NextHopType</span></span>
<span data-ttu-id="da90f-124">下一個躍點類型。</span><span class="sxs-lookup"><span data-stu-id="da90f-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="da90f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da90f-125">CommonParameters</span></span>
<span data-ttu-id="da90f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da90f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da90f-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="da90f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da90f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="da90f-128">INPUTS</span></span>

### <span data-ttu-id="da90f-129">System.object</span><span class="sxs-lookup"><span data-stu-id="da90f-129">System.String</span></span>

## <span data-ttu-id="da90f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="da90f-130">OUTPUTS</span></span>

### <span data-ttu-id="da90f-131">PSVHubRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="da90f-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="da90f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="da90f-132">NOTES</span></span>

## <span data-ttu-id="da90f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="da90f-133">RELATED LINKS</span></span>

[<span data-ttu-id="da90f-134">AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="da90f-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="da90f-135">新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="da90f-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="da90f-136">移除-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="da90f-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="da90f-137">更新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="da90f-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
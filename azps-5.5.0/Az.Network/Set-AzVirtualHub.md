---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132426"
---
# <span data-ttu-id="2048e-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2048e-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="2048e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2048e-102">SYNOPSIS</span></span>
<span data-ttu-id="2048e-103">修改虛擬中心以將虛擬中心路由表新增到其中。</span><span class="sxs-lookup"><span data-stu-id="2048e-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="2048e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2048e-104">SYNTAX</span></span>

### <span data-ttu-id="2048e-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="2048e-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2048e-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2048e-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2048e-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="2048e-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2048e-108">說明</span><span class="sxs-lookup"><span data-stu-id="2048e-108">DESCRIPTION</span></span>
<span data-ttu-id="2048e-109">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="2048e-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="2048e-110">示例</span><span class="sxs-lookup"><span data-stu-id="2048e-110">EXAMPLES</span></span>

### <span data-ttu-id="2048e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2048e-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="2048e-112">首先，我們建立一個虛擬中心路由物件，並使用它來建立虛擬中心路由資料表資源。</span><span class="sxs-lookup"><span data-stu-id="2048e-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="2048e-113">然後，使用 [Set-AzVirtualHub] 命令將這個 [路由表] 資源設定為虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="2048e-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="2048e-114">參數</span><span class="sxs-lookup"><span data-stu-id="2048e-114">PARAMETERS</span></span>

### <span data-ttu-id="2048e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2048e-115">-AsJob</span></span>
<span data-ttu-id="2048e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2048e-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2048e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2048e-117">-DefaultProfile</span></span>
<span data-ttu-id="2048e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2048e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2048e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2048e-119">-InputObject</span></span>
<span data-ttu-id="2048e-120">要修改的虛擬中心物件。</span><span class="sxs-lookup"><span data-stu-id="2048e-120">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2048e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2048e-121">-Name</span></span>
<span data-ttu-id="2048e-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2048e-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2048e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2048e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2048e-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2048e-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2048e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2048e-125">-ResourceId</span></span>
<span data-ttu-id="2048e-126">要修改之虛擬中心的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2048e-126">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2048e-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2048e-127">-RouteTable</span></span>
<span data-ttu-id="2048e-128">與此虛擬中樞相關聯的路由表。</span><span class="sxs-lookup"><span data-stu-id="2048e-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2048e-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="2048e-129">-Tag</span></span>
<span data-ttu-id="2048e-130">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="2048e-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2048e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="2048e-131">-Confirm</span></span>
<span data-ttu-id="2048e-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2048e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2048e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2048e-133">-WhatIf</span></span>
<span data-ttu-id="2048e-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2048e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2048e-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2048e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2048e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2048e-136">CommonParameters</span></span>
<span data-ttu-id="2048e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2048e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2048e-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2048e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2048e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2048e-139">INPUTS</span></span>

### <span data-ttu-id="2048e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="2048e-140">System.String</span></span>

### <span data-ttu-id="2048e-141">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2048e-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="2048e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="2048e-142">OUTPUTS</span></span>

### <span data-ttu-id="2048e-143">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2048e-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="2048e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="2048e-144">NOTES</span></span>

## <span data-ttu-id="2048e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="2048e-145">RELATED LINKS</span></span>

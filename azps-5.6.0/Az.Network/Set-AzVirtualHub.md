---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: a23b2ce975a67a87a5edd58b21835e16f812055b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906894"
---
# <span data-ttu-id="077d4-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="077d4-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="077d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="077d4-102">SYNOPSIS</span></span>
<span data-ttu-id="077d4-103">修改虛擬中樞以新增虛擬 HUb 路由資料表至該虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="077d4-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="077d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="077d4-104">SYNTAX</span></span>

### <span data-ttu-id="077d4-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="077d4-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="077d4-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="077d4-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077d4-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="077d4-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="077d4-108">描述</span><span class="sxs-lookup"><span data-stu-id="077d4-108">DESCRIPTION</span></span>
<span data-ttu-id="077d4-109">{{ 填寫描述 }}</span><span class="sxs-lookup"><span data-stu-id="077d4-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="077d4-110">例子</span><span class="sxs-lookup"><span data-stu-id="077d4-110">EXAMPLES</span></span>

### <span data-ttu-id="077d4-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="077d4-111">Example 1</span></span>
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

<span data-ttu-id="077d4-112">首先，我們建立虛擬中樞路由物件，然後使用它來建立虛擬中樞路由資料表資源。</span><span class="sxs-lookup"><span data-stu-id="077d4-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="077d4-113">接著，我們使用命令將路由資料表資源設定為虛擬Set-AzVirtualHub中樞。</span><span class="sxs-lookup"><span data-stu-id="077d4-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="077d4-114">參數</span><span class="sxs-lookup"><span data-stu-id="077d4-114">PARAMETERS</span></span>

### <span data-ttu-id="077d4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="077d4-115">-AsJob</span></span>
<span data-ttu-id="077d4-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="077d4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="077d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077d4-117">-DefaultProfile</span></span>
<span data-ttu-id="077d4-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="077d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="077d4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="077d4-119">-InputObject</span></span>
<span data-ttu-id="077d4-120">要修改的虛擬中樞物件。</span><span class="sxs-lookup"><span data-stu-id="077d4-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="077d4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="077d4-121">-Name</span></span>
<span data-ttu-id="077d4-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="077d4-122">The resource name.</span></span>

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

### <span data-ttu-id="077d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="077d4-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="077d4-124">The resource group name.</span></span>

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

### <span data-ttu-id="077d4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="077d4-125">-ResourceId</span></span>
<span data-ttu-id="077d4-126">要修改的虛擬中樞資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="077d4-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="077d4-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="077d4-127">-RouteTable</span></span>
<span data-ttu-id="077d4-128">與此虛擬中樞相關聯的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="077d4-128">The route tables associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="077d4-129">-標記</span><span class="sxs-lookup"><span data-stu-id="077d4-129">-Tag</span></span>
<span data-ttu-id="077d4-130">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="077d4-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="077d4-131">-確認</span><span class="sxs-lookup"><span data-stu-id="077d4-131">-Confirm</span></span>
<span data-ttu-id="077d4-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="077d4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="077d4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077d4-133">-WhatIf</span></span>
<span data-ttu-id="077d4-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="077d4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="077d4-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="077d4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="077d4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077d4-136">CommonParameters</span></span>
<span data-ttu-id="077d4-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="077d4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077d4-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="077d4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077d4-139">輸入</span><span class="sxs-lookup"><span data-stu-id="077d4-139">INPUTS</span></span>

### <span data-ttu-id="077d4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="077d4-140">System.String</span></span>

### <span data-ttu-id="077d4-141">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="077d4-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="077d4-142">輸出</span><span class="sxs-lookup"><span data-stu-id="077d4-142">OUTPUTS</span></span>

### <span data-ttu-id="077d4-143">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="077d4-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="077d4-144">筆記</span><span class="sxs-lookup"><span data-stu-id="077d4-144">NOTES</span></span>

## <span data-ttu-id="077d4-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="077d4-145">RELATED LINKS</span></span>

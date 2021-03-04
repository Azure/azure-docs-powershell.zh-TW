---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: a7b8e790892b14e053a07f83e6a27c4ce82c00ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910025"
---
# <span data-ttu-id="94f7a-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="94f7a-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="94f7a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="94f7a-103">建立 Azure VirtualHub 資源。</span><span class="sxs-lookup"><span data-stu-id="94f7a-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="94f7a-104">語法</span><span class="sxs-lookup"><span data-stu-id="94f7a-104">SYNTAX</span></span>

### <span data-ttu-id="94f7a-105">ByVirtualWanObject (預設) </span><span class="sxs-lookup"><span data-stu-id="94f7a-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f7a-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="94f7a-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f7a-107">描述</span><span class="sxs-lookup"><span data-stu-id="94f7a-107">DESCRIPTION</span></span>
<span data-ttu-id="94f7a-108">建立 Azure VirtualHub 資源。</span><span class="sxs-lookup"><span data-stu-id="94f7a-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="94f7a-109">例子</span><span class="sxs-lookup"><span data-stu-id="94f7a-109">EXAMPLES</span></span>

### <span data-ttu-id="94f7a-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="94f7a-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="94f7a-111">上述步驟將在 Azure 資源群組中建立資源群組「testRG」、一個虛擬 WAN，以及美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="94f7a-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="94f7a-112">虛擬中樞的位址空間為「10.0.1.0/24」。</span><span class="sxs-lookup"><span data-stu-id="94f7a-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="94f7a-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="94f7a-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="94f7a-114">上述步驟將在 Azure 資源群組中建立資源群組「testRG」、一個虛擬 WAN，以及美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="94f7a-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="94f7a-115">虛擬中樞的位址空間為「10.0.1.0/24」。</span><span class="sxs-lookup"><span data-stu-id="94f7a-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="94f7a-116">此範例與範例 1 類似，但使用資源識別碼來參照建立虛擬中樞所需的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="94f7a-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="94f7a-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="94f7a-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="94f7a-118">上述步驟將在 Azure 資源群組中建立資源群組「testRG」、一個虛擬 WAN，以及美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="94f7a-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="94f7a-119">虛擬中樞會附加位址空間"10.0.1.0/24"和路由資料表。</span><span class="sxs-lookup"><span data-stu-id="94f7a-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="94f7a-120">此範例與範例 2 類似，但也將路由資料表附加到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="94f7a-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="94f7a-121">參數</span><span class="sxs-lookup"><span data-stu-id="94f7a-121">PARAMETERS</span></span>

### <span data-ttu-id="94f7a-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="94f7a-122">-AddressPrefix</span></span>
<span data-ttu-id="94f7a-123">這個虛擬中樞的位址空間字串。</span><span class="sxs-lookup"><span data-stu-id="94f7a-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="94f7a-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94f7a-124">-AsJob</span></span>
<span data-ttu-id="94f7a-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94f7a-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94f7a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f7a-126">-DefaultProfile</span></span>
<span data-ttu-id="94f7a-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94f7a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f7a-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="94f7a-128">-HubVnetConnection</span></span>
<span data-ttu-id="94f7a-129">與此虛擬中樞相關聯的中樞虛擬網路連接。</span><span class="sxs-lookup"><span data-stu-id="94f7a-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f7a-130">-位置</span><span class="sxs-lookup"><span data-stu-id="94f7a-130">-Location</span></span>
<span data-ttu-id="94f7a-131">位置。</span><span class="sxs-lookup"><span data-stu-id="94f7a-131">location.</span></span>

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

### <span data-ttu-id="94f7a-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="94f7a-132">-Name</span></span>
<span data-ttu-id="94f7a-133">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="94f7a-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f7a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f7a-134">-ResourceGroupName</span></span>
<span data-ttu-id="94f7a-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="94f7a-135">The resource group name.</span></span>

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

### <span data-ttu-id="94f7a-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="94f7a-136">-RouteTable</span></span>
<span data-ttu-id="94f7a-137">與此虛擬中樞相關聯的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="94f7a-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f7a-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="94f7a-138">-Sku</span></span>
<span data-ttu-id="94f7a-139">虛擬中樞的 SKU。</span><span class="sxs-lookup"><span data-stu-id="94f7a-139">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="94f7a-140">-標記</span><span class="sxs-lookup"><span data-stu-id="94f7a-140">-Tag</span></span>
<span data-ttu-id="94f7a-141">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="94f7a-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="94f7a-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="94f7a-142">-VirtualWan</span></span>
<span data-ttu-id="94f7a-143">此中樞所連結的虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="94f7a-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7a-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="94f7a-144">-VirtualWanId</span></span>
<span data-ttu-id="94f7a-145">此中樞所連結之虛擬 wan 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="94f7a-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7a-146">-確認</span><span class="sxs-lookup"><span data-stu-id="94f7a-146">-Confirm</span></span>
<span data-ttu-id="94f7a-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="94f7a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f7a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f7a-148">-WhatIf</span></span>
<span data-ttu-id="94f7a-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94f7a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f7a-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f7a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f7a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f7a-151">CommonParameters</span></span>
<span data-ttu-id="94f7a-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94f7a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f7a-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94f7a-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f7a-154">輸入</span><span class="sxs-lookup"><span data-stu-id="94f7a-154">INPUTS</span></span>

### <span data-ttu-id="94f7a-155">Microsoft.Azure.Commands.Network.models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="94f7a-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="94f7a-156">System.String</span><span class="sxs-lookup"><span data-stu-id="94f7a-156">System.String</span></span>

## <span data-ttu-id="94f7a-157">輸出</span><span class="sxs-lookup"><span data-stu-id="94f7a-157">OUTPUTS</span></span>

### <span data-ttu-id="94f7a-158">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="94f7a-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="94f7a-159">筆記</span><span class="sxs-lookup"><span data-stu-id="94f7a-159">NOTES</span></span>

## <span data-ttu-id="94f7a-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="94f7a-160">RELATED LINKS</span></span>

[<span data-ttu-id="94f7a-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="94f7a-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="94f7a-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="94f7a-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="94f7a-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="94f7a-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)

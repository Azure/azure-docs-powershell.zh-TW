---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: 8527b383dd5469d1a9bc34b7916a1e28b3f673f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621718"
---
# <span data-ttu-id="5a73f-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5a73f-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="5a73f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a73f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a73f-103">建立 Azure VirtualHub 資源。</span><span class="sxs-lookup"><span data-stu-id="5a73f-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="5a73f-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a73f-104">SYNTAX</span></span>

### <span data-ttu-id="5a73f-105">ByVirtualWanObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5a73f-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a73f-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="5a73f-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a73f-107">說明</span><span class="sxs-lookup"><span data-stu-id="5a73f-107">DESCRIPTION</span></span>
<span data-ttu-id="5a73f-108">建立 Azure VirtualHub 資源。</span><span class="sxs-lookup"><span data-stu-id="5a73f-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="5a73f-109">示例</span><span class="sxs-lookup"><span data-stu-id="5a73f-109">EXAMPLES</span></span>

### <span data-ttu-id="5a73f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5a73f-110">Example 1</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="5a73f-111">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="5a73f-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="5a73f-112">虛擬中樞會將位址空間 "10.0.1.0/24"。</span><span class="sxs-lookup"><span data-stu-id="5a73f-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="5a73f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5a73f-113">Example 2</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="5a73f-114">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="5a73f-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="5a73f-115">虛擬中樞會將位址空間 "10.0.1.0/24"。</span><span class="sxs-lookup"><span data-stu-id="5a73f-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="5a73f-116">這個範例與範例1類似，但使用資源識別碼來參照建立虛擬中樞所需的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="5a73f-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="5a73f-117">範例3</span><span class="sxs-lookup"><span data-stu-id="5a73f-117">Example 3</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="5a73f-118">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="5a73f-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="5a73f-119">虛擬中樞會將位址空間 "10.0.1.0/24" 和附加路由表。</span><span class="sxs-lookup"><span data-stu-id="5a73f-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="5a73f-120">這個範例與範例2類似，但也會將路由資料表附加至虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="5a73f-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="5a73f-121">參數</span><span class="sxs-lookup"><span data-stu-id="5a73f-121">PARAMETERS</span></span>

### <span data-ttu-id="5a73f-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5a73f-122">-AddressPrefix</span></span>
<span data-ttu-id="5a73f-123">此虛擬中樞的位址空間字串。</span><span class="sxs-lookup"><span data-stu-id="5a73f-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="5a73f-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a73f-124">-AsJob</span></span>
<span data-ttu-id="5a73f-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a73f-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a73f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a73f-126">-DefaultProfile</span></span>
<span data-ttu-id="5a73f-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a73f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a73f-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5a73f-128">-HubVnetConnection</span></span>
<span data-ttu-id="5a73f-129">與此虛擬中樞相關聯的中心虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="5a73f-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a73f-130">-位置</span><span class="sxs-lookup"><span data-stu-id="5a73f-130">-Location</span></span>
<span data-ttu-id="5a73f-131">位於.</span><span class="sxs-lookup"><span data-stu-id="5a73f-131">location.</span></span>

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

### <span data-ttu-id="5a73f-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a73f-132">-Name</span></span>
<span data-ttu-id="5a73f-133">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5a73f-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a73f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a73f-134">-ResourceGroupName</span></span>
<span data-ttu-id="5a73f-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a73f-135">The resource group name.</span></span>

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

### <span data-ttu-id="5a73f-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5a73f-136">-RouteTable</span></span>
<span data-ttu-id="5a73f-137">與此虛擬中樞相關聯的路由表。</span><span class="sxs-lookup"><span data-stu-id="5a73f-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a73f-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a73f-138">-Tag</span></span>
<span data-ttu-id="5a73f-139">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="5a73f-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a73f-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="5a73f-140">-VirtualWan</span></span>
<span data-ttu-id="5a73f-141">此中樞所連結的虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="5a73f-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a73f-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="5a73f-142">-VirtualWanId</span></span>
<span data-ttu-id="5a73f-143">此中樞所連結的虛擬 wan 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a73f-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a73f-144">-確認</span><span class="sxs-lookup"><span data-stu-id="5a73f-144">-Confirm</span></span>
<span data-ttu-id="5a73f-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a73f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a73f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a73f-146">-WhatIf</span></span>
<span data-ttu-id="5a73f-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a73f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a73f-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a73f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a73f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a73f-149">CommonParameters</span></span>
<span data-ttu-id="5a73f-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a73f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a73f-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a73f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a73f-152">輸入</span><span class="sxs-lookup"><span data-stu-id="5a73f-152">INPUTS</span></span>

### <span data-ttu-id="5a73f-153">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a73f-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="5a73f-154">System.object</span><span class="sxs-lookup"><span data-stu-id="5a73f-154">System.String</span></span>

## <span data-ttu-id="5a73f-155">輸出</span><span class="sxs-lookup"><span data-stu-id="5a73f-155">OUTPUTS</span></span>

### <span data-ttu-id="5a73f-156">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a73f-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="5a73f-157">筆記</span><span class="sxs-lookup"><span data-stu-id="5a73f-157">NOTES</span></span>

## <span data-ttu-id="5a73f-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a73f-158">RELATED LINKS</span></span>

[<span data-ttu-id="5a73f-159">AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5a73f-159">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="5a73f-160">移除-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5a73f-160">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="5a73f-161">更新-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5a73f-161">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: 96ba4a6a80e7826b1cf95086f1410305322cf266
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791469"
---
# <span data-ttu-id="272fb-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="272fb-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="272fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="272fb-102">SYNOPSIS</span></span>
<span data-ttu-id="272fb-103">更新虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="272fb-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="272fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="272fb-104">SYNTAX</span></span>

### <span data-ttu-id="272fb-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="272fb-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="272fb-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="272fb-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="272fb-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="272fb-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="272fb-108">說明</span><span class="sxs-lookup"><span data-stu-id="272fb-108">DESCRIPTION</span></span>
<span data-ttu-id="272fb-109">**更新-AzVirtualHub** Cmdlet 會更新虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="272fb-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="272fb-110">示例</span><span class="sxs-lookup"><span data-stu-id="272fb-110">EXAMPLES</span></span>

### <span data-ttu-id="272fb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="272fb-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="272fb-112">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="272fb-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="272fb-113">虛擬中樞會將位址空間 "10.0.1.0/24"。</span><span class="sxs-lookup"><span data-stu-id="272fb-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="272fb-114">範例2</span><span class="sxs-lookup"><span data-stu-id="272fb-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="272fb-115">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="272fb-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="272fb-116">虛擬中樞會將位址空間 "10.0.1.0/24"。</span><span class="sxs-lookup"><span data-stu-id="272fb-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="272fb-117">這個範例與範例1類似，但也會將路由資料表附加至虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="272fb-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="272fb-118">參數</span><span class="sxs-lookup"><span data-stu-id="272fb-118">PARAMETERS</span></span>

### <span data-ttu-id="272fb-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="272fb-119">-AddressPrefix</span></span>
<span data-ttu-id="272fb-120">此虛擬中樞的位址空間字串。</span><span class="sxs-lookup"><span data-stu-id="272fb-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="272fb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="272fb-121">-AsJob</span></span>
<span data-ttu-id="272fb-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="272fb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="272fb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272fb-123">-DefaultProfile</span></span>
<span data-ttu-id="272fb-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="272fb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="272fb-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="272fb-125">-HubVnetConnection</span></span>
<span data-ttu-id="272fb-126">與此虛擬中樞相關聯的中心虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="272fb-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="272fb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="272fb-127">-InputObject</span></span>
<span data-ttu-id="272fb-128">要修改的虛擬中心物件。</span><span class="sxs-lookup"><span data-stu-id="272fb-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="272fb-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="272fb-129">-Name</span></span>
<span data-ttu-id="272fb-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="272fb-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272fb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272fb-131">-ResourceGroupName</span></span>
<span data-ttu-id="272fb-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="272fb-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272fb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="272fb-133">-ResourceId</span></span>
<span data-ttu-id="272fb-134">要修改之虛擬中心的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="272fb-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272fb-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="272fb-135">-RouteTable</span></span>
<span data-ttu-id="272fb-136">與此虛擬中樞相關聯的路由表。</span><span class="sxs-lookup"><span data-stu-id="272fb-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="272fb-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="272fb-137">-Tag</span></span>
<span data-ttu-id="272fb-138">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="272fb-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="272fb-139">-確認</span><span class="sxs-lookup"><span data-stu-id="272fb-139">-Confirm</span></span>
<span data-ttu-id="272fb-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="272fb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="272fb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="272fb-141">-WhatIf</span></span>
<span data-ttu-id="272fb-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="272fb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="272fb-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="272fb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="272fb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272fb-144">CommonParameters</span></span>
<span data-ttu-id="272fb-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="272fb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272fb-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="272fb-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272fb-147">輸入</span><span class="sxs-lookup"><span data-stu-id="272fb-147">INPUTS</span></span>

### <span data-ttu-id="272fb-148">System.object</span><span class="sxs-lookup"><span data-stu-id="272fb-148">System.String</span></span>

### <span data-ttu-id="272fb-149">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="272fb-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="272fb-150">輸出</span><span class="sxs-lookup"><span data-stu-id="272fb-150">OUTPUTS</span></span>

### <span data-ttu-id="272fb-151">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="272fb-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="272fb-152">筆記</span><span class="sxs-lookup"><span data-stu-id="272fb-152">NOTES</span></span>

## <span data-ttu-id="272fb-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="272fb-153">RELATED LINKS</span></span>

[<span data-ttu-id="272fb-154">AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="272fb-154">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="272fb-155">新-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="272fb-155">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="272fb-156">移除-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="272fb-156">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

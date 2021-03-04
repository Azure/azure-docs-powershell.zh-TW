---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: df81d3df31ad1d04914164d04321151e0df2dfdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907614"
---
# <span data-ttu-id="905b5-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="905b5-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="905b5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="905b5-102">SYNOPSIS</span></span>
<span data-ttu-id="905b5-103">建立可縮放的 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="905b5-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="905b5-104">語法</span><span class="sxs-lookup"><span data-stu-id="905b5-104">SYNTAX</span></span>

### <span data-ttu-id="905b5-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="905b5-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905b5-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="905b5-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905b5-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="905b5-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="905b5-108">描述</span><span class="sxs-lookup"><span data-stu-id="905b5-108">DESCRIPTION</span></span>

<span data-ttu-id="905b5-109">New-AzExpressRouteGateway建立可縮放的 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="905b5-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="905b5-110">這是針對 VirtualHub 內部部署至 Azure 的軟體定義連接。</span><span class="sxs-lookup"><span data-stu-id="905b5-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="905b5-111">此閘道可以依據在此或 Cmdlet 中指定的縮放比例Set-AzExpressRouteGateway縮放。</span><span class="sxs-lookup"><span data-stu-id="905b5-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="905b5-112">從內部部署 ExpressRoute 回路設定到可縮放閘道的連接。</span><span class="sxs-lookup"><span data-stu-id="905b5-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="905b5-113">ExpressRouteGateway 會位於與參照的 VirtualHub 相同的位置。</span><span class="sxs-lookup"><span data-stu-id="905b5-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="905b5-114">例子</span><span class="sxs-lookup"><span data-stu-id="905b5-114">EXAMPLES</span></span>

### <span data-ttu-id="905b5-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="905b5-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="905b5-116">上述步驟將在 Azure 的 「testRG」資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="905b5-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="905b5-117">在此之後，將會以 2 個縮放單位在虛擬中心中建立 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="905b5-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="905b5-118">參數</span><span class="sxs-lookup"><span data-stu-id="905b5-118">PARAMETERS</span></span>

### <span data-ttu-id="905b5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="905b5-119">-AsJob</span></span>
<span data-ttu-id="905b5-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="905b5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="905b5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905b5-121">-DefaultProfile</span></span>
<span data-ttu-id="905b5-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="905b5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="905b5-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="905b5-123">-MaxScaleUnits</span></span>
<span data-ttu-id="905b5-124">此 ExpressRouteGateway 的縮放單位上限。</span><span class="sxs-lookup"><span data-stu-id="905b5-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="905b5-125">有效範圍 > 2</span><span class="sxs-lookup"><span data-stu-id="905b5-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905b5-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="905b5-126">-MinScaleUnits</span></span>
<span data-ttu-id="905b5-127">此 ExpressRouteGateway 的最小刻度單位數目。</span><span class="sxs-lookup"><span data-stu-id="905b5-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="905b5-128">有效範圍 > 2</span><span class="sxs-lookup"><span data-stu-id="905b5-128">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905b5-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="905b5-129">-Name</span></span>
<span data-ttu-id="905b5-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="905b5-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905b5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905b5-131">-ResourceGroupName</span></span>
<span data-ttu-id="905b5-132">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="905b5-132">The resource name.</span></span>

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

### <span data-ttu-id="905b5-133">-標記</span><span class="sxs-lookup"><span data-stu-id="905b5-133">-Tag</span></span>
<span data-ttu-id="905b5-134">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="905b5-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="905b5-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="905b5-135">-VirtualHub</span></span>
<span data-ttu-id="905b5-136">這個 VpnGateway 的 VirtualHub 需要關聯。</span><span class="sxs-lookup"><span data-stu-id="905b5-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="905b5-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="905b5-137">-VirtualHubId</span></span>
<span data-ttu-id="905b5-138">這個 VpnGateway 的 VirtualHub 識別碼必須相關聯。</span><span class="sxs-lookup"><span data-stu-id="905b5-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="905b5-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="905b5-139">-VirtualHubName</span></span>
<span data-ttu-id="905b5-140">這個 VpnGateway 的 VirtualHub 識別碼必須相關聯。</span><span class="sxs-lookup"><span data-stu-id="905b5-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="905b5-141">-確認</span><span class="sxs-lookup"><span data-stu-id="905b5-141">-Confirm</span></span>
<span data-ttu-id="905b5-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="905b5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="905b5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="905b5-143">-WhatIf</span></span>
<span data-ttu-id="905b5-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="905b5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="905b5-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="905b5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="905b5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905b5-146">CommonParameters</span></span>
<span data-ttu-id="905b5-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="905b5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905b5-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="905b5-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905b5-149">輸入</span><span class="sxs-lookup"><span data-stu-id="905b5-149">INPUTS</span></span>

### <span data-ttu-id="905b5-150">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="905b5-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="905b5-151">System.String</span><span class="sxs-lookup"><span data-stu-id="905b5-151">System.String</span></span>

## <span data-ttu-id="905b5-152">輸出</span><span class="sxs-lookup"><span data-stu-id="905b5-152">OUTPUTS</span></span>

### <span data-ttu-id="905b5-153">Microsoft.Azure.Commands.Network.models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="905b5-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="905b5-154">筆記</span><span class="sxs-lookup"><span data-stu-id="905b5-154">NOTES</span></span>

## <span data-ttu-id="905b5-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="905b5-155">RELATED LINKS</span></span>

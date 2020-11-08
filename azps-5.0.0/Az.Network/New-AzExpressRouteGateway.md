---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141108"
---
# <span data-ttu-id="8c50e-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="8c50e-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="8c50e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c50e-102">SYNOPSIS</span></span>
<span data-ttu-id="8c50e-103">建立可伸縮的 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="8c50e-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="8c50e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c50e-104">SYNTAX</span></span>

### <span data-ttu-id="8c50e-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="8c50e-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c50e-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="8c50e-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c50e-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8c50e-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c50e-108">說明</span><span class="sxs-lookup"><span data-stu-id="8c50e-108">DESCRIPTION</span></span>

<span data-ttu-id="8c50e-109">New-AzExpressRouteGateway 建立可伸縮的 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="8c50e-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="8c50e-110">這是 VirtualHub 中的 Azure 內部部署的軟體定義連線。</span><span class="sxs-lookup"><span data-stu-id="8c50e-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="8c50e-111">此閘道可以根據在此或 Set-AzExpressRouteGateway Cmdlet 中指定的縮放單位來調整。</span><span class="sxs-lookup"><span data-stu-id="8c50e-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="8c50e-112">連線是從內部部署的 ExpressRoute 電路設定到可伸縮閘道。</span><span class="sxs-lookup"><span data-stu-id="8c50e-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="8c50e-113">ExpressRouteGateway 將會位於與參照 VirtualHub 相同的位置。</span><span class="sxs-lookup"><span data-stu-id="8c50e-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="8c50e-114">示例</span><span class="sxs-lookup"><span data-stu-id="8c50e-114">EXAMPLES</span></span>

### <span data-ttu-id="8c50e-115">範例1</span><span class="sxs-lookup"><span data-stu-id="8c50e-115">Example 1</span></span>

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

<span data-ttu-id="8c50e-116">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="8c50e-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8c50e-117">隨後便會在具有2個比例單位的虛擬中樞中建立 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="8c50e-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="8c50e-118">參數</span><span class="sxs-lookup"><span data-stu-id="8c50e-118">PARAMETERS</span></span>

### <span data-ttu-id="8c50e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c50e-119">-AsJob</span></span>
<span data-ttu-id="8c50e-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c50e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c50e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c50e-121">-DefaultProfile</span></span>
<span data-ttu-id="8c50e-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c50e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c50e-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="8c50e-123">-MaxScaleUnits</span></span>
<span data-ttu-id="8c50e-124">此 ExpressRouteGateway 的縮放單位數上限。</span><span class="sxs-lookup"><span data-stu-id="8c50e-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="8c50e-125">有效範圍 > 2</span><span class="sxs-lookup"><span data-stu-id="8c50e-125">Valid range > 2</span></span>

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

### <span data-ttu-id="8c50e-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="8c50e-126">-MinScaleUnits</span></span>
<span data-ttu-id="8c50e-127">此 ExpressRouteGateway 的最小縮放單位數。</span><span class="sxs-lookup"><span data-stu-id="8c50e-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="8c50e-128">有效範圍 > 2</span><span class="sxs-lookup"><span data-stu-id="8c50e-128">Valid range > 2</span></span>

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

### <span data-ttu-id="8c50e-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c50e-129">-Name</span></span>
<span data-ttu-id="8c50e-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8c50e-130">The resource name.</span></span>

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

### <span data-ttu-id="8c50e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c50e-131">-ResourceGroupName</span></span>
<span data-ttu-id="8c50e-132">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8c50e-132">The resource name.</span></span>

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

### <span data-ttu-id="8c50e-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c50e-133">-Tag</span></span>
<span data-ttu-id="8c50e-134">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="8c50e-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8c50e-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="8c50e-135">-VirtualHub</span></span>
<span data-ttu-id="8c50e-136">此 VpnGateway 需要關聯的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="8c50e-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="8c50e-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="8c50e-137">-VirtualHubId</span></span>
<span data-ttu-id="8c50e-138">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c50e-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="8c50e-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="8c50e-139">-VirtualHubName</span></span>
<span data-ttu-id="8c50e-140">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c50e-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="8c50e-141">-確認</span><span class="sxs-lookup"><span data-stu-id="8c50e-141">-Confirm</span></span>
<span data-ttu-id="8c50e-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c50e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c50e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c50e-143">-WhatIf</span></span>
<span data-ttu-id="8c50e-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c50e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c50e-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c50e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c50e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c50e-146">CommonParameters</span></span>
<span data-ttu-id="8c50e-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c50e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c50e-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c50e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c50e-149">輸入</span><span class="sxs-lookup"><span data-stu-id="8c50e-149">INPUTS</span></span>

### <span data-ttu-id="8c50e-150">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c50e-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="8c50e-151">System.object</span><span class="sxs-lookup"><span data-stu-id="8c50e-151">System.String</span></span>

## <span data-ttu-id="8c50e-152">輸出</span><span class="sxs-lookup"><span data-stu-id="8c50e-152">OUTPUTS</span></span>

### <span data-ttu-id="8c50e-153">PSExpressRouteGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c50e-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="8c50e-154">筆記</span><span class="sxs-lookup"><span data-stu-id="8c50e-154">NOTES</span></span>

## <span data-ttu-id="8c50e-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c50e-155">RELATED LINKS</span></span>

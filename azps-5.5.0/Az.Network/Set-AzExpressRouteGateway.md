---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: bd800f362a1a5fb66968e0f75b1211b2f0bbdf72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142110"
---
# <span data-ttu-id="12854-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="12854-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="12854-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12854-102">SYNOPSIS</span></span>
<span data-ttu-id="12854-103">更新可伸縮的 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="12854-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="12854-104">句法</span><span class="sxs-lookup"><span data-stu-id="12854-104">SYNTAX</span></span>

### <span data-ttu-id="12854-105">ByExpressRouteGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="12854-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12854-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="12854-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12854-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="12854-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12854-108">說明</span><span class="sxs-lookup"><span data-stu-id="12854-108">DESCRIPTION</span></span>

<span data-ttu-id="12854-109">**AzExpressRouteGateway** Cmdlet 可讓您更新現有 ExpressRouteGateway 的縮放單位，或更新資源標籤。</span><span class="sxs-lookup"><span data-stu-id="12854-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="12854-110">示例</span><span class="sxs-lookup"><span data-stu-id="12854-110">EXAMPLES</span></span>

### <span data-ttu-id="12854-111">範例1</span><span class="sxs-lookup"><span data-stu-id="12854-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="12854-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="12854-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="12854-113">在具有2個比例單位的虛擬中樞中將會建立 ExpressRoute 閘道，然後會將其修改成3個比例單位</span><span class="sxs-lookup"><span data-stu-id="12854-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="12854-114">參數</span><span class="sxs-lookup"><span data-stu-id="12854-114">PARAMETERS</span></span>

### <span data-ttu-id="12854-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12854-115">-AsJob</span></span>
<span data-ttu-id="12854-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="12854-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12854-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12854-117">-DefaultProfile</span></span>
<span data-ttu-id="12854-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12854-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12854-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12854-119">-InputObject</span></span>
<span data-ttu-id="12854-120">需要更新的 ExpressRouteGateway。</span><span class="sxs-lookup"><span data-stu-id="12854-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12854-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="12854-121">-MaxScaleUnits</span></span>
<span data-ttu-id="12854-122">此 ExpressRouteGateway 的縮放單位數上限。</span><span class="sxs-lookup"><span data-stu-id="12854-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="12854-123">有效範圍 > 2</span><span class="sxs-lookup"><span data-stu-id="12854-123">Valid range > 2</span></span>

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

### <span data-ttu-id="12854-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="12854-124">-MinScaleUnits</span></span>
<span data-ttu-id="12854-125">此 ExpressRouteGateway 的最小縮放單位數。</span><span class="sxs-lookup"><span data-stu-id="12854-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="12854-126">有效範圍 > 2</span><span class="sxs-lookup"><span data-stu-id="12854-126">Valid range > 2</span></span>

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

### <span data-ttu-id="12854-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="12854-127">-Name</span></span>
<span data-ttu-id="12854-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="12854-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12854-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12854-129">-ResourceGroupName</span></span>
<span data-ttu-id="12854-130">要更新之 ExpressRouteGateway 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="12854-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12854-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12854-131">-ResourceId</span></span>
<span data-ttu-id="12854-132">需要更新的 ExpressRouteGateway 識別碼。</span><span class="sxs-lookup"><span data-stu-id="12854-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12854-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="12854-133">-Tag</span></span>
<span data-ttu-id="12854-134">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="12854-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="12854-135">-確認</span><span class="sxs-lookup"><span data-stu-id="12854-135">-Confirm</span></span>
<span data-ttu-id="12854-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12854-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12854-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12854-137">-WhatIf</span></span>
<span data-ttu-id="12854-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12854-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12854-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12854-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12854-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12854-140">CommonParameters</span></span>
<span data-ttu-id="12854-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12854-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12854-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12854-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12854-143">輸入</span><span class="sxs-lookup"><span data-stu-id="12854-143">INPUTS</span></span>

### <span data-ttu-id="12854-144">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12854-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="12854-145">System.object</span><span class="sxs-lookup"><span data-stu-id="12854-145">System.String</span></span>

## <span data-ttu-id="12854-146">輸出</span><span class="sxs-lookup"><span data-stu-id="12854-146">OUTPUTS</span></span>

### <span data-ttu-id="12854-147">PSExpressRouteGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12854-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="12854-148">筆記</span><span class="sxs-lookup"><span data-stu-id="12854-148">NOTES</span></span>

## <span data-ttu-id="12854-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="12854-149">RELATED LINKS</span></span>

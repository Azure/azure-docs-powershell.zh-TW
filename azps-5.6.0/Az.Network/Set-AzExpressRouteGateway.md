---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: faa634facf6baa8d0d55490ec32a9395feaea5db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904918"
---
# <span data-ttu-id="0bbc7-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="0bbc7-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="0bbc7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0bbc7-102">SYNOPSIS</span></span>
<span data-ttu-id="0bbc7-103">更新可縮放的 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="0bbc7-104">語法</span><span class="sxs-lookup"><span data-stu-id="0bbc7-104">SYNTAX</span></span>

### <span data-ttu-id="0bbc7-105">ByExpressRouteGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="0bbc7-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bbc7-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="0bbc7-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bbc7-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="0bbc7-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bbc7-108">描述</span><span class="sxs-lookup"><span data-stu-id="0bbc7-108">DESCRIPTION</span></span>

<span data-ttu-id="0bbc7-109">**Set-AzExpressRouteGateway** Cmdlet 可讓您更新現有 ExpressRouteGateway 的縮放單位或更新資源標籤。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="0bbc7-110">例子</span><span class="sxs-lookup"><span data-stu-id="0bbc7-110">EXAMPLES</span></span>

### <span data-ttu-id="0bbc7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0bbc7-111">Example 1</span></span>

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

<span data-ttu-id="0bbc7-112">上述步驟將在 Azure 的 「testRG」資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="0bbc7-113">在此之後，將會以 2 個縮放單位在虛擬中心建立 ExpressRoute 閘道，之後將會修改為 3 個縮放單位</span><span class="sxs-lookup"><span data-stu-id="0bbc7-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="0bbc7-114">參數</span><span class="sxs-lookup"><span data-stu-id="0bbc7-114">PARAMETERS</span></span>

### <span data-ttu-id="0bbc7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bbc7-115">-AsJob</span></span>
<span data-ttu-id="0bbc7-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0bbc7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bbc7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bbc7-117">-DefaultProfile</span></span>
<span data-ttu-id="0bbc7-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bbc7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bbc7-119">-InputObject</span></span>
<span data-ttu-id="0bbc7-120">需要更新的 ExpressRouteGateway。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="0bbc7-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="0bbc7-121">-MaxScaleUnits</span></span>
<span data-ttu-id="0bbc7-122">此 ExpressRouteGateway 的縮放單位上限。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="0bbc7-123">有效範圍 > 2</span><span class="sxs-lookup"><span data-stu-id="0bbc7-123">Valid range > 2</span></span>

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

### <span data-ttu-id="0bbc7-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="0bbc7-124">-MinScaleUnits</span></span>
<span data-ttu-id="0bbc7-125">此 ExpressRouteGateway 的最小刻度單位數目。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="0bbc7-126">有效範圍 > 2</span><span class="sxs-lookup"><span data-stu-id="0bbc7-126">Valid range > 2</span></span>

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

### <span data-ttu-id="0bbc7-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bbc7-127">-Name</span></span>
<span data-ttu-id="0bbc7-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-128">The resource name.</span></span>

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

### <span data-ttu-id="0bbc7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbc7-129">-ResourceGroupName</span></span>
<span data-ttu-id="0bbc7-130">要更新的 ExpressRouteGateway 資源組名。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="0bbc7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bbc7-131">-ResourceId</span></span>
<span data-ttu-id="0bbc7-132">需要更新的 ExpressRouteGateway 識別碼。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="0bbc7-133">-標記</span><span class="sxs-lookup"><span data-stu-id="0bbc7-133">-Tag</span></span>
<span data-ttu-id="0bbc7-134">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0bbc7-135">-確認</span><span class="sxs-lookup"><span data-stu-id="0bbc7-135">-Confirm</span></span>
<span data-ttu-id="0bbc7-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bbc7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bbc7-137">-WhatIf</span></span>
<span data-ttu-id="0bbc7-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bbc7-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bbc7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bbc7-140">CommonParameters</span></span>
<span data-ttu-id="0bbc7-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bbc7-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0bbc7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bbc7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="0bbc7-143">INPUTS</span></span>

### <span data-ttu-id="0bbc7-144">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0bbc7-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="0bbc7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0bbc7-145">System.String</span></span>

## <span data-ttu-id="0bbc7-146">輸出</span><span class="sxs-lookup"><span data-stu-id="0bbc7-146">OUTPUTS</span></span>

### <span data-ttu-id="0bbc7-147">Microsoft.Azure.Commands.Network.models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="0bbc7-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="0bbc7-148">筆記</span><span class="sxs-lookup"><span data-stu-id="0bbc7-148">NOTES</span></span>

## <span data-ttu-id="0bbc7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bbc7-149">RELATED LINKS</span></span>

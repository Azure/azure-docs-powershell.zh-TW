---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 7e68e8e48ffa9d86222951b7ca2e076351872be6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910017"
---
# <span data-ttu-id="65ba2-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="65ba2-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="65ba2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="65ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="65ba2-103">建立可縮放 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="65ba2-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="65ba2-104">語法</span><span class="sxs-lookup"><span data-stu-id="65ba2-104">SYNTAX</span></span>

### <span data-ttu-id="65ba2-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="65ba2-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65ba2-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="65ba2-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65ba2-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="65ba2-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65ba2-108">描述</span><span class="sxs-lookup"><span data-stu-id="65ba2-108">DESCRIPTION</span></span>
<span data-ttu-id="65ba2-109">New-AzVpnGateway建立可縮放的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="65ba2-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="65ba2-110">這是針對 VirtualHub 內網站與網站連結的軟體定義之連接。</span><span class="sxs-lookup"><span data-stu-id="65ba2-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="65ba2-111">此閘道會依據此或 Cmdlet 中指定的縮放比例單位，Set-AzVpnGateway縮放。</span><span class="sxs-lookup"><span data-stu-id="65ba2-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="65ba2-112">從稱為 VPNSite 的分支/網站設定到可縮放閘道的連接。</span><span class="sxs-lookup"><span data-stu-id="65ba2-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="65ba2-113">每個連接由 2 個Active-Active組成。</span><span class="sxs-lookup"><span data-stu-id="65ba2-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="65ba2-114">VpnGateway 會位於與參照的 VirtualHub 相同的位置。</span><span class="sxs-lookup"><span data-stu-id="65ba2-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="65ba2-115">例子</span><span class="sxs-lookup"><span data-stu-id="65ba2-115">EXAMPLES</span></span>

### <span data-ttu-id="65ba2-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="65ba2-116">Example 1</span></span>
```
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2 -EnableRoutingPreferenceInternetFlag

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="65ba2-117">上述步驟將在 Azure 的 「testRG」資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="65ba2-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="65ba2-118">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="65ba2-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="65ba2-119">參數</span><span class="sxs-lookup"><span data-stu-id="65ba2-119">PARAMETERS</span></span>

### <span data-ttu-id="65ba2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65ba2-120">-AsJob</span></span>
<span data-ttu-id="65ba2-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="65ba2-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ba2-122">-DefaultProfile</span></span>
<span data-ttu-id="65ba2-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="65ba2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65ba2-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="65ba2-124">-Name</span></span>
<span data-ttu-id="65ba2-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="65ba2-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ba2-126">-ResourceGroupName</span></span>
<span data-ttu-id="65ba2-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="65ba2-127">The resource name.</span></span>

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

### <span data-ttu-id="65ba2-128">-標記</span><span class="sxs-lookup"><span data-stu-id="65ba2-128">-Tag</span></span>
<span data-ttu-id="65ba2-129">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="65ba2-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="65ba2-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="65ba2-130">-VirtualHub</span></span>
<span data-ttu-id="65ba2-131">這個 VpnGateway 的 VirtualHub 需要關聯。</span><span class="sxs-lookup"><span data-stu-id="65ba2-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="65ba2-132">-VirtualHubId</span></span>
<span data-ttu-id="65ba2-133">這個 VpnGateway 的 VirtualHub 識別碼必須相關聯。</span><span class="sxs-lookup"><span data-stu-id="65ba2-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="65ba2-134">-VirtualHubName</span></span>
<span data-ttu-id="65ba2-135">這個 VpnGateway 的 VirtualHub 識別碼必須相關聯。</span><span class="sxs-lookup"><span data-stu-id="65ba2-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="65ba2-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="65ba2-136">-VpnConnection</span></span>
<span data-ttu-id="65ba2-137">此 VpnGateway 所需的 VpnConnection 清單。</span><span class="sxs-lookup"><span data-stu-id="65ba2-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="65ba2-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="65ba2-139">與此 VpnGateway 相關聯的 VpnGatewayNatRules 清單。</span><span class="sxs-lookup"><span data-stu-id="65ba2-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="65ba2-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="65ba2-141">此 VpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="65ba2-141">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="65ba2-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="65ba2-143">在此 VpnGateway 上啟用路由喜好設定網際網路的標標。</span><span class="sxs-lookup"><span data-stu-id="65ba2-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

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

### <span data-ttu-id="65ba2-144">-確認</span><span class="sxs-lookup"><span data-stu-id="65ba2-144">-Confirm</span></span>
<span data-ttu-id="65ba2-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="65ba2-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ba2-146">-WhatIf</span></span>
<span data-ttu-id="65ba2-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65ba2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ba2-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65ba2-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ba2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ba2-149">CommonParameters</span></span>
<span data-ttu-id="65ba2-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="65ba2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ba2-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65ba2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ba2-152">輸入</span><span class="sxs-lookup"><span data-stu-id="65ba2-152">INPUTS</span></span>

### <span data-ttu-id="65ba2-153">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="65ba2-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="65ba2-154">System.String</span><span class="sxs-lookup"><span data-stu-id="65ba2-154">System.String</span></span>
## <span data-ttu-id="65ba2-155">輸出</span><span class="sxs-lookup"><span data-stu-id="65ba2-155">OUTPUTS</span></span>

### <span data-ttu-id="65ba2-156">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="65ba2-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="65ba2-157">筆記</span><span class="sxs-lookup"><span data-stu-id="65ba2-157">NOTES</span></span>

## <span data-ttu-id="65ba2-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="65ba2-158">RELATED LINKS</span></span>

[<span data-ttu-id="65ba2-159">Get-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="65ba2-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="65ba2-160">Remove-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="65ba2-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="65ba2-161">Update-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="65ba2-161">Update-AzVpnGateway</span></span>]()


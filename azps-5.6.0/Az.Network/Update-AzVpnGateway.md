---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: d04c665bce4c37425564e4eb65ff46da3b39fa8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901786"
---
# <span data-ttu-id="d92bc-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d92bc-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="d92bc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d92bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d92bc-103">更新可縮放的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="d92bc-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="d92bc-104">語法</span><span class="sxs-lookup"><span data-stu-id="d92bc-104">SYNTAX</span></span>

### <span data-ttu-id="d92bc-105">By VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="d92bc-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d92bc-106">By VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d92bc-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d92bc-107">By VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d92bc-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d92bc-108">描述</span><span class="sxs-lookup"><span data-stu-id="d92bc-108">DESCRIPTION</span></span>
<span data-ttu-id="d92bc-109">**Update-Az VpnGateway** Cmdlet 會更新可縮放的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="d92bc-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="d92bc-110">Azure VPN 閘道是一種軟體定義的虛擬Hub 網站與網站連結的連接。</span><span class="sxs-lookup"><span data-stu-id="d92bc-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="d92bc-111">此閘道會依據使用者指定的縮放單位來調整大小及縮放比例。</span><span class="sxs-lookup"><span data-stu-id="d92bc-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="d92bc-112">您可以設定從稱為 VPN 網站的分支/網站到可縮放閘道的連接。</span><span class="sxs-lookup"><span data-stu-id="d92bc-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="d92bc-113">每個連接由 2 個Active-Active組成</span><span class="sxs-lookup"><span data-stu-id="d92bc-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="d92bc-114">例子</span><span class="sxs-lookup"><span data-stu-id="d92bc-114">EXAMPLES</span></span>

### <span data-ttu-id="d92bc-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="d92bc-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="d92bc-116">上述步驟將在 Azure 的 「testRG」資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="d92bc-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d92bc-117">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="d92bc-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d92bc-118">閘道建立之後，它會使用 Update-AzVpnGateway將閘道升級為 3 個縮放單位。</span><span class="sxs-lookup"><span data-stu-id="d92bc-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="d92bc-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="d92bc-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="d92bc-120">上述步驟將在 Azure 的 「testRG」資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="d92bc-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d92bc-121">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="d92bc-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d92bc-122">閘道建立之後，它會使用 Set-AzVpnGateway更新 BgpPeeringAddress。</span><span class="sxs-lookup"><span data-stu-id="d92bc-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="d92bc-123">參數</span><span class="sxs-lookup"><span data-stu-id="d92bc-123">PARAMETERS</span></span>

### <span data-ttu-id="d92bc-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d92bc-124">-AsJob</span></span>
<span data-ttu-id="d92bc-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d92bc-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d92bc-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="d92bc-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="d92bc-127">此 VpnGateway bgpsetting 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="d92bc-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92bc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92bc-128">-DefaultProfile</span></span>
<span data-ttu-id="d92bc-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d92bc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d92bc-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d92bc-130">-InputObject</span></span>
<span data-ttu-id="d92bc-131">要修改的 vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="d92bc-131">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d92bc-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="d92bc-132">-Name</span></span>
<span data-ttu-id="d92bc-133">vpn 閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="d92bc-133">The vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92bc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92bc-134">-ResourceGroupName</span></span>
<span data-ttu-id="d92bc-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d92bc-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92bc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d92bc-136">-ResourceId</span></span>
<span data-ttu-id="d92bc-137">要修改之 VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d92bc-137">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d92bc-138">-標記</span><span class="sxs-lookup"><span data-stu-id="d92bc-138">-Tag</span></span>
<span data-ttu-id="d92bc-139">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d92bc-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d92bc-140">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d92bc-140">-VpnConnection</span></span>
<span data-ttu-id="d92bc-141">此 VpnGateway 所需的 VpnConnection 清單。</span><span class="sxs-lookup"><span data-stu-id="d92bc-141">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92bc-142">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="d92bc-142">-VpnGatewayNatRule</span></span>
<span data-ttu-id="d92bc-143">與此 VpnGateway 相關聯的 VpnGatewayNatRules 清單。</span><span class="sxs-lookup"><span data-stu-id="d92bc-143">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="d92bc-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="d92bc-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="d92bc-145">此 VpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="d92bc-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="d92bc-146">-確認</span><span class="sxs-lookup"><span data-stu-id="d92bc-146">-Confirm</span></span>
<span data-ttu-id="d92bc-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d92bc-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d92bc-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d92bc-148">-WhatIf</span></span>
<span data-ttu-id="d92bc-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d92bc-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d92bc-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d92bc-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d92bc-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92bc-151">CommonParameters</span></span>
<span data-ttu-id="d92bc-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d92bc-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92bc-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d92bc-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92bc-154">輸入</span><span class="sxs-lookup"><span data-stu-id="d92bc-154">INPUTS</span></span>

### <span data-ttu-id="d92bc-155">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d92bc-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="d92bc-156">System.String</span><span class="sxs-lookup"><span data-stu-id="d92bc-156">System.String</span></span>

## <span data-ttu-id="d92bc-157">輸出</span><span class="sxs-lookup"><span data-stu-id="d92bc-157">OUTPUTS</span></span>

### <span data-ttu-id="d92bc-158">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d92bc-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="d92bc-159">筆記</span><span class="sxs-lookup"><span data-stu-id="d92bc-159">NOTES</span></span>

## <span data-ttu-id="d92bc-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="d92bc-160">RELATED LINKS</span></span>

[<span data-ttu-id="d92bc-161">Get-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d92bc-161">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="d92bc-162">New-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d92bc-162">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="d92bc-163">Remove-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d92bc-163">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)
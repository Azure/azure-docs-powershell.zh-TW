---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135495"
---
# <span data-ttu-id="2b9d8-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2b9d8-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="2b9d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9d8-103">更新可伸縮的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="2b9d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b9d8-104">SYNTAX</span></span>

### <span data-ttu-id="2b9d8-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="2b9d8-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9d8-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2b9d8-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9d8-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2b9d8-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b9d8-108">說明</span><span class="sxs-lookup"><span data-stu-id="2b9d8-108">DESCRIPTION</span></span>
<span data-ttu-id="2b9d8-109">**AzVpnGateway** Cmdlet 會更新可伸縮的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="2b9d8-110">Azure VPN 閘道是軟體定義的連線至 VirtualHub 內的網站連線。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="2b9d8-111">此閘道會根據使用者指定的縮放比例來調整大小和縮放比例。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="2b9d8-112">您可以將連線從稱為 VPN 網站的分支/網站設定為可伸縮閘道。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="2b9d8-113">每個連線都包含2個 Active-Active 隧道</span><span class="sxs-lookup"><span data-stu-id="2b9d8-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="2b9d8-114">示例</span><span class="sxs-lookup"><span data-stu-id="2b9d8-114">EXAMPLES</span></span>

### <span data-ttu-id="2b9d8-115">範例1</span><span class="sxs-lookup"><span data-stu-id="2b9d8-115">Example 1</span></span>

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

<span data-ttu-id="2b9d8-116">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="2b9d8-117">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="2b9d8-118">建立閘道之後，它會使用 Update-AzVpnGateway 將閘道升級為3個比例單位。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="2b9d8-119">範例2</span><span class="sxs-lookup"><span data-stu-id="2b9d8-119">Example 2</span></span>

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

<span data-ttu-id="2b9d8-120">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="2b9d8-121">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="2b9d8-122">建立閘道之後，它會使用 Set-AzVpnGateway 來更新 BgpPeeringAddress。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="2b9d8-123">參數</span><span class="sxs-lookup"><span data-stu-id="2b9d8-123">PARAMETERS</span></span>

### <span data-ttu-id="2b9d8-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b9d8-124">-AsJob</span></span>
<span data-ttu-id="2b9d8-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b9d8-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b9d8-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="2b9d8-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="2b9d8-127">此 VpnGateway bgpsettings 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9d8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2b9d8-128">-Confirm</span></span>
<span data-ttu-id="2b9d8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9d8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9d8-130">-DefaultProfile</span></span>
<span data-ttu-id="2b9d8-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b9d8-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b9d8-132">-InputObject</span></span>
<span data-ttu-id="2b9d8-133">要修改的 vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="2b9d8-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9d8-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b9d8-134">-Name</span></span>
<span data-ttu-id="2b9d8-135">Vpn 閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9d8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9d8-136">-ResourceGroupName</span></span>
<span data-ttu-id="2b9d8-137">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9d8-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b9d8-138">-ResourceId</span></span>
<span data-ttu-id="2b9d8-139">要修改之 VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9d8-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b9d8-140">-Tag</span></span>
<span data-ttu-id="2b9d8-141">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2b9d8-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2b9d8-142">-VpnConnection</span></span>
<span data-ttu-id="2b9d8-143">此 VpnGateway 所需的 VpnConnections 清單。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="2b9d8-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="2b9d8-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="2b9d8-145">此 VpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9d8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9d8-146">-WhatIf</span></span>
<span data-ttu-id="2b9d8-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b9d8-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9d8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9d8-149">CommonParameters</span></span>
<span data-ttu-id="2b9d8-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9d8-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b9d8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9d8-152">輸入</span><span class="sxs-lookup"><span data-stu-id="2b9d8-152">INPUTS</span></span>

### <span data-ttu-id="2b9d8-153">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2b9d8-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="2b9d8-154">System.object</span><span class="sxs-lookup"><span data-stu-id="2b9d8-154">System.String</span></span>

## <span data-ttu-id="2b9d8-155">輸出</span><span class="sxs-lookup"><span data-stu-id="2b9d8-155">OUTPUTS</span></span>

### <span data-ttu-id="2b9d8-156">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2b9d8-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="2b9d8-157">筆記</span><span class="sxs-lookup"><span data-stu-id="2b9d8-157">NOTES</span></span>

## <span data-ttu-id="2b9d8-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b9d8-158">RELATED LINKS</span></span>
[<span data-ttu-id="2b9d8-159">AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2b9d8-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="2b9d8-160">新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2b9d8-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="2b9d8-161">移除-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2b9d8-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)
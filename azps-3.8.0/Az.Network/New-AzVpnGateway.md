---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798353"
---
# <span data-ttu-id="6fa8b-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6fa8b-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="6fa8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fa8b-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa8b-103">建立可伸縮的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="6fa8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6fa8b-104">SYNTAX</span></span>

### <span data-ttu-id="6fa8b-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="6fa8b-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fa8b-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6fa8b-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fa8b-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6fa8b-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fa8b-108">說明</span><span class="sxs-lookup"><span data-stu-id="6fa8b-108">DESCRIPTION</span></span>

<span data-ttu-id="6fa8b-109">New-AzVpnGateway 建立可伸縮的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="6fa8b-110">這是 VirtualHub 中的網站與網站連線的軟體定義連線。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="6fa8b-111">此閘道會根據在此或 Set-AzVpnGateway Cmdlet 中指定的縮放比例來調整大小並進行縮放。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="6fa8b-112">從稱為 VPNSite 的分支/網站將連接設定為可伸縮閘道。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="6fa8b-113">每個連線都由 2 Active-Active 隧道組成。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="6fa8b-114">VpnGateway 將會位於與參照 VirtualHub 相同的位置。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="6fa8b-115">示例</span><span class="sxs-lookup"><span data-stu-id="6fa8b-115">EXAMPLES</span></span>

### <span data-ttu-id="6fa8b-116">範例1</span><span class="sxs-lookup"><span data-stu-id="6fa8b-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="6fa8b-117">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6fa8b-118">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="6fa8b-119">參數</span><span class="sxs-lookup"><span data-stu-id="6fa8b-119">PARAMETERS</span></span>

### <span data-ttu-id="6fa8b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fa8b-120">-AsJob</span></span>
<span data-ttu-id="6fa8b-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6fa8b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fa8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa8b-122">-DefaultProfile</span></span>
<span data-ttu-id="6fa8b-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fa8b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="6fa8b-124">-Name</span></span>
<span data-ttu-id="6fa8b-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa8b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fa8b-126">-ResourceGroupName</span></span>
<span data-ttu-id="6fa8b-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-127">The resource name.</span></span>

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

### <span data-ttu-id="6fa8b-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="6fa8b-128">-Tag</span></span>
<span data-ttu-id="6fa8b-129">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6fa8b-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6fa8b-130">-VirtualHub</span></span>
<span data-ttu-id="6fa8b-131">此 VpnGateway 需要關聯的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6fa8b-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="6fa8b-132">-VirtualHubId</span></span>
<span data-ttu-id="6fa8b-133">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6fa8b-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="6fa8b-134">-VirtualHubName</span></span>
<span data-ttu-id="6fa8b-135">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6fa8b-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6fa8b-136">-VpnConnection</span></span>
<span data-ttu-id="6fa8b-137">此 VpnGateway 所需的 VpnConnections 清單。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="6fa8b-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="6fa8b-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="6fa8b-139">此 VpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="6fa8b-140">-確認</span><span class="sxs-lookup"><span data-stu-id="6fa8b-140">-Confirm</span></span>
<span data-ttu-id="6fa8b-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fa8b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fa8b-142">-WhatIf</span></span>
<span data-ttu-id="6fa8b-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fa8b-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fa8b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa8b-145">CommonParameters</span></span>
<span data-ttu-id="6fa8b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa8b-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6fa8b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa8b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6fa8b-148">INPUTS</span></span>

### <span data-ttu-id="6fa8b-149">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6fa8b-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6fa8b-150">System.object</span><span class="sxs-lookup"><span data-stu-id="6fa8b-150">System.String</span></span>

## <span data-ttu-id="6fa8b-151">輸出</span><span class="sxs-lookup"><span data-stu-id="6fa8b-151">OUTPUTS</span></span>

### <span data-ttu-id="6fa8b-152">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6fa8b-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="6fa8b-153">筆記</span><span class="sxs-lookup"><span data-stu-id="6fa8b-153">NOTES</span></span>

## <span data-ttu-id="6fa8b-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fa8b-154">RELATED LINKS</span></span>

[<span data-ttu-id="6fa8b-155">AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6fa8b-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="6fa8b-156">移除-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6fa8b-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="6fa8b-157">更新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6fa8b-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
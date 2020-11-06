---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 08915aaf72fbab91d8173480f4e608ebdbaa28ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621686"
---
# <span data-ttu-id="20653-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="20653-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="20653-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20653-102">SYNOPSIS</span></span>
<span data-ttu-id="20653-103">建立可伸縮的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="20653-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="20653-104">句法</span><span class="sxs-lookup"><span data-stu-id="20653-104">SYNTAX</span></span>

### <span data-ttu-id="20653-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="20653-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20653-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="20653-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20653-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="20653-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20653-108">說明</span><span class="sxs-lookup"><span data-stu-id="20653-108">DESCRIPTION</span></span>

<span data-ttu-id="20653-109">New-AzVpnGateway 建立可伸縮的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="20653-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="20653-110">這是 VirtualHub 中的網站與網站連線的軟體定義連線。</span><span class="sxs-lookup"><span data-stu-id="20653-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="20653-111">此閘道會根據在此或 Set-AzVpnGateway Cmdlet 中指定的縮放比例來調整大小並進行縮放。</span><span class="sxs-lookup"><span data-stu-id="20653-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="20653-112">從稱為 VPNSite 的分支/網站將連接設定為可伸縮閘道。</span><span class="sxs-lookup"><span data-stu-id="20653-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="20653-113">每個連線都由 2 Active-Active 隧道組成。</span><span class="sxs-lookup"><span data-stu-id="20653-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="20653-114">VpnGateway 將會位於與參照 VirtualHub 相同的位置。</span><span class="sxs-lookup"><span data-stu-id="20653-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="20653-115">示例</span><span class="sxs-lookup"><span data-stu-id="20653-115">EXAMPLES</span></span>

### <span data-ttu-id="20653-116">範例1</span><span class="sxs-lookup"><span data-stu-id="20653-116">Example 1</span></span>

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

<span data-ttu-id="20653-117">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="20653-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="20653-118">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="20653-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="20653-119">參數</span><span class="sxs-lookup"><span data-stu-id="20653-119">PARAMETERS</span></span>

### <span data-ttu-id="20653-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20653-120">-AsJob</span></span>
<span data-ttu-id="20653-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="20653-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20653-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20653-122">-DefaultProfile</span></span>
<span data-ttu-id="20653-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20653-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20653-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="20653-124">-Name</span></span>
<span data-ttu-id="20653-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="20653-125">The resource name.</span></span>

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

### <span data-ttu-id="20653-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20653-126">-ResourceGroupName</span></span>
<span data-ttu-id="20653-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="20653-127">The resource name.</span></span>

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

### <span data-ttu-id="20653-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="20653-128">-Tag</span></span>
<span data-ttu-id="20653-129">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="20653-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="20653-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="20653-130">-VirtualHub</span></span>
<span data-ttu-id="20653-131">此 VpnGateway 需要關聯的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="20653-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="20653-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="20653-132">-VirtualHubId</span></span>
<span data-ttu-id="20653-133">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20653-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="20653-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="20653-134">-VirtualHubName</span></span>
<span data-ttu-id="20653-135">此 VpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20653-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="20653-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="20653-136">-VpnConnection</span></span>
<span data-ttu-id="20653-137">此 VpnGateway 所需的 VpnConnections 清單。</span><span class="sxs-lookup"><span data-stu-id="20653-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="20653-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="20653-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="20653-139">此 VpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="20653-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="20653-140">-確認</span><span class="sxs-lookup"><span data-stu-id="20653-140">-Confirm</span></span>
<span data-ttu-id="20653-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20653-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20653-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20653-142">-WhatIf</span></span>
<span data-ttu-id="20653-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20653-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20653-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20653-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20653-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20653-145">CommonParameters</span></span>
<span data-ttu-id="20653-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20653-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20653-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20653-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20653-148">輸入</span><span class="sxs-lookup"><span data-stu-id="20653-148">INPUTS</span></span>

### <span data-ttu-id="20653-149">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="20653-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="20653-150">System.object</span><span class="sxs-lookup"><span data-stu-id="20653-150">System.String</span></span>

## <span data-ttu-id="20653-151">輸出</span><span class="sxs-lookup"><span data-stu-id="20653-151">OUTPUTS</span></span>

### <span data-ttu-id="20653-152">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="20653-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="20653-153">筆記</span><span class="sxs-lookup"><span data-stu-id="20653-153">NOTES</span></span>

## <span data-ttu-id="20653-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="20653-154">RELATED LINKS</span></span>

[<span data-ttu-id="20653-155">AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="20653-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="20653-156">移除-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="20653-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="20653-157">更新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="20653-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)

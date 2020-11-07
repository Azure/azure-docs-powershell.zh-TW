---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
ms.openlocfilehash: 00730f6e252373eebbbbc476fdd889b2eeb39e12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624358"
---
# <span data-ttu-id="9e5d4-101">Update-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9e5d4-101">Update-AzureRmVpnGateway</span></span>

## <span data-ttu-id="9e5d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5d4-103">Update-AzureRmVpnGateway 會將可伸縮的 VPN 閘道更新為適當的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-103">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e5d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e5d4-104">SYNTAX</span></span>

### <span data-ttu-id="9e5d4-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="9e5d4-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e5d4-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9e5d4-106">ByVpnGatewayObject</span></span>
```
Update-AzureRmVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e5d4-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9e5d4-107">ByVpnGatewayResourceId</span></span>
```
Update-AzureRmVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e5d4-108">說明</span><span class="sxs-lookup"><span data-stu-id="9e5d4-108">DESCRIPTION</span></span>
<span data-ttu-id="9e5d4-109">Update-AzureRmVpnGateway 會將可伸縮的 VPN 閘道更新為適當的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-109">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span> <span data-ttu-id="9e5d4-110">AzureRmVpnGateway 是一個軟體定義的連線至 VirtualHub 中的 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-110">An AzureRmVpnGateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="9e5d4-111">此閘道會根據使用者指定的縮放比例來調整大小和縮放比例。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="9e5d4-112">您可以將連線從稱為「VPNSite」的分支/網站設定為可伸縮閘道。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-112">A connection can be set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="9e5d4-113">每個連線都包含2個 Active-Active 隧道</span><span class="sxs-lookup"><span data-stu-id="9e5d4-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="9e5d4-114">示例</span><span class="sxs-lookup"><span data-stu-id="9e5d4-114">EXAMPLES</span></span>

### <span data-ttu-id="9e5d4-115">範例1</span><span class="sxs-lookup"><span data-stu-id="9e5d4-115">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="9e5d4-116">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="9e5d4-117">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="9e5d4-118">建立閘道之後，它會使用 Set-AzureRmVpnGateway 將閘道升級為3個比例單位。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-118">After the gateway has been created, it uses Set-AzureRmVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="9e5d4-119">參數</span><span class="sxs-lookup"><span data-stu-id="9e5d4-119">PARAMETERS</span></span>

### <span data-ttu-id="9e5d4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e5d4-120">-AsJob</span></span>
<span data-ttu-id="9e5d4-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9e5d4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e5d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5d4-122">-DefaultProfile</span></span>
<span data-ttu-id="9e5d4-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5d4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e5d4-124">-InputObject</span></span>
<span data-ttu-id="9e5d4-125">要修改的 vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="9e5d4-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="9e5d4-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e5d4-126">-Name</span></span>
<span data-ttu-id="9e5d4-127">虛擬 wan 名稱。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="9e5d4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5d4-128">-ResourceGroupName</span></span>
<span data-ttu-id="9e5d4-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-129">The resource group name.</span></span>

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

### <span data-ttu-id="9e5d4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e5d4-130">-ResourceId</span></span>
<span data-ttu-id="9e5d4-131">要修改之 VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="9e5d4-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e5d4-132">-Tag</span></span>
<span data-ttu-id="9e5d4-133">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9e5d4-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="9e5d4-134">-VpnConnection</span></span>
<span data-ttu-id="9e5d4-135">此 VpnGateway 所需的 VpnConnections 清單。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="9e5d4-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="9e5d4-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="9e5d4-137">此 VpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="9e5d4-138">-確認</span><span class="sxs-lookup"><span data-stu-id="9e5d4-138">-Confirm</span></span>
<span data-ttu-id="9e5d4-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e5d4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e5d4-140">-WhatIf</span></span>
<span data-ttu-id="9e5d4-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e5d4-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e5d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5d4-143">CommonParameters</span></span>
<span data-ttu-id="9e5d4-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5d4-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e5d4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5d4-146">輸入</span><span class="sxs-lookup"><span data-stu-id="9e5d4-146">INPUTS</span></span>

### <span data-ttu-id="9e5d4-147">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e5d4-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="9e5d4-148">System.object</span><span class="sxs-lookup"><span data-stu-id="9e5d4-148">System.String</span></span>

## <span data-ttu-id="9e5d4-149">輸出</span><span class="sxs-lookup"><span data-stu-id="9e5d4-149">OUTPUTS</span></span>

### <span data-ttu-id="9e5d4-150">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e5d4-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="9e5d4-151">筆記</span><span class="sxs-lookup"><span data-stu-id="9e5d4-151">NOTES</span></span>

## <span data-ttu-id="9e5d4-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e5d4-152">RELATED LINKS</span></span>

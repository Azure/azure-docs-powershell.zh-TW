---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 17731d3f864f429fdad58bf767fb5cb25950387d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621531"
---
# <span data-ttu-id="e1a96-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1a96-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="e1a96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1a96-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a96-103">Remove-AzVpnGateway Cmdlet 會移除 Azure VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="e1a96-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="e1a96-104">這是 Azure 虛擬 WAN 的軟體定義連線所專用的閘道。</span><span class="sxs-lookup"><span data-stu-id="e1a96-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="e1a96-105">句法</span><span class="sxs-lookup"><span data-stu-id="e1a96-105">SYNTAX</span></span>

### <span data-ttu-id="e1a96-106">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="e1a96-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1a96-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e1a96-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1a96-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e1a96-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1a96-109">說明</span><span class="sxs-lookup"><span data-stu-id="e1a96-109">DESCRIPTION</span></span>
<span data-ttu-id="e1a96-110">Remove-AzVpnGateway Cmdlet 會移除 Azure VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="e1a96-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="e1a96-111">這是 Azure 虛擬 WAN 的軟體定義連線所專用的閘道。</span><span class="sxs-lookup"><span data-stu-id="e1a96-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="e1a96-112">示例</span><span class="sxs-lookup"><span data-stu-id="e1a96-112">EXAMPLES</span></span>

### <span data-ttu-id="e1a96-113">範例1</span><span class="sxs-lookup"><span data-stu-id="e1a96-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="e1a96-114">這個範例會在美國中部建立資源群組、虛擬 WAN、虛擬中樞、可伸縮的 VPN 閘道，然後立即將其刪除。</span><span class="sxs-lookup"><span data-stu-id="e1a96-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="e1a96-115">若要在刪除虛擬閘道時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="e1a96-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="e1a96-116">這將會刪除 VpnGateway 及其附加的所有 VpnConnections。</span><span class="sxs-lookup"><span data-stu-id="e1a96-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="e1a96-117">範例2</span><span class="sxs-lookup"><span data-stu-id="e1a96-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="e1a96-118">這個範例會在美國中部建立資源群組、虛擬 WAN、虛擬中樞、可伸縮的 VPN 閘道，然後立即將其刪除。</span><span class="sxs-lookup"><span data-stu-id="e1a96-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="e1a96-119">此刪除會使用 powershell 管道執行，這會使用 Get-AzVpnGateway 命令所傳回的 VpnGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="e1a96-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="e1a96-120">若要在刪除虛擬閘道時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="e1a96-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="e1a96-121">這將會刪除 VpnGateway 及其附加的所有 VpnConnections。</span><span class="sxs-lookup"><span data-stu-id="e1a96-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="e1a96-122">參數</span><span class="sxs-lookup"><span data-stu-id="e1a96-122">PARAMETERS</span></span>

### <span data-ttu-id="e1a96-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a96-123">-DefaultProfile</span></span>
<span data-ttu-id="e1a96-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1a96-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1a96-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e1a96-125">-Force</span></span>
<span data-ttu-id="e1a96-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="e1a96-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e1a96-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1a96-127">-InputObject</span></span>
<span data-ttu-id="e1a96-128">要刪除的 vpnGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="e1a96-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="e1a96-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1a96-129">-Name</span></span>
<span data-ttu-id="e1a96-130">VpnGateway 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1a96-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a96-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1a96-131">-PassThru</span></span>
<span data-ttu-id="e1a96-132">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e1a96-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1a96-133">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e1a96-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1a96-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1a96-134">-ResourceGroupName</span></span>
<span data-ttu-id="e1a96-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1a96-135">The resource group name.</span></span>

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

### <span data-ttu-id="e1a96-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1a96-136">-ResourceId</span></span>
<span data-ttu-id="e1a96-137">要刪除之 vpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1a96-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a96-138">-確認</span><span class="sxs-lookup"><span data-stu-id="e1a96-138">-Confirm</span></span>
<span data-ttu-id="e1a96-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1a96-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1a96-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1a96-140">-WhatIf</span></span>
<span data-ttu-id="e1a96-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1a96-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1a96-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1a96-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1a96-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a96-143">CommonParameters</span></span>
<span data-ttu-id="e1a96-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1a96-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a96-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1a96-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a96-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e1a96-146">INPUTS</span></span>

### <span data-ttu-id="e1a96-147">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e1a96-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="e1a96-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e1a96-148">System.String</span></span>

## <span data-ttu-id="e1a96-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e1a96-149">OUTPUTS</span></span>

### <span data-ttu-id="e1a96-150">System.object</span><span class="sxs-lookup"><span data-stu-id="e1a96-150">System.Boolean</span></span>

## <span data-ttu-id="e1a96-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e1a96-151">NOTES</span></span>

## <span data-ttu-id="e1a96-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1a96-152">RELATED LINKS</span></span>

[<span data-ttu-id="e1a96-153">AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1a96-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="e1a96-154">新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1a96-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="e1a96-155">更新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1a96-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
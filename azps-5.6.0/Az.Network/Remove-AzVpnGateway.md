---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: c30ccf4f6e1f0d73112f5fc62ec6945baa9021a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914725"
---
# <span data-ttu-id="c034e-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c034e-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="c034e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c034e-102">SYNOPSIS</span></span>
<span data-ttu-id="c034e-103">Cmdlet Remove-AzVpnGateway移除 Azure VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="c034e-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="c034e-104">這是 Azure Virtual WAN 軟體定義之連接的特定閘道。</span><span class="sxs-lookup"><span data-stu-id="c034e-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="c034e-105">語法</span><span class="sxs-lookup"><span data-stu-id="c034e-105">SYNTAX</span></span>

### <span data-ttu-id="c034e-106">By VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="c034e-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c034e-107">By VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c034e-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c034e-108">By VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c034e-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c034e-109">描述</span><span class="sxs-lookup"><span data-stu-id="c034e-109">DESCRIPTION</span></span>
<span data-ttu-id="c034e-110">Cmdlet Remove-AzVpnGateway移除 Azure VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="c034e-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="c034e-111">這是 Azure Virtual WAN 軟體定義之連接的特定閘道。</span><span class="sxs-lookup"><span data-stu-id="c034e-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="c034e-112">例子</span><span class="sxs-lookup"><span data-stu-id="c034e-112">EXAMPLES</span></span>

### <span data-ttu-id="c034e-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="c034e-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="c034e-114">此範例會在美國中建立資源群組、虛擬 WAN、虛擬中樞、可縮放 VPN 閘道，然後立即刪除。</span><span class="sxs-lookup"><span data-stu-id="c034e-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="c034e-115">若要隱藏刪除虛擬閘道時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="c034e-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="c034e-116">這會刪除 VpnGateway 及其上的所有 VpnConnection。</span><span class="sxs-lookup"><span data-stu-id="c034e-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="c034e-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="c034e-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="c034e-118">此範例會在美國中建立資源群組、虛擬 WAN、虛擬中樞、可縮放 VPN 閘道，然後立即刪除。</span><span class="sxs-lookup"><span data-stu-id="c034e-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="c034e-119">此刪除會使用 powershell 管線執行，此管道使用由 Get-AzVpnGateway 命令所返回的 VpnGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="c034e-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="c034e-120">若要隱藏刪除虛擬閘道時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="c034e-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="c034e-121">這會刪除 VpnGateway 及其上的所有 VpnConnection。</span><span class="sxs-lookup"><span data-stu-id="c034e-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="c034e-122">參數</span><span class="sxs-lookup"><span data-stu-id="c034e-122">PARAMETERS</span></span>

### <span data-ttu-id="c034e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c034e-123">-DefaultProfile</span></span>
<span data-ttu-id="c034e-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c034e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c034e-125">-強制</span><span class="sxs-lookup"><span data-stu-id="c034e-125">-Force</span></span>
<span data-ttu-id="c034e-126">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="c034e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c034e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c034e-127">-InputObject</span></span>
<span data-ttu-id="c034e-128">要刪除的 vpnGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="c034e-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="c034e-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="c034e-129">-Name</span></span>
<span data-ttu-id="c034e-130">vpnGateway 名稱。</span><span class="sxs-lookup"><span data-stu-id="c034e-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="c034e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c034e-131">-PassThru</span></span>
<span data-ttu-id="c034e-132">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c034e-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c034e-133">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c034e-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c034e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c034e-134">-ResourceGroupName</span></span>
<span data-ttu-id="c034e-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c034e-135">The resource group name.</span></span>

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

### <span data-ttu-id="c034e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c034e-136">-ResourceId</span></span>
<span data-ttu-id="c034e-137">要刪除 vpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c034e-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="c034e-138">-確認</span><span class="sxs-lookup"><span data-stu-id="c034e-138">-Confirm</span></span>
<span data-ttu-id="c034e-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c034e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c034e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c034e-140">-WhatIf</span></span>
<span data-ttu-id="c034e-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c034e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c034e-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c034e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c034e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c034e-143">CommonParameters</span></span>
<span data-ttu-id="c034e-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c034e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c034e-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c034e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c034e-146">輸入</span><span class="sxs-lookup"><span data-stu-id="c034e-146">INPUTS</span></span>

### <span data-ttu-id="c034e-147">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="c034e-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="c034e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c034e-148">System.String</span></span>

## <span data-ttu-id="c034e-149">輸出</span><span class="sxs-lookup"><span data-stu-id="c034e-149">OUTPUTS</span></span>

### <span data-ttu-id="c034e-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c034e-150">System.Boolean</span></span>

## <span data-ttu-id="c034e-151">筆記</span><span class="sxs-lookup"><span data-stu-id="c034e-151">NOTES</span></span>

## <span data-ttu-id="c034e-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="c034e-152">RELATED LINKS</span></span>

[<span data-ttu-id="c034e-153">Get-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="c034e-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="c034e-154">New-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="c034e-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="c034e-155">Update-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="c034e-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)

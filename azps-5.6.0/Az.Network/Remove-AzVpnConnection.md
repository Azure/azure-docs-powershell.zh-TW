---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 5b728195c34db0261bd27525f0916c634cf3d9e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915341"
---
# <span data-ttu-id="fd3bd-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fd3bd-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="fd3bd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3bd-103">移除 VpnConnection。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="fd3bd-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd3bd-104">SYNTAX</span></span>

### <span data-ttu-id="fd3bd-105">By VpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="fd3bd-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd3bd-106">By VpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="fd3bd-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd3bd-107">By VpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="fd3bd-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd3bd-108">描述</span><span class="sxs-lookup"><span data-stu-id="fd3bd-108">DESCRIPTION</span></span>
<span data-ttu-id="fd3bd-109">移除 VpnConnection。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="fd3bd-110">例子</span><span class="sxs-lookup"><span data-stu-id="fd3bd-110">EXAMPLES</span></span>

### <span data-ttu-id="fd3bd-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="fd3bd-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="fd3bd-112">上述步驟將在 Azure 的 「testRG」資源群組中，建立美國西部的資源群組、虛擬 WAN、虛擬網路、虛擬中樞和 VpnS 網站。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fd3bd-113">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fd3bd-114">閘道建立完成後，即會使用 New-AzVpnConnection 命令連接到 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="fd3bd-115">接著，它會使用連接名稱移除連接。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="fd3bd-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="fd3bd-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="fd3bd-117">與範例 1 相同，但現在使用 Get-Az VpnConnection 中的管道物件移除連接。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="fd3bd-118">參數</span><span class="sxs-lookup"><span data-stu-id="fd3bd-118">PARAMETERS</span></span>

### <span data-ttu-id="fd3bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3bd-119">-DefaultProfile</span></span>
<span data-ttu-id="fd3bd-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd3bd-121">-強制</span><span class="sxs-lookup"><span data-stu-id="fd3bd-121">-Force</span></span>
<span data-ttu-id="fd3bd-122">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="fd3bd-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fd3bd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd3bd-123">-InputObject</span></span>
<span data-ttu-id="fd3bd-124">要更新的 VpnConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3bd-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd3bd-125">-Name</span></span>
<span data-ttu-id="fd3bd-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd3bd-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="fd3bd-127">-ParentResourceName</span></span>
<span data-ttu-id="fd3bd-128">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd3bd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd3bd-129">-PassThru</span></span>
<span data-ttu-id="fd3bd-130">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd3bd-131">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd3bd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd3bd-132">-ResourceGroupName</span></span>
<span data-ttu-id="fd3bd-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd3bd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd3bd-134">-ResourceId</span></span>
<span data-ttu-id="fd3bd-135">要刪除之 VpnConnection 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3bd-136">-確認</span><span class="sxs-lookup"><span data-stu-id="fd3bd-136">-Confirm</span></span>
<span data-ttu-id="fd3bd-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd3bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd3bd-138">-WhatIf</span></span>
<span data-ttu-id="fd3bd-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd3bd-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd3bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3bd-141">CommonParameters</span></span>
<span data-ttu-id="fd3bd-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd3bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3bd-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd3bd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3bd-144">輸入</span><span class="sxs-lookup"><span data-stu-id="fd3bd-144">INPUTS</span></span>

### <span data-ttu-id="fd3bd-145">System.String</span><span class="sxs-lookup"><span data-stu-id="fd3bd-145">System.String</span></span>

### <span data-ttu-id="fd3bd-146">Microsoft.Azure.Commands.Network.models.PS VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fd3bd-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="fd3bd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="fd3bd-147">OUTPUTS</span></span>

### <span data-ttu-id="fd3bd-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd3bd-148">System.Boolean</span></span>

## <span data-ttu-id="fd3bd-149">筆記</span><span class="sxs-lookup"><span data-stu-id="fd3bd-149">NOTES</span></span>

## <span data-ttu-id="fd3bd-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd3bd-150">RELATED LINKS</span></span>

[<span data-ttu-id="fd3bd-151">Get-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fd3bd-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="fd3bd-152">New-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fd3bd-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="fd3bd-153">Update-Az VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fd3bd-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

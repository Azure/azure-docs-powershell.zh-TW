---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959891"
---
# <span data-ttu-id="84c99-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="84c99-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="84c99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84c99-102">SYNOPSIS</span></span>
<span data-ttu-id="84c99-103">移除 VpnConnection。</span><span class="sxs-lookup"><span data-stu-id="84c99-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="84c99-104">句法</span><span class="sxs-lookup"><span data-stu-id="84c99-104">SYNTAX</span></span>

### <span data-ttu-id="84c99-105">ByVpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="84c99-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84c99-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="84c99-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84c99-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="84c99-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84c99-108">說明</span><span class="sxs-lookup"><span data-stu-id="84c99-108">DESCRIPTION</span></span>
<span data-ttu-id="84c99-109">移除 VpnConnection。</span><span class="sxs-lookup"><span data-stu-id="84c99-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="84c99-110">示例</span><span class="sxs-lookup"><span data-stu-id="84c99-110">EXAMPLES</span></span>

### <span data-ttu-id="84c99-111">範例1</span><span class="sxs-lookup"><span data-stu-id="84c99-111">Example 1</span></span>
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

<span data-ttu-id="84c99-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="84c99-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="84c99-113">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="84c99-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="84c99-114">建立閘道之後，就會使用 [New-AzVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="84c99-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="84c99-115">然後它會使用連接名稱移除連線。</span><span class="sxs-lookup"><span data-stu-id="84c99-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="84c99-116">範例2</span><span class="sxs-lookup"><span data-stu-id="84c99-116">Example 2</span></span>

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

<span data-ttu-id="84c99-117">與範例1相同，但現在它會從 AzVpnConnection 中移除使用管道物件的連接。</span><span class="sxs-lookup"><span data-stu-id="84c99-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="84c99-118">參數</span><span class="sxs-lookup"><span data-stu-id="84c99-118">PARAMETERS</span></span>

### <span data-ttu-id="84c99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c99-119">-DefaultProfile</span></span>
<span data-ttu-id="84c99-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84c99-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84c99-121">-Force</span><span class="sxs-lookup"><span data-stu-id="84c99-121">-Force</span></span>
<span data-ttu-id="84c99-122">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="84c99-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="84c99-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84c99-123">-InputObject</span></span>
<span data-ttu-id="84c99-124">要更新的 VpnConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="84c99-124">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="84c99-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="84c99-125">-Name</span></span>
<span data-ttu-id="84c99-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="84c99-126">The resource name.</span></span>

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

### <span data-ttu-id="84c99-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="84c99-127">-ParentResourceName</span></span>
<span data-ttu-id="84c99-128">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="84c99-128">The parent resource name.</span></span>

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

### <span data-ttu-id="84c99-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84c99-129">-PassThru</span></span>
<span data-ttu-id="84c99-130">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="84c99-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84c99-131">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="84c99-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="84c99-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c99-132">-ResourceGroupName</span></span>
<span data-ttu-id="84c99-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84c99-133">The resource group name.</span></span>

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

### <span data-ttu-id="84c99-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84c99-134">-ResourceId</span></span>
<span data-ttu-id="84c99-135">要刪除之 VpnConnection 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="84c99-135">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="84c99-136">-確認</span><span class="sxs-lookup"><span data-stu-id="84c99-136">-Confirm</span></span>
<span data-ttu-id="84c99-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84c99-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c99-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c99-138">-WhatIf</span></span>
<span data-ttu-id="84c99-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84c99-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c99-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84c99-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c99-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c99-141">CommonParameters</span></span>
<span data-ttu-id="84c99-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84c99-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c99-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84c99-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c99-144">輸入</span><span class="sxs-lookup"><span data-stu-id="84c99-144">INPUTS</span></span>

### <span data-ttu-id="84c99-145">System.object</span><span class="sxs-lookup"><span data-stu-id="84c99-145">System.String</span></span>

### <span data-ttu-id="84c99-146">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="84c99-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="84c99-147">輸出</span><span class="sxs-lookup"><span data-stu-id="84c99-147">OUTPUTS</span></span>

### <span data-ttu-id="84c99-148">System.object</span><span class="sxs-lookup"><span data-stu-id="84c99-148">System.Boolean</span></span>

## <span data-ttu-id="84c99-149">筆記</span><span class="sxs-lookup"><span data-stu-id="84c99-149">NOTES</span></span>

## <span data-ttu-id="84c99-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="84c99-150">RELATED LINKS</span></span>

[<span data-ttu-id="84c99-151">AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="84c99-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="84c99-152">新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="84c99-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="84c99-153">更新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="84c99-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

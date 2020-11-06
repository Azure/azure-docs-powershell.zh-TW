---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
ms.openlocfilehash: da023b7c0b060e9e263b6b0677065746568524b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448302"
---
# <span data-ttu-id="a7852-101">Remove-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a7852-101">Remove-AzureRmVpnConnection</span></span>

## <span data-ttu-id="a7852-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7852-102">SYNOPSIS</span></span>
<span data-ttu-id="a7852-103">移除 VpnConnection。</span><span class="sxs-lookup"><span data-stu-id="a7852-103">Removes a VpnConnection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7852-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7852-104">SYNTAX</span></span>

### <span data-ttu-id="a7852-105">ByVpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="a7852-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7852-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="a7852-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzureRmVpnConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7852-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="a7852-107">ByVpnConnectionObject</span></span>
```
Remove-AzureRmVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7852-108">說明</span><span class="sxs-lookup"><span data-stu-id="a7852-108">DESCRIPTION</span></span>
<span data-ttu-id="a7852-109">移除 VpnConnection。</span><span class="sxs-lookup"><span data-stu-id="a7852-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="a7852-110">示例</span><span class="sxs-lookup"><span data-stu-id="a7852-110">EXAMPLES</span></span>

### <span data-ttu-id="a7852-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a7852-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="a7852-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="a7852-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a7852-113">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="a7852-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a7852-114">建立閘道之後，就會使用 [New-AzureRmVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="a7852-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="a7852-115">然後它會使用連接名稱移除連線。</span><span class="sxs-lookup"><span data-stu-id="a7852-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="a7852-116">範例2</span><span class="sxs-lookup"><span data-stu-id="a7852-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzureRmVpnConnection
```

<span data-ttu-id="a7852-117">與範例1相同，但現在它會從 AzureRmVpnConnection 中移除使用管道物件的連接。</span><span class="sxs-lookup"><span data-stu-id="a7852-117">Same as example 1, but it now removes the connection using the piped object from Get-AzureRmVpnConnection.</span></span>

## <span data-ttu-id="a7852-118">參數</span><span class="sxs-lookup"><span data-stu-id="a7852-118">PARAMETERS</span></span>

### <span data-ttu-id="a7852-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7852-119">-DefaultProfile</span></span>
<span data-ttu-id="a7852-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7852-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7852-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a7852-121">-Force</span></span>
<span data-ttu-id="a7852-122">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="a7852-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="a7852-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7852-123">-InputObject</span></span>
<span data-ttu-id="a7852-124">要更新的 VpnConenction 物件。</span><span class="sxs-lookup"><span data-stu-id="a7852-124">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="a7852-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7852-125">-Name</span></span>
<span data-ttu-id="a7852-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a7852-126">The resource name.</span></span>

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

### <span data-ttu-id="a7852-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a7852-127">-ParentResourceName</span></span>
<span data-ttu-id="a7852-128">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a7852-128">The parent resource name.</span></span>

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

### <span data-ttu-id="a7852-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7852-129">-PassThru</span></span>
<span data-ttu-id="a7852-130">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a7852-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a7852-131">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a7852-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7852-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7852-132">-ResourceGroupName</span></span>
<span data-ttu-id="a7852-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7852-133">The resource group name.</span></span>

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

### <span data-ttu-id="a7852-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7852-134">-ResourceId</span></span>
<span data-ttu-id="a7852-135">要刪除之 VpnConenction 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7852-135">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="a7852-136">-確認</span><span class="sxs-lookup"><span data-stu-id="a7852-136">-Confirm</span></span>
<span data-ttu-id="a7852-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7852-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7852-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7852-138">-WhatIf</span></span>
<span data-ttu-id="a7852-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7852-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7852-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7852-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7852-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7852-141">CommonParameters</span></span>
<span data-ttu-id="a7852-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7852-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7852-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7852-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7852-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a7852-144">INPUTS</span></span>

### <span data-ttu-id="a7852-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a7852-145">System.String</span></span>

### <span data-ttu-id="a7852-146">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7852-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="a7852-147">輸出</span><span class="sxs-lookup"><span data-stu-id="a7852-147">OUTPUTS</span></span>

### <span data-ttu-id="a7852-148">System.object</span><span class="sxs-lookup"><span data-stu-id="a7852-148">System.Boolean</span></span>

## <span data-ttu-id="a7852-149">筆記</span><span class="sxs-lookup"><span data-stu-id="a7852-149">NOTES</span></span>

## <span data-ttu-id="a7852-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7852-150">RELATED LINKS</span></span>

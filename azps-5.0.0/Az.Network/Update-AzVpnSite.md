---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285852"
---
# <span data-ttu-id="4200d-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4200d-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="4200d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4200d-102">SYNOPSIS</span></span>
<span data-ttu-id="4200d-103">更新 VPN 網站。</span><span class="sxs-lookup"><span data-stu-id="4200d-103">Updates a VPN site.</span></span>

## <span data-ttu-id="4200d-104">句法</span><span class="sxs-lookup"><span data-stu-id="4200d-104">SYNTAX</span></span>

### <span data-ttu-id="4200d-105">ByVpnSiteNameNoVirtualWanUpdate (預設) </span><span class="sxs-lookup"><span data-stu-id="4200d-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4200d-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="4200d-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4200d-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="4200d-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4200d-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="4200d-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4200d-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="4200d-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4200d-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="4200d-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4200d-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="4200d-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4200d-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="4200d-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4200d-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="4200d-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4200d-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="4200d-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4200d-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="4200d-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4200d-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="4200d-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4200d-117">說明</span><span class="sxs-lookup"><span data-stu-id="4200d-117">DESCRIPTION</span></span>
<span data-ttu-id="4200d-118">**更新-AzVpnSite** Cmdlet 會更新 VPN 網站。</span><span class="sxs-lookup"><span data-stu-id="4200d-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="4200d-119">示例</span><span class="sxs-lookup"><span data-stu-id="4200d-119">EXAMPLES</span></span>

### <span data-ttu-id="4200d-120">範例1</span><span class="sxs-lookup"><span data-stu-id="4200d-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="4200d-121">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、[西部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="4200d-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="4200d-122">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="4200d-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="4200d-123">網站建立之後，就會使用 Set-AzVpnSite 命令來更新網站的 IpAddress。</span><span class="sxs-lookup"><span data-stu-id="4200d-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="4200d-124">參數</span><span class="sxs-lookup"><span data-stu-id="4200d-124">PARAMETERS</span></span>

### <span data-ttu-id="4200d-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="4200d-125">-AddressSpace</span></span>
<span data-ttu-id="4200d-126">虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="4200d-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="4200d-127">使用此或 AddressSpaceObject，但不能同時使用這兩者。</span><span class="sxs-lookup"><span data-stu-id="4200d-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4200d-128">-AsJob</span></span>
<span data-ttu-id="4200d-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4200d-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4200d-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="4200d-130">-BgpAsn</span></span>
<span data-ttu-id="4200d-131">此 VpnSite 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="4200d-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="4200d-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="4200d-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="4200d-133">此 VpnSite 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="4200d-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="4200d-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="4200d-135">此 VpnSite 的 BGP 對等權重。</span><span class="sxs-lookup"><span data-stu-id="4200d-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="4200d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4200d-136">-DefaultProfile</span></span>
<span data-ttu-id="4200d-137">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4200d-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4200d-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="4200d-138">-DeviceModel</span></span>
<span data-ttu-id="4200d-139">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="4200d-139">The device model of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="4200d-140">-DeviceVendor</span></span>
<span data-ttu-id="4200d-141">遠端 vpn 裝置的裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="4200d-141">The device vendor of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4200d-142">-InputObject</span></span>
<span data-ttu-id="4200d-143">要修改的 vpn 網站物件</span><span class="sxs-lookup"><span data-stu-id="4200d-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="4200d-144">-IpAddress</span></span>
<span data-ttu-id="4200d-145">本機網路閘道的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4200d-145">IP address of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="4200d-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="4200d-147">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="4200d-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="4200d-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="4200d-148">-Name</span></span>
<span data-ttu-id="4200d-149">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4200d-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="4200d-150">-O365Policy</span></span>
<span data-ttu-id="4200d-151">此 VpnSite 的 office 365 流量排列原則。</span><span class="sxs-lookup"><span data-stu-id="4200d-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4200d-152">-ResourceGroupName</span></span>
<span data-ttu-id="4200d-153">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4200d-153">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4200d-154">-ResourceId</span></span>
<span data-ttu-id="4200d-155">Vpn 網站的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4200d-155">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="4200d-156">-Tag</span></span>
<span data-ttu-id="4200d-157">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="4200d-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4200d-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="4200d-158">-VirtualWan</span></span>
<span data-ttu-id="4200d-159">此 VpnSite 需要連線至的 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="4200d-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="4200d-160">-VirtualWanId</span></span>
<span data-ttu-id="4200d-161">此 VpnSite 的 ResourceId VirtualWan 需要連線至。</span><span class="sxs-lookup"><span data-stu-id="4200d-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="4200d-162">-VirtualWanName</span></span>
<span data-ttu-id="4200d-163">此 VpnSite 需要連線至的 VirtualWan 名稱。</span><span class="sxs-lookup"><span data-stu-id="4200d-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4200d-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="4200d-165">此 VpnSite 需要連線至之 VirtualWan 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4200d-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="4200d-166">-VpnSiteLink</span></span>
<span data-ttu-id="4200d-167">此 VpnSite 的 VpnSiteLinks 清單。</span><span class="sxs-lookup"><span data-stu-id="4200d-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4200d-168">-確認</span><span class="sxs-lookup"><span data-stu-id="4200d-168">-Confirm</span></span>
<span data-ttu-id="4200d-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4200d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4200d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4200d-170">-WhatIf</span></span>
<span data-ttu-id="4200d-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4200d-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4200d-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4200d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4200d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4200d-173">CommonParameters</span></span>
<span data-ttu-id="4200d-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4200d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4200d-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4200d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4200d-176">輸入</span><span class="sxs-lookup"><span data-stu-id="4200d-176">INPUTS</span></span>

### <span data-ttu-id="4200d-177">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4200d-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="4200d-178">System.object</span><span class="sxs-lookup"><span data-stu-id="4200d-178">System.String</span></span>

## <span data-ttu-id="4200d-179">輸出</span><span class="sxs-lookup"><span data-stu-id="4200d-179">OUTPUTS</span></span>

### <span data-ttu-id="4200d-180">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4200d-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="4200d-181">筆記</span><span class="sxs-lookup"><span data-stu-id="4200d-181">NOTES</span></span>

## <span data-ttu-id="4200d-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="4200d-182">RELATED LINKS</span></span>

[<span data-ttu-id="4200d-183">AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4200d-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="4200d-184">新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4200d-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="4200d-185">移除-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4200d-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: bd9b0b2a61edf70dfb4cebf392bb64fa742c0417
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901781"
---
# <span data-ttu-id="83634-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="83634-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="83634-102">簡介</span><span class="sxs-lookup"><span data-stu-id="83634-102">SYNOPSIS</span></span>
<span data-ttu-id="83634-103">更新 VPN 網站。</span><span class="sxs-lookup"><span data-stu-id="83634-103">Updates a VPN site.</span></span>

## <span data-ttu-id="83634-104">語法</span><span class="sxs-lookup"><span data-stu-id="83634-104">SYNTAX</span></span>

### <span data-ttu-id="83634-105">By VpnSiteNameNoVirtualWanUpdate (預設) </span><span class="sxs-lookup"><span data-stu-id="83634-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83634-106">By VpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="83634-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83634-107">By VpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="83634-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83634-108">By VpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="83634-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83634-109">By VpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="83634-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83634-110">By VpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="83634-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83634-111">By VpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="83634-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83634-112">By VpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="83634-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83634-113">By VpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="83634-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83634-114">By VpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="83634-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83634-115">By VpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="83634-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83634-116">By VpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="83634-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83634-117">描述</span><span class="sxs-lookup"><span data-stu-id="83634-117">DESCRIPTION</span></span>
<span data-ttu-id="83634-118">**Update-Az VpnSite** Cmdlet 會更新 VPN 網站。</span><span class="sxs-lookup"><span data-stu-id="83634-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="83634-119">例子</span><span class="sxs-lookup"><span data-stu-id="83634-119">EXAMPLES</span></span>

### <span data-ttu-id="83634-120">範例 1</span><span class="sxs-lookup"><span data-stu-id="83634-120">Example 1</span></span>

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

<span data-ttu-id="83634-121">上述步驟將在 Azure 的「testRG」資源群組中，建立資源群組「美國西部虛擬 WAN」。</span><span class="sxs-lookup"><span data-stu-id="83634-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="83634-122">接著，它會建立一個 VpnSite 來代表客戶分支，並連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="83634-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="83634-123">網站建立後，會使用 Set-AzVpnSite 命令更新網站的 ipAddress。</span><span class="sxs-lookup"><span data-stu-id="83634-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="83634-124">參數</span><span class="sxs-lookup"><span data-stu-id="83634-124">PARAMETERS</span></span>

### <span data-ttu-id="83634-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="83634-125">-AddressSpace</span></span>
<span data-ttu-id="83634-126">虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="83634-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="83634-127">請使用這個或 AddressSpaceObject，但不要同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="83634-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="83634-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83634-128">-AsJob</span></span>
<span data-ttu-id="83634-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="83634-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83634-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="83634-130">-BgpAsn</span></span>
<span data-ttu-id="83634-131">此 VpnSite 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="83634-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="83634-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="83634-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="83634-133">此 VpnSite 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="83634-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="83634-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="83634-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="83634-135">此 VpnSite 的 BGP 對等權。</span><span class="sxs-lookup"><span data-stu-id="83634-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="83634-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83634-136">-DefaultProfile</span></span>
<span data-ttu-id="83634-137">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="83634-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83634-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="83634-138">-DeviceModel</span></span>
<span data-ttu-id="83634-139">遠端 vpn 裝置裝置模型。</span><span class="sxs-lookup"><span data-stu-id="83634-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="83634-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="83634-140">-DeviceVendor</span></span>
<span data-ttu-id="83634-141">遠端 vpn 裝置之裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="83634-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="83634-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83634-142">-InputObject</span></span>
<span data-ttu-id="83634-143">要修改的 vpn 網站物件</span><span class="sxs-lookup"><span data-stu-id="83634-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="83634-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="83634-144">-IpAddress</span></span>
<span data-ttu-id="83634-145">本地網路閘道的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="83634-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="83634-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="83634-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="83634-147">遠端 vpn 裝置裝置模型。</span><span class="sxs-lookup"><span data-stu-id="83634-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="83634-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="83634-148">-Name</span></span>
<span data-ttu-id="83634-149">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="83634-149">The resource name.</span></span>

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

### <span data-ttu-id="83634-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="83634-150">-O365Policy</span></span>
<span data-ttu-id="83634-151">此 VpnSite 的 Office 365 流量中斷策略。</span><span class="sxs-lookup"><span data-stu-id="83634-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="83634-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83634-152">-ResourceGroupName</span></span>
<span data-ttu-id="83634-153">資源組名。</span><span class="sxs-lookup"><span data-stu-id="83634-153">The resource group name.</span></span>

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

### <span data-ttu-id="83634-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83634-154">-ResourceId</span></span>
<span data-ttu-id="83634-155">vpn 網站的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="83634-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="83634-156">-標記</span><span class="sxs-lookup"><span data-stu-id="83634-156">-Tag</span></span>
<span data-ttu-id="83634-157">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="83634-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="83634-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="83634-158">-VirtualWan</span></span>
<span data-ttu-id="83634-159">這個 VpnSite 的 VirtualWan 必須連接。</span><span class="sxs-lookup"><span data-stu-id="83634-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="83634-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="83634-160">-VirtualWanId</span></span>
<span data-ttu-id="83634-161">這個 VpnSite 必須連接 ResourceId VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="83634-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="83634-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="83634-162">-VirtualWanName</span></span>
<span data-ttu-id="83634-163">這個 VpnSite 的名稱必須連接。</span><span class="sxs-lookup"><span data-stu-id="83634-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="83634-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83634-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="83634-165">這個 VpnSite 的資源組名必須連接。</span><span class="sxs-lookup"><span data-stu-id="83634-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="83634-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="83634-166">-VpnSiteLink</span></span>
<span data-ttu-id="83634-167">此 VpnSite 具有的 VpnSiteLink 清單。</span><span class="sxs-lookup"><span data-stu-id="83634-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="83634-168">-確認</span><span class="sxs-lookup"><span data-stu-id="83634-168">-Confirm</span></span>
<span data-ttu-id="83634-169">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="83634-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83634-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83634-170">-WhatIf</span></span>
<span data-ttu-id="83634-171">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83634-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83634-172">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83634-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83634-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83634-173">CommonParameters</span></span>
<span data-ttu-id="83634-174">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="83634-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83634-175">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83634-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83634-176">輸入</span><span class="sxs-lookup"><span data-stu-id="83634-176">INPUTS</span></span>

### <span data-ttu-id="83634-177">Microsoft.Azure.Commands.Network.models.PS VpnSite</span><span class="sxs-lookup"><span data-stu-id="83634-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="83634-178">System.String</span><span class="sxs-lookup"><span data-stu-id="83634-178">System.String</span></span>

## <span data-ttu-id="83634-179">輸出</span><span class="sxs-lookup"><span data-stu-id="83634-179">OUTPUTS</span></span>

### <span data-ttu-id="83634-180">Microsoft.Azure.Commands.Network.models.PS VpnSite</span><span class="sxs-lookup"><span data-stu-id="83634-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="83634-181">筆記</span><span class="sxs-lookup"><span data-stu-id="83634-181">NOTES</span></span>

## <span data-ttu-id="83634-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="83634-182">RELATED LINKS</span></span>

[<span data-ttu-id="83634-183">Get-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="83634-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="83634-184">New-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="83634-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="83634-185">Remove-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="83634-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

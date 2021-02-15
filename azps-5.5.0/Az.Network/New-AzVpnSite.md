---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134922"
---
# <span data-ttu-id="26f9f-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="26f9f-101">New-AzVpnSite</span></span>

## <span data-ttu-id="26f9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="26f9f-103">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="26f9f-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="26f9f-104">這是使用 Cortex 虛擬中樞上傳至 Azure 以進行 S2S 連線的客戶分支的 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="26f9f-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="26f9f-105">句法</span><span class="sxs-lookup"><span data-stu-id="26f9f-105">SYNTAX</span></span>

### <span data-ttu-id="26f9f-106">ByVirtualWanNameByVpnSiteIpAddress (預設) </span><span class="sxs-lookup"><span data-stu-id="26f9f-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f9f-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="26f9f-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f9f-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="26f9f-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26f9f-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="26f9f-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26f9f-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="26f9f-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26f9f-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="26f9f-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26f9f-112">說明</span><span class="sxs-lookup"><span data-stu-id="26f9f-112">DESCRIPTION</span></span>
<span data-ttu-id="26f9f-113">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="26f9f-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="26f9f-114">這是使用 Cortex 虛擬中樞上傳至 Azure 以進行 S2S 連線的客戶分支的 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="26f9f-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="26f9f-115">示例</span><span class="sxs-lookup"><span data-stu-id="26f9f-115">EXAMPLES</span></span>

### <span data-ttu-id="26f9f-116">範例1</span><span class="sxs-lookup"><span data-stu-id="26f9f-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="26f9f-117">上述將會在 Azure 中的 [nonlinkSite] 資源群組中，建立一個 [美國] 資源群組、[東部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="26f9f-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="26f9f-118">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="26f9f-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="26f9f-119">接著，就可以使用 [New-AzVpnConnection] 命令設定 IPSec 連線與此分支與 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="26f9f-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="26f9f-120">範例2</span><span class="sxs-lookup"><span data-stu-id="26f9f-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="26f9f-121">上述將會在 Azure 中的 [多重連結] 資源群組中，建立一個資源群組、虛擬 WAN 及 VpnSite，並在美國使用 1 VpnSiteLinks。</span><span class="sxs-lookup"><span data-stu-id="26f9f-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="26f9f-122">範例3</span><span class="sxs-lookup"><span data-stu-id="26f9f-122">Example 3</span></span>

<span data-ttu-id="26f9f-123">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="26f9f-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="26f9f-124"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="26f9f-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="26f9f-125">參數</span><span class="sxs-lookup"><span data-stu-id="26f9f-125">PARAMETERS</span></span>

### <span data-ttu-id="26f9f-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="26f9f-126">-AddressSpace</span></span>
<span data-ttu-id="26f9f-127">虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="26f9f-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="26f9f-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26f9f-128">-AsJob</span></span>
<span data-ttu-id="26f9f-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26f9f-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26f9f-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="26f9f-130">-BgpAsn</span></span>
<span data-ttu-id="26f9f-131">此 VpnSite 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="26f9f-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="26f9f-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="26f9f-133">此 VpnSite 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="26f9f-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="26f9f-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="26f9f-135">此 VpnSite 的 BGP 對等權重。</span><span class="sxs-lookup"><span data-stu-id="26f9f-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f9f-136">-DefaultProfile</span></span>
<span data-ttu-id="26f9f-137">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26f9f-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f9f-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="26f9f-138">-DeviceModel</span></span>
<span data-ttu-id="26f9f-139">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="26f9f-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="26f9f-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="26f9f-140">-DeviceVendor</span></span>
<span data-ttu-id="26f9f-141">遠端 vpn 裝置的裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="26f9f-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="26f9f-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="26f9f-142">-IpAddress</span></span>
<span data-ttu-id="26f9f-143">此 VpnSite 的 IPAddress。</span><span class="sxs-lookup"><span data-stu-id="26f9f-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="26f9f-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="26f9f-145">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="26f9f-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-146">-位置</span><span class="sxs-lookup"><span data-stu-id="26f9f-146">-Location</span></span>
<span data-ttu-id="26f9f-147">資源位置。</span><span class="sxs-lookup"><span data-stu-id="26f9f-147">The resource location.</span></span>

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

### <span data-ttu-id="26f9f-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="26f9f-148">-Name</span></span>
<span data-ttu-id="26f9f-149">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="26f9f-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="26f9f-150">-O365Policy</span></span>
<span data-ttu-id="26f9f-151">此 VpnSite 的 office 365 流量排列原則。</span><span class="sxs-lookup"><span data-stu-id="26f9f-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="26f9f-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f9f-152">-ResourceGroupName</span></span>
<span data-ttu-id="26f9f-153">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="26f9f-153">The resource name.</span></span>

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

### <span data-ttu-id="26f9f-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="26f9f-154">-Tag</span></span>
<span data-ttu-id="26f9f-155">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="26f9f-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="26f9f-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="26f9f-156">-VirtualWan</span></span>
<span data-ttu-id="26f9f-157">此 VpnSite 需要連線至的 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="26f9f-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="26f9f-158">-VirtualWanId</span></span>
<span data-ttu-id="26f9f-159">此 VpnSite 的 ResourceId VirtualWan 需要連線至。</span><span class="sxs-lookup"><span data-stu-id="26f9f-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="26f9f-160">-VirtualWanName</span></span>
<span data-ttu-id="26f9f-161">此 VpnSite 需要連線至的 VirtualWan 名稱。</span><span class="sxs-lookup"><span data-stu-id="26f9f-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f9f-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="26f9f-163">此 VpnSite 需要連線至之 VirtualWan 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="26f9f-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="26f9f-164">-VpnSiteLink</span></span>
<span data-ttu-id="26f9f-165">此 VpnSite 的 VpnSiteLinks 清單。</span><span class="sxs-lookup"><span data-stu-id="26f9f-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-166">-確認</span><span class="sxs-lookup"><span data-stu-id="26f9f-166">-Confirm</span></span>
<span data-ttu-id="26f9f-167">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26f9f-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f9f-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f9f-168">-WhatIf</span></span>
<span data-ttu-id="26f9f-169">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26f9f-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f9f-170">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f9f-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f9f-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f9f-171">CommonParameters</span></span>
<span data-ttu-id="26f9f-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26f9f-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f9f-173">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="26f9f-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f9f-174">輸入</span><span class="sxs-lookup"><span data-stu-id="26f9f-174">INPUTS</span></span>

### <span data-ttu-id="26f9f-175">所有</span><span class="sxs-lookup"><span data-stu-id="26f9f-175">None</span></span>

## <span data-ttu-id="26f9f-176">輸出</span><span class="sxs-lookup"><span data-stu-id="26f9f-176">OUTPUTS</span></span>

### <span data-ttu-id="26f9f-177">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26f9f-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="26f9f-178">筆記</span><span class="sxs-lookup"><span data-stu-id="26f9f-178">NOTES</span></span>

## <span data-ttu-id="26f9f-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f9f-179">RELATED LINKS</span></span>

[<span data-ttu-id="26f9f-180">AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="26f9f-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="26f9f-181">移除-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="26f9f-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="26f9f-182">更新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="26f9f-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)

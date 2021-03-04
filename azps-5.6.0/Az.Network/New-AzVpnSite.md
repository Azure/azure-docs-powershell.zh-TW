---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 578835b000b6efecb3a1429b884ad2416f6c289d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910006"
---
# <span data-ttu-id="44f95-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="44f95-101">New-AzVpnSite</span></span>

## <span data-ttu-id="44f95-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44f95-102">SYNOPSIS</span></span>
<span data-ttu-id="44f95-103">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="44f95-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="44f95-104">這是已上傳至 Azure 以使用 Cortex 虛擬中樞進行 S2S 連接的客戶分支 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="44f95-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="44f95-105">語法</span><span class="sxs-lookup"><span data-stu-id="44f95-105">SYNTAX</span></span>

### <span data-ttu-id="44f95-106">ByVirtualWanNameBy VpnSiteIpAddress (預設) </span><span class="sxs-lookup"><span data-stu-id="44f95-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44f95-107">ByVirtualWanNameBy VpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="44f95-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44f95-108">ByVirtualWanObjectBy VpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="44f95-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44f95-109">ByVirtualWanObjectBy VpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="44f95-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44f95-110">ByVirtualWanResourceIdBy VpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="44f95-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44f95-111">ByVirtualWanResourceIdBy VpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="44f95-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44f95-112">描述</span><span class="sxs-lookup"><span data-stu-id="44f95-112">DESCRIPTION</span></span>
<span data-ttu-id="44f95-113">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="44f95-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="44f95-114">這是已上傳至 Azure 以使用 Cortex 虛擬中樞進行 S2S 連接的客戶分支 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="44f95-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="44f95-115">例子</span><span class="sxs-lookup"><span data-stu-id="44f95-115">EXAMPLES</span></span>

### <span data-ttu-id="44f95-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="44f95-116">Example 1</span></span>

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

<span data-ttu-id="44f95-117">上述步驟將在 Azure 的「非連結網站」資源群組中建立資源群組，即美國東部的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="44f95-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="44f95-118">接著，它會建立一個 VpnSite 來代表客戶分支，並連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="44f95-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="44f95-119">接著，您可以使用這個分支來設定 IPSec 連接，然後使用 New-AzVpnConnection 命令設定 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="44f95-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="44f95-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="44f95-120">Example 2</span></span>
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

<span data-ttu-id="44f95-121">上述將在 Azure 的「多連結」資源群組中，建立一個資源群組、虛擬 WAN 和一個美國東部 1 個 VpnSiteLink 的 VpnSite 網站。</span><span class="sxs-lookup"><span data-stu-id="44f95-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="44f95-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="44f95-122">Example 3</span></span>

<span data-ttu-id="44f95-123">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="44f95-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="44f95-124"> (自動) </span><span class="sxs-lookup"><span data-stu-id="44f95-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="44f95-125">參數</span><span class="sxs-lookup"><span data-stu-id="44f95-125">PARAMETERS</span></span>

### <span data-ttu-id="44f95-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="44f95-126">-AddressSpace</span></span>
<span data-ttu-id="44f95-127">虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="44f95-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="44f95-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44f95-128">-AsJob</span></span>
<span data-ttu-id="44f95-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="44f95-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44f95-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="44f95-130">-BgpAsn</span></span>
<span data-ttu-id="44f95-131">此 VpnSite 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="44f95-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="44f95-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="44f95-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="44f95-133">此 VpnSite 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="44f95-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="44f95-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="44f95-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="44f95-135">此 VpnSite 的 BGP 對等權。</span><span class="sxs-lookup"><span data-stu-id="44f95-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="44f95-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f95-136">-DefaultProfile</span></span>
<span data-ttu-id="44f95-137">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44f95-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44f95-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="44f95-138">-DeviceModel</span></span>
<span data-ttu-id="44f95-139">遠端 vpn 裝置裝置模型。</span><span class="sxs-lookup"><span data-stu-id="44f95-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="44f95-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="44f95-140">-DeviceVendor</span></span>
<span data-ttu-id="44f95-141">遠端 vpn 裝置之裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="44f95-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="44f95-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="44f95-142">-IpAddress</span></span>
<span data-ttu-id="44f95-143">此 VpnSite 的 IPAddress。</span><span class="sxs-lookup"><span data-stu-id="44f95-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="44f95-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="44f95-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="44f95-145">遠端 vpn 裝置裝置模型。</span><span class="sxs-lookup"><span data-stu-id="44f95-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="44f95-146">-位置</span><span class="sxs-lookup"><span data-stu-id="44f95-146">-Location</span></span>
<span data-ttu-id="44f95-147">資源位置。</span><span class="sxs-lookup"><span data-stu-id="44f95-147">The resource location.</span></span>

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

### <span data-ttu-id="44f95-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="44f95-148">-Name</span></span>
<span data-ttu-id="44f95-149">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="44f95-149">The resource name.</span></span>

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

### <span data-ttu-id="44f95-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="44f95-150">-O365Policy</span></span>
<span data-ttu-id="44f95-151">此 VpnSite 的 Office 365 流量中斷策略。</span><span class="sxs-lookup"><span data-stu-id="44f95-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="44f95-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f95-152">-ResourceGroupName</span></span>
<span data-ttu-id="44f95-153">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="44f95-153">The resource name.</span></span>

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

### <span data-ttu-id="44f95-154">-標記</span><span class="sxs-lookup"><span data-stu-id="44f95-154">-Tag</span></span>
<span data-ttu-id="44f95-155">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="44f95-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="44f95-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="44f95-156">-VirtualWan</span></span>
<span data-ttu-id="44f95-157">這個 VpnSite 的 VirtualWan 必須連接。</span><span class="sxs-lookup"><span data-stu-id="44f95-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="44f95-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="44f95-158">-VirtualWanId</span></span>
<span data-ttu-id="44f95-159">這個 VpnSite 必須連接 ResourceId VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="44f95-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="44f95-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="44f95-160">-VirtualWanName</span></span>
<span data-ttu-id="44f95-161">這個 VpnSite 的名稱必須連接。</span><span class="sxs-lookup"><span data-stu-id="44f95-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="44f95-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f95-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="44f95-163">這個 VpnSite 的資源組名必須連接。</span><span class="sxs-lookup"><span data-stu-id="44f95-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="44f95-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="44f95-164">-VpnSiteLink</span></span>
<span data-ttu-id="44f95-165">此 VpnSite 具有的 VpnSiteLink 清單。</span><span class="sxs-lookup"><span data-stu-id="44f95-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="44f95-166">-確認</span><span class="sxs-lookup"><span data-stu-id="44f95-166">-Confirm</span></span>
<span data-ttu-id="44f95-167">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="44f95-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44f95-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44f95-168">-WhatIf</span></span>
<span data-ttu-id="44f95-169">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44f95-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44f95-170">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44f95-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44f95-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f95-171">CommonParameters</span></span>
<span data-ttu-id="44f95-172">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44f95-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f95-173">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44f95-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f95-174">輸入</span><span class="sxs-lookup"><span data-stu-id="44f95-174">INPUTS</span></span>

### <span data-ttu-id="44f95-175">沒有</span><span class="sxs-lookup"><span data-stu-id="44f95-175">None</span></span>

## <span data-ttu-id="44f95-176">輸出</span><span class="sxs-lookup"><span data-stu-id="44f95-176">OUTPUTS</span></span>

### <span data-ttu-id="44f95-177">Microsoft.Azure.Commands.Network.models.PS VpnSite</span><span class="sxs-lookup"><span data-stu-id="44f95-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="44f95-178">筆記</span><span class="sxs-lookup"><span data-stu-id="44f95-178">NOTES</span></span>

## <span data-ttu-id="44f95-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="44f95-179">RELATED LINKS</span></span>

[<span data-ttu-id="44f95-180">Get-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="44f95-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="44f95-181">Remove-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="44f95-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="44f95-182">Update-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="44f95-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)

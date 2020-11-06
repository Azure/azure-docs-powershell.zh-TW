---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnSite.md
ms.openlocfilehash: fa24f61d0e638cb38e7cf882aac2191a5119b1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450211"
---
# <span data-ttu-id="7ac96-101">Update-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="7ac96-101">Update-AzureRmVpnSite</span></span>

## <span data-ttu-id="7ac96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ac96-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac96-103">更新代表客戶分支至預期目標狀態的 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="7ac96-103">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ac96-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ac96-104">SYNTAX</span></span>

### <span data-ttu-id="7ac96-105">ByVpnSiteNameNoVirtualWanUpdate (預設) </span><span class="sxs-lookup"><span data-stu-id="7ac96-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="7ac96-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="7ac96-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="7ac96-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="7ac96-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="7ac96-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="7ac96-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="7ac96-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -InputObject <PSVpnSite> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="7ac96-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <System.Collections.Generic.List`1[System.String]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="7ac96-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="7ac96-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac96-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="7ac96-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzureRmVpnSite -ResourceId <String> [-IpAddress <String>]
 [-AddressSpace <System.Collections.Generic.List`1[System.String]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ac96-117">說明</span><span class="sxs-lookup"><span data-stu-id="7ac96-117">DESCRIPTION</span></span>
<span data-ttu-id="7ac96-118">更新代表客戶分支至預期目標狀態的 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="7ac96-118">Updates a VpnSite representing a customer branch to an intended goal state.</span></span>

## <span data-ttu-id="7ac96-119">示例</span><span class="sxs-lookup"><span data-stu-id="7ac96-119">EXAMPLES</span></span>

### <span data-ttu-id="7ac96-120">範例1</span><span class="sxs-lookup"><span data-stu-id="7ac96-120">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

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

<span data-ttu-id="7ac96-121">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、[西部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="7ac96-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="7ac96-122">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="7ac96-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="7ac96-123">網站建立之後，就會使用 Set-AzureRmVpnSite 命令來更新網站的 IpAddress。</span><span class="sxs-lookup"><span data-stu-id="7ac96-123">Once the site is created, it updates the IpAddress of the site using the Set-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="7ac96-124">參數</span><span class="sxs-lookup"><span data-stu-id="7ac96-124">PARAMETERS</span></span>

### <span data-ttu-id="7ac96-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="7ac96-125">-AddressSpace</span></span>
<span data-ttu-id="7ac96-126">虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="7ac96-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="7ac96-127">使用此或 AddressSpaceObject，但不能同時使用這兩者。</span><span class="sxs-lookup"><span data-stu-id="7ac96-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac96-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ac96-128">-AsJob</span></span>
<span data-ttu-id="7ac96-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ac96-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ac96-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="7ac96-130">-BgpAsn</span></span>
<span data-ttu-id="7ac96-131">此 VpnSite 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="7ac96-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="7ac96-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="7ac96-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="7ac96-133">此 VpnSite 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="7ac96-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="7ac96-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="7ac96-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="7ac96-135">此 VpnSite 的 BGP 對等權重。</span><span class="sxs-lookup"><span data-stu-id="7ac96-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="7ac96-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac96-136">-DefaultProfile</span></span>
<span data-ttu-id="7ac96-137">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ac96-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ac96-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="7ac96-138">-DeviceModel</span></span>
<span data-ttu-id="7ac96-139">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="7ac96-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="7ac96-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="7ac96-140">-DeviceVendor</span></span>
<span data-ttu-id="7ac96-141">遠端 vpn 裝置的裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="7ac96-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="7ac96-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ac96-142">-InputObject</span></span>
<span data-ttu-id="7ac96-143">要修改的 vpn 網站物件</span><span class="sxs-lookup"><span data-stu-id="7ac96-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="7ac96-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="7ac96-144">-IpAddress</span></span>
<span data-ttu-id="7ac96-145">本機網路閘道的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7ac96-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="7ac96-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="7ac96-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="7ac96-147">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="7ac96-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="7ac96-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ac96-148">-Name</span></span>
<span data-ttu-id="7ac96-149">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac96-149">The resource name.</span></span>

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

### <span data-ttu-id="7ac96-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac96-150">-ResourceGroupName</span></span>
<span data-ttu-id="7ac96-151">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac96-151">The resource group name.</span></span>

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

### <span data-ttu-id="7ac96-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ac96-152">-ResourceId</span></span>
<span data-ttu-id="7ac96-153">Vpn 網站的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ac96-153">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="7ac96-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ac96-154">-Tag</span></span>
<span data-ttu-id="7ac96-155">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="7ac96-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7ac96-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="7ac96-156">-VirtualWan</span></span>
<span data-ttu-id="7ac96-157">此 VpnSite 需要連線至的 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="7ac96-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="7ac96-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="7ac96-158">-VirtualWanId</span></span>
<span data-ttu-id="7ac96-159">此 VpnSite 的 ResourceId VirtualWan 需要連線至。</span><span class="sxs-lookup"><span data-stu-id="7ac96-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="7ac96-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="7ac96-160">-VirtualWanName</span></span>
<span data-ttu-id="7ac96-161">此 VpnSite 需要連線至的 VirtualWan 名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac96-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="7ac96-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac96-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="7ac96-163">此 VpnSite 需要連線至之 VirtualWan 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac96-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="7ac96-164">-確認</span><span class="sxs-lookup"><span data-stu-id="7ac96-164">-Confirm</span></span>
<span data-ttu-id="7ac96-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7ac96-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac96-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac96-166">-WhatIf</span></span>
<span data-ttu-id="7ac96-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ac96-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac96-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ac96-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac96-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac96-169">CommonParameters</span></span>
<span data-ttu-id="7ac96-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ac96-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac96-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7ac96-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac96-172">輸入</span><span class="sxs-lookup"><span data-stu-id="7ac96-172">INPUTS</span></span>

### <span data-ttu-id="7ac96-173">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ac96-173">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="7ac96-174">System.object</span><span class="sxs-lookup"><span data-stu-id="7ac96-174">System.String</span></span>

## <span data-ttu-id="7ac96-175">輸出</span><span class="sxs-lookup"><span data-stu-id="7ac96-175">OUTPUTS</span></span>

### <span data-ttu-id="7ac96-176">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ac96-176">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="7ac96-177">筆記</span><span class="sxs-lookup"><span data-stu-id="7ac96-177">NOTES</span></span>

## <span data-ttu-id="7ac96-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ac96-178">RELATED LINKS</span></span>

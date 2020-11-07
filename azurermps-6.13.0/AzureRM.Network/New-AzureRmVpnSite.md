---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
ms.openlocfilehash: b8594aab0b9475ed37a0a205010e92fdb2a4db7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623754"
---
# <span data-ttu-id="4f468-101">New-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="4f468-101">New-AzureRmVpnSite</span></span>

## <span data-ttu-id="4f468-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f468-102">SYNOPSIS</span></span>
<span data-ttu-id="4f468-103">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="4f468-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="4f468-104">這是使用 Cortex 虛擬中樞上傳至 Azure 以進行 S2S 連線的客戶分支的 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="4f468-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f468-105">句法</span><span class="sxs-lookup"><span data-stu-id="4f468-105">SYNTAX</span></span>

### <span data-ttu-id="4f468-106">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="4f468-106">ByVirtualWanName (Default)</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f468-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="4f468-107">ByVirtualWanObject</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f468-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="4f468-108">ByVirtualWanResourceId</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f468-109">說明</span><span class="sxs-lookup"><span data-stu-id="4f468-109">DESCRIPTION</span></span>
<span data-ttu-id="4f468-110">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="4f468-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="4f468-111">這是使用 Cortex 虛擬中樞上傳至 Azure 以進行 S2S 連線的客戶分支的 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="4f468-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="4f468-112">示例</span><span class="sxs-lookup"><span data-stu-id="4f468-112">EXAMPLES</span></span>

### <span data-ttu-id="4f468-113">範例1</span><span class="sxs-lookup"><span data-stu-id="4f468-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="4f468-114">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、[西部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="4f468-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="4f468-115">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="4f468-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="4f468-116">接著，就可以使用 [New-AzureRmVpnConnection] 命令設定 IPSec 連線與此分支與 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="4f468-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="4f468-117">參數</span><span class="sxs-lookup"><span data-stu-id="4f468-117">PARAMETERS</span></span>

### <span data-ttu-id="4f468-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="4f468-118">-AddressSpace</span></span>
<span data-ttu-id="4f468-119">虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="4f468-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="4f468-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f468-120">-AsJob</span></span>
<span data-ttu-id="4f468-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4f468-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f468-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="4f468-122">-BgpAsn</span></span>
<span data-ttu-id="4f468-123">此 VpnSite 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="4f468-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="4f468-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="4f468-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="4f468-125">此 VpnSite 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="4f468-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="4f468-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="4f468-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="4f468-127">此 VpnSite 的 BGP 對等權重。</span><span class="sxs-lookup"><span data-stu-id="4f468-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="4f468-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f468-128">-DefaultProfile</span></span>
<span data-ttu-id="4f468-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f468-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f468-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="4f468-130">-DeviceModel</span></span>
<span data-ttu-id="4f468-131">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="4f468-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="4f468-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="4f468-132">-DeviceVendor</span></span>
<span data-ttu-id="4f468-133">遠端 vpn 裝置的裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="4f468-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="4f468-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="4f468-134">-IpAddress</span></span>
<span data-ttu-id="4f468-135">此 VpnSite 的 IPAddress。</span><span class="sxs-lookup"><span data-stu-id="4f468-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="4f468-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="4f468-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="4f468-137">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="4f468-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="4f468-138">-位置</span><span class="sxs-lookup"><span data-stu-id="4f468-138">-Location</span></span>
<span data-ttu-id="4f468-139">資源位置。</span><span class="sxs-lookup"><span data-stu-id="4f468-139">The resource location.</span></span>

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

### <span data-ttu-id="4f468-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f468-140">-Name</span></span>
<span data-ttu-id="4f468-141">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4f468-141">The resource name.</span></span>

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

### <span data-ttu-id="4f468-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f468-142">-ResourceGroupName</span></span>
<span data-ttu-id="4f468-143">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4f468-143">The resource name.</span></span>

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

### <span data-ttu-id="4f468-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f468-144">-Tag</span></span>
<span data-ttu-id="4f468-145">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="4f468-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4f468-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="4f468-146">-VirtualWan</span></span>
<span data-ttu-id="4f468-147">此 VpnSite 需要連線至的 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="4f468-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f468-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="4f468-148">-VirtualWanId</span></span>
<span data-ttu-id="4f468-149">此 VpnSite 的 ResourceId VirtualWan 需要連線至。</span><span class="sxs-lookup"><span data-stu-id="4f468-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f468-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="4f468-150">-VirtualWanName</span></span>
<span data-ttu-id="4f468-151">此 VpnSite 需要連線至的 VirtualWan 名稱。</span><span class="sxs-lookup"><span data-stu-id="4f468-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f468-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f468-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="4f468-153">此 VpnSite 需要連線至之 VirtualWan 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4f468-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f468-154">-確認</span><span class="sxs-lookup"><span data-stu-id="4f468-154">-Confirm</span></span>
<span data-ttu-id="4f468-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f468-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f468-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f468-156">-WhatIf</span></span>
<span data-ttu-id="4f468-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f468-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f468-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f468-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f468-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f468-159">CommonParameters</span></span>
<span data-ttu-id="4f468-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f468-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f468-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f468-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f468-162">輸入</span><span class="sxs-lookup"><span data-stu-id="4f468-162">INPUTS</span></span>

### <span data-ttu-id="4f468-163">所有</span><span class="sxs-lookup"><span data-stu-id="4f468-163">None</span></span>

## <span data-ttu-id="4f468-164">輸出</span><span class="sxs-lookup"><span data-stu-id="4f468-164">OUTPUTS</span></span>

### <span data-ttu-id="4f468-165">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4f468-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="4f468-166">筆記</span><span class="sxs-lookup"><span data-stu-id="4f468-166">NOTES</span></span>

## <span data-ttu-id="4f468-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f468-167">RELATED LINKS</span></span>

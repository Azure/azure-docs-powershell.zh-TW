---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: e5ada12a6fd55cc882ba5b9ba33c817f7eb4daab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907094"
---
# <span data-ttu-id="021d9-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="021d9-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="021d9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="021d9-102">SYNOPSIS</span></span>
<span data-ttu-id="021d9-103">透過 VpnConnections，為透過此 WAN 連接的 VpnSites 子集進行 Vpn 組配置。</span><span class="sxs-lookup"><span data-stu-id="021d9-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="021d9-104">將產生的 Vpn 組配置上傳到客戶指定的儲存 Blob。</span><span class="sxs-lookup"><span data-stu-id="021d9-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="021d9-105">語法</span><span class="sxs-lookup"><span data-stu-id="021d9-105">SYNTAX</span></span>

### <span data-ttu-id="021d9-106">ByVirtualWanNameBy VpnSiteObject (預設) </span><span class="sxs-lookup"><span data-stu-id="021d9-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021d9-107">ByVirtualWanNameBy VpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="021d9-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021d9-108">ByVirtualWanObjectBy VpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="021d9-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021d9-109">ByVirtualWanObjectBy VpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="021d9-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021d9-110">ByVirtualWanResourceIdBy VpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="021d9-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021d9-111">ByVirtualWanResourceIdBy VpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="021d9-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="021d9-112">描述</span><span class="sxs-lookup"><span data-stu-id="021d9-112">DESCRIPTION</span></span>
<span data-ttu-id="021d9-113">透過 VpnConnections，為透過此 WAN 連接的 VpnSites 子集進行 Vpn 組配置。</span><span class="sxs-lookup"><span data-stu-id="021d9-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="021d9-114">將產生的 Vpn 組配置上傳到客戶指定的儲存 Blob。</span><span class="sxs-lookup"><span data-stu-id="021d9-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="021d9-115">例子</span><span class="sxs-lookup"><span data-stu-id="021d9-115">EXAMPLES</span></span>

### <span data-ttu-id="021d9-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="021d9-116">Example 1</span></span>
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

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="021d9-117">上述步驟將在 Azure 的 「testRG」資源群組中，建立美國西部的資源群組、虛擬 WAN、虛擬網路、虛擬中樞和 VpnS 網站。</span><span class="sxs-lookup"><span data-stu-id="021d9-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="021d9-118">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="021d9-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="021d9-119">閘道建立完成後，即會使用 New-AzVpnConnection 命令連接到 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="021d9-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="021d9-120">然後使用此命令小程式下載組配置。</span><span class="sxs-lookup"><span data-stu-id="021d9-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="021d9-121">如果命令小程式成功，下載組會寫入 SignedSasUrl 所指示的 Blob。</span><span class="sxs-lookup"><span data-stu-id="021d9-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="021d9-122">參數</span><span class="sxs-lookup"><span data-stu-id="021d9-122">PARAMETERS</span></span>

### <span data-ttu-id="021d9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021d9-123">-DefaultProfile</span></span>
<span data-ttu-id="021d9-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="021d9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="021d9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="021d9-125">-InputObject</span></span>
<span data-ttu-id="021d9-126">要修改的 vpn 網站物件</span><span class="sxs-lookup"><span data-stu-id="021d9-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="021d9-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="021d9-127">-Name</span></span>
<span data-ttu-id="021d9-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="021d9-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021d9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021d9-129">-ResourceGroupName</span></span>
<span data-ttu-id="021d9-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="021d9-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021d9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="021d9-131">-ResourceId</span></span>
<span data-ttu-id="021d9-132">虛擬 Wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="021d9-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="021d9-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="021d9-133">-StorageSasUrl</span></span>
<span data-ttu-id="021d9-134">要產生組配置的儲存位置的 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="021d9-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="021d9-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="021d9-135">-VpnSite</span></span>
<span data-ttu-id="021d9-136">要產生組配置的 VpnSite 資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="021d9-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021d9-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="021d9-137">-VpnSiteId</span></span>
<span data-ttu-id="021d9-138">要產生組配置的 VpnSite 資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="021d9-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021d9-139">-確認</span><span class="sxs-lookup"><span data-stu-id="021d9-139">-Confirm</span></span>
<span data-ttu-id="021d9-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="021d9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="021d9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="021d9-141">-WhatIf</span></span>
<span data-ttu-id="021d9-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="021d9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="021d9-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="021d9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="021d9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021d9-144">CommonParameters</span></span>
<span data-ttu-id="021d9-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="021d9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021d9-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="021d9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021d9-147">輸入</span><span class="sxs-lookup"><span data-stu-id="021d9-147">INPUTS</span></span>

### <span data-ttu-id="021d9-148">Microsoft.Azure.Commands.Network.models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="021d9-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="021d9-149">System.String</span><span class="sxs-lookup"><span data-stu-id="021d9-149">System.String</span></span>

## <span data-ttu-id="021d9-150">輸出</span><span class="sxs-lookup"><span data-stu-id="021d9-150">OUTPUTS</span></span>

### <span data-ttu-id="021d9-151">Microsoft.Azure.Commands.Network.models.PSVirtualWan VpnsitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="021d9-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="021d9-152">筆記</span><span class="sxs-lookup"><span data-stu-id="021d9-152">NOTES</span></span>

## <span data-ttu-id="021d9-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="021d9-153">RELATED LINKS</span></span>

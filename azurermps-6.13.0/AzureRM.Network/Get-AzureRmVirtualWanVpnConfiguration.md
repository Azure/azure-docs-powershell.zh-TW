---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
ms.openlocfilehash: be0fbc9b9fc6d91a5bf94344f432b67dfc38cab3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448374"
---
# <span data-ttu-id="c74e2-101">Get-AzureRmVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="c74e2-101">Get-AzureRmVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="c74e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c74e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c74e2-103">取得透過 VpnConnections 連線至此 WAN 之 VpnSites 子集的 Vpn 設定。</span><span class="sxs-lookup"><span data-stu-id="c74e2-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="c74e2-104">將產生的 Vpn 設定上傳到客戶指定的儲存 blob。</span><span class="sxs-lookup"><span data-stu-id="c74e2-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c74e2-105">句法</span><span class="sxs-lookup"><span data-stu-id="c74e2-105">SYNTAX</span></span>

### <span data-ttu-id="c74e2-106">ByVirtualWanNameByVpnSiteObject (預設) </span><span class="sxs-lookup"><span data-stu-id="c74e2-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c74e2-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="c74e2-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c74e2-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="c74e2-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c74e2-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="c74e2-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c74e2-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="c74e2-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c74e2-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="c74e2-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c74e2-112">說明</span><span class="sxs-lookup"><span data-stu-id="c74e2-112">DESCRIPTION</span></span>
<span data-ttu-id="c74e2-113">取得透過 VpnConnections 連線至此 WAN 之 VpnSites 子集的 Vpn 設定。</span><span class="sxs-lookup"><span data-stu-id="c74e2-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="c74e2-114">將產生的 Vpn 設定上傳到客戶指定的儲存 blob。</span><span class="sxs-lookup"><span data-stu-id="c74e2-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="c74e2-115">示例</span><span class="sxs-lookup"><span data-stu-id="c74e2-115">EXAMPLES</span></span>

### <span data-ttu-id="c74e2-116">範例1</span><span class="sxs-lookup"><span data-stu-id="c74e2-116">Example 1</span></span>
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

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzureRmVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="c74e2-117">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="c74e2-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c74e2-118">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="c74e2-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c74e2-119">建立閘道之後，就會使用 [New-AzureRmVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="c74e2-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="c74e2-120">接著，就會使用這個 commandlet 來下載該設定。</span><span class="sxs-lookup"><span data-stu-id="c74e2-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="c74e2-121">如果該 commandlet 成功，則會將下載設定寫入 SignedSasUrl 所指示的 blob。</span><span class="sxs-lookup"><span data-stu-id="c74e2-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="c74e2-122">參數</span><span class="sxs-lookup"><span data-stu-id="c74e2-122">PARAMETERS</span></span>

### <span data-ttu-id="c74e2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c74e2-123">-DefaultProfile</span></span>
<span data-ttu-id="c74e2-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c74e2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c74e2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c74e2-125">-InputObject</span></span>
<span data-ttu-id="c74e2-126">要修改的 vpn 網站物件</span><span class="sxs-lookup"><span data-stu-id="c74e2-126">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="c74e2-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="c74e2-127">-Name</span></span>
<span data-ttu-id="c74e2-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c74e2-128">The resource name.</span></span>

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

### <span data-ttu-id="c74e2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c74e2-129">-ResourceGroupName</span></span>
<span data-ttu-id="c74e2-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c74e2-130">The resource group name.</span></span>

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

### <span data-ttu-id="c74e2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c74e2-131">-ResourceId</span></span>
<span data-ttu-id="c74e2-132">虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c74e2-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="c74e2-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="c74e2-133">-StorageSasUrl</span></span>
<span data-ttu-id="c74e2-134">要產生配置之儲存位置的 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="c74e2-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="c74e2-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c74e2-135">-VpnSite</span></span>
<span data-ttu-id="c74e2-136">要為其產生配置的 VpnSite 資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="c74e2-136">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="c74e2-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="c74e2-137">-VpnSiteId</span></span>
<span data-ttu-id="c74e2-138">要為其產生配置的 VpnSite 資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="c74e2-138">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="c74e2-139">-確認</span><span class="sxs-lookup"><span data-stu-id="c74e2-139">-Confirm</span></span>
<span data-ttu-id="c74e2-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c74e2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c74e2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c74e2-141">-WhatIf</span></span>
<span data-ttu-id="c74e2-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c74e2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c74e2-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c74e2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c74e2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74e2-144">CommonParameters</span></span>
<span data-ttu-id="c74e2-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c74e2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74e2-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c74e2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74e2-147">輸入</span><span class="sxs-lookup"><span data-stu-id="c74e2-147">INPUTS</span></span>

### <span data-ttu-id="c74e2-148">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c74e2-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="c74e2-149">System.object</span><span class="sxs-lookup"><span data-stu-id="c74e2-149">System.String</span></span>

## <span data-ttu-id="c74e2-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c74e2-150">OUTPUTS</span></span>

### <span data-ttu-id="c74e2-151">PSVirtualWanVpnSitesConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c74e2-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="c74e2-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c74e2-152">NOTES</span></span>

## <span data-ttu-id="c74e2-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c74e2-153">RELATED LINKS</span></span>

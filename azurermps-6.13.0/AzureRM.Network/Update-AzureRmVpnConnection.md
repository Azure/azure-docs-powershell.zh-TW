---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
ms.openlocfilehash: 08b1e18fcd15dfb2667d0aec2410e7e0d7ea7b99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449004"
---
# <span data-ttu-id="dc599-101">Update-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="dc599-101">Update-AzureRmVpnConnection</span></span>

## <span data-ttu-id="dc599-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc599-102">SYNOPSIS</span></span>
<span data-ttu-id="dc599-103">將 VpnConnection 物件更新為目標狀態。</span><span class="sxs-lookup"><span data-stu-id="dc599-103">Updates a VpnConnection object to a goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc599-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc599-104">SYNTAX</span></span>

### <span data-ttu-id="dc599-105">ByVpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="dc599-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc599-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="dc599-106">ByVpnConnectionResourceId</span></span>
```
Update-AzureRmVpnConnection -ResourceId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc599-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="dc599-107">ByVpnConnectionObject</span></span>
```
Update-AzureRmVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc599-108">說明</span><span class="sxs-lookup"><span data-stu-id="dc599-108">DESCRIPTION</span></span>
<span data-ttu-id="dc599-109">建立可將 VpnGateway 連線至 RM 中所代表的遠端客戶分支的 IPSec 連線，成為 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="dc599-109">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="dc599-110">示例</span><span class="sxs-lookup"><span data-stu-id="dc599-110">EXAMPLES</span></span>

### <span data-ttu-id="dc599-111">範例1</span><span class="sxs-lookup"><span data-stu-id="dc599-111">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="dc599-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="dc599-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="dc599-113">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="dc599-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="dc599-114">建立閘道之後，就會使用 [New-AzureRmVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="dc599-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="dc599-115">接著，您可以使用 Set-AzureRmVpnConnection 命令來更新連接，以進行新的 IpSecPolicy。</span><span class="sxs-lookup"><span data-stu-id="dc599-115">The connection is then updated to have a new IpSecPolicy by using the Set-AzureRmVpnConnection command.</span></span>

### <span data-ttu-id="dc599-116">範例2</span><span class="sxs-lookup"><span data-stu-id="dc599-116">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="dc599-117">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="dc599-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="dc599-118">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="dc599-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="dc599-119">建立閘道之後，就會使用 [New-AzureRmVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="dc599-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="dc599-120">接著，就會使用安全的字串構造來更新連接，以建立新的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="dc599-120">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="dc599-121">參數</span><span class="sxs-lookup"><span data-stu-id="dc599-121">PARAMETERS</span></span>

### <span data-ttu-id="dc599-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc599-122">-AsJob</span></span>
<span data-ttu-id="dc599-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc599-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc599-124">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="dc599-124">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="dc599-125">需要由這個連線以 mbps 處理的 bandwith。</span><span class="sxs-lookup"><span data-stu-id="dc599-125">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="dc599-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc599-126">-DefaultProfile</span></span>
<span data-ttu-id="dc599-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc599-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc599-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="dc599-128">-EnableBgp</span></span>
<span data-ttu-id="dc599-129">針對此連線啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="dc599-129">Enable BGP for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc599-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc599-130">-InputObject</span></span>
<span data-ttu-id="dc599-131">要更新的 VpnConenction 物件。</span><span class="sxs-lookup"><span data-stu-id="dc599-131">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="dc599-132">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="dc599-132">-IpSecPolicy</span></span>
<span data-ttu-id="dc599-133">需要由這個連線以 mbps 處理的 bandwith。</span><span class="sxs-lookup"><span data-stu-id="dc599-133">The bandwith that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc599-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc599-134">-Name</span></span>
<span data-ttu-id="dc599-135">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="dc599-135">The resource name.</span></span>

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

### <span data-ttu-id="dc599-136">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="dc599-136">-ParentResourceName</span></span>
<span data-ttu-id="dc599-137">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="dc599-137">The parent resource name.</span></span>

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

### <span data-ttu-id="dc599-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc599-138">-ResourceGroupName</span></span>
<span data-ttu-id="dc599-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc599-139">The resource group name.</span></span>

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

### <span data-ttu-id="dc599-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc599-140">-ResourceId</span></span>
<span data-ttu-id="dc599-141">要刪除之 VpnConenction 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc599-141">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="dc599-142">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="dc599-142">-SharedKey</span></span>
<span data-ttu-id="dc599-143">設定此連線所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="dc599-143">The shared key required to set this connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc599-144">-確認</span><span class="sxs-lookup"><span data-stu-id="dc599-144">-Confirm</span></span>
<span data-ttu-id="dc599-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc599-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc599-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc599-146">-WhatIf</span></span>
<span data-ttu-id="dc599-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc599-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc599-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc599-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc599-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc599-149">CommonParameters</span></span>
<span data-ttu-id="dc599-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc599-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc599-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc599-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc599-152">輸入</span><span class="sxs-lookup"><span data-stu-id="dc599-152">INPUTS</span></span>

### <span data-ttu-id="dc599-153">System.object</span><span class="sxs-lookup"><span data-stu-id="dc599-153">System.String</span></span>

### <span data-ttu-id="dc599-154">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc599-154">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="dc599-155">輸出</span><span class="sxs-lookup"><span data-stu-id="dc599-155">OUTPUTS</span></span>

### <span data-ttu-id="dc599-156">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc599-156">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="dc599-157">筆記</span><span class="sxs-lookup"><span data-stu-id="dc599-157">NOTES</span></span>

## <span data-ttu-id="dc599-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc599-158">RELATED LINKS</span></span>

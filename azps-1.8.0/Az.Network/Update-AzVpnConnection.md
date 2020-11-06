---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 5161dfcb843310ad372739438e63adb6c81f1935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621368"
---
# <span data-ttu-id="29e1a-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="29e1a-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="29e1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="29e1a-103">更新 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="29e1a-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="29e1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="29e1a-104">SYNTAX</span></span>

### <span data-ttu-id="29e1a-105">ByVpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="29e1a-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29e1a-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="29e1a-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29e1a-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="29e1a-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29e1a-108">說明</span><span class="sxs-lookup"><span data-stu-id="29e1a-108">DESCRIPTION</span></span>
<span data-ttu-id="29e1a-109">**AzVpnConnection** Cmdlet 會更新 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="29e1a-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="29e1a-110">VPN 連線建立 IPsec 連線，該連線會將 VPN 閘道連線至 Azure 中代表 VPN 網站的遠端客戶分支。</span><span class="sxs-lookup"><span data-stu-id="29e1a-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="29e1a-111">示例</span><span class="sxs-lookup"><span data-stu-id="29e1a-111">EXAMPLES</span></span>

### <span data-ttu-id="29e1a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="29e1a-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

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

<span data-ttu-id="29e1a-113">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="29e1a-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="29e1a-114">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="29e1a-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="29e1a-115">建立閘道之後，就會使用 [New-AzVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="29e1a-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="29e1a-116">接著，您可以使用 Set-AzVpnConnection 命令來更新連接，以進行新的 IpSecPolicy。</span><span class="sxs-lookup"><span data-stu-id="29e1a-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="29e1a-117">範例2</span><span class="sxs-lookup"><span data-stu-id="29e1a-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

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

<span data-ttu-id="29e1a-118">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="29e1a-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="29e1a-119">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="29e1a-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="29e1a-120">建立閘道之後，就會使用 [New-AzVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="29e1a-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="29e1a-121">接著，就會使用安全的字串構造來更新連接，以建立新的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="29e1a-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="29e1a-122">參數</span><span class="sxs-lookup"><span data-stu-id="29e1a-122">PARAMETERS</span></span>

### <span data-ttu-id="29e1a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29e1a-123">-AsJob</span></span>
<span data-ttu-id="29e1a-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="29e1a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29e1a-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="29e1a-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="29e1a-126">需要由這個連線以 mbps 處理的 bandwith。</span><span class="sxs-lookup"><span data-stu-id="29e1a-126">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="29e1a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e1a-127">-DefaultProfile</span></span>
<span data-ttu-id="29e1a-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29e1a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29e1a-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="29e1a-129">-EnableBgp</span></span>
<span data-ttu-id="29e1a-130">針對此連線啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="29e1a-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="29e1a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29e1a-131">-InputObject</span></span>
<span data-ttu-id="29e1a-132">要更新的 VpnConenction 物件。</span><span class="sxs-lookup"><span data-stu-id="29e1a-132">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="29e1a-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="29e1a-133">-IpSecPolicy</span></span>
<span data-ttu-id="29e1a-134">需要由這個連線以 mbps 處理的 bandwith。</span><span class="sxs-lookup"><span data-stu-id="29e1a-134">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="29e1a-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="29e1a-135">-Name</span></span>
<span data-ttu-id="29e1a-136">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="29e1a-136">The resource name.</span></span>

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

### <span data-ttu-id="29e1a-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="29e1a-137">-ParentResourceName</span></span>
<span data-ttu-id="29e1a-138">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="29e1a-138">The parent resource name.</span></span>

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

### <span data-ttu-id="29e1a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29e1a-139">-ResourceGroupName</span></span>
<span data-ttu-id="29e1a-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29e1a-140">The resource group name.</span></span>

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

### <span data-ttu-id="29e1a-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29e1a-141">-ResourceId</span></span>
<span data-ttu-id="29e1a-142">要刪除之 VpnConenction 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="29e1a-142">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="29e1a-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="29e1a-143">-SharedKey</span></span>
<span data-ttu-id="29e1a-144">設定此連線所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="29e1a-144">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="29e1a-145">-確認</span><span class="sxs-lookup"><span data-stu-id="29e1a-145">-Confirm</span></span>
<span data-ttu-id="29e1a-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29e1a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29e1a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29e1a-147">-WhatIf</span></span>
<span data-ttu-id="29e1a-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29e1a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29e1a-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29e1a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29e1a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e1a-150">CommonParameters</span></span>
<span data-ttu-id="29e1a-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29e1a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e1a-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29e1a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e1a-153">輸入</span><span class="sxs-lookup"><span data-stu-id="29e1a-153">INPUTS</span></span>

### <span data-ttu-id="29e1a-154">System.object</span><span class="sxs-lookup"><span data-stu-id="29e1a-154">System.String</span></span>

### <span data-ttu-id="29e1a-155">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29e1a-155">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="29e1a-156">輸出</span><span class="sxs-lookup"><span data-stu-id="29e1a-156">OUTPUTS</span></span>

### <span data-ttu-id="29e1a-157">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29e1a-157">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="29e1a-158">筆記</span><span class="sxs-lookup"><span data-stu-id="29e1a-158">NOTES</span></span>

## <span data-ttu-id="29e1a-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="29e1a-159">RELATED LINKS</span></span>

[<span data-ttu-id="29e1a-160">AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="29e1a-160">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="29e1a-161">新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="29e1a-161">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="29e1a-162">移除-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="29e1a-162">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

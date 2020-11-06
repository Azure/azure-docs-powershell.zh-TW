---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 750af3bf948345a22c7cb7a86b09e07d4e266f9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621688"
---
# <span data-ttu-id="29f9b-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="29f9b-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="29f9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="29f9b-103">建立可將 VpnGateway 連線至 RM 中所代表的遠端客戶分支的 IPSec 連線，成為 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="29f9b-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="29f9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="29f9b-104">SYNTAX</span></span>

### <span data-ttu-id="29f9b-105">ByVpnGatewayNameByVpnSiteObject (預設) </span><span class="sxs-lookup"><span data-stu-id="29f9b-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f9b-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="29f9b-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f9b-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="29f9b-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f9b-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="29f9b-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f9b-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="29f9b-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f9b-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="29f9b-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29f9b-111">說明</span><span class="sxs-lookup"><span data-stu-id="29f9b-111">DESCRIPTION</span></span>
<span data-ttu-id="29f9b-112">建立可將 VpnGateway 連線至 RM 中所代表的遠端客戶分支的 IPSec 連線，成為 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="29f9b-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="29f9b-113">示例</span><span class="sxs-lookup"><span data-stu-id="29f9b-113">EXAMPLES</span></span>

### <span data-ttu-id="29f9b-114">範例1</span><span class="sxs-lookup"><span data-stu-id="29f9b-114">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="29f9b-115">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="29f9b-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="29f9b-116">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="29f9b-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="29f9b-117">建立閘道之後，就會使用 [New-AzVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="29f9b-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="29f9b-118">參數</span><span class="sxs-lookup"><span data-stu-id="29f9b-118">PARAMETERS</span></span>

### <span data-ttu-id="29f9b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29f9b-119">-AsJob</span></span>
<span data-ttu-id="29f9b-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="29f9b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29f9b-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="29f9b-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="29f9b-122">需要由這個連線以 mbps 處理的 bandwith。</span><span class="sxs-lookup"><span data-stu-id="29f9b-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="29f9b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f9b-123">-DefaultProfile</span></span>
<span data-ttu-id="29f9b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29f9b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29f9b-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="29f9b-125">-EnableBgp</span></span>
<span data-ttu-id="29f9b-126">針對此連線啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="29f9b-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="29f9b-127">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="29f9b-127">-IpSecPolicy</span></span>
<span data-ttu-id="29f9b-128">需要由這個連線以 mbps 處理的 bandwith。</span><span class="sxs-lookup"><span data-stu-id="29f9b-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="29f9b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="29f9b-129">-Name</span></span>
<span data-ttu-id="29f9b-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="29f9b-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f9b-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="29f9b-131">-ParentObject</span></span>
<span data-ttu-id="29f9b-132">此連接的父 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="29f9b-132">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29f9b-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="29f9b-133">-ParentResourceId</span></span>
<span data-ttu-id="29f9b-134">此連線之父 VpnGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="29f9b-134">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f9b-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="29f9b-135">-ParentResourceName</span></span>
<span data-ttu-id="29f9b-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29f9b-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f9b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f9b-137">-ResourceGroupName</span></span>
<span data-ttu-id="29f9b-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29f9b-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f9b-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="29f9b-139">-SharedKey</span></span>
<span data-ttu-id="29f9b-140">設定此連線所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="29f9b-140">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="29f9b-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="29f9b-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="29f9b-142">閘道連線通訊協定： IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="29f9b-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f9b-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="29f9b-143">-VpnSite</span></span>
<span data-ttu-id="29f9b-144">此中樞虛擬網路連線所連結的遠端 vpn 網站。</span><span class="sxs-lookup"><span data-stu-id="29f9b-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f9b-145">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="29f9b-145">-VpnSiteId</span></span>
<span data-ttu-id="29f9b-146">此中樞虛擬網路連線所連結的遠端 vpn 網站。</span><span class="sxs-lookup"><span data-stu-id="29f9b-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f9b-147">-確認</span><span class="sxs-lookup"><span data-stu-id="29f9b-147">-Confirm</span></span>
<span data-ttu-id="29f9b-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29f9b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29f9b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f9b-149">-WhatIf</span></span>
<span data-ttu-id="29f9b-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29f9b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29f9b-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29f9b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29f9b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f9b-152">CommonParameters</span></span>
<span data-ttu-id="29f9b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29f9b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f9b-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29f9b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f9b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="29f9b-155">INPUTS</span></span>

### <span data-ttu-id="29f9b-156">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29f9b-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="29f9b-157">System.object</span><span class="sxs-lookup"><span data-stu-id="29f9b-157">System.String</span></span>

## <span data-ttu-id="29f9b-158">輸出</span><span class="sxs-lookup"><span data-stu-id="29f9b-158">OUTPUTS</span></span>

### <span data-ttu-id="29f9b-159">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29f9b-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="29f9b-160">筆記</span><span class="sxs-lookup"><span data-stu-id="29f9b-160">NOTES</span></span>

## <span data-ttu-id="29f9b-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="29f9b-161">RELATED LINKS</span></span>

[<span data-ttu-id="29f9b-162">AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="29f9b-162">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="29f9b-163">移除-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="29f9b-163">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="29f9b-164">更新-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="29f9b-164">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
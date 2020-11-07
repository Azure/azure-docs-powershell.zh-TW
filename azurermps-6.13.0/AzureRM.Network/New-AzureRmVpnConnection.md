---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
ms.openlocfilehash: 8b7d0845e6a8fce2d6c496573a493dfd187c34af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625785"
---
# <span data-ttu-id="f9a9d-101">New-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f9a9d-101">New-AzureRmVpnConnection</span></span>

## <span data-ttu-id="f9a9d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a9d-103">建立可將 VpnGateway 連線至 RM 中所代表的遠端客戶分支的 IPSec 連線，成為 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a9d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9a9d-104">SYNTAX</span></span>

### <span data-ttu-id="f9a9d-105">ByVpnGatewayNameByVpnSiteObject (預設) </span><span class="sxs-lookup"><span data-stu-id="f9a9d-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9a9d-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="f9a9d-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSiteId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9a9d-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="f9a9d-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9a9d-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="f9a9d-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9a9d-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="f9a9d-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9a9d-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="f9a9d-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9a9d-111">說明</span><span class="sxs-lookup"><span data-stu-id="f9a9d-111">DESCRIPTION</span></span>
<span data-ttu-id="f9a9d-112">建立可將 VpnGateway 連線至 RM 中所代表的遠端客戶分支的 IPSec 連線，成為 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="f9a9d-113">示例</span><span class="sxs-lookup"><span data-stu-id="f9a9d-113">EXAMPLES</span></span>

### <span data-ttu-id="f9a9d-114">範例1</span><span class="sxs-lookup"><span data-stu-id="f9a9d-114">Example 1</span></span>

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

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

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

<span data-ttu-id="f9a9d-115">上述將會在 Azure 中的 [testRG] 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞及 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f9a9d-116">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="f9a9d-117">建立閘道之後，就會使用 [New-AzureRmVpnConnection] 命令將它連線至 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="f9a9d-118">參數</span><span class="sxs-lookup"><span data-stu-id="f9a9d-118">PARAMETERS</span></span>

### <span data-ttu-id="f9a9d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9a9d-119">-AsJob</span></span>
<span data-ttu-id="f9a9d-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9a9d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9a9d-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="f9a9d-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="f9a9d-122">需要由這個連線以 mbps 處理的 bandwith。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="f9a9d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a9d-123">-DefaultProfile</span></span>
<span data-ttu-id="f9a9d-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9a9d-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f9a9d-125">-EnableBgp</span></span>
<span data-ttu-id="f9a9d-126">針對此連線啟用 BGP</span><span class="sxs-lookup"><span data-stu-id="f9a9d-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="f9a9d-127">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="f9a9d-127">-IpSecPolicy</span></span>
<span data-ttu-id="f9a9d-128">需要由這個連線以 mbps 處理的 bandwith。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="f9a9d-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9a9d-129">-Name</span></span>
<span data-ttu-id="f9a9d-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-130">The resource name.</span></span>

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

### <span data-ttu-id="f9a9d-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f9a9d-131">-ParentObject</span></span>
<span data-ttu-id="f9a9d-132">此連接的父 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-132">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="f9a9d-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f9a9d-133">-ParentResourceId</span></span>
<span data-ttu-id="f9a9d-134">此連線之父 VpnGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-134">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="f9a9d-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f9a9d-135">-ParentResourceName</span></span>
<span data-ttu-id="f9a9d-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-136">The resource group name.</span></span>

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

### <span data-ttu-id="f9a9d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a9d-137">-ResourceGroupName</span></span>
<span data-ttu-id="f9a9d-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-138">The resource group name.</span></span>

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

### <span data-ttu-id="f9a9d-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f9a9d-139">-SharedKey</span></span>
<span data-ttu-id="f9a9d-140">設定此連線所需的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-140">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="f9a9d-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="f9a9d-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="f9a9d-142">閘道連線通訊協定： IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="f9a9d-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="f9a9d-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f9a9d-143">-VpnSite</span></span>
<span data-ttu-id="f9a9d-144">此中樞虛擬網路連線所連結的遠端 vpn 網站。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="f9a9d-145">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="f9a9d-145">-VpnSiteId</span></span>
<span data-ttu-id="f9a9d-146">此中樞虛擬網路連線所連結的遠端 vpn 網站。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="f9a9d-147">-確認</span><span class="sxs-lookup"><span data-stu-id="f9a9d-147">-Confirm</span></span>
<span data-ttu-id="f9a9d-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a9d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a9d-149">-WhatIf</span></span>
<span data-ttu-id="f9a9d-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9a9d-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a9d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a9d-152">CommonParameters</span></span>
<span data-ttu-id="f9a9d-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a9d-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9a9d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a9d-155">輸入</span><span class="sxs-lookup"><span data-stu-id="f9a9d-155">INPUTS</span></span>

### <span data-ttu-id="f9a9d-156">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f9a9d-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="f9a9d-157">System.object</span><span class="sxs-lookup"><span data-stu-id="f9a9d-157">System.String</span></span>

## <span data-ttu-id="f9a9d-158">輸出</span><span class="sxs-lookup"><span data-stu-id="f9a9d-158">OUTPUTS</span></span>

### <span data-ttu-id="f9a9d-159">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f9a9d-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="f9a9d-160">筆記</span><span class="sxs-lookup"><span data-stu-id="f9a9d-160">NOTES</span></span>

## <span data-ttu-id="f9a9d-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9a9d-161">RELATED LINKS</span></span>

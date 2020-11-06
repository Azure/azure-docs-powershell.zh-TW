---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451119"
---
# <span data-ttu-id="3dfc5-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3dfc5-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="3dfc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfc5-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dfc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dfc5-104">SYNTAX</span></span>

### <span data-ttu-id="3dfc5-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="3dfc5-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dfc5-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3dfc5-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dfc5-107">說明</span><span class="sxs-lookup"><span data-stu-id="3dfc5-107">DESCRIPTION</span></span>
<span data-ttu-id="3dfc5-108">**AzureRmVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="3dfc5-109">示例</span><span class="sxs-lookup"><span data-stu-id="3dfc5-109">EXAMPLES</span></span>

### <span data-ttu-id="3dfc5-110">範例1：設定虛擬網路閘道的目標狀態</span><span class="sxs-lookup"><span data-stu-id="3dfc5-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="3dfc5-111">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數會設定儲存在 variable $Gateway 中之虛擬網路閘道的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="3dfc5-112">此命令也會將 ASN 設定為1337。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="3dfc5-113">範例2：設定虛擬網路閘道的目標狀態</span><span class="sxs-lookup"><span data-stu-id="3dfc5-113">Example 2: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="3dfc5-114">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令所建立的 Vpn ipsec 原則物件，就像每個指定的 ipsec 參數一樣。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="3dfc5-115">第三個命令會針對儲存在 variable $Gateway 中的虛擬網路閘道設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-115">The third command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="3dfc5-116">此命令也會設定在虛擬網路閘道的 $vpnclientipsecpolicy 物件中指定的自訂 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="3dfc5-117">參數</span><span class="sxs-lookup"><span data-stu-id="3dfc5-117">PARAMETERS</span></span>

### <span data-ttu-id="3dfc5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dfc5-118">-AsJob</span></span>
<span data-ttu-id="3dfc5-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3dfc5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dfc5-120">-Asn</span><span class="sxs-lookup"><span data-stu-id="3dfc5-120">-Asn</span></span>
<span data-ttu-id="3dfc5-121">指定虛擬網路閘道自治系統號碼 (ASN) ，用來設定在 IPsec 隧道內 (BGP) 會話的邊界閘道通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dfc5-122">-DefaultProfile</span></span>
<span data-ttu-id="3dfc5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dfc5-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="3dfc5-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="3dfc5-125">停用作用中的功能。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="3dfc5-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="3dfc5-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="3dfc5-127">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="3dfc5-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="3dfc5-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="3dfc5-129">指定要用於強制隧道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="3dfc5-130">如果指定了預設網站，閘道的虛擬私人網路 (VPN) 的所有網際網路流量都會路由到該網站。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="3dfc5-131">-GatewaySku</span></span>
<span data-ttu-id="3dfc5-132">指定虛擬網路閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="3dfc5-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3dfc5-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dfc5-134">空白</span><span class="sxs-lookup"><span data-stu-id="3dfc5-134">Basic</span></span>
- <span data-ttu-id="3dfc5-135">標準</span><span class="sxs-lookup"><span data-stu-id="3dfc5-135">Standard</span></span>
- <span data-ttu-id="3dfc5-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="3dfc5-136">HighPerformance</span></span>
- <span data-ttu-id="3dfc5-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="3dfc5-137">VpnGw1</span></span>
- <span data-ttu-id="3dfc5-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="3dfc5-138">VpnGw2</span></span>
- <span data-ttu-id="3dfc5-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="3dfc5-139">VpnGw3</span></span>
- <span data-ttu-id="3dfc5-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="3dfc5-140">VpnGw1AZ</span></span>
- <span data-ttu-id="3dfc5-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="3dfc5-141">VpnGw2AZ</span></span>
- <span data-ttu-id="3dfc5-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="3dfc5-142">VpnGw3AZ</span></span>
- <span data-ttu-id="3dfc5-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="3dfc5-143">ErGw1AZ</span></span>
- <span data-ttu-id="3dfc5-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="3dfc5-144">ErGw2AZ</span></span>
- <span data-ttu-id="3dfc5-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="3dfc5-145">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3dfc5-146">-PeerWeight</span></span>
<span data-ttu-id="3dfc5-147">指定透過此虛擬網路閘道通過 BGP 瞭解的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="3dfc5-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="3dfc5-148">-RadiusServerAddress</span></span>
<span data-ttu-id="3dfc5-149">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-149">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="3dfc5-150">-RadiusServerSecret</span></span>
<span data-ttu-id="3dfc5-151">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-151">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3dfc5-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="3dfc5-153">指定要作為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="3dfc5-154">您可以使用 Get-AzureRmVirtualNetworkGateway Cmdlet 來取得虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-154">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="3dfc5-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="3dfc5-156">指定此 Cmdlet 用來從哪個位址空間來指派 VPN 用戶端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="3dfc5-157">這不應與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="3dfc5-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="3dfc5-159">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="3dfc5-160">-VpnClientProtocol</span></span>
<span data-ttu-id="3dfc5-161">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="3dfc5-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="3dfc5-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="3dfc5-163">指定已吊銷之 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="3dfc5-164">VPN 用戶端會移除與其中一個相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="3dfc5-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="3dfc5-166">指定要用於 VPN 用戶端驗證的 VPN 用戶端根憑證清單。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="3dfc5-167">[連線 VPN 用戶端] 必須出示從這些根憑證的其中一個證書產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-168">-確認</span><span class="sxs-lookup"><span data-stu-id="3dfc5-168">-Confirm</span></span>
<span data-ttu-id="3dfc5-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dfc5-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dfc5-170">-WhatIf</span></span>
<span data-ttu-id="3dfc5-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dfc5-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dfc5-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfc5-173">CommonParameters</span></span>
<span data-ttu-id="3dfc5-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfc5-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfc5-176">輸入</span><span class="sxs-lookup"><span data-stu-id="3dfc5-176">INPUTS</span></span>

### <span data-ttu-id="3dfc5-177">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3dfc5-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="3dfc5-178">參數： VirtualNetworkGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3dfc5-178">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="3dfc5-179">System.object</span><span class="sxs-lookup"><span data-stu-id="3dfc5-179">System.String</span></span>

### <span data-ttu-id="3dfc5-180">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3dfc5-180">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="3dfc5-181">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3dfc5-181">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3dfc5-182">[System.object]. 清單 ' 1 [PSVpnClientRootCertificate，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-182">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3dfc5-183">[System.object]. 清單 ' 1 [PSVpnClientRevokedCertificate，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-183">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3dfc5-184">[System.object]. 清單 ' 1 [PSIpsecPolicy，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="3dfc5-184">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3dfc5-185">UInt32</span><span class="sxs-lookup"><span data-stu-id="3dfc5-185">System.UInt32</span></span>

### <span data-ttu-id="3dfc5-186">System.object</span><span class="sxs-lookup"><span data-stu-id="3dfc5-186">System.Int32</span></span>

### <span data-ttu-id="3dfc5-187">SecureString</span><span class="sxs-lookup"><span data-stu-id="3dfc5-187">System.Security.SecureString</span></span>

## <span data-ttu-id="3dfc5-188">輸出</span><span class="sxs-lookup"><span data-stu-id="3dfc5-188">OUTPUTS</span></span>

### <span data-ttu-id="3dfc5-189">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3dfc5-189">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3dfc5-190">筆記</span><span class="sxs-lookup"><span data-stu-id="3dfc5-190">NOTES</span></span>
* <span data-ttu-id="3dfc5-191">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="3dfc5-191">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3dfc5-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dfc5-192">RELATED LINKS</span></span>

[<span data-ttu-id="3dfc5-193">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3dfc5-193">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3dfc5-194">新-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3dfc5-194">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3dfc5-195">移除-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3dfc5-195">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3dfc5-196">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3dfc5-196">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3dfc5-197">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3dfc5-197">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)



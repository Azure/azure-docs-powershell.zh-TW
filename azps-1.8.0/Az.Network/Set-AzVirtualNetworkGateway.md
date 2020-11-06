---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621408"
---
# <span data-ttu-id="70561-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="70561-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="70561-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70561-102">SYNOPSIS</span></span>
<span data-ttu-id="70561-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="70561-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="70561-104">句法</span><span class="sxs-lookup"><span data-stu-id="70561-104">SYNTAX</span></span>

### <span data-ttu-id="70561-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="70561-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70561-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="70561-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70561-107">說明</span><span class="sxs-lookup"><span data-stu-id="70561-107">DESCRIPTION</span></span>
<span data-ttu-id="70561-108">**AzVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="70561-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="70561-109">示例</span><span class="sxs-lookup"><span data-stu-id="70561-109">EXAMPLES</span></span>

### <span data-ttu-id="70561-110">範例1：更新虛擬網路閘道的 ASN</span><span class="sxs-lookup"><span data-stu-id="70561-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="70561-111">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令的變數會更新儲存在 variable $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="70561-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="70561-112">此命令也會將 ASN 設定為1337。</span><span class="sxs-lookup"><span data-stu-id="70561-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="70561-113">範例2：新增 IPsec 原則至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="70561-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="70561-114">第一個命令會取得屬於資源群組 ResourceGroup001 的虛擬網路閘道，並將其儲存到名為 $Gateway 第二個命令所建立的 Vpn ipsec 原則物件，就像每個指定的 ipsec 參數一樣。</span><span class="sxs-lookup"><span data-stu-id="70561-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="70561-115">第三個命令會更新儲存在 variable $Gateway 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="70561-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="70561-116">此命令也會設定在虛擬網路閘道的 $vpnclientipsecpolicy 物件中指定的自訂 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="70561-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="70561-117">參數</span><span class="sxs-lookup"><span data-stu-id="70561-117">PARAMETERS</span></span>

### <span data-ttu-id="70561-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70561-118">-AsJob</span></span>
<span data-ttu-id="70561-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="70561-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70561-120">-Asn</span><span class="sxs-lookup"><span data-stu-id="70561-120">-Asn</span></span>
<span data-ttu-id="70561-121">指定虛擬網路閘道自治系統號碼 (ASN) ，用來設定在 IPsec 隧道內 (BGP) 會話的邊界閘道通訊協定。</span><span class="sxs-lookup"><span data-stu-id="70561-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="70561-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70561-122">-DefaultProfile</span></span>
<span data-ttu-id="70561-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70561-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70561-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="70561-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="70561-125">停用作用中的功能。</span><span class="sxs-lookup"><span data-stu-id="70561-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="70561-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="70561-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="70561-127">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="70561-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="70561-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="70561-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="70561-129">指定要用於強制隧道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="70561-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="70561-130">如果指定了預設網站，閘道的虛擬私人網路 (VPN) 的所有網際網路流量都會路由到該網站。</span><span class="sxs-lookup"><span data-stu-id="70561-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="70561-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="70561-131">-GatewaySku</span></span>
<span data-ttu-id="70561-132">指定虛擬網路閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="70561-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="70561-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="70561-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70561-134">空白</span><span class="sxs-lookup"><span data-stu-id="70561-134">Basic</span></span>
- <span data-ttu-id="70561-135">標準</span><span class="sxs-lookup"><span data-stu-id="70561-135">Standard</span></span>
- <span data-ttu-id="70561-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="70561-136">HighPerformance</span></span>
- <span data-ttu-id="70561-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="70561-137">VpnGw1</span></span>
- <span data-ttu-id="70561-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="70561-138">VpnGw2</span></span>
- <span data-ttu-id="70561-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="70561-139">VpnGw3</span></span>
- <span data-ttu-id="70561-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="70561-140">VpnGw1AZ</span></span>
- <span data-ttu-id="70561-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="70561-141">VpnGw2AZ</span></span>
- <span data-ttu-id="70561-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="70561-142">VpnGw3AZ</span></span>
- <span data-ttu-id="70561-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="70561-143">ErGw1AZ</span></span>
- <span data-ttu-id="70561-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="70561-144">ErGw2AZ</span></span>
- <span data-ttu-id="70561-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="70561-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="70561-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="70561-146">-PeerWeight</span></span>
<span data-ttu-id="70561-147">指定透過此虛擬網路閘道通過 BGP 瞭解的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="70561-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="70561-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="70561-148">-RadiusServerAddress</span></span>
<span data-ttu-id="70561-149">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="70561-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="70561-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="70561-150">-RadiusServerSecret</span></span>
<span data-ttu-id="70561-151">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="70561-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="70561-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="70561-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="70561-153">指定要作為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="70561-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="70561-154">您可以使用 Get-AzVirtualNetworkGateway Cmdlet 來取得虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="70561-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="70561-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="70561-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="70561-156">指定此 Cmdlet 用來從哪個位址空間來指派 VPN 用戶端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="70561-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="70561-157">這不應與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="70561-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70561-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="70561-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="70561-159">P2S VPN 用戶端隧道通訊協定的 IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="70561-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70561-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="70561-160">-VpnClientProtocol</span></span>
<span data-ttu-id="70561-161">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="70561-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70561-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="70561-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="70561-163">指定已吊銷之 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="70561-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="70561-164">VPN 用戶端會移除與其中一個相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="70561-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70561-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="70561-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="70561-166">指定要用於 VPN 用戶端驗證的 VPN 用戶端根憑證清單。</span><span class="sxs-lookup"><span data-stu-id="70561-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="70561-167">[連線 VPN 用戶端] 必須出示從這些根憑證的其中一個證書產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="70561-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70561-168">-確認</span><span class="sxs-lookup"><span data-stu-id="70561-168">-Confirm</span></span>
<span data-ttu-id="70561-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="70561-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70561-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70561-170">-WhatIf</span></span>
<span data-ttu-id="70561-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70561-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70561-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70561-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70561-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70561-173">CommonParameters</span></span>
<span data-ttu-id="70561-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70561-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70561-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70561-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70561-176">輸入</span><span class="sxs-lookup"><span data-stu-id="70561-176">INPUTS</span></span>

### <span data-ttu-id="70561-177">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70561-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="70561-178">System.object</span><span class="sxs-lookup"><span data-stu-id="70561-178">System.String</span></span>

### <span data-ttu-id="70561-179">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70561-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="70561-180">System.object []</span><span class="sxs-lookup"><span data-stu-id="70561-180">System.String[]</span></span>

### <span data-ttu-id="70561-181">PSVpnClientRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="70561-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="70561-182">PSVpnClientRevokedCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="70561-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="70561-183">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="70561-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="70561-184">UInt32</span><span class="sxs-lookup"><span data-stu-id="70561-184">System.UInt32</span></span>

### <span data-ttu-id="70561-185">System.object</span><span class="sxs-lookup"><span data-stu-id="70561-185">System.Int32</span></span>

### <span data-ttu-id="70561-186">SecureString</span><span class="sxs-lookup"><span data-stu-id="70561-186">System.Security.SecureString</span></span>

## <span data-ttu-id="70561-187">輸出</span><span class="sxs-lookup"><span data-stu-id="70561-187">OUTPUTS</span></span>

### <span data-ttu-id="70561-188">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70561-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="70561-189">筆記</span><span class="sxs-lookup"><span data-stu-id="70561-189">NOTES</span></span>
* <span data-ttu-id="70561-190">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="70561-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="70561-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="70561-191">RELATED LINKS</span></span>

[<span data-ttu-id="70561-192">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="70561-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="70561-193">新-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="70561-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="70561-194">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="70561-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="70561-195">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="70561-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="70561-196">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="70561-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

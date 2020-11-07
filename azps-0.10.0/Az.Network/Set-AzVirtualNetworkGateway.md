---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 87840267cf85997da83af590664c473a61f74033
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795382"
---
# <span data-ttu-id="67526-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67526-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="67526-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67526-102">SYNOPSIS</span></span>
<span data-ttu-id="67526-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="67526-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="67526-104">句法</span><span class="sxs-lookup"><span data-stu-id="67526-104">SYNTAX</span></span>

### <span data-ttu-id="67526-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="67526-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67526-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="67526-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67526-107">說明</span><span class="sxs-lookup"><span data-stu-id="67526-107">DESCRIPTION</span></span>
<span data-ttu-id="67526-108">**AzVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="67526-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="67526-109">示例</span><span class="sxs-lookup"><span data-stu-id="67526-109">EXAMPLES</span></span>

### <span data-ttu-id="67526-110">範例1：設定虛擬網路閘道的目標狀態</span><span class="sxs-lookup"><span data-stu-id="67526-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="67526-111">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 的變數</span><span class="sxs-lookup"><span data-stu-id="67526-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="67526-112">第二個命令會針對儲存在 variable $Gateway 中的虛擬網路閘道設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="67526-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="67526-113">此命令也會將 ASN 設定為1337。</span><span class="sxs-lookup"><span data-stu-id="67526-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="67526-114">參數</span><span class="sxs-lookup"><span data-stu-id="67526-114">PARAMETERS</span></span>

### <span data-ttu-id="67526-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67526-115">-AsJob</span></span>
<span data-ttu-id="67526-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67526-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67526-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="67526-117">-Asn</span></span>
<span data-ttu-id="67526-118">指定虛擬網路閘道自治系統號碼 (ASN) ，用來設定在 IPsec 隧道內 (BGP) 會話的邊界閘道通訊協定。</span><span class="sxs-lookup"><span data-stu-id="67526-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67526-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67526-119">-DefaultProfile</span></span>
<span data-ttu-id="67526-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67526-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67526-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="67526-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="67526-122">停用作用中的功能。</span><span class="sxs-lookup"><span data-stu-id="67526-122">Disables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67526-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="67526-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="67526-124">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="67526-124">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67526-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="67526-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="67526-126">指定要用於強制隧道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="67526-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="67526-127">如果指定了預設網站，閘道的虛擬私人網路 (VPN) 的所有網際網路流量都會路由到該網站。</span><span class="sxs-lookup"><span data-stu-id="67526-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67526-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="67526-128">-GatewaySku</span></span>
<span data-ttu-id="67526-129">指定虛擬網路閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="67526-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="67526-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="67526-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67526-131">空白</span><span class="sxs-lookup"><span data-stu-id="67526-131">Basic</span></span>
- <span data-ttu-id="67526-132">標準</span><span class="sxs-lookup"><span data-stu-id="67526-132">Standard</span></span>
- <span data-ttu-id="67526-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="67526-133">HighPerformance</span></span>
- <span data-ttu-id="67526-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="67526-134">VpnGw1</span></span>
- <span data-ttu-id="67526-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="67526-135">VpnGw2</span></span>
- <span data-ttu-id="67526-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="67526-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67526-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="67526-137">-PeerWeight</span></span>
<span data-ttu-id="67526-138">指定透過此虛擬網路閘道通過 BGP 瞭解的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="67526-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67526-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="67526-139">-RadiusServerAddress</span></span>
<span data-ttu-id="67526-140">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="67526-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67526-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="67526-141">-RadiusServerSecret</span></span>
<span data-ttu-id="67526-142">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="67526-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67526-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67526-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="67526-144">指定要作為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="67526-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="67526-145">您可以使用 Get-AzVirtualNetworkGateway Cmdlet 來取得虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="67526-145">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67526-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="67526-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="67526-147">指定此 Cmdlet 用來從哪個位址空間來指派 VPN 用戶端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="67526-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="67526-148">這不應與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="67526-148">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="67526-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="67526-149">-VpnClientProtocol</span></span>
<span data-ttu-id="67526-150">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="67526-150">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67526-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="67526-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="67526-152">指定已吊銷之 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="67526-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="67526-153">VPN 用戶端會移除與其中一個相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="67526-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="67526-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="67526-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="67526-155">指定要用於 VPN 用戶端驗證的 VPN 用戶端根憑證清單。</span><span class="sxs-lookup"><span data-stu-id="67526-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="67526-156">[連線 VPN 用戶端] 必須出示從這些根憑證的其中一個證書產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="67526-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="67526-157">-確認</span><span class="sxs-lookup"><span data-stu-id="67526-157">-Confirm</span></span>
<span data-ttu-id="67526-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67526-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67526-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67526-159">-WhatIf</span></span>
<span data-ttu-id="67526-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67526-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67526-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67526-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67526-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67526-162">CommonParameters</span></span>
<span data-ttu-id="67526-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67526-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67526-164">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67526-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67526-165">輸入</span><span class="sxs-lookup"><span data-stu-id="67526-165">INPUTS</span></span>

### <span data-ttu-id="67526-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67526-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="67526-167">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="67526-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="67526-168">輸出</span><span class="sxs-lookup"><span data-stu-id="67526-168">OUTPUTS</span></span>

### <span data-ttu-id="67526-169">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="67526-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="67526-170">筆記</span><span class="sxs-lookup"><span data-stu-id="67526-170">NOTES</span></span>
* <span data-ttu-id="67526-171">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="67526-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="67526-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="67526-172">RELATED LINKS</span></span>

[<span data-ttu-id="67526-173">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67526-173">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="67526-174">新-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67526-174">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="67526-175">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67526-175">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="67526-176">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67526-176">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="67526-177">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67526-177">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)



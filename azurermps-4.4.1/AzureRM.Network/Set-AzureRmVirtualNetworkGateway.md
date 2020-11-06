---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449598"
---
# <span data-ttu-id="af429-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af429-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="af429-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af429-102">SYNOPSIS</span></span>
<span data-ttu-id="af429-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="af429-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af429-104">句法</span><span class="sxs-lookup"><span data-stu-id="af429-104">SYNTAX</span></span>

### <span data-ttu-id="af429-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="af429-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af429-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="af429-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af429-107">說明</span><span class="sxs-lookup"><span data-stu-id="af429-107">DESCRIPTION</span></span>
<span data-ttu-id="af429-108">**AzureRmVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="af429-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="af429-109">示例</span><span class="sxs-lookup"><span data-stu-id="af429-109">EXAMPLES</span></span>

### <span data-ttu-id="af429-110">範例1：設定虛擬網路閘道的目標狀態</span><span class="sxs-lookup"><span data-stu-id="af429-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="af429-111">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 的變數</span><span class="sxs-lookup"><span data-stu-id="af429-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="af429-112">第二個命令會針對儲存在 variable $Gateway 中的虛擬網路閘道設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="af429-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="af429-113">此命令也會將 ASN 設定為1337。</span><span class="sxs-lookup"><span data-stu-id="af429-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="af429-114">參數</span><span class="sxs-lookup"><span data-stu-id="af429-114">PARAMETERS</span></span>

### <span data-ttu-id="af429-115">-Asn</span><span class="sxs-lookup"><span data-stu-id="af429-115">-Asn</span></span>
<span data-ttu-id="af429-116">指定虛擬網路閘道自治系統號碼 (ASN) ，用來設定在 IPsec 隧道內 (BGP) 會話的邊界閘道通訊協定。</span><span class="sxs-lookup"><span data-stu-id="af429-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="af429-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af429-117">-DefaultProfile</span></span>
<span data-ttu-id="af429-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af429-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="af429-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="af429-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="af429-120">停用作用中的功能。</span><span class="sxs-lookup"><span data-stu-id="af429-120">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="af429-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="af429-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="af429-122">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="af429-122">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="af429-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="af429-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="af429-124">指定要用於強制隧道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="af429-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="af429-125">如果指定了預設網站，閘道的虛擬私人網路 (VPN) 的所有網際網路流量都會路由到該網站。</span><span class="sxs-lookup"><span data-stu-id="af429-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="af429-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="af429-126">-GatewaySku</span></span>
<span data-ttu-id="af429-127">指定虛擬網路閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="af429-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="af429-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="af429-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af429-129">空白</span><span class="sxs-lookup"><span data-stu-id="af429-129">Basic</span></span>
- <span data-ttu-id="af429-130">標準</span><span class="sxs-lookup"><span data-stu-id="af429-130">Standard</span></span>
- <span data-ttu-id="af429-131">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="af429-131">HighPerformance</span></span>
- <span data-ttu-id="af429-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="af429-132">VpnGw1</span></span>
- <span data-ttu-id="af429-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="af429-133">VpnGw2</span></span>
- <span data-ttu-id="af429-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="af429-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af429-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="af429-135">-PeerWeight</span></span>
<span data-ttu-id="af429-136">指定透過此虛擬網路閘道通過 BGP 瞭解的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="af429-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="af429-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="af429-137">-RadiusServerAddress</span></span>
<span data-ttu-id="af429-138">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="af429-138">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="af429-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="af429-139">-RadiusServerSecret</span></span>
<span data-ttu-id="af429-140">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="af429-140">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="af429-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af429-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="af429-142">指定要作為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="af429-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="af429-143">您可以使用 Get-AzureRmVirtualNetworkGateway Cmdlet 來取得虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="af429-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="af429-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="af429-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="af429-145">指定此 Cmdlet 用來從哪個位址空間來指派 VPN 用戶端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="af429-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="af429-146">這不應與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="af429-146">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="af429-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="af429-147">-VpnClientProtocol</span></span>
<span data-ttu-id="af429-148">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="af429-148">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="af429-149">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="af429-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="af429-150">指定已吊銷之 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="af429-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="af429-151">VPN 用戶端會移除與其中一個相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="af429-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="af429-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="af429-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="af429-153">指定要用於 VPN 用戶端驗證的 VPN 用戶端根憑證清單。</span><span class="sxs-lookup"><span data-stu-id="af429-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="af429-154">[連線 VPN 用戶端] 必須出示從這些根憑證的其中一個證書產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="af429-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="af429-155">-確認</span><span class="sxs-lookup"><span data-stu-id="af429-155">-Confirm</span></span>
<span data-ttu-id="af429-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af429-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af429-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af429-157">-WhatIf</span></span>
<span data-ttu-id="af429-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af429-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af429-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af429-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af429-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af429-160">CommonParameters</span></span>
<span data-ttu-id="af429-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af429-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af429-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af429-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af429-163">輸入</span><span class="sxs-lookup"><span data-stu-id="af429-163">INPUTS</span></span>

### <span data-ttu-id="af429-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af429-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="af429-165">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="af429-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="af429-166">輸出</span><span class="sxs-lookup"><span data-stu-id="af429-166">OUTPUTS</span></span>

### <span data-ttu-id="af429-167">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af429-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="af429-168">筆記</span><span class="sxs-lookup"><span data-stu-id="af429-168">NOTES</span></span>
* <span data-ttu-id="af429-169">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="af429-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="af429-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="af429-170">RELATED LINKS</span></span>

[<span data-ttu-id="af429-171">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af429-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="af429-172">新-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af429-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="af429-173">移除-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af429-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="af429-174">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af429-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="af429-175">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="af429-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)



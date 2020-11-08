---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136256"
---
# <span data-ttu-id="520d6-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="520d6-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="520d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="520d6-102">SYNOPSIS</span></span>
<span data-ttu-id="520d6-103">這個命令可讓使用者建立 Vpn ipsec 原則物件，指定一個或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="520d6-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="520d6-104">這個命令 let 輸出物件是用來設定新的/現有閘道的 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="520d6-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="520d6-105">句法</span><span class="sxs-lookup"><span data-stu-id="520d6-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="520d6-106">說明</span><span class="sxs-lookup"><span data-stu-id="520d6-106">DESCRIPTION</span></span>
<span data-ttu-id="520d6-107">這個命令可讓使用者建立 Vpn ipsec 原則物件，指定一個或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="520d6-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="520d6-108">這個命令 let 輸出物件是用來設定新的/現有閘道的 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="520d6-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="520d6-109">示例</span><span class="sxs-lookup"><span data-stu-id="520d6-109">EXAMPLES</span></span>

### <span data-ttu-id="520d6-110">範例1：定義 vpn ipsec 原則物件：</span><span class="sxs-lookup"><span data-stu-id="520d6-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="520d6-111">這個 Cmdlet 是用來建立 vpn ipsec 原則物件，使用的是使用者可傳遞至 param 的一個或所有參數值： VpnClientIpsecPolicy (New-AzVirtualNetworkGateway 的新 VPN 閘道建立) /Set-AzVirtualNetworkGateway (在 ResourceGroup 中的現有 VPN 閘道更新) ：</span><span class="sxs-lookup"><span data-stu-id="520d6-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="520d6-112">範例2：使用設定 vpn 自訂 ipsec 原則建立新的虛擬網路閘道：</span><span class="sxs-lookup"><span data-stu-id="520d6-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="520d6-113">這個 Cmdlet 會在建立之後傳回虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="520d6-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="520d6-114">範例3：在現有的虛擬網路閘道上設定 vpn 自訂 ipsec 原則：</span><span class="sxs-lookup"><span data-stu-id="520d6-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="520d6-115">在設定 vpn 自訂 ipsec 原則之後，這個 Cmdlet 會傳回虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="520d6-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="520d6-116">範例4：取得虛擬網路閘道以查看是否正確設定 vpn 自訂原則：</span><span class="sxs-lookup"><span data-stu-id="520d6-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="520d6-117">這個 Cmdlet 會傳回虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="520d6-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="520d6-118">參數</span><span class="sxs-lookup"><span data-stu-id="520d6-118">PARAMETERS</span></span>

### <span data-ttu-id="520d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520d6-119">-DefaultProfile</span></span>
<span data-ttu-id="520d6-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="520d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="520d6-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="520d6-121">-DhGroup</span></span>
<span data-ttu-id="520d6-122">在 IKE 階段1中用於初始 SA 的 VpnClient DH 群組</span><span class="sxs-lookup"><span data-stu-id="520d6-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d6-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="520d6-123">-IkeEncryption</span></span>
<span data-ttu-id="520d6-124">VpnClient IKE 加密演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="520d6-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d6-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="520d6-125">-IkeIntegrity</span></span>
<span data-ttu-id="520d6-126">VpnClient IKE 完整性演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="520d6-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d6-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="520d6-127">-IpsecEncryption</span></span>
<span data-ttu-id="520d6-128">VpnClient IPSec 加密演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="520d6-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d6-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="520d6-129">-IpsecIntegrity</span></span>
<span data-ttu-id="520d6-130">VpnClient IPSec 完整性演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="520d6-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d6-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="520d6-131">-PfsGroup</span></span>
<span data-ttu-id="520d6-132">在適用于新的子 SA 的 IKE 階段2中使用的 VpnClient PFS 群組</span><span class="sxs-lookup"><span data-stu-id="520d6-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d6-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="520d6-133">-SADataSize</span></span>
<span data-ttu-id="520d6-134">VpnClient IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 負載大小（KB）</span><span class="sxs-lookup"><span data-stu-id="520d6-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d6-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="520d6-135">-SALifeTime</span></span>
<span data-ttu-id="520d6-136">VpnClient IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 存留期（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="520d6-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520d6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520d6-137">CommonParameters</span></span>
<span data-ttu-id="520d6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="520d6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520d6-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="520d6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520d6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="520d6-140">INPUTS</span></span>

### <span data-ttu-id="520d6-141">所有</span><span class="sxs-lookup"><span data-stu-id="520d6-141">None</span></span>

## <span data-ttu-id="520d6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="520d6-142">OUTPUTS</span></span>

### <span data-ttu-id="520d6-143">PSIpsecPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="520d6-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="520d6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="520d6-144">NOTES</span></span>

## <span data-ttu-id="520d6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="520d6-145">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904950"
---
# <span data-ttu-id="22ac2-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="22ac2-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="22ac2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="22ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="22ac2-103">此命令可讓使用者建立 Vpn ipsec 原則物件，指定一或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="22ac2-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="22ac2-104">此命令讓輸出物件用來設定新/現有閘道的 vpn ipsec 策略。</span><span class="sxs-lookup"><span data-stu-id="22ac2-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="22ac2-105">語法</span><span class="sxs-lookup"><span data-stu-id="22ac2-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22ac2-106">描述</span><span class="sxs-lookup"><span data-stu-id="22ac2-106">DESCRIPTION</span></span>
<span data-ttu-id="22ac2-107">此命令可讓使用者建立 Vpn ipsec 原則物件，指定一或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="22ac2-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="22ac2-108">此命令讓輸出物件用來設定新/現有閘道的 vpn ipsec 策略。</span><span class="sxs-lookup"><span data-stu-id="22ac2-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="22ac2-109">例子</span><span class="sxs-lookup"><span data-stu-id="22ac2-109">EXAMPLES</span></span>

### <span data-ttu-id="22ac2-110">範例 1：定義 vpn ipsec 策略物件：</span><span class="sxs-lookup"><span data-stu-id="22ac2-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="22ac2-111">此 Cmdlet 會使用傳遞的一或所有參數值來建立 vpn ipsec policy 物件，使用者可以將這些值傳遞至 param：PS 的 VpnClientIpsecPolicy 命令，讓：New-AzVirtualNetworkGateway (ResourceGroup 中的現有 VPN 閘道更新) / Set-AzVirtualNetworkGateway (現有 VPN 閘道更新) ：</span><span class="sxs-lookup"><span data-stu-id="22ac2-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="22ac2-112">範例 2：使用設定 vpn 自訂 ipsec 策略建立新虛擬網路閘道：</span><span class="sxs-lookup"><span data-stu-id="22ac2-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="22ac2-113">此 Cmdlet 在建立後會返回虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="22ac2-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="22ac2-114">範例 3：在現有的虛擬網路閘道上設定 vpn 自訂 ipsec 策略：</span><span class="sxs-lookup"><span data-stu-id="22ac2-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="22ac2-115">此 Cmdlet 在設定 vpn 自訂 ipsec 策略之後，會返回虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="22ac2-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="22ac2-116">範例 4：取得虛擬網路閘道，以查看 vpn 自訂策略設定是否正確：</span><span class="sxs-lookup"><span data-stu-id="22ac2-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="22ac2-117">此 Cmdlet 會返回虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="22ac2-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="22ac2-118">參數</span><span class="sxs-lookup"><span data-stu-id="22ac2-118">PARAMETERS</span></span>

### <span data-ttu-id="22ac2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ac2-119">-DefaultProfile</span></span>
<span data-ttu-id="22ac2-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="22ac2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22ac2-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="22ac2-121">-DhGroup</span></span>
<span data-ttu-id="22ac2-122">IKE 階段 1 中用於初始 SA 的 VpnClient DH 群組</span><span class="sxs-lookup"><span data-stu-id="22ac2-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="22ac2-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="22ac2-123">-IkeEncryption</span></span>
<span data-ttu-id="22ac2-124">IKE 階段 2 (的 VpnClient IKE 加密演算法) </span><span class="sxs-lookup"><span data-stu-id="22ac2-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="22ac2-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="22ac2-125">-IkeIntegrity</span></span>
<span data-ttu-id="22ac2-126">IKE 階段 2 (的 VpnClient IKE 完整性演算法) </span><span class="sxs-lookup"><span data-stu-id="22ac2-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="22ac2-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="22ac2-127">-IpsecEncryption</span></span>
<span data-ttu-id="22ac2-128">IKE 階段 1 (中的 VpnClient IPSec 加密演算法) </span><span class="sxs-lookup"><span data-stu-id="22ac2-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="22ac2-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="22ac2-129">-IpsecIntegrity</span></span>
<span data-ttu-id="22ac2-130">IKE 階段 1 (的 VpnClient IPSec 完整性演算法) </span><span class="sxs-lookup"><span data-stu-id="22ac2-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="22ac2-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="22ac2-131">-PfsGroup</span></span>
<span data-ttu-id="22ac2-132">新子 SA 在 IKE 階段 2 中使用的 VpnClient PFS 群組</span><span class="sxs-lookup"><span data-stu-id="22ac2-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="22ac2-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="22ac2-133">-SADataSize</span></span>
<span data-ttu-id="22ac2-134">VpnClient IPSec 安全性關聯 (稱為快速模式或階段 2 SA) KB 的負載大小</span><span class="sxs-lookup"><span data-stu-id="22ac2-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="22ac2-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="22ac2-135">-SALifeTime</span></span>
<span data-ttu-id="22ac2-136">VpnClient IPSec 安全性關聯 (稱為快速模式或階段 2 SA 生命週期) 秒</span><span class="sxs-lookup"><span data-stu-id="22ac2-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="22ac2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ac2-137">CommonParameters</span></span>
<span data-ttu-id="22ac2-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="22ac2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ac2-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="22ac2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ac2-140">輸入</span><span class="sxs-lookup"><span data-stu-id="22ac2-140">INPUTS</span></span>

### <span data-ttu-id="22ac2-141">沒有</span><span class="sxs-lookup"><span data-stu-id="22ac2-141">None</span></span>

## <span data-ttu-id="22ac2-142">輸出</span><span class="sxs-lookup"><span data-stu-id="22ac2-142">OUTPUTS</span></span>

### <span data-ttu-id="22ac2-143">Microsoft.Azure.Commands.Network.models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="22ac2-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="22ac2-144">筆記</span><span class="sxs-lookup"><span data-stu-id="22ac2-144">NOTES</span></span>

## <span data-ttu-id="22ac2-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="22ac2-145">RELATED LINKS</span></span>

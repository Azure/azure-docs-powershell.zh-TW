---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3b34fb1de6b661a622690f93808eaf0660da461b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913145"
---
# <span data-ttu-id="00d42-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00d42-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="00d42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00d42-102">SYNOPSIS</span></span>
<span data-ttu-id="00d42-103">此命令可讓使用者建立 Vpn ipsec 參數物件，指定一或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在現有的 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="00d42-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="00d42-104">語法</span><span class="sxs-lookup"><span data-stu-id="00d42-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00d42-105">描述</span><span class="sxs-lookup"><span data-stu-id="00d42-105">DESCRIPTION</span></span>
<span data-ttu-id="00d42-106">此命令可讓使用者建立 Vpn ipsec 參數物件，指定一或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在現有的 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="00d42-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="00d42-107">例子</span><span class="sxs-lookup"><span data-stu-id="00d42-107">EXAMPLES</span></span>

### <span data-ttu-id="00d42-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="00d42-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="00d42-109">New-AzVpnClientIpsecParameter Cmdlet 用來建立 vpn ipsec 參數物件，使用使用者可針對 ResourceGroup 中任何現有虛擬網路閘道所設定之傳遞的一或所有參數值。</span><span class="sxs-lookup"><span data-stu-id="00d42-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="00d42-110">此建立 VpnClientIPsecParameters 物件會傳遞至 Set-AzVpnClientIpsecParameter 命令，以在虛擬網路閘道上設定指定的 Vpn ipsec 自訂策略，如上述範例所示。</span><span class="sxs-lookup"><span data-stu-id="00d42-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="00d42-111">此命令會返回 VpnClientIPsecParameters 的物件，該物件會顯示 set 參數。</span><span class="sxs-lookup"><span data-stu-id="00d42-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="00d42-112">參數</span><span class="sxs-lookup"><span data-stu-id="00d42-112">PARAMETERS</span></span>

### <span data-ttu-id="00d42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d42-113">-DefaultProfile</span></span>
<span data-ttu-id="00d42-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00d42-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00d42-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="00d42-115">-DhGroup</span></span>
<span data-ttu-id="00d42-116">用於 IKE 階段 1 初始 SA 的 VpnClient DH 群組。</span><span class="sxs-lookup"><span data-stu-id="00d42-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="00d42-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="00d42-117">-IkeEncryption</span></span>
<span data-ttu-id="00d42-118">IKE 階段 2 (的 VpnClient IKE 加密演算法) </span><span class="sxs-lookup"><span data-stu-id="00d42-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="00d42-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="00d42-119">-IkeIntegrity</span></span>
<span data-ttu-id="00d42-120">IKE 階段 2 (的 VpnClient IKE 完整性演算法) </span><span class="sxs-lookup"><span data-stu-id="00d42-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="00d42-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="00d42-121">-IpsecEncryption</span></span>
<span data-ttu-id="00d42-122">IKE 階段 1 (中的 VpnClient IPSec 加密演算法) </span><span class="sxs-lookup"><span data-stu-id="00d42-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="00d42-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="00d42-123">-IpsecIntegrity</span></span>
<span data-ttu-id="00d42-124">IKE 階段 1 (的 VpnClient IPSec 完整性演算法) </span><span class="sxs-lookup"><span data-stu-id="00d42-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="00d42-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="00d42-125">-PfsGroup</span></span>
<span data-ttu-id="00d42-126">新子 SA 在 IKE 階段 2 中使用的 VpnClient PFS 群組</span><span class="sxs-lookup"><span data-stu-id="00d42-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="00d42-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="00d42-127">-SADataSize</span></span>
<span data-ttu-id="00d42-128">VpnClient IPSec 安全性關聯 (稱為快速模式或階段 2 SA) KB 的負載大小</span><span class="sxs-lookup"><span data-stu-id="00d42-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="00d42-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="00d42-129">-SALifeTime</span></span>
<span data-ttu-id="00d42-130">VpnClient IPSec 安全性關聯 (稱為快速模式或階段 2 SA 生命週期) 秒</span><span class="sxs-lookup"><span data-stu-id="00d42-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="00d42-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d42-131">CommonParameters</span></span>
<span data-ttu-id="00d42-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00d42-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d42-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="00d42-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d42-134">輸入</span><span class="sxs-lookup"><span data-stu-id="00d42-134">INPUTS</span></span>

### <span data-ttu-id="00d42-135">沒有</span><span class="sxs-lookup"><span data-stu-id="00d42-135">None</span></span>

## <span data-ttu-id="00d42-136">輸出</span><span class="sxs-lookup"><span data-stu-id="00d42-136">OUTPUTS</span></span>

### <span data-ttu-id="00d42-137">Microsoft.Azure.Commands.Network.models.PS VpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="00d42-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="00d42-138">筆記</span><span class="sxs-lookup"><span data-stu-id="00d42-138">NOTES</span></span>

## <span data-ttu-id="00d42-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="00d42-139">RELATED LINKS</span></span>

[<span data-ttu-id="00d42-140">Get-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00d42-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="00d42-141">Remove-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00d42-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="00d42-142">Set-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="00d42-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)

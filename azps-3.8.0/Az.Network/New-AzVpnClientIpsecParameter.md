---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: f57c3d4711fe0c05e79f0d7dbeca897475f78421
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959159"
---
# <span data-ttu-id="8d86c-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d86c-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8d86c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d86c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d86c-103">這個命令可讓使用者建立 Vpn ipsec 參數物件，指定一個或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在現有的 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="8d86c-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="8d86c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d86c-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d86c-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d86c-105">DESCRIPTION</span></span>
<span data-ttu-id="8d86c-106">這個命令可讓使用者建立 Vpn ipsec 參數物件，指定一個或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在現有的 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="8d86c-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="8d86c-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d86c-107">EXAMPLES</span></span>

### <span data-ttu-id="8d86c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8d86c-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="8d86c-109">New-AzVpnClientIpsecParameter Cmdlet 是用來建立 vpn ipsec 參數物件，其中使用的是使用者可針對 ResourceGroup 中任何現有虛擬網路閘道設定的一個或所有參數值。</span><span class="sxs-lookup"><span data-stu-id="8d86c-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="8d86c-110">這個建立的 VpnClientIPsecParameters 物件會傳遞給 Set-AzVpnClientIpsecParameter 命令，以在虛擬網路閘道上設定指定的 Vpn ipsec 自訂原則，如上述範例所示。</span><span class="sxs-lookup"><span data-stu-id="8d86c-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="8d86c-111">這個命令會傳回 VpnClientIPsecParameters 的物件，其中會顯示設定的參數。</span><span class="sxs-lookup"><span data-stu-id="8d86c-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="8d86c-112">參數</span><span class="sxs-lookup"><span data-stu-id="8d86c-112">PARAMETERS</span></span>

### <span data-ttu-id="8d86c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d86c-113">-DefaultProfile</span></span>
<span data-ttu-id="8d86c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d86c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d86c-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="8d86c-115">-DhGroup</span></span>
<span data-ttu-id="8d86c-116">在 IKE 階段1中用於初始 SA 的 VpnClient DH 群組。</span><span class="sxs-lookup"><span data-stu-id="8d86c-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="8d86c-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="8d86c-117">-IkeEncryption</span></span>
<span data-ttu-id="8d86c-118">VpnClient IKE 加密演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="8d86c-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="8d86c-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="8d86c-119">-IkeIntegrity</span></span>
<span data-ttu-id="8d86c-120">VpnClient IKE 完整性演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="8d86c-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="8d86c-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="8d86c-121">-IpsecEncryption</span></span>
<span data-ttu-id="8d86c-122">VpnClient IPSec 加密演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="8d86c-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="8d86c-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="8d86c-123">-IpsecIntegrity</span></span>
<span data-ttu-id="8d86c-124">VpnClient IPSec 完整性演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="8d86c-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="8d86c-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="8d86c-125">-PfsGroup</span></span>
<span data-ttu-id="8d86c-126">在適用于新的子 SA 的 IKE 階段2中使用的 VpnClient PFS 群組</span><span class="sxs-lookup"><span data-stu-id="8d86c-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="8d86c-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="8d86c-127">-SADataSize</span></span>
<span data-ttu-id="8d86c-128">VpnClient IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 負載大小（KB）</span><span class="sxs-lookup"><span data-stu-id="8d86c-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="8d86c-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="8d86c-129">-SALifeTime</span></span>
<span data-ttu-id="8d86c-130">VpnClient IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 存留期（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="8d86c-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="8d86c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d86c-131">CommonParameters</span></span>
<span data-ttu-id="8d86c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d86c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d86c-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d86c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d86c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8d86c-134">INPUTS</span></span>

### <span data-ttu-id="8d86c-135">所有</span><span class="sxs-lookup"><span data-stu-id="8d86c-135">None</span></span>

## <span data-ttu-id="8d86c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="8d86c-136">OUTPUTS</span></span>

### <span data-ttu-id="8d86c-137">PSVpnClientIPsecParameters 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d86c-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="8d86c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="8d86c-138">NOTES</span></span>

## <span data-ttu-id="8d86c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d86c-139">RELATED LINKS</span></span>

[<span data-ttu-id="8d86c-140">AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d86c-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8d86c-141">移除-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d86c-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8d86c-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d86c-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)

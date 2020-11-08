---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957751"
---
# <span data-ttu-id="6ef45-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="6ef45-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="6ef45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ef45-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef45-103">建立 IPSec 原則。</span><span class="sxs-lookup"><span data-stu-id="6ef45-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="6ef45-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ef45-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ef45-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ef45-105">DESCRIPTION</span></span>
<span data-ttu-id="6ef45-106">New-AzIpsecPolicy Cmdlet 會建立要在虛擬網路閘道連線中使用的 IPSec 原則建議。</span><span class="sxs-lookup"><span data-stu-id="6ef45-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="6ef45-107">示例</span><span class="sxs-lookup"><span data-stu-id="6ef45-107">EXAMPLES</span></span>

### <span data-ttu-id="6ef45-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6ef45-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="6ef45-109">建立要用於新的虛擬網路閘道連線的 IPSec 原則。</span><span class="sxs-lookup"><span data-stu-id="6ef45-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="6ef45-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ef45-110">PARAMETERS</span></span>

### <span data-ttu-id="6ef45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef45-111">-DefaultProfile</span></span>
<span data-ttu-id="6ef45-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ef45-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ef45-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="6ef45-113">-DhGroup</span></span>
<span data-ttu-id="6ef45-114">在 IKE 階段1中用於初始 SA 的 DH 群組</span><span class="sxs-lookup"><span data-stu-id="6ef45-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef45-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="6ef45-115">-IkeEncryption</span></span>
<span data-ttu-id="6ef45-116">IKE 階段 1 (ike 加密演算法) </span><span class="sxs-lookup"><span data-stu-id="6ef45-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef45-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="6ef45-117">-IkeIntegrity</span></span>
<span data-ttu-id="6ef45-118">Ike 完整性演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="6ef45-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef45-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="6ef45-119">-IpsecEncryption</span></span>
<span data-ttu-id="6ef45-120">IPSec 加密演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="6ef45-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef45-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="6ef45-121">-IpsecIntegrity</span></span>
<span data-ttu-id="6ef45-122">IPSec 完整性演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="6ef45-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef45-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="6ef45-123">-PfsGroup</span></span>
<span data-ttu-id="6ef45-124">在 IKE 階段2中針對新的子 SA 使用的 DH 群組</span><span class="sxs-lookup"><span data-stu-id="6ef45-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef45-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="6ef45-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="6ef45-126">IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 負載大小（KB）</span><span class="sxs-lookup"><span data-stu-id="6ef45-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="6ef45-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="6ef45-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="6ef45-128">IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 存留期（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="6ef45-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="6ef45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef45-129">CommonParameters</span></span>
<span data-ttu-id="6ef45-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ef45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef45-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ef45-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef45-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6ef45-132">INPUTS</span></span>

### <span data-ttu-id="6ef45-133">所有</span><span class="sxs-lookup"><span data-stu-id="6ef45-133">None</span></span>

## <span data-ttu-id="6ef45-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6ef45-134">OUTPUTS</span></span>

### <span data-ttu-id="6ef45-135">PSIpsecPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ef45-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="6ef45-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6ef45-136">NOTES</span></span>

## <span data-ttu-id="6ef45-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ef45-137">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 059f94c8289b601d5a368266310e61d665e217fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915349"
---
# <span data-ttu-id="1a6ff-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1a6ff-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="1a6ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1a6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6ff-103">建立 IPSec 策略。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="1a6ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="1a6ff-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a6ff-105">描述</span><span class="sxs-lookup"><span data-stu-id="1a6ff-105">DESCRIPTION</span></span>
<span data-ttu-id="1a6ff-106">此New-AzIpsecPolicy Cmdlet 會建立一個 IPSec 策略提案，以用於虛擬網路閘道連接。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="1a6ff-107">例子</span><span class="sxs-lookup"><span data-stu-id="1a6ff-107">EXAMPLES</span></span>

### <span data-ttu-id="1a6ff-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1a6ff-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="1a6ff-109">建立要用於新虛擬網路閘道連接的 IPSec 策略。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="1a6ff-110">參數</span><span class="sxs-lookup"><span data-stu-id="1a6ff-110">PARAMETERS</span></span>

### <span data-ttu-id="1a6ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6ff-111">-DefaultProfile</span></span>
<span data-ttu-id="1a6ff-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a6ff-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="1a6ff-113">-DhGroup</span></span>
<span data-ttu-id="1a6ff-114">IKE 階段 1 中用於初始 SA 的 DH 群組</span><span class="sxs-lookup"><span data-stu-id="1a6ff-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="1a6ff-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="1a6ff-115">-IkeEncryption</span></span>
<span data-ttu-id="1a6ff-116">IKE 加密演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="1a6ff-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="1a6ff-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="1a6ff-117">-IkeIntegrity</span></span>
<span data-ttu-id="1a6ff-118">IKE 完整性演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="1a6ff-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="1a6ff-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="1a6ff-119">-IpsecEncryption</span></span>
<span data-ttu-id="1a6ff-120">IKE 階段 2 (的 IPSec 加密演算法) </span><span class="sxs-lookup"><span data-stu-id="1a6ff-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="1a6ff-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="1a6ff-121">-IpsecIntegrity</span></span>
<span data-ttu-id="1a6ff-122">IKE 階段 2 (的 IPSec 完整性演算法) </span><span class="sxs-lookup"><span data-stu-id="1a6ff-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="1a6ff-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="1a6ff-123">-PfsGroup</span></span>
<span data-ttu-id="1a6ff-124">IKE 階段 2 中用於新子 SA 的 DH 群組</span><span class="sxs-lookup"><span data-stu-id="1a6ff-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="1a6ff-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="1a6ff-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="1a6ff-126">IPSec 安全性關聯 (稱為快速模式或階段 2 SA) KB 的負載大小</span><span class="sxs-lookup"><span data-stu-id="1a6ff-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="1a6ff-127">-SALifeTime秒</span><span class="sxs-lookup"><span data-stu-id="1a6ff-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="1a6ff-128">IPSec 安全性關聯 (稱為快速模式或階段 2 SA 生命週期) 秒</span><span class="sxs-lookup"><span data-stu-id="1a6ff-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="1a6ff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6ff-129">CommonParameters</span></span>
<span data-ttu-id="1a6ff-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6ff-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6ff-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1a6ff-132">INPUTS</span></span>

### <span data-ttu-id="1a6ff-133">沒有</span><span class="sxs-lookup"><span data-stu-id="1a6ff-133">None</span></span>

## <span data-ttu-id="1a6ff-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1a6ff-134">OUTPUTS</span></span>

### <span data-ttu-id="1a6ff-135">Microsoft.Azure.Commands.Network.models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1a6ff-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="1a6ff-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1a6ff-136">NOTES</span></span>

## <span data-ttu-id="1a6ff-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a6ff-137">RELATED LINKS</span></span>

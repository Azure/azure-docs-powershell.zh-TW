---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
ms.openlocfilehash: 642284e7e1aa732983ee660ea323707be030b640
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800786"
---
# <span data-ttu-id="fe3d9-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="fe3d9-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="fe3d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3d9-103">建立 IPSec 原則。</span><span class="sxs-lookup"><span data-stu-id="fe3d9-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe3d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe3d9-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe3d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe3d9-105">DESCRIPTION</span></span>
<span data-ttu-id="fe3d9-106">New-AzureRmIpsecPolicy Cmdlet 會建立要在虛擬網路閘道連線中使用的 IPSec 原則建議。</span><span class="sxs-lookup"><span data-stu-id="fe3d9-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="fe3d9-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe3d9-107">EXAMPLES</span></span>

### <span data-ttu-id="fe3d9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fe3d9-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="fe3d9-109">建立要用於新的虛擬網路閘道連線的 IPSec 原則。</span><span class="sxs-lookup"><span data-stu-id="fe3d9-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="fe3d9-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe3d9-110">PARAMETERS</span></span>

### <span data-ttu-id="fe3d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3d9-111">-DefaultProfile</span></span>
<span data-ttu-id="fe3d9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe3d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe3d9-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="fe3d9-113">-DhGroup</span></span>
<span data-ttu-id="fe3d9-114">在 IKE 階段1中用於初始 SA 的 DH 群組</span><span class="sxs-lookup"><span data-stu-id="fe3d9-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d9-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="fe3d9-115">-IkeEncryption</span></span>
<span data-ttu-id="fe3d9-116">IKE 階段 2 (IKE 加密演算法) </span><span class="sxs-lookup"><span data-stu-id="fe3d9-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d9-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="fe3d9-117">-IkeIntegrity</span></span>
<span data-ttu-id="fe3d9-118">IKE 完整性演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="fe3d9-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d9-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="fe3d9-119">-IpsecEncryption</span></span>
<span data-ttu-id="fe3d9-120">IPSec 加密演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="fe3d9-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d9-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="fe3d9-121">-IpsecIntegrity</span></span>
<span data-ttu-id="fe3d9-122">IPSec 完整性演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="fe3d9-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d9-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="fe3d9-123">-PfsGroup</span></span>
<span data-ttu-id="fe3d9-124">在 IKE 階段2中針對新的子 SA 使用的 DH 群組</span><span class="sxs-lookup"><span data-stu-id="fe3d9-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d9-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="fe3d9-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="fe3d9-126">IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 負載大小（KB）</span><span class="sxs-lookup"><span data-stu-id="fe3d9-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d9-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="fe3d9-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="fe3d9-128">IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 存留期（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="fe3d9-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3d9-129">CommonParameters</span></span>
<span data-ttu-id="fe3d9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe3d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3d9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe3d9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3d9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fe3d9-132">INPUTS</span></span>

### <span data-ttu-id="fe3d9-133">所有</span><span class="sxs-lookup"><span data-stu-id="fe3d9-133">None</span></span>

## <span data-ttu-id="fe3d9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="fe3d9-134">OUTPUTS</span></span>

### <span data-ttu-id="fe3d9-135">PSIpsecPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe3d9-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="fe3d9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="fe3d9-136">NOTES</span></span>

## <span data-ttu-id="fe3d9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe3d9-137">RELATED LINKS</span></span>


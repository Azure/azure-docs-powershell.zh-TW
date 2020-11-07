---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626371"
---
# <span data-ttu-id="28a4d-101">New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="28a4d-101">New-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="28a4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="28a4d-103">這個命令可讓使用者建立 Vpn ipsec 參數物件，指定一個或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在現有的 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="28a4d-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28a4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="28a4d-104">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a4d-105">說明</span><span class="sxs-lookup"><span data-stu-id="28a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="28a4d-106">這個命令可讓使用者建立 Vpn ipsec 參數物件，指定一個或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在現有的 VPN 閘道上設定。</span><span class="sxs-lookup"><span data-stu-id="28a4d-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="28a4d-107">示例</span><span class="sxs-lookup"><span data-stu-id="28a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="28a4d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="28a4d-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="28a4d-109">New-AzureRmVpnClientIpsecParameter Cmdlet 是用來建立 vpn ipsec 參數物件，其中使用的是使用者可針對 ResourceGroup 中任何現有虛擬網路閘道設定的一個或所有參數值。</span><span class="sxs-lookup"><span data-stu-id="28a4d-109">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="28a4d-110">這個建立的 VpnClientIPsecParameters 物件會傳遞給 Set-AzureRmVpnClientIpsecParameter 命令，以在虛擬網路閘道上設定指定的 Vpn ipsec 自訂原則，如上述範例所示。</span><span class="sxs-lookup"><span data-stu-id="28a4d-110">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="28a4d-111">這個命令會傳回 VpnClientIPsecParameters 的物件，其中會顯示設定的參數。</span><span class="sxs-lookup"><span data-stu-id="28a4d-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="28a4d-112">參數</span><span class="sxs-lookup"><span data-stu-id="28a4d-112">PARAMETERS</span></span>

### <span data-ttu-id="28a4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a4d-113">-DefaultProfile</span></span>
<span data-ttu-id="28a4d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28a4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a4d-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="28a4d-115">-DhGroup</span></span>
<span data-ttu-id="28a4d-116">在 IKE 階段1中用於初始 SA 的 Vpnclient DH 群組。</span><span class="sxs-lookup"><span data-stu-id="28a4d-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="28a4d-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="28a4d-117">-IkeEncryption</span></span>
<span data-ttu-id="28a4d-118">Vpnclient IKE 加密演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="28a4d-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="28a4d-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="28a4d-119">-IkeIntegrity</span></span>
<span data-ttu-id="28a4d-120">Vpnclient IKE 完整性演算法 (IKE 階段 2) </span><span class="sxs-lookup"><span data-stu-id="28a4d-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="28a4d-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="28a4d-121">-IpsecEncryption</span></span>
<span data-ttu-id="28a4d-122">Vpnclient IPSec 加密演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="28a4d-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="28a4d-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="28a4d-123">-IpsecIntegrity</span></span>
<span data-ttu-id="28a4d-124">Vpnclient IPSec 完整性演算法 (IKE 階段 1) </span><span class="sxs-lookup"><span data-stu-id="28a4d-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="28a4d-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="28a4d-125">-PfsGroup</span></span>
<span data-ttu-id="28a4d-126">在適用于新的子 SA 的 IKE 階段2中使用的 Vpnclient PFS 群組</span><span class="sxs-lookup"><span data-stu-id="28a4d-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="28a4d-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="28a4d-127">-SADataSize</span></span>
<span data-ttu-id="28a4d-128">Vpnclient IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 負載大小（KB）</span><span class="sxs-lookup"><span data-stu-id="28a4d-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="28a4d-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="28a4d-129">-SALifeTime</span></span>
<span data-ttu-id="28a4d-130">Vpnclient IPSec 安全性關聯 (也稱為 [快速模式] 或 [階段 2 SA]) 存留期（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="28a4d-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="28a4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a4d-131">CommonParameters</span></span>
<span data-ttu-id="28a4d-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28a4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a4d-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28a4d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a4d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="28a4d-134">INPUTS</span></span>

### <span data-ttu-id="28a4d-135">所有</span><span class="sxs-lookup"><span data-stu-id="28a4d-135">None</span></span>

## <span data-ttu-id="28a4d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="28a4d-136">OUTPUTS</span></span>

### <span data-ttu-id="28a4d-137">PSVpnClientIPsecParameters 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="28a4d-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="28a4d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="28a4d-138">NOTES</span></span>

## <span data-ttu-id="28a4d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="28a4d-139">RELATED LINKS</span></span>

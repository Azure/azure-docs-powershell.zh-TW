---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959865"
---
# <span data-ttu-id="db194-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="db194-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="db194-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db194-102">SYNOPSIS</span></span>
<span data-ttu-id="db194-103">設定或更新直連連線資訊。</span><span class="sxs-lookup"><span data-stu-id="db194-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="db194-104">句法</span><span class="sxs-lookup"><span data-stu-id="db194-104">SYNTAX</span></span>

### <span data-ttu-id="db194-105">頻寬 (預設) </span><span class="sxs-lookup"><span data-stu-id="db194-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db194-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="db194-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db194-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="db194-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db194-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="db194-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db194-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="db194-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db194-110">說明</span><span class="sxs-lookup"><span data-stu-id="db194-110">DESCRIPTION</span></span>
<span data-ttu-id="db194-111">與更新 AzPeering 搭配使用，這是記憶體中的作業，只會持續保持 `Update-AzPeering` 。</span><span class="sxs-lookup"><span data-stu-id="db194-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="db194-112">示例</span><span class="sxs-lookup"><span data-stu-id="db194-112">EXAMPLES</span></span>

### <span data-ttu-id="db194-113">升級頻寬</span><span class="sxs-lookup"><span data-stu-id="db194-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="db194-114">針對記憶體中對等物件的第一個連接升級頻寬。</span><span class="sxs-lookup"><span data-stu-id="db194-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="db194-115">更新 Bgp 會話位址</span><span class="sxs-lookup"><span data-stu-id="db194-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="db194-116">更新記憶體中對等物件的第一個連接的對等位址。</span><span class="sxs-lookup"><span data-stu-id="db194-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="db194-117">對等服務的更新使用</span><span class="sxs-lookup"><span data-stu-id="db194-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="db194-118">更新與對等服務搭配使用的連線</span><span class="sxs-lookup"><span data-stu-id="db194-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="db194-119">參數</span><span class="sxs-lookup"><span data-stu-id="db194-119">PARAMETERS</span></span>

### <span data-ttu-id="db194-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="db194-120">-BandwidthInMbps</span></span>
<span data-ttu-id="db194-121">此位置提供的頻寬（以 Mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="db194-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db194-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db194-122">-DefaultProfile</span></span>
<span data-ttu-id="db194-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db194-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db194-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db194-124">-InputObject</span></span>
<span data-ttu-id="db194-125">直接連接物件</span><span class="sxs-lookup"><span data-stu-id="db194-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db194-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="db194-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="db194-127">播發的最大 IPv4</span><span class="sxs-lookup"><span data-stu-id="db194-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db194-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="db194-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="db194-129">播發的最大 IPv6</span><span class="sxs-lookup"><span data-stu-id="db194-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db194-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="db194-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="db194-131">[會話] 的 [MD5 驗證金鑰]。</span><span class="sxs-lookup"><span data-stu-id="db194-131">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db194-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="db194-132">-SessionPrefixV4</span></span>
<span data-ttu-id="db194-133">點對點工作階段 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="db194-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db194-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="db194-134">-SessionPrefixV6</span></span>
<span data-ttu-id="db194-135">點對點工作階段 IPv6 位址</span><span class="sxs-lookup"><span data-stu-id="db194-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db194-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="db194-136">-UseForPeeringService</span></span>
<span data-ttu-id="db194-137">啟用以搭配 Microsoft 對等服務 (MPS) 使用。</span><span class="sxs-lookup"><span data-stu-id="db194-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db194-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db194-138">CommonParameters</span></span>
<span data-ttu-id="db194-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db194-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db194-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="db194-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db194-141">輸入</span><span class="sxs-lookup"><span data-stu-id="db194-141">INPUTS</span></span>

### <span data-ttu-id="db194-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="db194-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="db194-143">輸出</span><span class="sxs-lookup"><span data-stu-id="db194-143">OUTPUTS</span></span>

### <span data-ttu-id="db194-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="db194-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="db194-145">筆記</span><span class="sxs-lookup"><span data-stu-id="db194-145">NOTES</span></span>

## <span data-ttu-id="db194-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="db194-146">RELATED LINKS</span></span>

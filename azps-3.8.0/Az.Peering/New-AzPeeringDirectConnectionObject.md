---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798658"
---
# <span data-ttu-id="dfd4a-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="dfd4a-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="dfd4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfd4a-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd4a-103">在記憶體 PSObject 中建立，以用於建立或修改對等。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="dfd4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfd4a-104">SYNTAX</span></span>

### <span data-ttu-id="dfd4a-105">IPv4PrefixIPv6Prefix (預設) </span><span class="sxs-lookup"><span data-stu-id="dfd4a-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfd4a-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="dfd4a-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfd4a-107">說明</span><span class="sxs-lookup"><span data-stu-id="dfd4a-107">DESCRIPTION</span></span>
<span data-ttu-id="dfd4a-108">在記憶體 PSObject 中建立</span><span class="sxs-lookup"><span data-stu-id="dfd4a-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="dfd4a-109">示例</span><span class="sxs-lookup"><span data-stu-id="dfd4a-109">EXAMPLES</span></span>

### <span data-ttu-id="dfd4a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="dfd4a-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="dfd4a-111">新的本機連線</span><span class="sxs-lookup"><span data-stu-id="dfd4a-111">New local connection</span></span>

### <span data-ttu-id="dfd4a-112">範例2</span><span class="sxs-lookup"><span data-stu-id="dfd4a-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="dfd4a-113">建立直接對等連線，且已啟用對等服務並使用 Microsoft 提供的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="dfd4a-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="dfd4a-114">範例3</span><span class="sxs-lookup"><span data-stu-id="dfd4a-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="dfd4a-115">建立直接對等連線，且已啟用對等服務及對等提供的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="dfd4a-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="dfd4a-116">範例4</span><span class="sxs-lookup"><span data-stu-id="dfd4a-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="dfd4a-117">建立不含 bgp 會話 IP 位址的直接對等連接。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="dfd4a-118">對等將必須先設定 IP 位址，然後才能設定 bgp 會話。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="dfd4a-119">參數</span><span class="sxs-lookup"><span data-stu-id="dfd4a-119">PARAMETERS</span></span>

### <span data-ttu-id="dfd4a-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="dfd4a-120">-BandwidthInMbps</span></span>
<span data-ttu-id="dfd4a-121">此位置提供的頻寬（以 Mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd4a-122">-DefaultProfile</span></span>
<span data-ttu-id="dfd4a-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfd4a-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="dfd4a-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="dfd4a-125">播發的最大 IPv4</span><span class="sxs-lookup"><span data-stu-id="dfd4a-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4a-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="dfd4a-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="dfd4a-127">播發的最大 IPv6</span><span class="sxs-lookup"><span data-stu-id="dfd4a-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4a-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="dfd4a-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="dfd4a-129">[會話] 的 [MD5 驗證金鑰]。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4a-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="dfd4a-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="dfd4a-131">[啟用] 標誌，告訴 Microsoft 提供 BGP 會話位址。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4a-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="dfd4a-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="dfd4a-133">在上找到的對等資金融通 Id https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="dfd4a-133">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4a-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="dfd4a-134">-SessionPrefixV4</span></span>
<span data-ttu-id="dfd4a-135">點對點工作階段 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="dfd4a-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4a-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="dfd4a-136">-SessionPrefixV6</span></span>
<span data-ttu-id="dfd4a-137">點對點工作階段 IPv6 位址</span><span class="sxs-lookup"><span data-stu-id="dfd4a-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4a-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="dfd4a-138">-UseForPeeringService</span></span>
<span data-ttu-id="dfd4a-139">啟用以搭配 Microsoft 對等服務 (MPS) 使用。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="dfd4a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd4a-140">CommonParameters</span></span>
<span data-ttu-id="dfd4a-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd4a-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dfd4a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd4a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="dfd4a-143">INPUTS</span></span>

### <span data-ttu-id="dfd4a-144">所有</span><span class="sxs-lookup"><span data-stu-id="dfd4a-144">None</span></span>

## <span data-ttu-id="dfd4a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="dfd4a-145">OUTPUTS</span></span>

### <span data-ttu-id="dfd4a-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="dfd4a-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="dfd4a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="dfd4a-147">NOTES</span></span>

## <span data-ttu-id="dfd4a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfd4a-148">RELATED LINKS</span></span>

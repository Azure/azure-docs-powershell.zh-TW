---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 2903b06d95a053b522203e9c590fe136e02ebf83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911462"
---
# <span data-ttu-id="c2bd8-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c2bd8-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="c2bd8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c2bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="c2bd8-103">在記憶體中建立 PSObject，以用於建立或修改對等。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="c2bd8-104">語法</span><span class="sxs-lookup"><span data-stu-id="c2bd8-104">SYNTAX</span></span>

### <span data-ttu-id="c2bd8-105">IPv4PrefixIPv6Prefix (預設) </span><span class="sxs-lookup"><span data-stu-id="c2bd8-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2bd8-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="c2bd8-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2bd8-107">描述</span><span class="sxs-lookup"><span data-stu-id="c2bd8-107">DESCRIPTION</span></span>
<span data-ttu-id="c2bd8-108">在記憶體中建立 PSObject</span><span class="sxs-lookup"><span data-stu-id="c2bd8-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="c2bd8-109">例子</span><span class="sxs-lookup"><span data-stu-id="c2bd8-109">EXAMPLES</span></span>

### <span data-ttu-id="c2bd8-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c2bd8-110">Example 1</span></span>
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

<span data-ttu-id="c2bd8-111">新的本地連接</span><span class="sxs-lookup"><span data-stu-id="c2bd8-111">New local connection</span></span>

### <span data-ttu-id="c2bd8-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="c2bd8-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="c2bd8-113">使用啟用對等服務和 Microsoft 提供的 IP 位址建立直接對等連接</span><span class="sxs-lookup"><span data-stu-id="c2bd8-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="c2bd8-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="c2bd8-114">Example 3</span></span>
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

<span data-ttu-id="c2bd8-115">使用啟用對等服務和對等提供的 IP 位址建立直接對等連接</span><span class="sxs-lookup"><span data-stu-id="c2bd8-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="c2bd8-116">範例 4</span><span class="sxs-lookup"><span data-stu-id="c2bd8-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="c2bd8-117">建立沒有 bgp 會話 IP 位址的直接對等互連連接。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="c2bd8-118">對等程式必須設定 IP 位址，才能設定 bgp 會話。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="c2bd8-119">參數</span><span class="sxs-lookup"><span data-stu-id="c2bd8-119">PARAMETERS</span></span>

### <span data-ttu-id="c2bd8-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="c2bd8-120">-BandwidthInMbps</span></span>
<span data-ttu-id="c2bd8-121">此位置以 Mbps 表示的頻寬。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="c2bd8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2bd8-122">-DefaultProfile</span></span>
<span data-ttu-id="c2bd8-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2bd8-124">-MaxPrefixesAdvertvertvertIPv4</span><span class="sxs-lookup"><span data-stu-id="c2bd8-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="c2bd8-125">已公佈 IPv4 的最大值</span><span class="sxs-lookup"><span data-stu-id="c2bd8-125">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="c2bd8-126">-MaxPrefixesAdvertvertvertIPv6</span><span class="sxs-lookup"><span data-stu-id="c2bd8-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="c2bd8-127">已公佈 IPv6 的最大值</span><span class="sxs-lookup"><span data-stu-id="c2bd8-127">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="c2bd8-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="c2bd8-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="c2bd8-129">會話的 MD5 驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-129">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="c2bd8-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="c2bd8-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="c2bd8-131">啟用指示 Microsoft 提供 BGP 會話位址的標標。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

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

### <span data-ttu-id="c2bd8-132">-PeeringDBFac一Id</span><span class="sxs-lookup"><span data-stu-id="c2bd8-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="c2bd8-133">找到的對等設備識別碼 https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="c2bd8-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="c2bd8-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="c2bd8-134">-SessionPrefixV4</span></span>
<span data-ttu-id="c2bd8-135">點對點工作階段 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="c2bd8-135">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="c2bd8-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="c2bd8-136">-SessionPrefixV6</span></span>
<span data-ttu-id="c2bd8-137">點對點工作階段 IPv6 位址</span><span class="sxs-lookup"><span data-stu-id="c2bd8-137">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="c2bd8-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="c2bd8-138">-UseForPeeringService</span></span>
<span data-ttu-id="c2bd8-139">啟用以用於 MPS (Microsoft 對等) 。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="c2bd8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2bd8-140">CommonParameters</span></span>
<span data-ttu-id="c2bd8-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c2bd8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2bd8-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2bd8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2bd8-143">輸入</span><span class="sxs-lookup"><span data-stu-id="c2bd8-143">INPUTS</span></span>

### <span data-ttu-id="c2bd8-144">沒有</span><span class="sxs-lookup"><span data-stu-id="c2bd8-144">None</span></span>

## <span data-ttu-id="c2bd8-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c2bd8-145">OUTPUTS</span></span>

### <span data-ttu-id="c2bd8-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="c2bd8-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="c2bd8-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c2bd8-147">NOTES</span></span>

## <span data-ttu-id="c2bd8-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2bd8-148">RELATED LINKS</span></span>

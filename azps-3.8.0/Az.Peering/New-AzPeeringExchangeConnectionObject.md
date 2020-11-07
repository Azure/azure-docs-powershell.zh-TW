---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965920"
---
# <span data-ttu-id="251e7-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="251e7-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="251e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="251e7-102">SYNOPSIS</span></span>
<span data-ttu-id="251e7-103">在記憶體 PSObject 中建立，以用於建立或修改對等。</span><span class="sxs-lookup"><span data-stu-id="251e7-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="251e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="251e7-104">SYNTAX</span></span>

### <span data-ttu-id="251e7-105">IPv4Address (預設) </span><span class="sxs-lookup"><span data-stu-id="251e7-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="251e7-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="251e7-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="251e7-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="251e7-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="251e7-108">說明</span><span class="sxs-lookup"><span data-stu-id="251e7-108">DESCRIPTION</span></span>
<span data-ttu-id="251e7-109">在記憶體 PSObject 中建立</span><span class="sxs-lookup"><span data-stu-id="251e7-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="251e7-110">示例</span><span class="sxs-lookup"><span data-stu-id="251e7-110">EXAMPLES</span></span>

### <span data-ttu-id="251e7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="251e7-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="251e7-112">本機連線物件</span><span class="sxs-lookup"><span data-stu-id="251e7-112">Local connection object</span></span>

## <span data-ttu-id="251e7-113">參數</span><span class="sxs-lookup"><span data-stu-id="251e7-113">PARAMETERS</span></span>

### <span data-ttu-id="251e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="251e7-114">-DefaultProfile</span></span>
<span data-ttu-id="251e7-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="251e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="251e7-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="251e7-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="251e7-117">播發的最大 IPv4</span><span class="sxs-lookup"><span data-stu-id="251e7-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251e7-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="251e7-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="251e7-119">播發的最大 IPv6</span><span class="sxs-lookup"><span data-stu-id="251e7-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251e7-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="251e7-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="251e7-121">[會話] 的 [MD5 驗證金鑰]。</span><span class="sxs-lookup"><span data-stu-id="251e7-121">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251e7-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="251e7-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="251e7-123">在上找到的對等資金融通 Id https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="251e7-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="251e7-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="251e7-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="251e7-125">點對點工作階段 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="251e7-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251e7-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="251e7-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="251e7-127">點對點工作階段 IPv6 位址</span><span class="sxs-lookup"><span data-stu-id="251e7-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251e7-128">CommonParameters</span></span>
<span data-ttu-id="251e7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="251e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251e7-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="251e7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251e7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="251e7-131">INPUTS</span></span>

### <span data-ttu-id="251e7-132">所有</span><span class="sxs-lookup"><span data-stu-id="251e7-132">None</span></span>

## <span data-ttu-id="251e7-133">輸出</span><span class="sxs-lookup"><span data-stu-id="251e7-133">OUTPUTS</span></span>

### <span data-ttu-id="251e7-134">PSExchangeConnection 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="251e7-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="251e7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="251e7-135">NOTES</span></span>

## <span data-ttu-id="251e7-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="251e7-136">RELATED LINKS</span></span>

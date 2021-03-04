---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c4e57d3d7945f4ae06fc2461e660945bf7edfd6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911441"
---
# <span data-ttu-id="2c6c4-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="2c6c4-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="2c6c4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6c4-103">在記憶體中建立 PSObject，以用於建立或修改對等。</span><span class="sxs-lookup"><span data-stu-id="2c6c4-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="2c6c4-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c6c4-104">SYNTAX</span></span>

### <span data-ttu-id="2c6c4-105">IPv4Address (預設) </span><span class="sxs-lookup"><span data-stu-id="2c6c4-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6c4-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="2c6c4-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6c4-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="2c6c4-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c6c4-108">描述</span><span class="sxs-lookup"><span data-stu-id="2c6c4-108">DESCRIPTION</span></span>
<span data-ttu-id="2c6c4-109">在記憶體中建立 PSObject</span><span class="sxs-lookup"><span data-stu-id="2c6c4-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="2c6c4-110">例子</span><span class="sxs-lookup"><span data-stu-id="2c6c4-110">EXAMPLES</span></span>

### <span data-ttu-id="2c6c4-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2c6c4-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="2c6c4-112">本地連線物件</span><span class="sxs-lookup"><span data-stu-id="2c6c4-112">Local connection object</span></span>

## <span data-ttu-id="2c6c4-113">參數</span><span class="sxs-lookup"><span data-stu-id="2c6c4-113">PARAMETERS</span></span>

### <span data-ttu-id="2c6c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6c4-114">-DefaultProfile</span></span>
<span data-ttu-id="2c6c4-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c6c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c6c4-116">-MaxPrefixesAdvertvertvertIPv4</span><span class="sxs-lookup"><span data-stu-id="2c6c4-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="2c6c4-117">已公佈 IPv4 的最大值</span><span class="sxs-lookup"><span data-stu-id="2c6c4-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="2c6c4-118">-MaxPrefixesAdvertvertvertIPv6</span><span class="sxs-lookup"><span data-stu-id="2c6c4-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="2c6c4-119">已公佈 IPv6 的最大值</span><span class="sxs-lookup"><span data-stu-id="2c6c4-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="2c6c4-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="2c6c4-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="2c6c4-121">會話的 MD5 驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="2c6c4-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="2c6c4-122">-PeeringDBFac一Id</span><span class="sxs-lookup"><span data-stu-id="2c6c4-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="2c6c4-123">找到的對等設備識別碼 https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="2c6c4-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="2c6c4-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="2c6c4-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="2c6c4-125">點對點工作階段 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="2c6c4-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="2c6c4-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="2c6c4-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="2c6c4-127">點對點工作階段 IPv6 位址</span><span class="sxs-lookup"><span data-stu-id="2c6c4-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="2c6c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6c4-128">CommonParameters</span></span>
<span data-ttu-id="2c6c4-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c6c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6c4-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c6c4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6c4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2c6c4-131">INPUTS</span></span>

### <span data-ttu-id="2c6c4-132">沒有</span><span class="sxs-lookup"><span data-stu-id="2c6c4-132">None</span></span>

## <span data-ttu-id="2c6c4-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2c6c4-133">OUTPUTS</span></span>

### <span data-ttu-id="2c6c4-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="2c6c4-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="2c6c4-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2c6c4-135">NOTES</span></span>

## <span data-ttu-id="2c6c4-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c6c4-136">RELATED LINKS</span></span>

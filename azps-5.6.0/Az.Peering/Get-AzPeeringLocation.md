---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: a4367087bd248589f3345c14f6c7681be5eae9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911505"
---
# <span data-ttu-id="27c4b-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="27c4b-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="27c4b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="27c4b-103">獲得 Microsoft 提供的對等位置</span><span class="sxs-lookup"><span data-stu-id="27c4b-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="27c4b-104">語法</span><span class="sxs-lookup"><span data-stu-id="27c4b-104">SYNTAX</span></span>

### <span data-ttu-id="27c4b-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="27c4b-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27c4b-106">LocationByFac一Id</span><span class="sxs-lookup"><span data-stu-id="27c4b-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c4b-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="27c4b-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27c4b-108">描述</span><span class="sxs-lookup"><span data-stu-id="27c4b-108">DESCRIPTION</span></span>
<span data-ttu-id="27c4b-109">獲得使用者可以使用 ARM 進行連接的對等設備。</span><span class="sxs-lookup"><span data-stu-id="27c4b-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="27c4b-110">例子</span><span class="sxs-lookup"><span data-stu-id="27c4b-110">EXAMPLES</span></span>

### <span data-ttu-id="27c4b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="27c4b-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="27c4b-112">這是一份很長的位置清單。</span><span class="sxs-lookup"><span data-stu-id="27c4b-112">Its a long list of locations.</span></span> <span data-ttu-id="27c4b-113">獲得所有直接對等設備。</span><span class="sxs-lookup"><span data-stu-id="27c4b-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="27c4b-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="27c4b-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="27c4b-115">為 Hono一次獲得 Exchange 對等位置。</span><span class="sxs-lookup"><span data-stu-id="27c4b-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="27c4b-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="27c4b-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="27c4b-117">獲得對等設備識別碼 71 的 Exchange 對等位置。</span><span class="sxs-lookup"><span data-stu-id="27c4b-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="27c4b-118">參數</span><span class="sxs-lookup"><span data-stu-id="27c4b-118">PARAMETERS</span></span>

### <span data-ttu-id="27c4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c4b-119">-DefaultProfile</span></span>
<span data-ttu-id="27c4b-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="27c4b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27c4b-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="27c4b-121">-DirectPeeringType</span></span>
<span data-ttu-id="27c4b-122">選取 'Edge'、'CDN 和 'Transit'。</span><span class="sxs-lookup"><span data-stu-id="27c4b-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c4b-123">-Kind</span><span class="sxs-lookup"><span data-stu-id="27c4b-123">-Kind</span></span>
<span data-ttu-id="27c4b-124">顯示所有對等資源 ，並按類型顯示。</span><span class="sxs-lookup"><span data-stu-id="27c4b-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c4b-125">-PeeringDbFac一Id</span><span class="sxs-lookup"><span data-stu-id="27c4b-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="27c4b-126">PeeringDB.com設備識別碼</span><span class="sxs-lookup"><span data-stu-id="27c4b-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c4b-127">-對等位置</span><span class="sxs-lookup"><span data-stu-id="27c4b-127">-PeeringLocation</span></span>
<span data-ttu-id="27c4b-128">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="27c4b-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c4b-129">CommonParameters</span></span>
<span data-ttu-id="27c4b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27c4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c4b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27c4b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c4b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="27c4b-132">INPUTS</span></span>

### <span data-ttu-id="27c4b-133">沒有</span><span class="sxs-lookup"><span data-stu-id="27c4b-133">None</span></span>

## <span data-ttu-id="27c4b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="27c4b-134">OUTPUTS</span></span>

### <span data-ttu-id="27c4b-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="27c4b-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="27c4b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="27c4b-136">NOTES</span></span>

## <span data-ttu-id="27c4b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="27c4b-137">RELATED LINKS</span></span>

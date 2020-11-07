---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: cc8e0c5e4ce47b3157d5518ce1e5bc6b9919ff41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791742"
---
# <span data-ttu-id="330e1-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="330e1-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="330e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="330e1-102">SYNOPSIS</span></span>
<span data-ttu-id="330e1-103">取得 Microsoft 提供的對等位置</span><span class="sxs-lookup"><span data-stu-id="330e1-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="330e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="330e1-104">SYNTAX</span></span>

### <span data-ttu-id="330e1-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="330e1-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="330e1-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="330e1-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="330e1-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="330e1-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType] <String>
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="330e1-108">說明</span><span class="sxs-lookup"><span data-stu-id="330e1-108">DESCRIPTION</span></span>
<span data-ttu-id="330e1-109">取得使用者可與 ARM 連接的對等功能。</span><span class="sxs-lookup"><span data-stu-id="330e1-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="330e1-110">示例</span><span class="sxs-lookup"><span data-stu-id="330e1-110">EXAMPLES</span></span>

### <span data-ttu-id="330e1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="330e1-111">Example 1</span></span>
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

<span data-ttu-id="330e1-112">其位置的長清單。</span><span class="sxs-lookup"><span data-stu-id="330e1-112">Its a long list of locations.</span></span> <span data-ttu-id="330e1-113">取得所有直接對等功能。</span><span class="sxs-lookup"><span data-stu-id="330e1-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="330e1-114">範例2</span><span class="sxs-lookup"><span data-stu-id="330e1-114">Example 2</span></span>
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

<span data-ttu-id="330e1-115">取得 Honolulu 的 exchange 對等位置。</span><span class="sxs-lookup"><span data-stu-id="330e1-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="330e1-116">範例3</span><span class="sxs-lookup"><span data-stu-id="330e1-116">Example 3</span></span>
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

<span data-ttu-id="330e1-117">取得對等資金融通 id 71 的 exchange 對等位置。</span><span class="sxs-lookup"><span data-stu-id="330e1-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="330e1-118">參數</span><span class="sxs-lookup"><span data-stu-id="330e1-118">PARAMETERS</span></span>

### <span data-ttu-id="330e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="330e1-119">-DefaultProfile</span></span>
<span data-ttu-id="330e1-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="330e1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="330e1-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="330e1-121">-DirectPeeringType</span></span>
<span data-ttu-id="330e1-122">選取 [Edge]、「CDN」和「中轉」。</span><span class="sxs-lookup"><span data-stu-id="330e1-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="330e1-123">類型</span><span class="sxs-lookup"><span data-stu-id="330e1-123">-Kind</span></span>
<span data-ttu-id="330e1-124">依類型顯示所有對等資源。</span><span class="sxs-lookup"><span data-stu-id="330e1-124">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="330e1-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="330e1-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="330e1-126">PeeringDB.com 工具識別碼</span><span class="sxs-lookup"><span data-stu-id="330e1-126">The PeeringDB.com Facility ID</span></span>

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

### <span data-ttu-id="330e1-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="330e1-127">-PeeringLocation</span></span>
<span data-ttu-id="330e1-128">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="330e1-128">The location of the resource.</span></span>

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

### <span data-ttu-id="330e1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="330e1-129">CommonParameters</span></span>
<span data-ttu-id="330e1-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="330e1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="330e1-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="330e1-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="330e1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="330e1-132">INPUTS</span></span>

### <span data-ttu-id="330e1-133">所有</span><span class="sxs-lookup"><span data-stu-id="330e1-133">None</span></span>

## <span data-ttu-id="330e1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="330e1-134">OUTPUTS</span></span>

### <span data-ttu-id="330e1-135">PSPeeringLocation 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="330e1-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="330e1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="330e1-136">NOTES</span></span>

## <span data-ttu-id="330e1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="330e1-137">RELATED LINKS</span></span>

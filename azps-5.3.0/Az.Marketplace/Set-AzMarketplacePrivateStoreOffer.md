---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436455"
---
# <span data-ttu-id="4e9e2-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="4e9e2-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="4e9e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9e2-103">更新或建立私人商店優惠。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="4e9e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e9e2-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e9e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="4e9e2-106">更新或建立在租使用者範圍內建立的私人儲存方案。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="4e9e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="4e9e2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4e9e2-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="4e9e2-109">針對在 [租使用者範圍] 下建立的私人儲存，建立 [私人 + 公用計畫]。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="4e9e2-110">範例2</span><span class="sxs-lookup"><span data-stu-id="4e9e2-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="4e9e2-111">僅針對在訂閱範圍內建立的私人商店建立優惠方案。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="4e9e2-112">範例3</span><span class="sxs-lookup"><span data-stu-id="4e9e2-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="4e9e2-113">更新：針對在租使用者範圍內建立的私人儲存，提供私人 + 公用方案。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="4e9e2-114">需要 Etag。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-114">Etag is needed.</span></span>

### <span data-ttu-id="4e9e2-115">範例4</span><span class="sxs-lookup"><span data-stu-id="4e9e2-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="4e9e2-116">只有在 [訂閱範圍] 下建立的專用方案，才會提供私人儲存的更新。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="4e9e2-117">需要 Etag。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-117">Etag is needed.</span></span>


## <span data-ttu-id="4e9e2-118">參數</span><span class="sxs-lookup"><span data-stu-id="4e9e2-118">PARAMETERS</span></span>

### <span data-ttu-id="4e9e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9e2-119">-DefaultProfile</span></span>
<span data-ttu-id="4e9e2-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e9e2-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="4e9e2-121">-ETag</span></span>
<span data-ttu-id="4e9e2-122">Azure Marketplace privateStore 提供的 eTag 以進行更新</span><span class="sxs-lookup"><span data-stu-id="4e9e2-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="4e9e2-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="4e9e2-123">-OfferId</span></span>
<span data-ttu-id="4e9e2-124">所需的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="4e9e2-124">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9e2-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="4e9e2-125">-PrivateStoreId</span></span>
<span data-ttu-id="4e9e2-126">所需的 Azure Marketplace privateStore 提供</span><span class="sxs-lookup"><span data-stu-id="4e9e2-126">Required Azure Marketplace privateStore offers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9e2-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="4e9e2-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="4e9e2-128">所需的 Azure Marketplace privateStore 優惠的特定方案識別碼限制</span><span class="sxs-lookup"><span data-stu-id="4e9e2-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9e2-129">-確認</span><span class="sxs-lookup"><span data-stu-id="4e9e2-129">-Confirm</span></span>
<span data-ttu-id="4e9e2-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e9e2-131">-WhatIf</span></span>
<span data-ttu-id="4e9e2-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e9e2-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9e2-134">CommonParameters</span></span>
<span data-ttu-id="4e9e2-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9e2-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e9e2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9e2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4e9e2-137">INPUTS</span></span>

### <span data-ttu-id="4e9e2-138">所有</span><span class="sxs-lookup"><span data-stu-id="4e9e2-138">None</span></span>

## <span data-ttu-id="4e9e2-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4e9e2-139">OUTPUTS</span></span>

### <span data-ttu-id="4e9e2-140">[PrivateStore]. [PSPrivateStoreOffer]</span><span class="sxs-lookup"><span data-stu-id="4e9e2-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="4e9e2-141">筆記</span><span class="sxs-lookup"><span data-stu-id="4e9e2-141">NOTES</span></span>

## <span data-ttu-id="4e9e2-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e9e2-142">RELATED LINKS</span></span>

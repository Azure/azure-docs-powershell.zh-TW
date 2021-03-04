---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 9a2f5744f5595b7be4a0a59c3181435e4f1d0eb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916628"
---
# <span data-ttu-id="1bf00-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="1bf00-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="1bf00-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1bf00-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf00-103">更新或建立私人市面的優惠。</span><span class="sxs-lookup"><span data-stu-id="1bf00-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="1bf00-104">語法</span><span class="sxs-lookup"><span data-stu-id="1bf00-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf00-105">描述</span><span class="sxs-lookup"><span data-stu-id="1bf00-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf00-106">在租使用者範圍下建立的私人市場更新或建立優惠。</span><span class="sxs-lookup"><span data-stu-id="1bf00-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="1bf00-107">例子</span><span class="sxs-lookup"><span data-stu-id="1bf00-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf00-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1bf00-108">Example 1</span></span>
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

<span data-ttu-id="1bf00-109">針對在租使用者範圍下建立的私人市場，使用私人 + 公用方案建立優惠。</span><span class="sxs-lookup"><span data-stu-id="1bf00-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="1bf00-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="1bf00-110">Example 2</span></span>
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

<span data-ttu-id="1bf00-111">僅針對在訂閱範圍下建立的私人市/市，使用私人方案建立優惠。</span><span class="sxs-lookup"><span data-stu-id="1bf00-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="1bf00-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="1bf00-112">Example 3</span></span>
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

<span data-ttu-id="1bf00-113">更新提供在租使用者範圍下建立的私人市場之私人 + 公用方案。</span><span class="sxs-lookup"><span data-stu-id="1bf00-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="1bf00-114">需要 Etag。</span><span class="sxs-lookup"><span data-stu-id="1bf00-114">Etag is needed.</span></span>

### <span data-ttu-id="1bf00-115">範例 4</span><span class="sxs-lookup"><span data-stu-id="1bf00-115">Example 4</span></span>
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

<span data-ttu-id="1bf00-116">只有訂閱範圍下所建立之私人方案的私人市場更新優惠。</span><span class="sxs-lookup"><span data-stu-id="1bf00-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="1bf00-117">需要 Etag。</span><span class="sxs-lookup"><span data-stu-id="1bf00-117">Etag is needed.</span></span>


## <span data-ttu-id="1bf00-118">參數</span><span class="sxs-lookup"><span data-stu-id="1bf00-118">PARAMETERS</span></span>

### <span data-ttu-id="1bf00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf00-119">-DefaultProfile</span></span>
<span data-ttu-id="1bf00-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bf00-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf00-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="1bf00-121">-ETag</span></span>
<span data-ttu-id="1bf00-122">Azure Marketplace privateStore 優惠的 eTag 更新</span><span class="sxs-lookup"><span data-stu-id="1bf00-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="1bf00-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="1bf00-123">-OfferId</span></span>
<span data-ttu-id="1bf00-124">必要的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="1bf00-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="1bf00-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="1bf00-125">-PrivateStoreId</span></span>
<span data-ttu-id="1bf00-126">必要的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="1bf00-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="1bf00-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="1bf00-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="1bf00-128">必要的 Azure Marketplace privateStore 優惠的特定方案識別碼限制</span><span class="sxs-lookup"><span data-stu-id="1bf00-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="1bf00-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1bf00-129">-Confirm</span></span>
<span data-ttu-id="1bf00-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1bf00-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf00-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf00-131">-WhatIf</span></span>
<span data-ttu-id="1bf00-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1bf00-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bf00-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bf00-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf00-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf00-134">CommonParameters</span></span>
<span data-ttu-id="1bf00-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1bf00-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf00-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bf00-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf00-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1bf00-137">INPUTS</span></span>

### <span data-ttu-id="1bf00-138">沒有</span><span class="sxs-lookup"><span data-stu-id="1bf00-138">None</span></span>

## <span data-ttu-id="1bf00-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1bf00-139">OUTPUTS</span></span>

### <span data-ttu-id="1bf00-140">Microsoft.Azure.Commands.Marketplace.models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="1bf00-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="1bf00-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1bf00-141">NOTES</span></span>

## <span data-ttu-id="1bf00-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bf00-142">RELATED LINKS</span></span>

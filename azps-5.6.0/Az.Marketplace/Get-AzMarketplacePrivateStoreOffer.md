---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 3c7356768db35ce2c21499db0a94402f040b5162
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915398"
---
# <span data-ttu-id="cf270-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="cf270-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="cf270-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf270-102">SYNOPSIS</span></span>
<span data-ttu-id="cf270-103">取得一或多個私人商店的優惠。</span><span class="sxs-lookup"><span data-stu-id="cf270-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="cf270-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf270-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf270-105">描述</span><span class="sxs-lookup"><span data-stu-id="cf270-105">DESCRIPTION</span></span>
<span data-ttu-id="cf270-106">使用租使用者範圍中新增的公用 + 私人方案，取得一或多個私人商店的優惠。</span><span class="sxs-lookup"><span data-stu-id="cf270-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="cf270-107">如果訂閱識別碼為展示，請只在訂閱範圍下取得一或多個私人市面的優惠與私人方案</span><span class="sxs-lookup"><span data-stu-id="cf270-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="cf270-108">例子</span><span class="sxs-lookup"><span data-stu-id="cf270-108">EXAMPLES</span></span>

### <span data-ttu-id="cf270-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="cf270-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="cf270-110">使用租使用者範圍中新增的私人 + 公用方案取得私人市市優惠。</span><span class="sxs-lookup"><span data-stu-id="cf270-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="cf270-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="cf270-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="cf270-112">取得私人市面的優惠，只提供訂閱範圍下新增的私人方案。</span><span class="sxs-lookup"><span data-stu-id="cf270-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="cf270-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="cf270-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="cf270-114">使用租使用者範圍中新增的私人 + 公用方案取得私人市場的優惠。</span><span class="sxs-lookup"><span data-stu-id="cf270-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="cf270-115">範例 4</span><span class="sxs-lookup"><span data-stu-id="cf270-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="cf270-116">僅取得租使用者範圍中新增之私人方案的私人商店優惠。</span><span class="sxs-lookup"><span data-stu-id="cf270-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="cf270-117">參數</span><span class="sxs-lookup"><span data-stu-id="cf270-117">PARAMETERS</span></span>

### <span data-ttu-id="cf270-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf270-118">-DefaultProfile</span></span>
<span data-ttu-id="cf270-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf270-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf270-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="cf270-120">-OfferId</span></span>
<span data-ttu-id="cf270-121">必要的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="cf270-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="cf270-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="cf270-122">-PrivateStoreId</span></span>
<span data-ttu-id="cf270-123">必要的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="cf270-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="cf270-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf270-124">-SubscriptionId</span></span>
<span data-ttu-id="cf270-125">Azure Marketplace 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="cf270-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="cf270-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf270-126">CommonParameters</span></span>
<span data-ttu-id="cf270-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf270-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf270-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf270-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf270-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cf270-129">INPUTS</span></span>

### <span data-ttu-id="cf270-130">沒有</span><span class="sxs-lookup"><span data-stu-id="cf270-130">None</span></span>

## <span data-ttu-id="cf270-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cf270-131">OUTPUTS</span></span>

### <span data-ttu-id="cf270-132">Microsoft.Azure.Commands.Marketplace.models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="cf270-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="cf270-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cf270-133">NOTES</span></span>

## <span data-ttu-id="cf270-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf270-134">RELATED LINKS</span></span>

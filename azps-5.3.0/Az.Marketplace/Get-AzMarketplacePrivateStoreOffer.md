---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436456"
---
# <span data-ttu-id="9baee-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="9baee-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="9baee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9baee-102">SYNOPSIS</span></span>
<span data-ttu-id="9baee-103">取得一或多個私人商店優惠。</span><span class="sxs-lookup"><span data-stu-id="9baee-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="9baee-104">句法</span><span class="sxs-lookup"><span data-stu-id="9baee-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9baee-105">說明</span><span class="sxs-lookup"><span data-stu-id="9baee-105">DESCRIPTION</span></span>
<span data-ttu-id="9baee-106">取得一或多個私人商店提供的公用 + 私人方案（在 [租使用者範圍] 下新增）。</span><span class="sxs-lookup"><span data-stu-id="9baee-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="9baee-107">如果有提供訂閱識別碼，請在 [訂閱範圍] 底下取得一或多個私人商店提供的私人方案</span><span class="sxs-lookup"><span data-stu-id="9baee-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="9baee-108">示例</span><span class="sxs-lookup"><span data-stu-id="9baee-108">EXAMPLES</span></span>

### <span data-ttu-id="9baee-109">範例1</span><span class="sxs-lookup"><span data-stu-id="9baee-109">Example 1</span></span>
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

<span data-ttu-id="9baee-110">取得私人商店提供的私人 + 公用方案（在租使用者範圍內新增）。</span><span class="sxs-lookup"><span data-stu-id="9baee-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="9baee-111">範例2</span><span class="sxs-lookup"><span data-stu-id="9baee-111">Example 2</span></span>
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

<span data-ttu-id="9baee-112">只有在 [訂閱範圍] 下新增的私人方案，才能取得私人商店的提供。</span><span class="sxs-lookup"><span data-stu-id="9baee-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="9baee-113">範例3</span><span class="sxs-lookup"><span data-stu-id="9baee-113">Example 3</span></span>
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

<span data-ttu-id="9baee-114">取得私人商店提供的私人 + 公用方案（在租使用者範圍內新增）。</span><span class="sxs-lookup"><span data-stu-id="9baee-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="9baee-115">範例4</span><span class="sxs-lookup"><span data-stu-id="9baee-115">Example 4</span></span>
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

<span data-ttu-id="9baee-116">只有在租使用者範圍下新增私人方案，才能取得私人商店優惠。</span><span class="sxs-lookup"><span data-stu-id="9baee-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="9baee-117">參數</span><span class="sxs-lookup"><span data-stu-id="9baee-117">PARAMETERS</span></span>

### <span data-ttu-id="9baee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9baee-118">-DefaultProfile</span></span>
<span data-ttu-id="9baee-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9baee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9baee-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="9baee-120">-OfferId</span></span>
<span data-ttu-id="9baee-121">所需的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="9baee-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="9baee-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="9baee-122">-PrivateStoreId</span></span>
<span data-ttu-id="9baee-123">所需的 Azure Marketplace privateStore 提供</span><span class="sxs-lookup"><span data-stu-id="9baee-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="9baee-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9baee-124">-SubscriptionId</span></span>
<span data-ttu-id="9baee-125">Azure Marketplace 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="9baee-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="9baee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9baee-126">CommonParameters</span></span>
<span data-ttu-id="9baee-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9baee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9baee-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9baee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9baee-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9baee-129">INPUTS</span></span>

### <span data-ttu-id="9baee-130">所有</span><span class="sxs-lookup"><span data-stu-id="9baee-130">None</span></span>

## <span data-ttu-id="9baee-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9baee-131">OUTPUTS</span></span>

### <span data-ttu-id="9baee-132">[PrivateStore]. [PSPrivateStoreOffer]</span><span class="sxs-lookup"><span data-stu-id="9baee-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="9baee-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9baee-133">NOTES</span></span>

## <span data-ttu-id="9baee-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9baee-134">RELATED LINKS</span></span>

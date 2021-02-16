---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134114"
---
# <span data-ttu-id="8954c-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="8954c-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="8954c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8954c-102">SYNOPSIS</span></span>
<span data-ttu-id="8954c-103">取得一或多個私人商店優惠。</span><span class="sxs-lookup"><span data-stu-id="8954c-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="8954c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8954c-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8954c-105">說明</span><span class="sxs-lookup"><span data-stu-id="8954c-105">DESCRIPTION</span></span>
<span data-ttu-id="8954c-106">取得一或多個私人商店提供的公用 + 私人方案（在 [租使用者範圍] 下新增）。</span><span class="sxs-lookup"><span data-stu-id="8954c-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="8954c-107">如果有提供訂閱識別碼，請在 [訂閱範圍] 底下取得一或多個私人商店提供的私人方案</span><span class="sxs-lookup"><span data-stu-id="8954c-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="8954c-108">示例</span><span class="sxs-lookup"><span data-stu-id="8954c-108">EXAMPLES</span></span>

### <span data-ttu-id="8954c-109">範例1</span><span class="sxs-lookup"><span data-stu-id="8954c-109">Example 1</span></span>
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

<span data-ttu-id="8954c-110">取得私人商店提供的私人 + 公用方案（在租使用者範圍內新增）。</span><span class="sxs-lookup"><span data-stu-id="8954c-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="8954c-111">範例2</span><span class="sxs-lookup"><span data-stu-id="8954c-111">Example 2</span></span>
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

<span data-ttu-id="8954c-112">只有在 [訂閱範圍] 下新增的私人方案，才能取得私人商店的提供。</span><span class="sxs-lookup"><span data-stu-id="8954c-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="8954c-113">範例3</span><span class="sxs-lookup"><span data-stu-id="8954c-113">Example 3</span></span>
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

<span data-ttu-id="8954c-114">取得私人商店提供的私人 + 公用方案（在租使用者範圍內新增）。</span><span class="sxs-lookup"><span data-stu-id="8954c-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="8954c-115">範例4</span><span class="sxs-lookup"><span data-stu-id="8954c-115">Example 4</span></span>
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

<span data-ttu-id="8954c-116">只有在租使用者範圍下新增私人方案，才能取得私人商店優惠。</span><span class="sxs-lookup"><span data-stu-id="8954c-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="8954c-117">參數</span><span class="sxs-lookup"><span data-stu-id="8954c-117">PARAMETERS</span></span>

### <span data-ttu-id="8954c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8954c-118">-DefaultProfile</span></span>
<span data-ttu-id="8954c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8954c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8954c-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="8954c-120">-OfferId</span></span>
<span data-ttu-id="8954c-121">所需的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="8954c-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="8954c-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="8954c-122">-PrivateStoreId</span></span>
<span data-ttu-id="8954c-123">所需的 Azure Marketplace privateStore 提供</span><span class="sxs-lookup"><span data-stu-id="8954c-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="8954c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8954c-124">-SubscriptionId</span></span>
<span data-ttu-id="8954c-125">Azure Marketplace 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="8954c-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="8954c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8954c-126">CommonParameters</span></span>
<span data-ttu-id="8954c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8954c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8954c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8954c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8954c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8954c-129">INPUTS</span></span>

### <span data-ttu-id="8954c-130">所有</span><span class="sxs-lookup"><span data-stu-id="8954c-130">None</span></span>

## <span data-ttu-id="8954c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8954c-131">OUTPUTS</span></span>

### <span data-ttu-id="8954c-132">[PrivateStore]. [PSPrivateStoreOffer]</span><span class="sxs-lookup"><span data-stu-id="8954c-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="8954c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8954c-133">NOTES</span></span>

## <span data-ttu-id="8954c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8954c-134">RELATED LINKS</span></span>

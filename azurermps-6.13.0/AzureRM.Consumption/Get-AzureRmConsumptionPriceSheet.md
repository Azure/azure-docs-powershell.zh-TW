---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionPriceSheet.md
ms.openlocfilehash: 46e38df713483b60735247c7fafe984fc5fb6d52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447399"
---
# <span data-ttu-id="5ba53-101">Get-AzureRmConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="5ba53-101">Get-AzureRmConsumptionPriceSheet</span></span>

## <span data-ttu-id="5ba53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ba53-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba53-103">取得訂閱的價格表。</span><span class="sxs-lookup"><span data-stu-id="5ba53-103">Get price sheets of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ba53-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ba53-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba53-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ba53-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba53-106">**AzureRmConsumptionPriceSheet** Cmdlet 會取得訂閱的價格表。</span><span class="sxs-lookup"><span data-stu-id="5ba53-106">The **Get-AzureRmConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="5ba53-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ba53-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba53-108">範例1：取得價格表</span><span class="sxs-lookup"><span data-stu-id="5ba53-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="5ba53-109">範例2：使用展開 MeterDetails 來取得價格表</span><span class="sxs-lookup"><span data-stu-id="5ba53-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="5ba53-110">範例3：取得 BillingPeriodName 的價格表</span><span class="sxs-lookup"><span data-stu-id="5ba53-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### <span data-ttu-id="5ba53-111">範例4：取得前5筆的價目表記錄</span><span class="sxs-lookup"><span data-stu-id="5ba53-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## <span data-ttu-id="5ba53-112">參數</span><span class="sxs-lookup"><span data-stu-id="5ba53-112">PARAMETERS</span></span>

### <span data-ttu-id="5ba53-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="5ba53-113">-BillingPeriodName</span></span>
<span data-ttu-id="5ba53-114">特定帳單期間的名稱，以取得與相關聯的價格表。</span><span class="sxs-lookup"><span data-stu-id="5ba53-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="5ba53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba53-115">-DefaultProfile</span></span>
<span data-ttu-id="5ba53-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ba53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba53-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="5ba53-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="5ba53-118">展開 [以 MeterDetails 為基礎的價格表]。</span><span class="sxs-lookup"><span data-stu-id="5ba53-118">Expand the price sheets based on MeterDetails.</span></span>

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

### <span data-ttu-id="5ba53-119">-上方</span><span class="sxs-lookup"><span data-stu-id="5ba53-119">-Top</span></span>
<span data-ttu-id="5ba53-120">決定要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="5ba53-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba53-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba53-121">CommonParameters</span></span>
<span data-ttu-id="5ba53-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ba53-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba53-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ba53-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba53-124">輸入</span><span class="sxs-lookup"><span data-stu-id="5ba53-124">INPUTS</span></span>

### <span data-ttu-id="5ba53-125">所有</span><span class="sxs-lookup"><span data-stu-id="5ba53-125">None</span></span>

## <span data-ttu-id="5ba53-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5ba53-126">OUTPUTS</span></span>

### <span data-ttu-id="5ba53-127">PSPriceSheet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ba53-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="5ba53-128">筆記</span><span class="sxs-lookup"><span data-stu-id="5ba53-128">NOTES</span></span>

## <span data-ttu-id="5ba53-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ba53-129">RELATED LINKS</span></span>

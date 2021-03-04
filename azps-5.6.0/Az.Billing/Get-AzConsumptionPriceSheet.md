---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: 601048df040ed317f158d473ac484ce53529d20a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908321"
---
# <span data-ttu-id="b7b05-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="b7b05-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="b7b05-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7b05-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b05-103">取得訂閱的價格表。</span><span class="sxs-lookup"><span data-stu-id="b7b05-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="b7b05-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7b05-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b05-105">描述</span><span class="sxs-lookup"><span data-stu-id="b7b05-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b05-106">**Get-AzConsumptionPriceSheet** Cmdlet 會取得訂閱的價格表。</span><span class="sxs-lookup"><span data-stu-id="b7b05-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="b7b05-107">例子</span><span class="sxs-lookup"><span data-stu-id="b7b05-107">EXAMPLES</span></span>

### <span data-ttu-id="b7b05-108">範例 1：取得價格表</span><span class="sxs-lookup"><span data-stu-id="b7b05-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet
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

### <span data-ttu-id="b7b05-109">範例 2：使用展開的 MeterDetails 取得價格表</span><span class="sxs-lookup"><span data-stu-id="b7b05-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -ExpandMeterDetail
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

### <span data-ttu-id="b7b05-110">範例 3：取得 BillingPeriodName 的價格表</span><span class="sxs-lookup"><span data-stu-id="b7b05-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -BillingPeriodName 201712
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

### <span data-ttu-id="b7b05-111">範例 4：取得價格工作表的前 5 個記錄</span><span class="sxs-lookup"><span data-stu-id="b7b05-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -Top 5
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

## <span data-ttu-id="b7b05-112">參數</span><span class="sxs-lookup"><span data-stu-id="b7b05-112">PARAMETERS</span></span>

### <span data-ttu-id="b7b05-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="b7b05-113">-BillingPeriodName</span></span>
<span data-ttu-id="b7b05-114">取得與價格表相關聯的特定計費期間名稱。</span><span class="sxs-lookup"><span data-stu-id="b7b05-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="b7b05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b05-115">-DefaultProfile</span></span>
<span data-ttu-id="b7b05-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7b05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7b05-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="b7b05-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="b7b05-118">根據計量表詳細資料展開價格表。</span><span class="sxs-lookup"><span data-stu-id="b7b05-118">Expand the price sheets based on MeterDetails.</span></span>

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

### <span data-ttu-id="b7b05-119">-頂端</span><span class="sxs-lookup"><span data-stu-id="b7b05-119">-Top</span></span>
<span data-ttu-id="b7b05-120">決定要退回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="b7b05-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="b7b05-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b05-121">CommonParameters</span></span>
<span data-ttu-id="b7b05-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7b05-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b05-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b7b05-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b05-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b7b05-124">INPUTS</span></span>

### <span data-ttu-id="b7b05-125">沒有</span><span class="sxs-lookup"><span data-stu-id="b7b05-125">None</span></span>

## <span data-ttu-id="b7b05-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b7b05-126">OUTPUTS</span></span>

### <span data-ttu-id="b7b05-127">Microsoft.Azure.Commands.Consumption.models.PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="b7b05-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="b7b05-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b7b05-128">NOTES</span></span>

## <span data-ttu-id="b7b05-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7b05-129">RELATED LINKS</span></span>

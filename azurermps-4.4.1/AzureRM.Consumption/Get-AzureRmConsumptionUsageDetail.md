---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: f8347fca355080f11e69bae9793cc0367325ce98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626335"
---
# <span data-ttu-id="acc26-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="acc26-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="acc26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acc26-102">SYNOPSIS</span></span>
<span data-ttu-id="acc26-103">取得訂閱的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="acc26-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acc26-104">句法</span><span class="sxs-lookup"><span data-stu-id="acc26-104">SYNTAX</span></span>

### <span data-ttu-id="acc26-105">訂閱 (預設) </span><span class="sxs-lookup"><span data-stu-id="acc26-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc26-106">之</span><span class="sxs-lookup"><span data-stu-id="acc26-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc26-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="acc26-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc26-108">說明</span><span class="sxs-lookup"><span data-stu-id="acc26-108">DESCRIPTION</span></span>
<span data-ttu-id="acc26-109">**AzureRmConsumptionUsageDetail** Cmdlet 會取得訂閱的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="acc26-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="acc26-110">示例</span><span class="sxs-lookup"><span data-stu-id="acc26-110">EXAMPLES</span></span>

### <span data-ttu-id="acc26-111">範例1</span><span class="sxs-lookup"><span data-stu-id="acc26-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="acc26-112">取得指定名稱的發票使用狀況詳細資料，並在結果中包含 MeterDetails 屬性。</span><span class="sxs-lookup"><span data-stu-id="acc26-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="acc26-113">範例2</span><span class="sxs-lookup"><span data-stu-id="acc26-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="acc26-114">以指定名稱取得計費期間的使用狀況詳細資料，並在結果中包含 AdditionalProperties 屬性。</span><span class="sxs-lookup"><span data-stu-id="acc26-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="acc26-115">範例3</span><span class="sxs-lookup"><span data-stu-id="acc26-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="acc26-116">取得2017-01-17 至2017-01-19 之間之訂閱的使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="acc26-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="acc26-117">參數</span><span class="sxs-lookup"><span data-stu-id="acc26-117">PARAMETERS</span></span>

### <span data-ttu-id="acc26-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="acc26-118">-BillingPeriodName</span></span>
<span data-ttu-id="acc26-119">特定帳單期間的名稱，以取得與相關聯的使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="acc26-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc26-120">-結束日期</span><span class="sxs-lookup"><span data-stu-id="acc26-120">-EndDate</span></span>
<span data-ttu-id="acc26-121">使用方式之 UTC) 的 [結束日期] (。</span><span class="sxs-lookup"><span data-stu-id="acc26-121">The end date (in UTC) of the usages.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc26-122">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="acc26-122">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="acc26-123">在用法中包含其他屬性。</span><span class="sxs-lookup"><span data-stu-id="acc26-123">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="acc26-124">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="acc26-124">-IncludeMeterDetails</span></span>
<span data-ttu-id="acc26-125">在用法中包含測光的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="acc26-125">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="acc26-126">-InvoiceName</span><span class="sxs-lookup"><span data-stu-id="acc26-126">-InvoiceName</span></span>
<span data-ttu-id="acc26-127">特定發票的名稱，以取得與相關聯的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="acc26-127">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc26-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="acc26-128">-MaxCount</span></span>
<span data-ttu-id="acc26-129">決定要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="acc26-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="acc26-130">-開始日期</span><span class="sxs-lookup"><span data-stu-id="acc26-130">-StartDate</span></span>
<span data-ttu-id="acc26-131">使用方式 (UTC) 的開始日期。</span><span class="sxs-lookup"><span data-stu-id="acc26-131">The start date (in UTC) of the usages.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc26-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc26-132">-DefaultProfile</span></span>
<span data-ttu-id="acc26-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acc26-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc26-134">CommonParameters</span></span>
<span data-ttu-id="acc26-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acc26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc26-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acc26-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc26-137">輸入</span><span class="sxs-lookup"><span data-stu-id="acc26-137">INPUTS</span></span>

### <span data-ttu-id="acc26-138">所有</span><span class="sxs-lookup"><span data-stu-id="acc26-138">None</span></span>

## <span data-ttu-id="acc26-139">輸出</span><span class="sxs-lookup"><span data-stu-id="acc26-139">OUTPUTS</span></span>

### <span data-ttu-id="acc26-140">[System.object]。清單 ' 1 [PSUsageDetail，0.1.0.0，，，Culture = 中性，PublicKeyToken = null]」））））。）</span><span class="sxs-lookup"><span data-stu-id="acc26-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="acc26-141">筆記</span><span class="sxs-lookup"><span data-stu-id="acc26-141">NOTES</span></span>

## <span data-ttu-id="acc26-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="acc26-142">RELATED LINKS</span></span>


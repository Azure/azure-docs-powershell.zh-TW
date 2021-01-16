---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: 0dfdec27fe53aaf40ebd46a2c623047381faa554
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446776"
---
# <span data-ttu-id="7c02d-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="7c02d-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="7c02d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c02d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c02d-103">取得訂閱的市場。</span><span class="sxs-lookup"><span data-stu-id="7c02d-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="7c02d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c02d-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c02d-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c02d-105">DESCRIPTION</span></span>
<span data-ttu-id="7c02d-106">**AzConsumptionMarketplace** Cmdlet 會取得訂閱的市場。</span><span class="sxs-lookup"><span data-stu-id="7c02d-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="7c02d-107">示例</span><span class="sxs-lookup"><span data-stu-id="7c02d-107">EXAMPLES</span></span>

### <span data-ttu-id="7c02d-108">範例1：取得市場使用量</span><span class="sxs-lookup"><span data-stu-id="7c02d-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

### <span data-ttu-id="7c02d-109">範例2：使用日期範圍取得 marketplace 使用量</span><span class="sxs-lookup"><span data-stu-id="7c02d-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1/providers/Microsoft.Consumption/marketplaces/0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-01-04T00:00:00Z
UsageStart:  2018-01-03T00:00:00Z
```

### <span data-ttu-id="7c02d-110">範例3：取得 BillingPeriodName 的 marketplace 使用量</span><span class="sxs-lookup"><span data-stu-id="7c02d-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1/providers/Microsoft.Consumption/marketplaces/ea82233a-9f76-7eaa-4478-42bd61cf6287
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  ea82233a-9f76-7eaa-4478-42bd61cf6287
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2017-10-29T00:00:00Z
UsageStart:  2017-10-28T00:00:00Z
```

### <span data-ttu-id="7c02d-111">範例4：使用 InstanceName 篩選取得 marketplace 的使用方式</span><span class="sxs-lookup"><span data-stu-id="7c02d-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -InstanceName TestVM -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

## <span data-ttu-id="7c02d-112">參數</span><span class="sxs-lookup"><span data-stu-id="7c02d-112">PARAMETERS</span></span>

### <span data-ttu-id="7c02d-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="7c02d-113">-BillingPeriodName</span></span>
<span data-ttu-id="7c02d-114">要取得關聯之市場之特定帳單期間的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c02d-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="7c02d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c02d-115">-DefaultProfile</span></span>
<span data-ttu-id="7c02d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c02d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c02d-117">-結束日期</span><span class="sxs-lookup"><span data-stu-id="7c02d-117">-EndDate</span></span>
<span data-ttu-id="7c02d-118">要篩選之市場之 [UTC]) 的 [結束日期] (。</span><span class="sxs-lookup"><span data-stu-id="7c02d-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="7c02d-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="7c02d-119">-InstanceId</span></span>
<span data-ttu-id="7c02d-120">要篩選之市場的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c02d-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="7c02d-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7c02d-121">-InstanceName</span></span>
<span data-ttu-id="7c02d-122">要篩選之市場的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="7c02d-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="7c02d-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7c02d-123">-ResourceGroup</span></span>
<span data-ttu-id="7c02d-124">要篩選之市場的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="7c02d-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="7c02d-125">-開始日期</span><span class="sxs-lookup"><span data-stu-id="7c02d-125">-StartDate</span></span>
<span data-ttu-id="7c02d-126">要篩選之市場的 [開始日期] (（UTC) ）。</span><span class="sxs-lookup"><span data-stu-id="7c02d-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="7c02d-127">-上方</span><span class="sxs-lookup"><span data-stu-id="7c02d-127">-Top</span></span>
<span data-ttu-id="7c02d-128">決定要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="7c02d-128">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="7c02d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c02d-129">CommonParameters</span></span>
<span data-ttu-id="7c02d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c02d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c02d-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c02d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c02d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7c02d-132">INPUTS</span></span>

### <span data-ttu-id="7c02d-133">所有</span><span class="sxs-lookup"><span data-stu-id="7c02d-133">None</span></span>

## <span data-ttu-id="7c02d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7c02d-134">OUTPUTS</span></span>

### <span data-ttu-id="7c02d-135">PSMarketplace 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7c02d-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="7c02d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7c02d-136">NOTES</span></span>

## <span data-ttu-id="7c02d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c02d-137">RELATED LINKS</span></span>

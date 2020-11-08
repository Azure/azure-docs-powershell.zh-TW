---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 8eeee753fda32f40dfabf156b352724b0bd87b92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129643"
---
# <span data-ttu-id="52415-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="52415-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="52415-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52415-102">SYNOPSIS</span></span>
<span data-ttu-id="52415-103">取得訂閱的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="52415-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="52415-104">句法</span><span class="sxs-lookup"><span data-stu-id="52415-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52415-105">說明</span><span class="sxs-lookup"><span data-stu-id="52415-105">DESCRIPTION</span></span>
<span data-ttu-id="52415-106">**AzConsumptionUsageDetail** Cmdlet 會取得訂閱的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="52415-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="52415-107">示例</span><span class="sxs-lookup"><span data-stu-id="52415-107">EXAMPLES</span></span>

### <span data-ttu-id="52415-108">範例1：使用 [展開 MeterDetails] 來取得使用狀況詳細資料</span><span class="sxs-lookup"><span data-stu-id="52415-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -Expand MeterDetails -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
ConsumedService:  Microsoft.Compute
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/usageDetails/24b9dff0-f022-55a1-886b-17b330000db3
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/MAR-CCM/providers/Microsoft.Compute/disks/mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
InstanceLocation:  usnorthcentral
InstanceName:  mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
IsEstimated:  true
MeterDetails:  MeterCategory:  Data Management
               MeterLocation:  usnorthcentral
               MeterName:  Standard Managed Disk Operations (in 10,000s)
               MeterSubCategory:  Data Management
               Unit:  Operations
MeterId:  82cd70ab-1aee-4b30-bc04-8b71e1204dbc
Name:  24b9dff0-f022-55a1-886b-17b330000db3
PretaxCost:  0
Product:  Data Management Standard Managed Disk Operations
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  6/1/2018 11:59:59 PM
UsageQuantity:  3.8218
UsageStart:  6/1/2018 12:00:00 AM
```

### <span data-ttu-id="52415-109">範例2：取得日期範圍的使用狀況詳細資料</span><span class="sxs-lookup"><span data-stu-id="52415-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/732582e5-40ad-bb23-7a69-ca1ff7c8b004
InstanceId:  storsimplezc9q6r2t7f
InstanceLocation:  US West Central
InstanceName:  storsimplezc9q6r2t7f
IsEstimated:  false
MeterId:  ad22fac8-9da5-4577-8683-56ae94d39e42
Name:  732582e5-40ad-bb23-7a69-ca1ff7c8b004
PretaxCost:  0
Product:  Data Management Geo Redundant Standard IO - Table Write
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/2/2017 11:59:59 PM
UsageQuantity:  0.0006
UsageStart:  10/2/2017 12:00:00 AM
```

### <span data-ttu-id="52415-110">範例3：使用 InstanceName 篩選取得 BillingPeriodName 的使用狀況詳細資料</span><span class="sxs-lookup"><span data-stu-id="52415-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Microsoft.Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/8abc8b65-e8f1-31e1-f02b-058a7572363f
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/securitydata/providers/Microsoft.Storage/storageAccounts/1c2052westus
InstanceLocation:  uswest
InstanceName:  1c2052westus
IsEstimated:  false
MeterId:  9995d93a-7d35-4d3f-9c69-7a7fea447ef4
Name:  8abc8b65-e8f1-31e1-f02b-058a7572363f
PretaxCost:  0.000000693016692
Product:  Data Transfer Out - Zone 1
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/1/2017 11:59:59 PM
UsageQuantity:  0.000009
UsageStart:  10/1/2017 12:00:00 AM
```

## <span data-ttu-id="52415-111">參數</span><span class="sxs-lookup"><span data-stu-id="52415-111">PARAMETERS</span></span>

### <span data-ttu-id="52415-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="52415-112">-BillingPeriodName</span></span>
<span data-ttu-id="52415-113">特定帳單期間的名稱，以取得與相關聯的使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="52415-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="52415-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52415-114">-DefaultProfile</span></span>
<span data-ttu-id="52415-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52415-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52415-116">-結束日期</span><span class="sxs-lookup"><span data-stu-id="52415-116">-EndDate</span></span>
<span data-ttu-id="52415-117">要篩選的使用方式 (UTC) 的結束日期。</span><span class="sxs-lookup"><span data-stu-id="52415-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="52415-118">-展開</span><span class="sxs-lookup"><span data-stu-id="52415-118">-Expand</span></span>
<span data-ttu-id="52415-119">根據 MeterDetails 或 AdditionalInfo 展開使用實例。</span><span class="sxs-lookup"><span data-stu-id="52415-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="52415-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="52415-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="52415-121">在用法中包含其他屬性。</span><span class="sxs-lookup"><span data-stu-id="52415-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="52415-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="52415-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="52415-123">在用法中包含測光的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="52415-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="52415-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="52415-124">-InstanceId</span></span>
<span data-ttu-id="52415-125">要篩選之用法的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="52415-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="52415-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="52415-126">-InstanceName</span></span>
<span data-ttu-id="52415-127">要篩選之用法的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="52415-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="52415-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="52415-128">-MaxCount</span></span>
<span data-ttu-id="52415-129">決定要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="52415-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="52415-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52415-130">-ResourceGroup</span></span>
<span data-ttu-id="52415-131">要篩選之使用方式的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="52415-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="52415-132">-開始日期</span><span class="sxs-lookup"><span data-stu-id="52415-132">-StartDate</span></span>
<span data-ttu-id="52415-133">要篩選的使用方式在 UTC) 中 (開始日期。</span><span class="sxs-lookup"><span data-stu-id="52415-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="52415-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="52415-134">-Tag</span></span>
<span data-ttu-id="52415-135">要篩選的用法標記。</span><span class="sxs-lookup"><span data-stu-id="52415-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="52415-136">-上方</span><span class="sxs-lookup"><span data-stu-id="52415-136">-Top</span></span>
<span data-ttu-id="52415-137">決定要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="52415-137">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="52415-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52415-138">CommonParameters</span></span>
<span data-ttu-id="52415-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52415-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52415-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52415-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52415-141">輸入</span><span class="sxs-lookup"><span data-stu-id="52415-141">INPUTS</span></span>

### <span data-ttu-id="52415-142">所有</span><span class="sxs-lookup"><span data-stu-id="52415-142">None</span></span>

## <span data-ttu-id="52415-143">輸出</span><span class="sxs-lookup"><span data-stu-id="52415-143">OUTPUTS</span></span>

### <span data-ttu-id="52415-144">PSUsageDetail 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52415-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="52415-145">筆記</span><span class="sxs-lookup"><span data-stu-id="52415-145">NOTES</span></span>

## <span data-ttu-id="52415-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="52415-146">RELATED LINKS</span></span>

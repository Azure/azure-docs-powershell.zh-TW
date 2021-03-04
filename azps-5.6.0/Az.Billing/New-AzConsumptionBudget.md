---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 698f4c19b7747ae39495c1893e7a715ca5750be1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909782"
---
# <span data-ttu-id="ef188-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="ef188-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="ef188-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef188-102">SYNOPSIS</span></span>
<span data-ttu-id="ef188-103">在訂閱或資源群組中建立預算。</span><span class="sxs-lookup"><span data-stu-id="ef188-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="ef188-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef188-104">SYNTAX</span></span>

### <span data-ttu-id="ef188-105">訂閱 (預設) </span><span class="sxs-lookup"><span data-stu-id="ef188-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef188-106">通知</span><span class="sxs-lookup"><span data-stu-id="ef188-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef188-107">描述</span><span class="sxs-lookup"><span data-stu-id="ef188-107">DESCRIPTION</span></span>
<span data-ttu-id="ef188-108">Cmdlet New-AzConsumptionBudget訂閱或資源群組中建立預算。</span><span class="sxs-lookup"><span data-stu-id="ef188-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="ef188-109">例子</span><span class="sxs-lookup"><span data-stu-id="ef188-109">EXAMPLES</span></span>

### <span data-ttu-id="ef188-110">範例 1：在訂閱層級使用預算名稱建立成本預算</span><span class="sxs-lookup"><span data-stu-id="ef188-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="ef188-111">範例 2：在資源群組層級使用預算名稱建立成本預算</span><span class="sxs-lookup"><span data-stu-id="ef188-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="ef188-112">參數</span><span class="sxs-lookup"><span data-stu-id="ef188-112">PARAMETERS</span></span>

### <span data-ttu-id="ef188-113">-金額</span><span class="sxs-lookup"><span data-stu-id="ef188-113">-Amount</span></span>
<span data-ttu-id="ef188-114">預算金額。</span><span class="sxs-lookup"><span data-stu-id="ef188-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-115">-類別</span><span class="sxs-lookup"><span data-stu-id="ef188-115">-Category</span></span>
<span data-ttu-id="ef188-116">預算類別可以是成本或使用量。</span><span class="sxs-lookup"><span data-stu-id="ef188-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="ef188-117">-ContactEmail</span></span>
<span data-ttu-id="ef188-118">要傳送預算通知的電子郵件地址，以在超過閾值時傳送。</span><span class="sxs-lookup"><span data-stu-id="ef188-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="ef188-119">-ContactGroup</span></span>
<span data-ttu-id="ef188-120">超出閾值時傳送預算通知的動作群組。</span><span class="sxs-lookup"><span data-stu-id="ef188-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="ef188-121">-ContactRole</span></span>
<span data-ttu-id="ef188-122">與角色聯繫，以在超過閾值時傳送預算通知。</span><span class="sxs-lookup"><span data-stu-id="ef188-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef188-123">-DefaultProfile</span></span>
<span data-ttu-id="ef188-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef188-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef188-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ef188-125">-EndDate</span></span>
<span data-ttu-id="ef188-126">以 UTC (YYYY-MM-DD 的結束日期) 預算期間。</span><span class="sxs-lookup"><span data-stu-id="ef188-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="ef188-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="ef188-127">-MeterFilter</span></span>
<span data-ttu-id="ef188-128">要篩選的公尺逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="ef188-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="ef188-129">類別為使用量時為必填項。</span><span class="sxs-lookup"><span data-stu-id="ef188-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef188-130">-Name</span></span>
<span data-ttu-id="ef188-131">預算名稱。</span><span class="sxs-lookup"><span data-stu-id="ef188-131">Name of a budget.</span></span>

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

### <span data-ttu-id="ef188-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="ef188-132">-NotificationEnabled</span></span>
<span data-ttu-id="ef188-133">通知已啟用或不啟用。</span><span class="sxs-lookup"><span data-stu-id="ef188-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="ef188-134">-NotificationKey</span></span>
<span data-ttu-id="ef188-135">與預算關聯的通知金鑰，建立通知時必須啟用通知切換、通知門檻、連絡人電子郵件、連絡人群組或連絡人角色。</span><span class="sxs-lookup"><span data-stu-id="ef188-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="ef188-136">-NotificationThreshold</span></span>
<span data-ttu-id="ef188-137">與通知相關聯的閾值。</span><span class="sxs-lookup"><span data-stu-id="ef188-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="ef188-138">當成本或使用量超過閾值時，會收到通知。</span><span class="sxs-lookup"><span data-stu-id="ef188-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="ef188-139">一直是百分比，而且必須介於 0 到 1000 之間。</span><span class="sxs-lookup"><span data-stu-id="ef188-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="ef188-140">-ResourceFilter</span></span>
<span data-ttu-id="ef188-141">要篩選的資源實例以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="ef188-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="ef188-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="ef188-143">要篩選的資源群組逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="ef188-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef188-144">-ResourceGroupName</span></span>
<span data-ttu-id="ef188-145">預算的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ef188-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="ef188-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ef188-146">-StartDate</span></span>
<span data-ttu-id="ef188-147">開始日期 (使用 UTC 的 YYYY-MM-DD) 預算期間。</span><span class="sxs-lookup"><span data-stu-id="ef188-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="ef188-148">每月時間谷類不會在當月之前。</span><span class="sxs-lookup"><span data-stu-id="ef188-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="ef188-149">每季時間谷類不會在三個月之前。</span><span class="sxs-lookup"><span data-stu-id="ef188-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="ef188-150">每年時數的谷類不會在 12 個月之前。</span><span class="sxs-lookup"><span data-stu-id="ef188-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="ef188-151">未來開始日期不超過三個月。</span><span class="sxs-lookup"><span data-stu-id="ef188-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="ef188-152">-TimeGrain</span></span>
<span data-ttu-id="ef188-153">預算的時間紋理可以是每月、每季或每年。</span><span class="sxs-lookup"><span data-stu-id="ef188-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef188-154">-確認</span><span class="sxs-lookup"><span data-stu-id="ef188-154">-Confirm</span></span>
<span data-ttu-id="ef188-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef188-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef188-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef188-156">-WhatIf</span></span>
<span data-ttu-id="ef188-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef188-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef188-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef188-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef188-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef188-159">CommonParameters</span></span>
<span data-ttu-id="ef188-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef188-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef188-161">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ef188-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef188-162">輸入</span><span class="sxs-lookup"><span data-stu-id="ef188-162">INPUTS</span></span>

### <span data-ttu-id="ef188-163">沒有</span><span class="sxs-lookup"><span data-stu-id="ef188-163">None</span></span>

## <span data-ttu-id="ef188-164">輸出</span><span class="sxs-lookup"><span data-stu-id="ef188-164">OUTPUTS</span></span>

### <span data-ttu-id="ef188-165">Microsoft.Azure.Commands.Consumption.models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="ef188-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="ef188-166">筆記</span><span class="sxs-lookup"><span data-stu-id="ef188-166">NOTES</span></span>

## <span data-ttu-id="ef188-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef188-167">RELATED LINKS</span></span>

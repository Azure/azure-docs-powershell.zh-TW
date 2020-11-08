---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: 89d628790297bfb677dab11f0b19ba525d8b9e47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141008"
---
# <span data-ttu-id="3a9d7-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="3a9d7-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="3a9d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9d7-103">更新訂閱或資源群組中的預算。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="3a9d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a9d7-104">SYNTAX</span></span>

### <span data-ttu-id="3a9d7-105">訂閱 (預設) </span><span class="sxs-lookup"><span data-stu-id="3a9d7-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9d7-106">通知</span><span class="sxs-lookup"><span data-stu-id="3a9d7-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9d7-107">管線</span><span class="sxs-lookup"><span data-stu-id="3a9d7-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a9d7-108">管道與通知</span><span class="sxs-lookup"><span data-stu-id="3a9d7-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9d7-109">說明</span><span class="sxs-lookup"><span data-stu-id="3a9d7-109">DESCRIPTION</span></span>
<span data-ttu-id="3a9d7-110">Set-AzConsumptionBudget Cmdlet 會更新訂閱或資源群組中的預算。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="3a9d7-111">示例</span><span class="sxs-lookup"><span data-stu-id="3a9d7-111">EXAMPLES</span></span>

### <span data-ttu-id="3a9d7-112">範例1：在訂閱層級使用預算名稱更新預算</span><span class="sxs-lookup"><span data-stu-id="3a9d7-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="3a9d7-113">範例2：在成本或使用量達到訂閱階層的金額90% 時，使用通知更新預算</span><span class="sxs-lookup"><span data-stu-id="3a9d7-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="3a9d7-114">範例3：在資源群組層級使用預算名稱更新預算的新金額</span><span class="sxs-lookup"><span data-stu-id="3a9d7-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="3a9d7-115">參數</span><span class="sxs-lookup"><span data-stu-id="3a9d7-115">PARAMETERS</span></span>

### <span data-ttu-id="3a9d7-116">金額</span><span class="sxs-lookup"><span data-stu-id="3a9d7-116">-Amount</span></span>
<span data-ttu-id="3a9d7-117">預算金額。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-118">-類別</span><span class="sxs-lookup"><span data-stu-id="3a9d7-118">-Category</span></span>
<span data-ttu-id="3a9d7-119">預算類別可以是成本或使用量。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="3a9d7-120">-ContactEmail</span></span>
<span data-ttu-id="3a9d7-121">將預算通知傳送至超過閾值的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="3a9d7-122">-ContactGroup</span></span>
<span data-ttu-id="3a9d7-123">將預算通知傳送至超過閾值的動作群組。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="3a9d7-124">-ContactRole</span></span>
<span data-ttu-id="3a9d7-125">[連絡人角色] 可將預算通知傳送到超出閾值的時間。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9d7-126">-DefaultProfile</span></span>
<span data-ttu-id="3a9d7-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a9d7-128">-結束日期</span><span class="sxs-lookup"><span data-stu-id="3a9d7-128">-EndDate</span></span>
<span data-ttu-id="3a9d7-129">預算的時間週期) UTC (YYYY-MM 的結束日期。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="3a9d7-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a9d7-130">-InputObject</span></span>
<span data-ttu-id="3a9d7-131">預算物件。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="3a9d7-132">-MeterFilter</span></span>
<span data-ttu-id="3a9d7-133">要篩選的米清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="3a9d7-134">如果是使用類別，則為必要。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="3a9d7-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a9d7-135">-Name</span></span>
<span data-ttu-id="3a9d7-136">預算的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="3a9d7-137">-NotificationEnabled</span></span>
<span data-ttu-id="3a9d7-138">通知即會啟用。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-138">The notification is enabled.</span></span>
<span data-ttu-id="3a9d7-139">如果沒有指定，則預設會停用通知。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="3a9d7-140">-NotificationKey</span></span>
<span data-ttu-id="3a9d7-141">與預算相關聯之通知的索引鍵，以建立通知已啟用通知、通知門檻、連絡人電子郵件、連絡人群組或連絡人角色所需。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="3a9d7-142">-NotificationThreshold</span></span>
<span data-ttu-id="3a9d7-143">與通知相關聯的臨界值。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="3a9d7-144">當成本或使用量超過閾值時，就會傳送通知。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="3a9d7-145">它總是百分比，且必須介於0到1000。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="3a9d7-146">-ResourceFilter</span></span>
<span data-ttu-id="3a9d7-147">要篩選的資源實例清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="3a9d7-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="3a9d7-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="3a9d7-149">要篩選的資源群組清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="3a9d7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a9d7-150">-ResourceGroupName</span></span>
<span data-ttu-id="3a9d7-151">預算的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-152">-開始日期</span><span class="sxs-lookup"><span data-stu-id="3a9d7-152">-StartDate</span></span>
<span data-ttu-id="3a9d7-153">預算的時間週期 (YYYY MM) UTC 的開始日期。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="3a9d7-154">針對每月時間細微性，不在目前的月份之前。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="3a9d7-155">在三個月前不在每季時間細微性之前。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="3a9d7-156">在每年的時間顆粒前不到12個月。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="3a9d7-157">未來的開始日期不超過三個月。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="3a9d7-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="3a9d7-158">-TimeGrain</span></span>
<span data-ttu-id="3a9d7-159">預算的時間細微性可以是 [每月]、[每季] 或 [每年]。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d7-160">-確認</span><span class="sxs-lookup"><span data-stu-id="3a9d7-160">-Confirm</span></span>
<span data-ttu-id="3a9d7-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a9d7-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9d7-162">-WhatIf</span></span>
<span data-ttu-id="3a9d7-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a9d7-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a9d7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9d7-165">CommonParameters</span></span>
<span data-ttu-id="3a9d7-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9d7-167">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a9d7-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9d7-168">輸入</span><span class="sxs-lookup"><span data-stu-id="3a9d7-168">INPUTS</span></span>

### <span data-ttu-id="3a9d7-169">PSBudget 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3a9d7-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="3a9d7-170">輸出</span><span class="sxs-lookup"><span data-stu-id="3a9d7-170">OUTPUTS</span></span>

### <span data-ttu-id="3a9d7-171">PSBudget 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3a9d7-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="3a9d7-172">筆記</span><span class="sxs-lookup"><span data-stu-id="3a9d7-172">NOTES</span></span>

## <span data-ttu-id="3a9d7-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a9d7-173">RELATED LINKS</span></span>

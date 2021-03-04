---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: fa0b8ae9adaca5a187136f068dfd8797ed9e4b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904142"
---
# <span data-ttu-id="333a1-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="333a1-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="333a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="333a1-102">SYNOPSIS</span></span>
<span data-ttu-id="333a1-103">更新訂閱或資源群組中的預算。</span><span class="sxs-lookup"><span data-stu-id="333a1-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="333a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="333a1-104">SYNTAX</span></span>

### <span data-ttu-id="333a1-105">訂閱 (預設) </span><span class="sxs-lookup"><span data-stu-id="333a1-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333a1-106">通知</span><span class="sxs-lookup"><span data-stu-id="333a1-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333a1-107">管道</span><span class="sxs-lookup"><span data-stu-id="333a1-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="333a1-108">管線與通知</span><span class="sxs-lookup"><span data-stu-id="333a1-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="333a1-109">描述</span><span class="sxs-lookup"><span data-stu-id="333a1-109">DESCRIPTION</span></span>
<span data-ttu-id="333a1-110">Cmdlet Set-AzConsumptionBudget訂閱或資源群組中的預算。</span><span class="sxs-lookup"><span data-stu-id="333a1-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="333a1-111">例子</span><span class="sxs-lookup"><span data-stu-id="333a1-111">EXAMPLES</span></span>

### <span data-ttu-id="333a1-112">範例 1：以訂閱層級的預算名稱以新金額更新預算</span><span class="sxs-lookup"><span data-stu-id="333a1-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
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

### <span data-ttu-id="333a1-113">範例 2：當成本或使用量達到訂閱層級金額的 90% 閾值時，以通知更新預算</span><span class="sxs-lookup"><span data-stu-id="333a1-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
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

### <span data-ttu-id="333a1-114">範例 3：使用資源群組層級的預算名稱以新金額更新預算</span><span class="sxs-lookup"><span data-stu-id="333a1-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
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

## <span data-ttu-id="333a1-115">參數</span><span class="sxs-lookup"><span data-stu-id="333a1-115">PARAMETERS</span></span>

### <span data-ttu-id="333a1-116">-金額</span><span class="sxs-lookup"><span data-stu-id="333a1-116">-Amount</span></span>
<span data-ttu-id="333a1-117">預算金額。</span><span class="sxs-lookup"><span data-stu-id="333a1-117">Amount of a budget.</span></span>

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

### <span data-ttu-id="333a1-118">-類別</span><span class="sxs-lookup"><span data-stu-id="333a1-118">-Category</span></span>
<span data-ttu-id="333a1-119">預算類別可以是成本或使用量。</span><span class="sxs-lookup"><span data-stu-id="333a1-119">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="333a1-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="333a1-120">-ContactEmail</span></span>
<span data-ttu-id="333a1-121">要傳送預算通知的電子郵件地址，以在超過閾值時傳送。</span><span class="sxs-lookup"><span data-stu-id="333a1-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="333a1-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="333a1-122">-ContactGroup</span></span>
<span data-ttu-id="333a1-123">超出閾值時傳送預算通知的動作群組。</span><span class="sxs-lookup"><span data-stu-id="333a1-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="333a1-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="333a1-124">-ContactRole</span></span>
<span data-ttu-id="333a1-125">與角色聯繫，以在超過閾值時傳送預算通知。</span><span class="sxs-lookup"><span data-stu-id="333a1-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="333a1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333a1-126">-DefaultProfile</span></span>
<span data-ttu-id="333a1-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="333a1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="333a1-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="333a1-128">-EndDate</span></span>
<span data-ttu-id="333a1-129">以 UTC (YYYY-MM-DD 的結束日期) 預算期間。</span><span class="sxs-lookup"><span data-stu-id="333a1-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="333a1-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="333a1-130">-InputObject</span></span>
<span data-ttu-id="333a1-131">Budget 物件。</span><span class="sxs-lookup"><span data-stu-id="333a1-131">Budget object.</span></span>

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

### <span data-ttu-id="333a1-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="333a1-132">-MeterFilter</span></span>
<span data-ttu-id="333a1-133">要篩選的公尺逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="333a1-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="333a1-134">類別為使用量時為必填項。</span><span class="sxs-lookup"><span data-stu-id="333a1-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="333a1-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="333a1-135">-Name</span></span>
<span data-ttu-id="333a1-136">預算名稱。</span><span class="sxs-lookup"><span data-stu-id="333a1-136">Name of a budget.</span></span>

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

### <span data-ttu-id="333a1-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="333a1-137">-NotificationEnabled</span></span>
<span data-ttu-id="333a1-138">通知已啟用。</span><span class="sxs-lookup"><span data-stu-id="333a1-138">The notification is enabled.</span></span>
<span data-ttu-id="333a1-139">如果未指定，則通知預設為停用。</span><span class="sxs-lookup"><span data-stu-id="333a1-139">If not specified, the notification is disabled by default.</span></span>

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

### <span data-ttu-id="333a1-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="333a1-140">-NotificationKey</span></span>
<span data-ttu-id="333a1-141">與預算相關聯的通知金鑰，用於建立啟用通知切換的通知、通知門檻、連絡人電子郵件、連絡人群組或連絡人角色。</span><span class="sxs-lookup"><span data-stu-id="333a1-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="333a1-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="333a1-142">-NotificationThreshold</span></span>
<span data-ttu-id="333a1-143">與通知相關聯的閾值。</span><span class="sxs-lookup"><span data-stu-id="333a1-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="333a1-144">當成本或使用量超過閾值時，會收到通知。</span><span class="sxs-lookup"><span data-stu-id="333a1-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="333a1-145">一直是百分比，而且必須介於 0 到 1000 之間。</span><span class="sxs-lookup"><span data-stu-id="333a1-145">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="333a1-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="333a1-146">-ResourceFilter</span></span>
<span data-ttu-id="333a1-147">要篩選的資源實例以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="333a1-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="333a1-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="333a1-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="333a1-149">要篩選的資源群組逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="333a1-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="333a1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333a1-150">-ResourceGroupName</span></span>
<span data-ttu-id="333a1-151">預算的資源群組。</span><span class="sxs-lookup"><span data-stu-id="333a1-151">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="333a1-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="333a1-152">-StartDate</span></span>
<span data-ttu-id="333a1-153">開始日期 (使用 UTC 的 YYYY-MM-DD) 預算期間。</span><span class="sxs-lookup"><span data-stu-id="333a1-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="333a1-154">每月時間谷類不會在當月之前。</span><span class="sxs-lookup"><span data-stu-id="333a1-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="333a1-155">每季時間谷類不會在三個月之前。</span><span class="sxs-lookup"><span data-stu-id="333a1-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="333a1-156">每年時數的谷類不會在 12 個月之前。</span><span class="sxs-lookup"><span data-stu-id="333a1-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="333a1-157">未來開始日期不超過三個月。</span><span class="sxs-lookup"><span data-stu-id="333a1-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="333a1-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="333a1-158">-TimeGrain</span></span>
<span data-ttu-id="333a1-159">預算的時間紋理可以是每月、每季或每年。</span><span class="sxs-lookup"><span data-stu-id="333a1-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="333a1-160">-確認</span><span class="sxs-lookup"><span data-stu-id="333a1-160">-Confirm</span></span>
<span data-ttu-id="333a1-161">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="333a1-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333a1-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333a1-162">-WhatIf</span></span>
<span data-ttu-id="333a1-163">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="333a1-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333a1-164">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="333a1-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333a1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333a1-165">CommonParameters</span></span>
<span data-ttu-id="333a1-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="333a1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333a1-167">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="333a1-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333a1-168">輸入</span><span class="sxs-lookup"><span data-stu-id="333a1-168">INPUTS</span></span>

### <span data-ttu-id="333a1-169">Microsoft.Azure.Commands.Consumption.models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="333a1-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="333a1-170">輸出</span><span class="sxs-lookup"><span data-stu-id="333a1-170">OUTPUTS</span></span>

### <span data-ttu-id="333a1-171">Microsoft.Azure.Commands.Consumption.models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="333a1-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="333a1-172">筆記</span><span class="sxs-lookup"><span data-stu-id="333a1-172">NOTES</span></span>

## <span data-ttu-id="333a1-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="333a1-173">RELATED LINKS</span></span>

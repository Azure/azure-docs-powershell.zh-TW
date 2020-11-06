---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/new-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/New-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/New-AzureRmConsumptionBudget.md
ms.openlocfilehash: 9c89a4791b4e32637d069a672ddde06862518332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453824"
---
# <span data-ttu-id="abadd-101">New-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="abadd-101">New-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="abadd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abadd-102">SYNOPSIS</span></span>
<span data-ttu-id="abadd-103">在訂閱或資源群組中建立預算。</span><span class="sxs-lookup"><span data-stu-id="abadd-103">Create a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abadd-104">句法</span><span class="sxs-lookup"><span data-stu-id="abadd-104">SYNTAX</span></span>

### <span data-ttu-id="abadd-105">訂閱 (預設) </span><span class="sxs-lookup"><span data-stu-id="abadd-105">Subscription (Default)</span></span>
```
New-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abadd-106">通知</span><span class="sxs-lookup"><span data-stu-id="abadd-106">Notification</span></span>
```
New-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abadd-107">說明</span><span class="sxs-lookup"><span data-stu-id="abadd-107">DESCRIPTION</span></span>
<span data-ttu-id="abadd-108">New-AzureRmConsumptionBudget Cmdlet 會在訂閱或資源群組中建立預算。</span><span class="sxs-lookup"><span data-stu-id="abadd-108">The New-AzureRmConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="abadd-109">示例</span><span class="sxs-lookup"><span data-stu-id="abadd-109">EXAMPLES</span></span>

### <span data-ttu-id="abadd-110">範例1：在訂閱層級建立含預算名稱的成本預算</span><span class="sxs-lookup"><span data-stu-id="abadd-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzureRmConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

### <span data-ttu-id="abadd-111">範例2：在資源群組層級建立含預算名稱的成本預算</span><span class="sxs-lookup"><span data-stu-id="abadd-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

## <span data-ttu-id="abadd-112">參數</span><span class="sxs-lookup"><span data-stu-id="abadd-112">PARAMETERS</span></span>

### <span data-ttu-id="abadd-113">金額</span><span class="sxs-lookup"><span data-stu-id="abadd-113">-Amount</span></span>
<span data-ttu-id="abadd-114">預算金額。</span><span class="sxs-lookup"><span data-stu-id="abadd-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="abadd-115">-類別</span><span class="sxs-lookup"><span data-stu-id="abadd-115">-Category</span></span>
<span data-ttu-id="abadd-116">預算類別可以是成本或使用量。</span><span class="sxs-lookup"><span data-stu-id="abadd-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="abadd-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="abadd-117">-ContactEmail</span></span>
<span data-ttu-id="abadd-118">將預算通知傳送至超過閾值的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="abadd-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="abadd-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="abadd-119">-ContactGroup</span></span>
<span data-ttu-id="abadd-120">將預算通知傳送至超過閾值的動作群組。</span><span class="sxs-lookup"><span data-stu-id="abadd-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="abadd-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="abadd-121">-ContactRole</span></span>
<span data-ttu-id="abadd-122">[連絡人角色] 可將預算通知傳送到超出閾值的時間。</span><span class="sxs-lookup"><span data-stu-id="abadd-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="abadd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abadd-123">-DefaultProfile</span></span>
<span data-ttu-id="abadd-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="abadd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abadd-125">-結束日期</span><span class="sxs-lookup"><span data-stu-id="abadd-125">-EndDate</span></span>
<span data-ttu-id="abadd-126">預算的時間週期) UTC (YYYY-MM 的結束日期。</span><span class="sxs-lookup"><span data-stu-id="abadd-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="abadd-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="abadd-127">-MeterFilter</span></span>
<span data-ttu-id="abadd-128">要篩選的米清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="abadd-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="abadd-129">如果是使用類別，則為必要。</span><span class="sxs-lookup"><span data-stu-id="abadd-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="abadd-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="abadd-130">-Name</span></span>
<span data-ttu-id="abadd-131">預算的名稱。</span><span class="sxs-lookup"><span data-stu-id="abadd-131">Name of a budget.</span></span>

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

### <span data-ttu-id="abadd-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="abadd-132">-NotificationEnabled</span></span>
<span data-ttu-id="abadd-133">通知即會啟用。</span><span class="sxs-lookup"><span data-stu-id="abadd-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="abadd-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="abadd-134">-NotificationKey</span></span>
<span data-ttu-id="abadd-135">與預算相關聯之通知的索引鍵，以建立通知已啟用通知、通知門檻、連絡人電子郵件、連絡人群組或連絡人角色所需。</span><span class="sxs-lookup"><span data-stu-id="abadd-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="abadd-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="abadd-136">-NotificationThreshold</span></span>
<span data-ttu-id="abadd-137">與通知相關聯的臨界值。</span><span class="sxs-lookup"><span data-stu-id="abadd-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="abadd-138">當成本或使用量超過閾值時，就會傳送通知。</span><span class="sxs-lookup"><span data-stu-id="abadd-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="abadd-139">它總是百分比，且必須介於0到1000。</span><span class="sxs-lookup"><span data-stu-id="abadd-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="abadd-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="abadd-140">-ResourceFilter</span></span>
<span data-ttu-id="abadd-141">要篩選的資源實例清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="abadd-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="abadd-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="abadd-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="abadd-143">要篩選的資源群組清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="abadd-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="abadd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abadd-144">-ResourceGroupName</span></span>
<span data-ttu-id="abadd-145">預算的資源群組。</span><span class="sxs-lookup"><span data-stu-id="abadd-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="abadd-146">-開始日期</span><span class="sxs-lookup"><span data-stu-id="abadd-146">-StartDate</span></span>
<span data-ttu-id="abadd-147">預算的時間週期 (YYYY MM) UTC 的開始日期。</span><span class="sxs-lookup"><span data-stu-id="abadd-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="abadd-148">針對每月時間細微性，不在目前的月份之前。</span><span class="sxs-lookup"><span data-stu-id="abadd-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="abadd-149">在三個月前不在每季時間細微性之前。</span><span class="sxs-lookup"><span data-stu-id="abadd-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="abadd-150">在每年的時間顆粒前不到12個月。</span><span class="sxs-lookup"><span data-stu-id="abadd-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="abadd-151">未來的開始日期不超過三個月。</span><span class="sxs-lookup"><span data-stu-id="abadd-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="abadd-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="abadd-152">-TimeGrain</span></span>
<span data-ttu-id="abadd-153">預算的時間細微性可以是 [每月]、[每季] 或 [每年]。</span><span class="sxs-lookup"><span data-stu-id="abadd-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="abadd-154">-確認</span><span class="sxs-lookup"><span data-stu-id="abadd-154">-Confirm</span></span>
<span data-ttu-id="abadd-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="abadd-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abadd-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abadd-156">-WhatIf</span></span>
<span data-ttu-id="abadd-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="abadd-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abadd-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abadd-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abadd-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abadd-159">CommonParameters</span></span>
<span data-ttu-id="abadd-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abadd-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abadd-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="abadd-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abadd-162">輸入</span><span class="sxs-lookup"><span data-stu-id="abadd-162">INPUTS</span></span>

### <span data-ttu-id="abadd-163">所有</span><span class="sxs-lookup"><span data-stu-id="abadd-163">None</span></span>

## <span data-ttu-id="abadd-164">輸出</span><span class="sxs-lookup"><span data-stu-id="abadd-164">OUTPUTS</span></span>

### <span data-ttu-id="abadd-165">PSBudget 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="abadd-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="abadd-166">筆記</span><span class="sxs-lookup"><span data-stu-id="abadd-166">NOTES</span></span>

## <span data-ttu-id="abadd-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="abadd-167">RELATED LINKS</span></span>

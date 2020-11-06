---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: 44273f05793e8f84b28e6dc68f8cc12633fadf0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447806"
---
# <span data-ttu-id="1c242-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="1c242-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="1c242-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c242-102">SYNOPSIS</span></span>
<span data-ttu-id="1c242-103">建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="1c242-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c242-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c242-104">SYNTAX</span></span>

### <span data-ttu-id="1c242-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="1c242-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String> -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c242-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="1c242-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c242-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="1c242-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c242-108">說明</span><span class="sxs-lookup"><span data-stu-id="1c242-108">DESCRIPTION</span></span>
<span data-ttu-id="1c242-109">**新的-AzureRmAutoscaleProfile** Cmdlet 會建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="1c242-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="1c242-110">示例</span><span class="sxs-lookup"><span data-stu-id="1c242-110">EXAMPLES</span></span>

### <span data-ttu-id="1c242-111">範例1：使用固定日期建立單一設定檔</span><span class="sxs-lookup"><span data-stu-id="1c242-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="1c242-112">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c242-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="1c242-113">第二個命令會使用 $Rule 中的規則，建立一個名為 Profile01 且具有固定日期的設定檔。</span><span class="sxs-lookup"><span data-stu-id="1c242-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="1c242-114">範例2：使用排程建立設定檔</span><span class="sxs-lookup"><span data-stu-id="1c242-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="1c242-115">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c242-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="1c242-116">第二個命令會使用 $Rule 中的規則，建立一個名為 SecondProfileName 的設定檔與一個週期性排程。</span><span class="sxs-lookup"><span data-stu-id="1c242-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="1c242-117">範例3：使用兩個規則建立設定檔</span><span class="sxs-lookup"><span data-stu-id="1c242-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="1c242-118">前兩個命令會建立規則，並分別將它們儲存在 $Rule 1 和 $Rule 2 的變數中。</span><span class="sxs-lookup"><span data-stu-id="1c242-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="1c242-119">第三個命令會使用 Rule1 和 Rule2 中的規則，建立名為 ProfileName 的設定檔，然後將其儲存在 $Profile 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c242-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="1c242-120">最終命令會使用 Rule1 和 Rule2 中的規則來建立名為 SecondProfileName 的設定檔，然後將其儲存在 $Profile 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c242-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="1c242-121">範例4：建立沒有排程或固定日期的設定檔</span><span class="sxs-lookup"><span data-stu-id="1c242-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="1c242-122">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c242-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="1c242-123">第二個命令會建立不含排程或固定日期的設定檔，然後將它儲存在 $Profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c242-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="1c242-124">參數</span><span class="sxs-lookup"><span data-stu-id="1c242-124">PARAMETERS</span></span>

### <span data-ttu-id="1c242-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="1c242-125">-DefaultCapacity</span></span>
<span data-ttu-id="1c242-126">指定預設的容量。</span><span class="sxs-lookup"><span data-stu-id="1c242-126">Specifies the default capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c242-127">-DefaultProfile</span></span>
<span data-ttu-id="1c242-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1c242-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="1c242-129">-EndTimeWindow</span></span>
<span data-ttu-id="1c242-130">指定時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="1c242-130">Specifies the end of the time window.</span></span>

```yaml
Type: DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="1c242-131">-MaximumCapacity</span></span>
<span data-ttu-id="1c242-132">指定最大的容量。</span><span class="sxs-lookup"><span data-stu-id="1c242-132">Specifies the maximum capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="1c242-133">-MinimumCapacity</span></span>
<span data-ttu-id="1c242-134">指定最小容量。</span><span class="sxs-lookup"><span data-stu-id="1c242-134">Specifies the minimum capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c242-135">-Name</span></span>
<span data-ttu-id="1c242-136">指定要建立的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="1c242-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="1c242-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="1c242-138">指定週期的頻率。</span><span class="sxs-lookup"><span data-stu-id="1c242-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="1c242-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1c242-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c242-140">所有</span><span class="sxs-lookup"><span data-stu-id="1c242-140">None</span></span>
- <span data-ttu-id="1c242-141">第二個</span><span class="sxs-lookup"><span data-stu-id="1c242-141">Second</span></span>
- <span data-ttu-id="1c242-142">數</span><span class="sxs-lookup"><span data-stu-id="1c242-142">Minute</span></span>
- <span data-ttu-id="1c242-143">每</span><span class="sxs-lookup"><span data-stu-id="1c242-143">Hour</span></span>
- <span data-ttu-id="1c242-144">之內</span><span class="sxs-lookup"><span data-stu-id="1c242-144">Day</span></span>
- <span data-ttu-id="1c242-145">周</span><span class="sxs-lookup"><span data-stu-id="1c242-145">Week</span></span>
- <span data-ttu-id="1c242-146">月</span><span class="sxs-lookup"><span data-stu-id="1c242-146">Month</span></span>
- <span data-ttu-id="1c242-147">年</span><span class="sxs-lookup"><span data-stu-id="1c242-147">Year</span></span>

<span data-ttu-id="1c242-148">並非所有這些值都受支援。</span><span class="sxs-lookup"><span data-stu-id="1c242-148">Not all of these values are supported.</span></span>

```yaml
Type: RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-149">-規則</span><span class="sxs-lookup"><span data-stu-id="1c242-149">-Rule</span></span>
<span data-ttu-id="1c242-150">指定要新增至設定檔的規則清單。</span><span class="sxs-lookup"><span data-stu-id="1c242-150">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases: Rules

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-151">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="1c242-151">-ScheduleDay</span></span>
<span data-ttu-id="1c242-152">指定排程的天數。</span><span class="sxs-lookup"><span data-stu-id="1c242-152">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleDays

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-153">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="1c242-153">-ScheduleHour</span></span>
<span data-ttu-id="1c242-154">指定排程的時數。</span><span class="sxs-lookup"><span data-stu-id="1c242-154">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleHours

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-155">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="1c242-155">-ScheduleMinute</span></span>
<span data-ttu-id="1c242-156">指定排程的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="1c242-156">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleMinutes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-157">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="1c242-157">-ScheduleTimeZone</span></span>
<span data-ttu-id="1c242-158">指定排程的時區。</span><span class="sxs-lookup"><span data-stu-id="1c242-158">Specifies the time zone of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-159">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="1c242-159">-StartTimeWindow</span></span>
<span data-ttu-id="1c242-160">指定時間範圍的開始。</span><span class="sxs-lookup"><span data-stu-id="1c242-160">Specifies the start of the time window.</span></span>

```yaml
Type: DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-161">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="1c242-161">-TimeWindowTimeZone</span></span>
<span data-ttu-id="1c242-162">指定時間視窗的時區。</span><span class="sxs-lookup"><span data-stu-id="1c242-162">Specifies the time zone of the time window.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c242-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c242-163">CommonParameters</span></span>
<span data-ttu-id="1c242-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c242-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c242-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c242-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c242-166">輸入</span><span class="sxs-lookup"><span data-stu-id="1c242-166">INPUTS</span></span>

### <span data-ttu-id="1c242-167">所有</span><span class="sxs-lookup"><span data-stu-id="1c242-167">None</span></span>
<span data-ttu-id="1c242-168">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1c242-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c242-169">輸出</span><span class="sxs-lookup"><span data-stu-id="1c242-169">OUTPUTS</span></span>

### <span data-ttu-id="1c242-170">AutoscaleProfile 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="1c242-170">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="1c242-171">筆記</span><span class="sxs-lookup"><span data-stu-id="1c242-171">NOTES</span></span>

## <span data-ttu-id="1c242-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c242-172">RELATED LINKS</span></span>

[<span data-ttu-id="1c242-173">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1c242-173">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1c242-174">AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="1c242-174">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="1c242-175">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1c242-175">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1c242-176">新-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="1c242-176">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="1c242-177">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1c242-177">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)



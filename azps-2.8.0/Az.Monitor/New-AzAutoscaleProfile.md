---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: b83f7429b326267304536318063b5245031db2c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789825"
---
# <span data-ttu-id="7c15e-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="7c15e-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="7c15e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c15e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c15e-103">建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c15e-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="7c15e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c15e-104">SYNTAX</span></span>

### <span data-ttu-id="7c15e-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="7c15e-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c15e-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="7c15e-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c15e-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="7c15e-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c15e-108">說明</span><span class="sxs-lookup"><span data-stu-id="7c15e-108">DESCRIPTION</span></span>
<span data-ttu-id="7c15e-109">**新的-AzAutoscaleProfile** Cmdlet 會建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c15e-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="7c15e-110">示例</span><span class="sxs-lookup"><span data-stu-id="7c15e-110">EXAMPLES</span></span>

### <span data-ttu-id="7c15e-111">範例1：使用固定日期建立單一設定檔</span><span class="sxs-lookup"><span data-stu-id="7c15e-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="7c15e-112">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="7c15e-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="7c15e-113">第二個命令會使用 $Rule 中的規則，建立一個名為 Profile01 且具有固定日期的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c15e-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="7c15e-114">範例2：使用排程建立設定檔</span><span class="sxs-lookup"><span data-stu-id="7c15e-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="7c15e-115">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="7c15e-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="7c15e-116">第二個命令會使用 $Rule 中的規則，建立一個名為 SecondProfileName 的設定檔與一個週期性排程。</span><span class="sxs-lookup"><span data-stu-id="7c15e-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="7c15e-117">範例3：使用兩個規則建立設定檔</span><span class="sxs-lookup"><span data-stu-id="7c15e-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDay "1" -ScheduleHour 5 -ScheduleMinute 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="7c15e-118">前兩個命令會建立規則，並分別將它們儲存在 $Rule 1 和 $Rule 2 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7c15e-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="7c15e-119">第三個命令會使用 Rule1 和 Rule2 中的規則，建立名為 ProfileName 的設定檔，然後將其儲存在 $Profile 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="7c15e-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="7c15e-120">最終命令會使用 Rule1 和 Rule2 中的規則來建立名為 SecondProfileName 的設定檔，然後將其儲存在 $Profile 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="7c15e-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="7c15e-121">範例4：建立沒有排程或固定日期的設定檔</span><span class="sxs-lookup"><span data-stu-id="7c15e-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="7c15e-122">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="7c15e-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="7c15e-123">第二個命令會建立不含排程或固定日期的設定檔，然後將它儲存在 $Profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="7c15e-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="7c15e-124">參數</span><span class="sxs-lookup"><span data-stu-id="7c15e-124">PARAMETERS</span></span>

### <span data-ttu-id="7c15e-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="7c15e-125">-DefaultCapacity</span></span>
<span data-ttu-id="7c15e-126">指定預設的容量。</span><span class="sxs-lookup"><span data-stu-id="7c15e-126">Specifies the default capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c15e-127">-DefaultProfile</span></span>
<span data-ttu-id="7c15e-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7c15e-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c15e-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="7c15e-129">-EndTimeWindow</span></span>
<span data-ttu-id="7c15e-130">指定時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="7c15e-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="7c15e-131">-MaximumCapacity</span></span>
<span data-ttu-id="7c15e-132">指定最大的容量。</span><span class="sxs-lookup"><span data-stu-id="7c15e-132">Specifies the maximum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="7c15e-133">-MinimumCapacity</span></span>
<span data-ttu-id="7c15e-134">指定最小容量。</span><span class="sxs-lookup"><span data-stu-id="7c15e-134">Specifies the minimum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c15e-135">-Name</span></span>
<span data-ttu-id="7c15e-136">指定要建立的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="7c15e-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="7c15e-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="7c15e-138">指定週期的頻率。</span><span class="sxs-lookup"><span data-stu-id="7c15e-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="7c15e-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7c15e-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c15e-140">所有</span><span class="sxs-lookup"><span data-stu-id="7c15e-140">None</span></span>
- <span data-ttu-id="7c15e-141">第二個</span><span class="sxs-lookup"><span data-stu-id="7c15e-141">Second</span></span>
- <span data-ttu-id="7c15e-142">數</span><span class="sxs-lookup"><span data-stu-id="7c15e-142">Minute</span></span>
- <span data-ttu-id="7c15e-143">每</span><span class="sxs-lookup"><span data-stu-id="7c15e-143">Hour</span></span>
- <span data-ttu-id="7c15e-144">之內</span><span class="sxs-lookup"><span data-stu-id="7c15e-144">Day</span></span>
- <span data-ttu-id="7c15e-145">周</span><span class="sxs-lookup"><span data-stu-id="7c15e-145">Week</span></span>
- <span data-ttu-id="7c15e-146">月</span><span class="sxs-lookup"><span data-stu-id="7c15e-146">Month</span></span>
- <span data-ttu-id="7c15e-147">不支援年份中的所有值。</span><span class="sxs-lookup"><span data-stu-id="7c15e-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-148">-規則</span><span class="sxs-lookup"><span data-stu-id="7c15e-148">-Rule</span></span>
<span data-ttu-id="7c15e-149">指定要新增至設定檔的規則清單。</span><span class="sxs-lookup"><span data-stu-id="7c15e-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="7c15e-150">-ScheduleDay</span></span>
<span data-ttu-id="7c15e-151">指定排程的天數。</span><span class="sxs-lookup"><span data-stu-id="7c15e-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="7c15e-152">-ScheduleHour</span></span>
<span data-ttu-id="7c15e-153">指定排程的時數。</span><span class="sxs-lookup"><span data-stu-id="7c15e-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="7c15e-154">-ScheduleMinute</span></span>
<span data-ttu-id="7c15e-155">指定排程的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="7c15e-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="7c15e-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="7c15e-157">指定排程的時區。</span><span class="sxs-lookup"><span data-stu-id="7c15e-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="7c15e-158">-StartTimeWindow</span></span>
<span data-ttu-id="7c15e-159">指定時間範圍的開始。</span><span class="sxs-lookup"><span data-stu-id="7c15e-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="7c15e-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="7c15e-161">指定時間視窗的時區。</span><span class="sxs-lookup"><span data-stu-id="7c15e-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c15e-162">CommonParameters</span></span>
<span data-ttu-id="7c15e-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c15e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c15e-164">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7c15e-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c15e-165">輸入</span><span class="sxs-lookup"><span data-stu-id="7c15e-165">INPUTS</span></span>

### <span data-ttu-id="7c15e-166">System.object</span><span class="sxs-lookup"><span data-stu-id="7c15e-166">System.String</span></span>

### <span data-ttu-id="7c15e-167">System.object</span><span class="sxs-lookup"><span data-stu-id="7c15e-167">System.DateTime</span></span>

### <span data-ttu-id="7c15e-168">RecurrenceFrequency 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="7c15e-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="7c15e-169">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7c15e-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7c15e-170">[System.object]。清單 `1[[System.Nullable` 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，publickeytoken = 7cec85d7bea7798e]]，system.object = 中立，版本 = 4.0.0.0，Culture = 中性，publickeytoken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7c15e-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7c15e-171">[System.object]。清單 ' 1 [ScaleRule，，Marvell. PowerShell. Monitor，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="7c15e-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7c15e-172">輸出</span><span class="sxs-lookup"><span data-stu-id="7c15e-172">OUTPUTS</span></span>

### <span data-ttu-id="7c15e-173">AutoscaleProfile 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="7c15e-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="7c15e-174">筆記</span><span class="sxs-lookup"><span data-stu-id="7c15e-174">NOTES</span></span>

## <span data-ttu-id="7c15e-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c15e-175">RELATED LINKS</span></span>

[<span data-ttu-id="7c15e-176">附加 AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7c15e-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="7c15e-177">AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="7c15e-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="7c15e-178">AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7c15e-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="7c15e-179">新-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="7c15e-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="7c15e-180">移除-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7c15e-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)



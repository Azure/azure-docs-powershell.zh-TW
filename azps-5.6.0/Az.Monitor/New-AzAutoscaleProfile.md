---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: 52c3849a7e0e5ce732f54cd1136b2cc52dfbb94c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909586"
---
# <span data-ttu-id="ff554-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="ff554-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="ff554-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ff554-102">SYNOPSIS</span></span>
<span data-ttu-id="ff554-103">建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="ff554-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="ff554-104">語法</span><span class="sxs-lookup"><span data-stu-id="ff554-104">SYNTAX</span></span>

### <span data-ttu-id="ff554-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="ff554-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff554-106">CreateWithFixedDate 排程</span><span class="sxs-lookup"><span data-stu-id="ff554-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff554-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="ff554-107">CreateUsingRecurrentScheduling</span></span>
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

## <span data-ttu-id="ff554-108">描述</span><span class="sxs-lookup"><span data-stu-id="ff554-108">DESCRIPTION</span></span>
<span data-ttu-id="ff554-109">**New-AzAutoscaleProfile** Cmdlet 會建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="ff554-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="ff554-110">例子</span><span class="sxs-lookup"><span data-stu-id="ff554-110">EXAMPLES</span></span>

### <span data-ttu-id="ff554-111">範例 1：建立具有固定日期的單一設定檔</span><span class="sxs-lookup"><span data-stu-id="ff554-111">Example 1: Create single profile with a fixed date</span></span>
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

<span data-ttu-id="ff554-112">第一個命令會建立名為 Requests 的自動縮放規則，然後將它儲存在$Rule變數。</span><span class="sxs-lookup"><span data-stu-id="ff554-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="ff554-113">第二個命令會使用 $Rule 中的規則，建立名為 Profile01 的設定檔與固定$Rule。</span><span class="sxs-lookup"><span data-stu-id="ff554-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="ff554-114">範例 2：建立具有排程的設定檔</span><span class="sxs-lookup"><span data-stu-id="ff554-114">Example 2: Create a profile with a schedule</span></span>
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

<span data-ttu-id="ff554-115">第一個命令會建立名為 Requests 的自動縮放規則，然後將它儲存在$Rule變數。</span><span class="sxs-lookup"><span data-stu-id="ff554-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="ff554-116">第二個命令會使用 $Rule 中的規則建立名為 SecondProfileName 的設定檔和週期性$Rule。</span><span class="sxs-lookup"><span data-stu-id="ff554-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="ff554-117">範例 3：使用兩個規則建立設定檔</span><span class="sxs-lookup"><span data-stu-id="ff554-117">Example 3: Create profiles with two rules</span></span>
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

<span data-ttu-id="ff554-118">前兩個命令會建立規則，並分別儲存在 $Rule 1 和 $Rule 2 的變數中。</span><span class="sxs-lookup"><span data-stu-id="ff554-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="ff554-119">第三個命令會使用 Rule1 和 Rule2 中的規則建立名為 ProfileName 的設定檔，然後將它儲存在 $Profile 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="ff554-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="ff554-120">最後一個命令會使用 Rule1 和 Rule2 中的規則建立名為 SecondProfileName 的設定檔，然後將它儲存在 $Profile 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="ff554-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="ff554-121">範例 4：建立沒有排程或固定日期的設定檔</span><span class="sxs-lookup"><span data-stu-id="ff554-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="ff554-122">第一個命令會建立名為 Requests 的自動縮放規則，然後將它儲存在$Rule變數。</span><span class="sxs-lookup"><span data-stu-id="ff554-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="ff554-123">第二個命令會建立不含排程或固定日期的設定檔，然後將它儲存在$Profile變數。</span><span class="sxs-lookup"><span data-stu-id="ff554-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="ff554-124">參數</span><span class="sxs-lookup"><span data-stu-id="ff554-124">PARAMETERS</span></span>

### <span data-ttu-id="ff554-125">-Default進位</span><span class="sxs-lookup"><span data-stu-id="ff554-125">-DefaultCapacity</span></span>
<span data-ttu-id="ff554-126">指定預設容量。</span><span class="sxs-lookup"><span data-stu-id="ff554-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="ff554-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff554-127">-DefaultProfile</span></span>
<span data-ttu-id="ff554-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ff554-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff554-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="ff554-129">-EndTimeWindow</span></span>
<span data-ttu-id="ff554-130">指定時間視窗的結尾。</span><span class="sxs-lookup"><span data-stu-id="ff554-130">Specifies the end of the time window.</span></span>

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

### <span data-ttu-id="ff554-131">-Maximum可</span><span class="sxs-lookup"><span data-stu-id="ff554-131">-MaximumCapacity</span></span>
<span data-ttu-id="ff554-132">指定最大容量。</span><span class="sxs-lookup"><span data-stu-id="ff554-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="ff554-133">-Minimum一級</span><span class="sxs-lookup"><span data-stu-id="ff554-133">-MinimumCapacity</span></span>
<span data-ttu-id="ff554-134">指定最小容量。</span><span class="sxs-lookup"><span data-stu-id="ff554-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="ff554-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff554-135">-Name</span></span>
<span data-ttu-id="ff554-136">指定要建立之設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff554-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="ff554-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="ff554-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="ff554-138">指定週期的頻率。</span><span class="sxs-lookup"><span data-stu-id="ff554-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="ff554-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ff554-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff554-140">沒有</span><span class="sxs-lookup"><span data-stu-id="ff554-140">None</span></span>
- <span data-ttu-id="ff554-141">第二</span><span class="sxs-lookup"><span data-stu-id="ff554-141">Second</span></span>
- <span data-ttu-id="ff554-142">分鐘</span><span class="sxs-lookup"><span data-stu-id="ff554-142">Minute</span></span>
- <span data-ttu-id="ff554-143">小時</span><span class="sxs-lookup"><span data-stu-id="ff554-143">Hour</span></span>
- <span data-ttu-id="ff554-144">一天</span><span class="sxs-lookup"><span data-stu-id="ff554-144">Day</span></span>
- <span data-ttu-id="ff554-145">周</span><span class="sxs-lookup"><span data-stu-id="ff554-145">Week</span></span>
- <span data-ttu-id="ff554-146">月</span><span class="sxs-lookup"><span data-stu-id="ff554-146">Month</span></span>
- <span data-ttu-id="ff554-147">年份並非所有的值都受到支援。</span><span class="sxs-lookup"><span data-stu-id="ff554-147">Year Not all of these values are supported.</span></span>

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

### <span data-ttu-id="ff554-148">-規則</span><span class="sxs-lookup"><span data-stu-id="ff554-148">-Rule</span></span>
<span data-ttu-id="ff554-149">指定要新加入設定檔的規則清單。</span><span class="sxs-lookup"><span data-stu-id="ff554-149">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="ff554-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="ff554-150">-ScheduleDay</span></span>
<span data-ttu-id="ff554-151">指定已排程的天數。</span><span class="sxs-lookup"><span data-stu-id="ff554-151">Specifies the scheduled days.</span></span>

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

### <span data-ttu-id="ff554-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="ff554-152">-ScheduleHour</span></span>
<span data-ttu-id="ff554-153">指定排程的時數。</span><span class="sxs-lookup"><span data-stu-id="ff554-153">Specifies the scheduled hours.</span></span>

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

### <span data-ttu-id="ff554-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="ff554-154">-ScheduleMinute</span></span>
<span data-ttu-id="ff554-155">指定排程的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="ff554-155">Specifies the scheduled minutes.</span></span>

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

### <span data-ttu-id="ff554-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="ff554-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="ff554-157">指定排程的時區。</span><span class="sxs-lookup"><span data-stu-id="ff554-157">Specifies the time zone of the schedule.</span></span>

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

### <span data-ttu-id="ff554-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="ff554-158">-StartTimeWindow</span></span>
<span data-ttu-id="ff554-159">指定時間視窗的開始。</span><span class="sxs-lookup"><span data-stu-id="ff554-159">Specifies the start of the time window.</span></span>

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

### <span data-ttu-id="ff554-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="ff554-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="ff554-161">指定時間視窗的時區。</span><span class="sxs-lookup"><span data-stu-id="ff554-161">Specifies the time zone of the time window.</span></span>

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

### <span data-ttu-id="ff554-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff554-162">CommonParameters</span></span>
<span data-ttu-id="ff554-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ff554-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff554-164">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff554-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff554-165">輸入</span><span class="sxs-lookup"><span data-stu-id="ff554-165">INPUTS</span></span>

### <span data-ttu-id="ff554-166">System.String</span><span class="sxs-lookup"><span data-stu-id="ff554-166">System.String</span></span>

### <span data-ttu-id="ff554-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="ff554-167">System.DateTime</span></span>

### <span data-ttu-id="ff554-168">Microsoft.Azure.management.monitor.management.models.RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="ff554-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="ff554-169">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ff554-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ff554-170">System.Collections.generic.List `1[[System.Nullable` 1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ff554-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ff554-171">System.Collections.generic.List'1[[Microsoft.Azure.management.Monitor.management.models.ScaleRule，Microsoft.Azure.PowerShell.Cmdlets.Monitor， Version=1.0.0.0， Culture=neutral， PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="ff554-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ff554-172">輸出</span><span class="sxs-lookup"><span data-stu-id="ff554-172">OUTPUTS</span></span>

### <span data-ttu-id="ff554-173">Microsoft.Azure.management.Monitor.management.Models.AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="ff554-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="ff554-174">筆記</span><span class="sxs-lookup"><span data-stu-id="ff554-174">NOTES</span></span>

## <span data-ttu-id="ff554-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff554-175">RELATED LINKS</span></span>

[<span data-ttu-id="ff554-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ff554-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="ff554-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="ff554-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="ff554-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ff554-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="ff554-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="ff554-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="ff554-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ff554-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)



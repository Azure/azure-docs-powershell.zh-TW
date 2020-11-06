---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455804"
---
# <span data-ttu-id="91586-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="91586-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="91586-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91586-102">SYNOPSIS</span></span>
<span data-ttu-id="91586-103">建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="91586-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91586-104">句法</span><span class="sxs-lookup"><span data-stu-id="91586-104">SYNTAX</span></span>

### <span data-ttu-id="91586-105">不含排程時間的 New-AzureRmAutoscaleProfile Cmdlet 參數</span><span class="sxs-lookup"><span data-stu-id="91586-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91586-106">使用修正日期排程 New-AzureRmAutoscaleProfile Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="91586-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91586-107">使用定期排程 New-AzureRmAutoscaleProfile Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="91586-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91586-108">說明</span><span class="sxs-lookup"><span data-stu-id="91586-108">DESCRIPTION</span></span>
<span data-ttu-id="91586-109">**新的-AzureRmAutoscaleProfile** Cmdlet 會建立自動縮放設定檔。</span><span class="sxs-lookup"><span data-stu-id="91586-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="91586-110">示例</span><span class="sxs-lookup"><span data-stu-id="91586-110">EXAMPLES</span></span>

### <span data-ttu-id="91586-111">範例1：使用固定日期建立單一設定檔</span><span class="sxs-lookup"><span data-stu-id="91586-111">Example 1: Create single profile with a fixed date</span></span>
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

<span data-ttu-id="91586-112">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="91586-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="91586-113">第二個命令會使用 $Rule 中的規則，建立一個名為 Profile01 且具有固定日期的設定檔。</span><span class="sxs-lookup"><span data-stu-id="91586-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="91586-114">範例2：使用排程建立設定檔</span><span class="sxs-lookup"><span data-stu-id="91586-114">Example 2: Create a profile with a schedule</span></span>
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

<span data-ttu-id="91586-115">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="91586-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="91586-116">第二個命令會使用 $Rule 中的規則，建立一個名為 SecondProfileName 的設定檔與一個週期性排程。</span><span class="sxs-lookup"><span data-stu-id="91586-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="91586-117">範例3：使用兩個規則建立設定檔</span><span class="sxs-lookup"><span data-stu-id="91586-117">Example 3: Create profiles with two rules</span></span>
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

<span data-ttu-id="91586-118">前兩個命令會建立規則，並分別將它們儲存在 $Rule 1 和 $Rule 2 的變數中。</span><span class="sxs-lookup"><span data-stu-id="91586-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="91586-119">第三個命令會使用 Rule1 和 Rule2 中的規則，建立名為 ProfileName 的設定檔，然後將其儲存在 $Profile 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="91586-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="91586-120">最終命令會使用 Rule1 和 Rule2 中的規則來建立名為 SecondProfileName 的設定檔，然後將其儲存在 $Profile 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="91586-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="91586-121">範例4：建立沒有排程或固定日期的設定檔</span><span class="sxs-lookup"><span data-stu-id="91586-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="91586-122">第一個命令會建立名為「要求」的自動縮放規則，然後將其儲存在 $Rule 變數中。</span><span class="sxs-lookup"><span data-stu-id="91586-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="91586-123">第二個命令會建立不含排程或固定日期的設定檔，然後將它儲存在 $Profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="91586-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="91586-124">參數</span><span class="sxs-lookup"><span data-stu-id="91586-124">PARAMETERS</span></span>

### <span data-ttu-id="91586-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="91586-125">-DefaultCapacity</span></span>
<span data-ttu-id="91586-126">指定預設的容量。</span><span class="sxs-lookup"><span data-stu-id="91586-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="91586-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="91586-127">-EndTimeWindow</span></span>
<span data-ttu-id="91586-128">指定時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="91586-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91586-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="91586-129">-MaximumCapacity</span></span>
<span data-ttu-id="91586-130">指定最大的容量。</span><span class="sxs-lookup"><span data-stu-id="91586-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="91586-131">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="91586-131">-MinimumCapacity</span></span>
<span data-ttu-id="91586-132">指定最小容量。</span><span class="sxs-lookup"><span data-stu-id="91586-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="91586-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="91586-133">-Name</span></span>
<span data-ttu-id="91586-134">指定要建立的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="91586-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="91586-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="91586-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="91586-136">指定週期的頻率。</span><span class="sxs-lookup"><span data-stu-id="91586-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="91586-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="91586-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91586-138">所有</span><span class="sxs-lookup"><span data-stu-id="91586-138">None</span></span>
- <span data-ttu-id="91586-139">第二個</span><span class="sxs-lookup"><span data-stu-id="91586-139">Second</span></span>
- <span data-ttu-id="91586-140">數</span><span class="sxs-lookup"><span data-stu-id="91586-140">Minute</span></span>
- <span data-ttu-id="91586-141">每</span><span class="sxs-lookup"><span data-stu-id="91586-141">Hour</span></span>
- <span data-ttu-id="91586-142">之內</span><span class="sxs-lookup"><span data-stu-id="91586-142">Day</span></span>
- <span data-ttu-id="91586-143">周</span><span class="sxs-lookup"><span data-stu-id="91586-143">Week</span></span>
- <span data-ttu-id="91586-144">月</span><span class="sxs-lookup"><span data-stu-id="91586-144">Month</span></span>
- <span data-ttu-id="91586-145">年</span><span class="sxs-lookup"><span data-stu-id="91586-145">Year</span></span>

<span data-ttu-id="91586-146">並非所有這些值都受支援。</span><span class="sxs-lookup"><span data-stu-id="91586-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91586-147">-規則</span><span class="sxs-lookup"><span data-stu-id="91586-147">-Rules</span></span>
<span data-ttu-id="91586-148">指定要新增至設定檔的規則清單。</span><span class="sxs-lookup"><span data-stu-id="91586-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="91586-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="91586-149">-ScheduleDays</span></span>
<span data-ttu-id="91586-150">指定排程的天數。</span><span class="sxs-lookup"><span data-stu-id="91586-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91586-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="91586-151">-ScheduleHours</span></span>
<span data-ttu-id="91586-152">指定排程的時數。</span><span class="sxs-lookup"><span data-stu-id="91586-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91586-153">-ScheduleMinutes</span><span class="sxs-lookup"><span data-stu-id="91586-153">-ScheduleMinutes</span></span>
<span data-ttu-id="91586-154">指定排程的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="91586-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91586-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="91586-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="91586-156">指定排程的時區。</span><span class="sxs-lookup"><span data-stu-id="91586-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91586-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="91586-157">-StartTimeWindow</span></span>
<span data-ttu-id="91586-158">指定時間範圍的開始。</span><span class="sxs-lookup"><span data-stu-id="91586-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91586-159">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="91586-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="91586-160">指定時間視窗的時區。</span><span class="sxs-lookup"><span data-stu-id="91586-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91586-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91586-161">-DefaultProfile</span></span>
<span data-ttu-id="91586-162">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91586-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91586-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91586-163">CommonParameters</span></span>
<span data-ttu-id="91586-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91586-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91586-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91586-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91586-166">輸入</span><span class="sxs-lookup"><span data-stu-id="91586-166">INPUTS</span></span>

## <span data-ttu-id="91586-167">輸出</span><span class="sxs-lookup"><span data-stu-id="91586-167">OUTPUTS</span></span>

### <span data-ttu-id="91586-168">AutoscaleProfile 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="91586-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="91586-169">筆記</span><span class="sxs-lookup"><span data-stu-id="91586-169">NOTES</span></span>

## <span data-ttu-id="91586-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="91586-170">RELATED LINKS</span></span>

[<span data-ttu-id="91586-171">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="91586-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="91586-172">AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="91586-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="91586-173">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="91586-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="91586-174">新-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="91586-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="91586-175">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="91586-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)



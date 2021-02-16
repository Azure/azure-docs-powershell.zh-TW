---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139538"
---
# <span data-ttu-id="f79f2-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f79f2-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="f79f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f79f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f79f2-103">建立自動化排程。</span><span class="sxs-lookup"><span data-stu-id="f79f2-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="f79f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="f79f2-104">SYNTAX</span></span>

### <span data-ttu-id="f79f2-105">ByDaily (預設) </span><span class="sxs-lookup"><span data-stu-id="f79f2-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f79f2-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="f79f2-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f79f2-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="f79f2-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f79f2-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="f79f2-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f79f2-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="f79f2-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f79f2-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="f79f2-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f79f2-111">說明</span><span class="sxs-lookup"><span data-stu-id="f79f2-111">DESCRIPTION</span></span>
<span data-ttu-id="f79f2-112">**新的-AzAutomationSchedule** Cmdlet 會在 Azure 自動化中建立排程。</span><span class="sxs-lookup"><span data-stu-id="f79f2-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="f79f2-113">示例</span><span class="sxs-lookup"><span data-stu-id="f79f2-113">EXAMPLES</span></span>

### <span data-ttu-id="f79f2-114">範例1：以當地時間建立一次時間排程</span><span class="sxs-lookup"><span data-stu-id="f79f2-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="f79f2-115">第一個命令會從系統中取得時區識別碼，並將它儲存在 $TimeZone 變數中。</span><span class="sxs-lookup"><span data-stu-id="f79f2-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="f79f2-116">第二個命令會建立一個排程，該排程會在目前日期於指定的時區中的 11:00 PM 執行一次。</span><span class="sxs-lookup"><span data-stu-id="f79f2-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="f79f2-117">範例2：建立週期性排程</span><span class="sxs-lookup"><span data-stu-id="f79f2-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f79f2-118">第一個命令會使用 [ **取得日期** ] Cmdlet 來建立 date 物件，然後將物件儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="f79f2-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="f79f2-119">指定未來最少五分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="f79f2-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="f79f2-120">第二個命令會使用 [ **取得日期** ] Cmdlet 來建立 date 物件，然後將物件儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="f79f2-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="f79f2-121">該命令會指定未來的時間。</span><span class="sxs-lookup"><span data-stu-id="f79f2-121">The command specifies a future time.</span></span>
<span data-ttu-id="f79f2-122">最後一個命令會建立名為 Schedule02 的每日排程，以在儲存在 $StartDate 的時間開始，並在 $EndDate 儲存的時間到期。</span><span class="sxs-lookup"><span data-stu-id="f79f2-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="f79f2-123">範例3：建立每週週期性排程</span><span class="sxs-lookup"><span data-stu-id="f79f2-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f79f2-124">第一個命令會使用 [ **取得日期** ] Cmdlet 來建立 date 物件，然後將物件儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="f79f2-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="f79f2-125">第二個命令會建立包含星期一、星期二、星期三、週四和星期五的周數陣列。</span><span class="sxs-lookup"><span data-stu-id="f79f2-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="f79f2-126">最後一個命令會建立名為 Schedule03 的每日排程，每週的13:00 都會執行一次。</span><span class="sxs-lookup"><span data-stu-id="f79f2-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="f79f2-127">排程永遠不會過期。</span><span class="sxs-lookup"><span data-stu-id="f79f2-127">The schedule will never expire.</span></span>

## <span data-ttu-id="f79f2-128">參數</span><span class="sxs-lookup"><span data-stu-id="f79f2-128">PARAMETERS</span></span>

### <span data-ttu-id="f79f2-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f79f2-129">-AutomationAccountName</span></span>
<span data-ttu-id="f79f2-130">指定此 Cmdlet 建立排程之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f79f2-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="f79f2-131">-DayInterval</span></span>
<span data-ttu-id="f79f2-132">指定排程的間隔（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="f79f2-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="f79f2-133">如果您沒有指定此參數，且未指定 *OneTime* 參數，則預設值為 1 (1) 。</span><span class="sxs-lookup"><span data-stu-id="f79f2-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="f79f2-134">-DayOfWeek</span></span>
<span data-ttu-id="f79f2-135">指定每週排程的天數清單。</span><span class="sxs-lookup"><span data-stu-id="f79f2-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="f79f2-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="f79f2-137">指定排程執行時間在月份中的第一周。</span><span class="sxs-lookup"><span data-stu-id="f79f2-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="f79f2-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="f79f2-138">psdx_paramvalues</span></span>
- <span data-ttu-id="f79f2-139">sr-1</span><span class="sxs-lookup"><span data-stu-id="f79f2-139">1</span></span>
- <span data-ttu-id="f79f2-140">pplx-2</span><span class="sxs-lookup"><span data-stu-id="f79f2-140">2</span></span>
- <span data-ttu-id="f79f2-141">3</span><span class="sxs-lookup"><span data-stu-id="f79f2-141">3</span></span>
- <span data-ttu-id="f79f2-142">4</span><span class="sxs-lookup"><span data-stu-id="f79f2-142">4</span></span>
- <span data-ttu-id="f79f2-143">-1</span><span class="sxs-lookup"><span data-stu-id="f79f2-143">-1</span></span>
- <span data-ttu-id="f79f2-144">一</span><span class="sxs-lookup"><span data-stu-id="f79f2-144">First</span></span>
- <span data-ttu-id="f79f2-145">第二個</span><span class="sxs-lookup"><span data-stu-id="f79f2-145">Second</span></span>
- <span data-ttu-id="f79f2-146">個</span><span class="sxs-lookup"><span data-stu-id="f79f2-146">Third</span></span>
- <span data-ttu-id="f79f2-147">1/4</span><span class="sxs-lookup"><span data-stu-id="f79f2-147">Fourth</span></span>
- <span data-ttu-id="f79f2-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="f79f2-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="f79f2-149">-DaysOfMonth</span></span>
<span data-ttu-id="f79f2-150">針對每月排程指定月份的天數清單。</span><span class="sxs-lookup"><span data-stu-id="f79f2-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="f79f2-151">-DaysOfWeek</span></span>
<span data-ttu-id="f79f2-152">指定每週排程的天數清單。</span><span class="sxs-lookup"><span data-stu-id="f79f2-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79f2-153">-DefaultProfile</span></span>
<span data-ttu-id="f79f2-154">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f79f2-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f79f2-155">-描述</span><span class="sxs-lookup"><span data-stu-id="f79f2-155">-Description</span></span>
<span data-ttu-id="f79f2-156">指定排程的描述。</span><span class="sxs-lookup"><span data-stu-id="f79f2-156">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f79f2-157">-ExpiryTime</span></span>
<span data-ttu-id="f79f2-158">指定排程的到期時間做為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="f79f2-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="f79f2-159">您可以指定可轉換成有效 **DateTimeOffset** 的字串。</span><span class="sxs-lookup"><span data-stu-id="f79f2-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f79f2-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="f79f2-161">表示此排程物件將用於排程軟體更新設定</span><span class="sxs-lookup"><span data-stu-id="f79f2-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="f79f2-162">-HourInterval</span></span>
<span data-ttu-id="f79f2-163">指定排程的間隔（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="f79f2-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="f79f2-164">-MonthInterval</span></span>
<span data-ttu-id="f79f2-165">指定排程的間隔（以月為單位）。</span><span class="sxs-lookup"><span data-stu-id="f79f2-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-166">-名稱</span><span class="sxs-lookup"><span data-stu-id="f79f2-166">-Name</span></span>
<span data-ttu-id="f79f2-167">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="f79f2-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="f79f2-168">-OneTime</span></span>
<span data-ttu-id="f79f2-169">指定 Cmdlet 建立一次時間排程。</span><span class="sxs-lookup"><span data-stu-id="f79f2-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f79f2-170">-ResourceGroupName</span></span>
<span data-ttu-id="f79f2-171">指定此 Cmdlet 建立排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f79f2-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f79f2-172">-StartTime</span></span>
<span data-ttu-id="f79f2-173">指定排程的開始時間做為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="f79f2-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="f79f2-174">您可以指定可轉換成有效 **DateTimeOffset** 的字串。</span><span class="sxs-lookup"><span data-stu-id="f79f2-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="f79f2-175">如果指定了 *時區* 參數，則會忽略偏移，並使用指定的時區。</span><span class="sxs-lookup"><span data-stu-id="f79f2-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-176">-時區</span><span class="sxs-lookup"><span data-stu-id="f79f2-176">-TimeZone</span></span>
<span data-ttu-id="f79f2-177">指定排程的時區。</span><span class="sxs-lookup"><span data-stu-id="f79f2-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="f79f2-178">這個字串可以是 IANA ID 或 Windows 時區 ID。</span><span class="sxs-lookup"><span data-stu-id="f79f2-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="f79f2-179">-WeekInterval</span></span>
<span data-ttu-id="f79f2-180">指定排程的間隔（以周為單位）。</span><span class="sxs-lookup"><span data-stu-id="f79f2-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79f2-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79f2-181">CommonParameters</span></span>
<span data-ttu-id="f79f2-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f79f2-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79f2-183">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f79f2-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79f2-184">輸入</span><span class="sxs-lookup"><span data-stu-id="f79f2-184">INPUTS</span></span>

### <span data-ttu-id="f79f2-185">System.object</span><span class="sxs-lookup"><span data-stu-id="f79f2-185">System.String</span></span>

### <span data-ttu-id="f79f2-186">System.object</span><span class="sxs-lookup"><span data-stu-id="f79f2-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="f79f2-187">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f79f2-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f79f2-188">輸出</span><span class="sxs-lookup"><span data-stu-id="f79f2-188">OUTPUTS</span></span>

### <span data-ttu-id="f79f2-189">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="f79f2-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="f79f2-190">筆記</span><span class="sxs-lookup"><span data-stu-id="f79f2-190">NOTES</span></span>

## <span data-ttu-id="f79f2-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="f79f2-191">RELATED LINKS</span></span>

[<span data-ttu-id="f79f2-192">AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f79f2-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="f79f2-193">移除-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f79f2-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="f79f2-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f79f2-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)



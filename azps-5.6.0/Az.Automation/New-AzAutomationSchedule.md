---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 1c3837bffcf5b3cde03623e06ad1233ed833a4c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915662"
---
# <span data-ttu-id="19b1e-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19b1e-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="19b1e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="19b1e-103">建立自動化排程。</span><span class="sxs-lookup"><span data-stu-id="19b1e-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="19b1e-104">語法</span><span class="sxs-lookup"><span data-stu-id="19b1e-104">SYNTAX</span></span>

### <span data-ttu-id="19b1e-105">ByDaily (預設) </span><span class="sxs-lookup"><span data-stu-id="19b1e-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19b1e-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="19b1e-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19b1e-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="19b1e-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19b1e-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="19b1e-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19b1e-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="19b1e-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19b1e-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="19b1e-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19b1e-111">描述</span><span class="sxs-lookup"><span data-stu-id="19b1e-111">DESCRIPTION</span></span>
<span data-ttu-id="19b1e-112">**New-AzAutomationSchedule** Cmdlet 在 Azure Automation 中建立排程。</span><span class="sxs-lookup"><span data-stu-id="19b1e-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="19b1e-113">例子</span><span class="sxs-lookup"><span data-stu-id="19b1e-113">EXAMPLES</span></span>

### <span data-ttu-id="19b1e-114">範例 1：在當地時間建立一次排程</span><span class="sxs-lookup"><span data-stu-id="19b1e-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="19b1e-115">第一個命令會從系統獲得時區識別碼，並儲存在$TimeZone變數。</span><span class="sxs-lookup"><span data-stu-id="19b1e-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="19b1e-116">第二個命令會建立一個排程，該排程會于目前日期於指定時區的下午 11：00 執行一次。</span><span class="sxs-lookup"><span data-stu-id="19b1e-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="19b1e-117">範例 2：建立週期性排程</span><span class="sxs-lookup"><span data-stu-id="19b1e-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19b1e-118">第一個命令會使用 **Get-Date** Cmdlet 建立日期物件，然後將該物件儲存在$StartDate變數中。</span><span class="sxs-lookup"><span data-stu-id="19b1e-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="19b1e-119">指定未來至少五分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="19b1e-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="19b1e-120">第二個命令會使用 **Get-Date** Cmdlet 建立日期物件，然後將該物件儲存在$EndDate變數。</span><span class="sxs-lookup"><span data-stu-id="19b1e-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="19b1e-121">命令會指定未來時間。</span><span class="sxs-lookup"><span data-stu-id="19b1e-121">The command specifies a future time.</span></span>
<span data-ttu-id="19b1e-122">最後一個命令會建立名為 Schedule02 的每日排程，從儲存在 $StartDate 的時間開始，然後于儲存于 $EndDate 的時間到期。</span><span class="sxs-lookup"><span data-stu-id="19b1e-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="19b1e-123">範例 3：建立每週週期性排程</span><span class="sxs-lookup"><span data-stu-id="19b1e-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19b1e-124">第一個命令會使用 **Get-Date** Cmdlet 建立日期物件，然後將該物件儲存在$StartDate變數中。</span><span class="sxs-lookup"><span data-stu-id="19b1e-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="19b1e-125">第二個命令會建立包含星期一、星期二、星期三、星期四和星期五的星期幾陣列。</span><span class="sxs-lookup"><span data-stu-id="19b1e-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="19b1e-126">最後一個命令會建立名為 Schedule03 的每日排程，將于每週 13：00 執行星期一至星期五。</span><span class="sxs-lookup"><span data-stu-id="19b1e-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="19b1e-127">排程永遠不會過期。</span><span class="sxs-lookup"><span data-stu-id="19b1e-127">The schedule will never expire.</span></span>

## <span data-ttu-id="19b1e-128">參數</span><span class="sxs-lookup"><span data-stu-id="19b1e-128">PARAMETERS</span></span>

### <span data-ttu-id="19b1e-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19b1e-129">-AutomationAccountName</span></span>
<span data-ttu-id="19b1e-130">指定此 Cmdlet 建立排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="19b1e-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="19b1e-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="19b1e-131">-DayInterval</span></span>
<span data-ttu-id="19b1e-132">指定排程的時間間隔 ，以天為單位。</span><span class="sxs-lookup"><span data-stu-id="19b1e-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="19b1e-133">如果您未指定此參數，而且未指定 *OneTime* 參數，預設值為 1 (1) 。</span><span class="sxs-lookup"><span data-stu-id="19b1e-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="19b1e-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="19b1e-134">-DayOfWeek</span></span>
<span data-ttu-id="19b1e-135">指定每週排程的星期數清單。</span><span class="sxs-lookup"><span data-stu-id="19b1e-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="19b1e-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="19b1e-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="19b1e-137">指定排程執行月份中的星期。</span><span class="sxs-lookup"><span data-stu-id="19b1e-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="19b1e-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="19b1e-138">psdx_paramvalues</span></span>
- <span data-ttu-id="19b1e-139">1</span><span class="sxs-lookup"><span data-stu-id="19b1e-139">1</span></span>
- <span data-ttu-id="19b1e-140">2</span><span class="sxs-lookup"><span data-stu-id="19b1e-140">2</span></span>
- <span data-ttu-id="19b1e-141">3</span><span class="sxs-lookup"><span data-stu-id="19b1e-141">3</span></span>
- <span data-ttu-id="19b1e-142">4</span><span class="sxs-lookup"><span data-stu-id="19b1e-142">4</span></span>
- <span data-ttu-id="19b1e-143">-1</span><span class="sxs-lookup"><span data-stu-id="19b1e-143">-1</span></span>
- <span data-ttu-id="19b1e-144">第一</span><span class="sxs-lookup"><span data-stu-id="19b1e-144">First</span></span>
- <span data-ttu-id="19b1e-145">第二</span><span class="sxs-lookup"><span data-stu-id="19b1e-145">Second</span></span>
- <span data-ttu-id="19b1e-146">第三</span><span class="sxs-lookup"><span data-stu-id="19b1e-146">Third</span></span>
- <span data-ttu-id="19b1e-147">四</span><span class="sxs-lookup"><span data-stu-id="19b1e-147">Fourth</span></span>
- <span data-ttu-id="19b1e-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="19b1e-148">LastDay</span></span>

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

### <span data-ttu-id="19b1e-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="19b1e-149">-DaysOfMonth</span></span>
<span data-ttu-id="19b1e-150">指定每月排程的月份天數清單。</span><span class="sxs-lookup"><span data-stu-id="19b1e-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="19b1e-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="19b1e-151">-DaysOfWeek</span></span>
<span data-ttu-id="19b1e-152">指定每週排程的星期數清單。</span><span class="sxs-lookup"><span data-stu-id="19b1e-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="19b1e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b1e-153">-DefaultProfile</span></span>
<span data-ttu-id="19b1e-154">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="19b1e-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19b1e-155">-描述</span><span class="sxs-lookup"><span data-stu-id="19b1e-155">-Description</span></span>
<span data-ttu-id="19b1e-156">指定排程的描述。</span><span class="sxs-lookup"><span data-stu-id="19b1e-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="19b1e-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="19b1e-157">-ExpiryTime</span></span>
<span data-ttu-id="19b1e-158">將排程的到期時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="19b1e-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="19b1e-159">您可以指定可以轉換成有效 **DateTimeOffset 的字串**。</span><span class="sxs-lookup"><span data-stu-id="19b1e-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="19b1e-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="19b1e-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="19b1e-161">表示此排程物件將用於排程軟體更新組</span><span class="sxs-lookup"><span data-stu-id="19b1e-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="19b1e-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="19b1e-162">-HourInterval</span></span>
<span data-ttu-id="19b1e-163">指定排程的時間間隔 ，以小時為單位。</span><span class="sxs-lookup"><span data-stu-id="19b1e-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="19b1e-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="19b1e-164">-MonthInterval</span></span>
<span data-ttu-id="19b1e-165">指定排程的時間間隔 ，以月為單位。</span><span class="sxs-lookup"><span data-stu-id="19b1e-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="19b1e-166">-名稱</span><span class="sxs-lookup"><span data-stu-id="19b1e-166">-Name</span></span>
<span data-ttu-id="19b1e-167">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="19b1e-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="19b1e-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="19b1e-168">-OneTime</span></span>
<span data-ttu-id="19b1e-169">指定 Cmdlet 會建立一次排程。</span><span class="sxs-lookup"><span data-stu-id="19b1e-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="19b1e-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b1e-170">-ResourceGroupName</span></span>
<span data-ttu-id="19b1e-171">指定此 Cmdlet 建立排程的資源組名。</span><span class="sxs-lookup"><span data-stu-id="19b1e-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="19b1e-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="19b1e-172">-StartTime</span></span>
<span data-ttu-id="19b1e-173">將排程的開始時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="19b1e-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="19b1e-174">您可以指定可以轉換成有效 **DateTimeOffset 的字串**。</span><span class="sxs-lookup"><span data-stu-id="19b1e-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="19b1e-175">如果 *指定時區* 參數，將會忽略位移，並且使用指定的時區。</span><span class="sxs-lookup"><span data-stu-id="19b1e-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="19b1e-176">-時區</span><span class="sxs-lookup"><span data-stu-id="19b1e-176">-TimeZone</span></span>
<span data-ttu-id="19b1e-177">指定排程的時區。</span><span class="sxs-lookup"><span data-stu-id="19b1e-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="19b1e-178">此字串可以是 IANA 識別碼或 Windows 時區識別碼。</span><span class="sxs-lookup"><span data-stu-id="19b1e-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="19b1e-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="19b1e-179">-WeekInterval</span></span>
<span data-ttu-id="19b1e-180">指定排程的間隔 ，以周為單位。</span><span class="sxs-lookup"><span data-stu-id="19b1e-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="19b1e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b1e-181">CommonParameters</span></span>
<span data-ttu-id="19b1e-182">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19b1e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b1e-183">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="19b1e-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b1e-184">輸入</span><span class="sxs-lookup"><span data-stu-id="19b1e-184">INPUTS</span></span>

### <span data-ttu-id="19b1e-185">System.String</span><span class="sxs-lookup"><span data-stu-id="19b1e-185">System.String</span></span>

### <span data-ttu-id="19b1e-186">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="19b1e-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="19b1e-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19b1e-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19b1e-188">輸出</span><span class="sxs-lookup"><span data-stu-id="19b1e-188">OUTPUTS</span></span>

### <span data-ttu-id="19b1e-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="19b1e-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="19b1e-190">筆記</span><span class="sxs-lookup"><span data-stu-id="19b1e-190">NOTES</span></span>

## <span data-ttu-id="19b1e-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="19b1e-191">RELATED LINKS</span></span>

[<span data-ttu-id="19b1e-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19b1e-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="19b1e-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19b1e-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="19b1e-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19b1e-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)



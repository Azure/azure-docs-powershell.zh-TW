---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 3528a95e9dab3c92571ec49e9bf5d567012fb5b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454763"
---
# <span data-ttu-id="e897c-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e897c-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="e897c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e897c-102">SYNOPSIS</span></span>
<span data-ttu-id="e897c-103">建立自動化排程。</span><span class="sxs-lookup"><span data-stu-id="e897c-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e897c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e897c-104">SYNTAX</span></span>

### <span data-ttu-id="e897c-105">ByDaily (預設) </span><span class="sxs-lookup"><span data-stu-id="e897c-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e897c-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="e897c-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e897c-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="e897c-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e897c-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e897c-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e897c-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="e897c-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e897c-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="e897c-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e897c-111">說明</span><span class="sxs-lookup"><span data-stu-id="e897c-111">DESCRIPTION</span></span>
<span data-ttu-id="e897c-112">**新的-AzureRmAutomationSchedule** Cmdlet 會在 Azure 自動化中建立排程。</span><span class="sxs-lookup"><span data-stu-id="e897c-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="e897c-113">示例</span><span class="sxs-lookup"><span data-stu-id="e897c-113">EXAMPLES</span></span>

### <span data-ttu-id="e897c-114">範例1：以當地時間建立一次時間排程</span><span class="sxs-lookup"><span data-stu-id="e897c-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="e897c-115">第一個命令會從系統中取得時區識別碼，並將它儲存在 $TimeZone 變數中。</span><span class="sxs-lookup"><span data-stu-id="e897c-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="e897c-116">第二個命令會建立一個排程，該排程會在目前日期於指定的時區中的 11:00 PM 執行一次。</span><span class="sxs-lookup"><span data-stu-id="e897c-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="e897c-117">範例2：建立週期性排程</span><span class="sxs-lookup"><span data-stu-id="e897c-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e897c-118">第一個命令會使用 [ **取得日期** ] Cmdlet 來建立 date 物件，然後將物件儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="e897c-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="e897c-119">指定未來最少五分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="e897c-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="e897c-120">第二個命令會使用 [ **取得日期** ] Cmdlet 來建立 date 物件，然後將物件儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="e897c-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="e897c-121">該命令會指定未來的時間。</span><span class="sxs-lookup"><span data-stu-id="e897c-121">The command specifies a future time.</span></span>

<span data-ttu-id="e897c-122">最後一個命令會建立名為 Schedule01 的每日排程，以在儲存在 $StartDate 的時間開始，並在 $EndDate 儲存的時間到期。</span><span class="sxs-lookup"><span data-stu-id="e897c-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="e897c-123">參數</span><span class="sxs-lookup"><span data-stu-id="e897c-123">PARAMETERS</span></span>

### <span data-ttu-id="e897c-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e897c-124">-AutomationAccountName</span></span>
<span data-ttu-id="e897c-125">指定此 Cmdlet 建立排程之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e897c-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="e897c-126">-DayInterval</span></span>
<span data-ttu-id="e897c-127">指定排程的間隔（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="e897c-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="e897c-128">如果您沒有指定此參數，且未指定 *OneTime* 參數，則預設值為 1 (1) 。</span><span class="sxs-lookup"><span data-stu-id="e897c-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e897c-129">-DayOfWeek</span></span>
<span data-ttu-id="e897c-130">指定每週排程的天數清單。</span><span class="sxs-lookup"><span data-stu-id="e897c-130">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="e897c-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="e897c-132">指定排程執行時間在月份中的第一周。</span><span class="sxs-lookup"><span data-stu-id="e897c-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="e897c-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="e897c-133">psdx_paramvalues</span></span>

- <span data-ttu-id="e897c-134">sr-1</span><span class="sxs-lookup"><span data-stu-id="e897c-134">1</span></span>
- <span data-ttu-id="e897c-135">pplx-2</span><span class="sxs-lookup"><span data-stu-id="e897c-135">2</span></span>
- <span data-ttu-id="e897c-136">3</span><span class="sxs-lookup"><span data-stu-id="e897c-136">3</span></span>
- <span data-ttu-id="e897c-137">4</span><span class="sxs-lookup"><span data-stu-id="e897c-137">4</span></span>
- <span data-ttu-id="e897c-138">-1</span><span class="sxs-lookup"><span data-stu-id="e897c-138">-1</span></span>
- <span data-ttu-id="e897c-139">一</span><span class="sxs-lookup"><span data-stu-id="e897c-139">First</span></span>
- <span data-ttu-id="e897c-140">第二個</span><span class="sxs-lookup"><span data-stu-id="e897c-140">Second</span></span>
- <span data-ttu-id="e897c-141">個</span><span class="sxs-lookup"><span data-stu-id="e897c-141">Third</span></span>
- <span data-ttu-id="e897c-142">1/4</span><span class="sxs-lookup"><span data-stu-id="e897c-142">Fourth</span></span>
- <span data-ttu-id="e897c-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="e897c-143">LastDay</span></span>

```yaml
Type: DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="e897c-144">-DaysOfMonth</span></span>
<span data-ttu-id="e897c-145">針對每月排程指定月份的天數清單。</span><span class="sxs-lookup"><span data-stu-id="e897c-145">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases: 
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="e897c-146">-DaysOfWeek</span></span>
<span data-ttu-id="e897c-147">指定每週排程的天數清單。</span><span class="sxs-lookup"><span data-stu-id="e897c-147">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: ByWeekly
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e897c-148">-DefaultProfile</span></span>
<span data-ttu-id="e897c-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e897c-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e897c-150">-描述</span><span class="sxs-lookup"><span data-stu-id="e897c-150">-Description</span></span>
<span data-ttu-id="e897c-151">指定排程的描述。</span><span class="sxs-lookup"><span data-stu-id="e897c-151">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-152">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e897c-152">-ExpiryTime</span></span>
<span data-ttu-id="e897c-153">指定排程的到期時間作為 **DateTimeOffest** 物件。</span><span class="sxs-lookup"><span data-stu-id="e897c-153">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="e897c-154">您可以指定可轉換成有效 **DateTimeOffset** 的字串。</span><span class="sxs-lookup"><span data-stu-id="e897c-154">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-155">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="e897c-155">-HourInterval</span></span>
<span data-ttu-id="e897c-156">指定排程的間隔（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="e897c-156">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-157">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="e897c-157">-MonthInterval</span></span>
<span data-ttu-id="e897c-158">指定排程的間隔（以月為單位）。</span><span class="sxs-lookup"><span data-stu-id="e897c-158">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="e897c-159">-Name</span></span>
<span data-ttu-id="e897c-160">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="e897c-160">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-161">-OneTime</span><span class="sxs-lookup"><span data-stu-id="e897c-161">-OneTime</span></span>
<span data-ttu-id="e897c-162">指定 Cmdlet 建立一次時間排程。</span><span class="sxs-lookup"><span data-stu-id="e897c-162">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e897c-163">-ResourceGroupName</span></span>
<span data-ttu-id="e897c-164">指定此 Cmdlet 建立排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e897c-164">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e897c-165">-StartTime</span></span>
<span data-ttu-id="e897c-166">指定排程的開始時間做為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="e897c-166">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="e897c-167">您可以指定可轉換成有效 **DateTimeOffset** 的字串。</span><span class="sxs-lookup"><span data-stu-id="e897c-167">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="e897c-168">.</span><span class="sxs-lookup"><span data-stu-id="e897c-168">.</span></span> <span data-ttu-id="e897c-169">如果指定了 *時區* 參數，則會忽略偏移，並使用指定的時區。</span><span class="sxs-lookup"><span data-stu-id="e897c-169">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-170">-時區</span><span class="sxs-lookup"><span data-stu-id="e897c-170">-TimeZone</span></span>
<span data-ttu-id="e897c-171">指定排程的時區。</span><span class="sxs-lookup"><span data-stu-id="e897c-171">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="e897c-172">這個字串可以是 IANA ID 或 Windows 時區 ID。</span><span class="sxs-lookup"><span data-stu-id="e897c-172">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-173">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="e897c-173">-WeekInterval</span></span>
<span data-ttu-id="e897c-174">指定排程的間隔（以周為單位）。</span><span class="sxs-lookup"><span data-stu-id="e897c-174">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByWeekly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e897c-175">CommonParameters</span></span>
<span data-ttu-id="e897c-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e897c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e897c-177">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e897c-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e897c-178">輸入</span><span class="sxs-lookup"><span data-stu-id="e897c-178">INPUTS</span></span>

### <span data-ttu-id="e897c-179">所有</span><span class="sxs-lookup"><span data-stu-id="e897c-179">None</span></span>
<span data-ttu-id="e897c-180">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e897c-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e897c-181">輸出</span><span class="sxs-lookup"><span data-stu-id="e897c-181">OUTPUTS</span></span>

### <span data-ttu-id="e897c-182">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="e897c-182">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="e897c-183">筆記</span><span class="sxs-lookup"><span data-stu-id="e897c-183">NOTES</span></span>

## <span data-ttu-id="e897c-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="e897c-184">RELATED LINKS</span></span>

[<span data-ttu-id="e897c-185">AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e897c-185">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="e897c-186">移除-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e897c-186">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="e897c-187">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e897c-187">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)



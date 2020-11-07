---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967665"
---
# <span data-ttu-id="03bb2-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="03bb2-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="03bb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03bb2-102">SYNOPSIS</span></span>

<span data-ttu-id="03bb2-103">建立自動化排程。</span><span class="sxs-lookup"><span data-stu-id="03bb2-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="03bb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="03bb2-104">SYNTAX</span></span>

### <span data-ttu-id="03bb2-105">ByDaily (預設) </span><span class="sxs-lookup"><span data-stu-id="03bb2-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="03bb2-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="03bb2-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="03bb2-107">ByHourly</span><span class="sxs-lookup"><span data-stu-id="03bb2-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="03bb2-108">說明</span><span class="sxs-lookup"><span data-stu-id="03bb2-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="03bb2-109">**新的-AzureAutomationSchedule** Cmdlet 會在 Microsoft Azure 自動化中建立排程。</span><span class="sxs-lookup"><span data-stu-id="03bb2-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="03bb2-110">示例</span><span class="sxs-lookup"><span data-stu-id="03bb2-110">EXAMPLES</span></span>

### <span data-ttu-id="03bb2-111">範例1：建立一次性排程</span><span class="sxs-lookup"><span data-stu-id="03bb2-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="03bb2-112">下列命令會建立一個排程，該排程會在目前日期的 11:00 PM 執行一次。</span><span class="sxs-lookup"><span data-stu-id="03bb2-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="03bb2-113">範例2：建立週期性排程</span><span class="sxs-lookup"><span data-stu-id="03bb2-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="03bb2-114">下列命令會建立一個新排程，該排程會在每一年的 1:00 PM 開始（從當天起）。</span><span class="sxs-lookup"><span data-stu-id="03bb2-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="03bb2-115">參數</span><span class="sxs-lookup"><span data-stu-id="03bb2-115">PARAMETERS</span></span>

### <span data-ttu-id="03bb2-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03bb2-116">-AutomationAccountName</span></span>
<span data-ttu-id="03bb2-117">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="03bb2-117">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="03bb2-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="03bb2-118">-DayInterval</span></span>
<span data-ttu-id="03bb2-119">指定排程的間隔（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="03bb2-119">Specifies an interval, in days, for the schedule.</span></span>

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

### <span data-ttu-id="03bb2-120">-描述</span><span class="sxs-lookup"><span data-stu-id="03bb2-120">-Description</span></span>
<span data-ttu-id="03bb2-121">指定描述。</span><span class="sxs-lookup"><span data-stu-id="03bb2-121">Specifies a description.</span></span>

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

### <span data-ttu-id="03bb2-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="03bb2-122">-ExpiryTime</span></span>
<span data-ttu-id="03bb2-123">指定排程的到期時間。</span><span class="sxs-lookup"><span data-stu-id="03bb2-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="03bb2-124">如果可將字串轉換成有效的 **日期時間** ，就可以提供字串。</span><span class="sxs-lookup"><span data-stu-id="03bb2-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bb2-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="03bb2-125">-HourInterval</span></span>
<span data-ttu-id="03bb2-126">指定排程的間隔（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="03bb2-126">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="03bb2-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="03bb2-127">-Name</span></span>
<span data-ttu-id="03bb2-128">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="03bb2-128">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="03bb2-129">-OneTime</span><span class="sxs-lookup"><span data-stu-id="03bb2-129">-OneTime</span></span>
<span data-ttu-id="03bb2-130">表示此作業會建立一次排程。</span><span class="sxs-lookup"><span data-stu-id="03bb2-130">Indicates that this operation creates a one-time schedule.</span></span>

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

### <span data-ttu-id="03bb2-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="03bb2-131">-Profile</span></span>
<span data-ttu-id="03bb2-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="03bb2-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03bb2-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="03bb2-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bb2-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="03bb2-134">-StartTime</span></span>
<span data-ttu-id="03bb2-135">指定排程的開始時間。</span><span class="sxs-lookup"><span data-stu-id="03bb2-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="03bb2-136">如果可將字串轉換成有效的 **日期時間** ，就可以提供字串。</span><span class="sxs-lookup"><span data-stu-id="03bb2-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bb2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bb2-137">CommonParameters</span></span>
<span data-ttu-id="03bb2-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03bb2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bb2-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03bb2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bb2-140">輸入</span><span class="sxs-lookup"><span data-stu-id="03bb2-140">INPUTS</span></span>

## <span data-ttu-id="03bb2-141">輸出</span><span class="sxs-lookup"><span data-stu-id="03bb2-141">OUTPUTS</span></span>

### <span data-ttu-id="03bb2-142">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="03bb2-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="03bb2-143">筆記</span><span class="sxs-lookup"><span data-stu-id="03bb2-143">NOTES</span></span>

## <span data-ttu-id="03bb2-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="03bb2-144">RELATED LINKS</span></span>

[<span data-ttu-id="03bb2-145">AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="03bb2-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="03bb2-146">移除-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="03bb2-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="03bb2-147">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="03bb2-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)



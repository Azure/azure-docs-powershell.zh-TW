---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 3637709ca347a8e00433f247c80ec1c916e42017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447163"
---
# <span data-ttu-id="105c6-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="105c6-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="105c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="105c6-102">SYNOPSIS</span></span>
<span data-ttu-id="105c6-103">建立備份保留原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="105c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="105c6-104">SYNTAX</span></span>

### <span data-ttu-id="105c6-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="105c6-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105c6-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="105c6-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105c6-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="105c6-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105c6-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="105c6-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105c6-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="105c6-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105c6-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="105c6-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="105c6-111">說明</span><span class="sxs-lookup"><span data-stu-id="105c6-111">DESCRIPTION</span></span>
<span data-ttu-id="105c6-112">**新的-AzureRmBackupRetentionPolicyObject** Cmdlet 會建立 Azure 備份保留原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="105c6-113">保留原則定義備份保留復原點的時間長度。</span><span class="sxs-lookup"><span data-stu-id="105c6-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="105c6-114">保留類型如下：</span><span class="sxs-lookup"><span data-stu-id="105c6-114">The types of retention are the following:</span></span> 

- <span data-ttu-id="105c6-115">日常</span><span class="sxs-lookup"><span data-stu-id="105c6-115">Daily</span></span> 
- <span data-ttu-id="105c6-116">周更新</span><span class="sxs-lookup"><span data-stu-id="105c6-116">Weekly</span></span> 
- <span data-ttu-id="105c6-117">次</span><span class="sxs-lookup"><span data-stu-id="105c6-117">Monthly</span></span> 
- <span data-ttu-id="105c6-118">每年</span><span class="sxs-lookup"><span data-stu-id="105c6-118">Yearly</span></span> 

<span data-ttu-id="105c6-119">針對您打算使用的每個保留類型，建立一個保留原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-119">Create one retention policy for each type of retention that you plan to use.</span></span>

<span data-ttu-id="105c6-120">備份原則與至少一個保留原則相關聯。</span><span class="sxs-lookup"><span data-stu-id="105c6-120">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="105c6-121">若要建立備份原則，請使用 New-AzureRmBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="105c6-121">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="105c6-122">您可以改為提供 Enable-AzureRmBackupProtection Cmdlet 的保留原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-122">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="105c6-123">示例</span><span class="sxs-lookup"><span data-stu-id="105c6-123">EXAMPLES</span></span>

### <span data-ttu-id="105c6-124">範例1：針對日常保留建立保留原則</span><span class="sxs-lookup"><span data-stu-id="105c6-124">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="105c6-125">第一個命令會在每日保留30天內建立保留原則，然後將它儲存在 $Daily 變數中。</span><span class="sxs-lookup"><span data-stu-id="105c6-125">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="105c6-126">第二個命令會顯示 $Daily 的內容。</span><span class="sxs-lookup"><span data-stu-id="105c6-126">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="105c6-127">範例2：建立每月保留原則</span><span class="sxs-lookup"><span data-stu-id="105c6-127">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="105c6-128">第一個命令會建立保留原則，在每個月的第10個和第二十個月為12個月保留備份。</span><span class="sxs-lookup"><span data-stu-id="105c6-128">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="105c6-129">該命令會將保留原則儲存在 $Monthly 變數中。</span><span class="sxs-lookup"><span data-stu-id="105c6-129">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="105c6-130">第二個命令會顯示 $Monthly 的內容。</span><span class="sxs-lookup"><span data-stu-id="105c6-130">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="105c6-131">參數</span><span class="sxs-lookup"><span data-stu-id="105c6-131">PARAMETERS</span></span>

### <span data-ttu-id="105c6-132">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="105c6-132">-DailyRetention</span></span>
<span data-ttu-id="105c6-133">表示此 Cmdlet 會建立每日保留原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-133">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-134">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="105c6-134">-DaysOfMonth</span></span>
<span data-ttu-id="105c6-135">指定月份的天數，確定備份會保留哪些復原點數，以及需要多久的時間。</span><span class="sxs-lookup"><span data-stu-id="105c6-135">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="105c6-136">此參數可接受的值為：1到28和最後的整數。</span><span class="sxs-lookup"><span data-stu-id="105c6-136">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="105c6-137">如果您指定 *DailyRetention* 、 *MonthlyRetentionInDailyFormat* 和 *YearlyRetentionInDailyFormat* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="105c6-137">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-138">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="105c6-138">-DaysOfWeek</span></span>
<span data-ttu-id="105c6-139">指定一周中的天數陣列。</span><span class="sxs-lookup"><span data-stu-id="105c6-139">Specifies an array of days of the week.</span></span>
<span data-ttu-id="105c6-140">此 Cmdlet 指定的天數會識別備份會保留哪些復原點，以及需要多久的時間。</span><span class="sxs-lookup"><span data-stu-id="105c6-140">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="105c6-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="105c6-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="105c6-142">從</span><span class="sxs-lookup"><span data-stu-id="105c6-142">Monday</span></span> 
- <span data-ttu-id="105c6-143">星期二</span><span class="sxs-lookup"><span data-stu-id="105c6-143">Tuesday</span></span> 
- <span data-ttu-id="105c6-144">星期三</span><span class="sxs-lookup"><span data-stu-id="105c6-144">Wednesday</span></span> 
- <span data-ttu-id="105c6-145">星期四</span><span class="sxs-lookup"><span data-stu-id="105c6-145">Thursday</span></span> 
- <span data-ttu-id="105c6-146">日</span><span class="sxs-lookup"><span data-stu-id="105c6-146">Friday</span></span> 
- <span data-ttu-id="105c6-147">星期六</span><span class="sxs-lookup"><span data-stu-id="105c6-147">Saturday</span></span> 
- <span data-ttu-id="105c6-148">日</span><span class="sxs-lookup"><span data-stu-id="105c6-148">Sunday</span></span>

<span data-ttu-id="105c6-149">如果您指定 *WeeklyRetention* 、 *MonthlyRetentionInWeeklyFormat* 和 *YearlyRetentionInWeeklyFormat* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="105c6-149">Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>

<span data-ttu-id="105c6-150">請確定您針對 [備份] 和 [保留] 選取的周數已對齊。</span><span class="sxs-lookup"><span data-stu-id="105c6-150">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="105c6-151">例如，如果您的備份是針對星期六設定，則保留原則也必須使用星期六。</span><span class="sxs-lookup"><span data-stu-id="105c6-151">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="105c6-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="105c6-153">表示此 Cmdlet 會以每日格式建立每月原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="105c6-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="105c6-155">表示此 Cmdlet 會以每週格式建立每月原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="105c6-156">-MonthsOfYear</span></span>
<span data-ttu-id="105c6-157">指定年份中哪些月份的復原點數會每年保留一次。</span><span class="sxs-lookup"><span data-stu-id="105c6-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="105c6-158">此參數可接受的值為：月份的名稱，例如一月或二月。</span><span class="sxs-lookup"><span data-stu-id="105c6-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-159">-保留</span><span class="sxs-lookup"><span data-stu-id="105c6-159">-Retention</span></span>
<span data-ttu-id="105c6-160">指定備份儲存備份點的保留期間（以天、月或年為單位）。</span><span class="sxs-lookup"><span data-stu-id="105c6-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="105c6-161">單位視這個 Cmdlet 是否選取 [每日]、[每月] 或 [每年] 保留選項而定。</span><span class="sxs-lookup"><span data-stu-id="105c6-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="105c6-162">例如，如果您指定 *DailyRetention* 參數，則 Cmdlet 會將目前的參數轉譯為數天。</span><span class="sxs-lookup"><span data-stu-id="105c6-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="105c6-163">-WeeklyRetention</span></span>
<span data-ttu-id="105c6-164">表示此 Cmdlet 會建立每週保留原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="105c6-165">-WeekNumber</span></span>
<span data-ttu-id="105c6-166">指定月份的周數，找出備份會保留哪些復原點數，以及需要多久的時間。</span><span class="sxs-lookup"><span data-stu-id="105c6-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="105c6-167">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="105c6-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="105c6-168">一</span><span class="sxs-lookup"><span data-stu-id="105c6-168">First</span></span> 
- <span data-ttu-id="105c6-169">第二個</span><span class="sxs-lookup"><span data-stu-id="105c6-169">Second</span></span> 
- <span data-ttu-id="105c6-170">個</span><span class="sxs-lookup"><span data-stu-id="105c6-170">Third</span></span> 
- <span data-ttu-id="105c6-171">1/4</span><span class="sxs-lookup"><span data-stu-id="105c6-171">Fourth</span></span> 
- <span data-ttu-id="105c6-172">年</span><span class="sxs-lookup"><span data-stu-id="105c6-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="105c6-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="105c6-174">表示此 Cmdlet 會以每日格式建立每年保留原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="105c6-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="105c6-176">表示此 Cmdlet 會以每週格式建立每年保留原則。</span><span class="sxs-lookup"><span data-stu-id="105c6-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105c6-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105c6-177">-DefaultProfile</span></span>
<span data-ttu-id="105c6-178">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="105c6-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="105c6-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105c6-179">CommonParameters</span></span>
<span data-ttu-id="105c6-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="105c6-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105c6-181">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="105c6-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105c6-182">輸入</span><span class="sxs-lookup"><span data-stu-id="105c6-182">INPUTS</span></span>

### <span data-ttu-id="105c6-183">所有</span><span class="sxs-lookup"><span data-stu-id="105c6-183">None</span></span>

## <span data-ttu-id="105c6-184">輸出</span><span class="sxs-lookup"><span data-stu-id="105c6-184">OUTPUTS</span></span>

### <span data-ttu-id="105c6-185">AzureRmBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="105c6-185">AzureRmBackupRetentionPolicy</span></span>

## <span data-ttu-id="105c6-186">筆記</span><span class="sxs-lookup"><span data-stu-id="105c6-186">NOTES</span></span>
* <span data-ttu-id="105c6-187">所有</span><span class="sxs-lookup"><span data-stu-id="105c6-187">None</span></span>

## <span data-ttu-id="105c6-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="105c6-188">RELATED LINKS</span></span>

[<span data-ttu-id="105c6-189">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="105c6-189">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="105c6-190">新-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="105c6-190">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)



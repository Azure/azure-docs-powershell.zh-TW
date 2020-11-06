---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 740077def0ba0eccb1d962b88317fadb3c5c897c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445740"
---
# <span data-ttu-id="330a0-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="330a0-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="330a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="330a0-102">SYNOPSIS</span></span>
<span data-ttu-id="330a0-103">建立備份保留原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="330a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="330a0-104">SYNTAX</span></span>

### <span data-ttu-id="330a0-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="330a0-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="330a0-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="330a0-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="330a0-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="330a0-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="330a0-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="330a0-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="330a0-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="330a0-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="330a0-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="330a0-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="330a0-111">說明</span><span class="sxs-lookup"><span data-stu-id="330a0-111">DESCRIPTION</span></span>
<span data-ttu-id="330a0-112">**新的-AzureRmBackupRetentionPolicyObject** Cmdlet 會建立 Azure 備份保留原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="330a0-113">保留原則定義備份保留復原點的時間長度。</span><span class="sxs-lookup"><span data-stu-id="330a0-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="330a0-114">保留類型如下：</span><span class="sxs-lookup"><span data-stu-id="330a0-114">The types of retention are the following:</span></span> 
- <span data-ttu-id="330a0-115">日常</span><span class="sxs-lookup"><span data-stu-id="330a0-115">Daily</span></span> 
- <span data-ttu-id="330a0-116">周更新</span><span class="sxs-lookup"><span data-stu-id="330a0-116">Weekly</span></span> 
- <span data-ttu-id="330a0-117">次</span><span class="sxs-lookup"><span data-stu-id="330a0-117">Monthly</span></span> 
- <span data-ttu-id="330a0-118">每年針對您打算使用的每個保留類型建立一個保留原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-118">Yearly Create one retention policy for each type of retention that you plan to use.</span></span>
<span data-ttu-id="330a0-119">備份原則與至少一個保留原則相關聯。</span><span class="sxs-lookup"><span data-stu-id="330a0-119">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="330a0-120">若要建立備份原則，請使用 New-AzureRmBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="330a0-120">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="330a0-121">您可以改為提供 Enable-AzureRmBackupProtection Cmdlet 的保留原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-121">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="330a0-122">示例</span><span class="sxs-lookup"><span data-stu-id="330a0-122">EXAMPLES</span></span>

### <span data-ttu-id="330a0-123">範例1：針對日常保留建立保留原則</span><span class="sxs-lookup"><span data-stu-id="330a0-123">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="330a0-124">第一個命令會在每日保留30天內建立保留原則，然後將它儲存在 $Daily 變數中。</span><span class="sxs-lookup"><span data-stu-id="330a0-124">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="330a0-125">第二個命令會顯示 $Daily 的內容。</span><span class="sxs-lookup"><span data-stu-id="330a0-125">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="330a0-126">範例2：建立每月保留原則</span><span class="sxs-lookup"><span data-stu-id="330a0-126">Example 2: Create a monthly retention policy</span></span>
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

<span data-ttu-id="330a0-127">第一個命令會建立保留原則，在每個月的第10個和第二十個月為12個月保留備份。</span><span class="sxs-lookup"><span data-stu-id="330a0-127">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="330a0-128">該命令會將保留原則儲存在 $Monthly 變數中。</span><span class="sxs-lookup"><span data-stu-id="330a0-128">The command stores the retention policy in the $Monthly variable.</span></span>
<span data-ttu-id="330a0-129">第二個命令會顯示 $Monthly 的內容。</span><span class="sxs-lookup"><span data-stu-id="330a0-129">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="330a0-130">參數</span><span class="sxs-lookup"><span data-stu-id="330a0-130">PARAMETERS</span></span>

### <span data-ttu-id="330a0-131">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="330a0-131">-DailyRetention</span></span>
<span data-ttu-id="330a0-132">表示此 Cmdlet 會建立每日保留原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-132">Indicates that this cmdlet creates a Daily retention policy.</span></span>

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

### <span data-ttu-id="330a0-133">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="330a0-133">-DaysOfMonth</span></span>
<span data-ttu-id="330a0-134">指定月份的天數，確定備份會保留哪些復原點數，以及需要多久的時間。</span><span class="sxs-lookup"><span data-stu-id="330a0-134">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="330a0-135">此參數可接受的值為：1到28和最後的整數。</span><span class="sxs-lookup"><span data-stu-id="330a0-135">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="330a0-136">如果您指定 *DailyRetention* 、 *MonthlyRetentionInDailyFormat* 和 *YearlyRetentionInDailyFormat* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="330a0-136">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

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

### <span data-ttu-id="330a0-137">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="330a0-137">-DaysOfWeek</span></span>
<span data-ttu-id="330a0-138">指定一周中的天數陣列。</span><span class="sxs-lookup"><span data-stu-id="330a0-138">Specifies an array of days of the week.</span></span>
<span data-ttu-id="330a0-139">此 Cmdlet 指定的天數會識別備份會保留哪些復原點，以及需要多久的時間。</span><span class="sxs-lookup"><span data-stu-id="330a0-139">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="330a0-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="330a0-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="330a0-141">從</span><span class="sxs-lookup"><span data-stu-id="330a0-141">Monday</span></span> 
- <span data-ttu-id="330a0-142">星期二</span><span class="sxs-lookup"><span data-stu-id="330a0-142">Tuesday</span></span> 
- <span data-ttu-id="330a0-143">星期三</span><span class="sxs-lookup"><span data-stu-id="330a0-143">Wednesday</span></span> 
- <span data-ttu-id="330a0-144">星期四</span><span class="sxs-lookup"><span data-stu-id="330a0-144">Thursday</span></span> 
- <span data-ttu-id="330a0-145">日</span><span class="sxs-lookup"><span data-stu-id="330a0-145">Friday</span></span> 
- <span data-ttu-id="330a0-146">星期六</span><span class="sxs-lookup"><span data-stu-id="330a0-146">Saturday</span></span> 
- <span data-ttu-id="330a0-147">星期天如果您指定 *WeeklyRetention* 、 *MonthlyRetentionInWeeklyFormat* 和 *YearlyRetentionInWeeklyFormat* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="330a0-147">Sunday Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>
<span data-ttu-id="330a0-148">請確定您針對 [備份] 和 [保留] 選取的周數已對齊。</span><span class="sxs-lookup"><span data-stu-id="330a0-148">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="330a0-149">例如，如果您的備份是針對星期六設定，則保留原則也必須使用星期六。</span><span class="sxs-lookup"><span data-stu-id="330a0-149">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

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

### <span data-ttu-id="330a0-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="330a0-150">-DefaultProfile</span></span>
<span data-ttu-id="330a0-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="330a0-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="330a0-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="330a0-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="330a0-153">表示此 Cmdlet 會以每日格式建立每月原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

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

### <span data-ttu-id="330a0-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="330a0-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="330a0-155">表示此 Cmdlet 會以每週格式建立每月原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

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

### <span data-ttu-id="330a0-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="330a0-156">-MonthsOfYear</span></span>
<span data-ttu-id="330a0-157">指定年份中哪些月份的復原點數會每年保留一次。</span><span class="sxs-lookup"><span data-stu-id="330a0-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="330a0-158">此參數可接受的值為：月份的名稱，例如一月或二月。</span><span class="sxs-lookup"><span data-stu-id="330a0-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

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

### <span data-ttu-id="330a0-159">-保留</span><span class="sxs-lookup"><span data-stu-id="330a0-159">-Retention</span></span>
<span data-ttu-id="330a0-160">指定備份儲存備份點的保留期間（以天、月或年為單位）。</span><span class="sxs-lookup"><span data-stu-id="330a0-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="330a0-161">單位視這個 Cmdlet 是否選取 [每日]、[每月] 或 [每年] 保留選項而定。</span><span class="sxs-lookup"><span data-stu-id="330a0-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="330a0-162">例如，如果您指定 *DailyRetention* 參數，則 Cmdlet 會將目前的參數轉譯為數天。</span><span class="sxs-lookup"><span data-stu-id="330a0-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

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

### <span data-ttu-id="330a0-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="330a0-163">-WeeklyRetention</span></span>
<span data-ttu-id="330a0-164">表示此 Cmdlet 會建立每週保留原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

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

### <span data-ttu-id="330a0-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="330a0-165">-WeekNumber</span></span>
<span data-ttu-id="330a0-166">指定月份的周數，找出備份會保留哪些復原點數，以及需要多久的時間。</span><span class="sxs-lookup"><span data-stu-id="330a0-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="330a0-167">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="330a0-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="330a0-168">一</span><span class="sxs-lookup"><span data-stu-id="330a0-168">First</span></span> 
- <span data-ttu-id="330a0-169">第二個</span><span class="sxs-lookup"><span data-stu-id="330a0-169">Second</span></span> 
- <span data-ttu-id="330a0-170">個</span><span class="sxs-lookup"><span data-stu-id="330a0-170">Third</span></span> 
- <span data-ttu-id="330a0-171">1/4</span><span class="sxs-lookup"><span data-stu-id="330a0-171">Fourth</span></span> 
- <span data-ttu-id="330a0-172">年</span><span class="sxs-lookup"><span data-stu-id="330a0-172">Last</span></span>

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

### <span data-ttu-id="330a0-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="330a0-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="330a0-174">表示此 Cmdlet 會以每日格式建立每年保留原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

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

### <span data-ttu-id="330a0-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="330a0-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="330a0-176">表示此 Cmdlet 會以每週格式建立每年保留原則。</span><span class="sxs-lookup"><span data-stu-id="330a0-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

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

### <span data-ttu-id="330a0-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="330a0-177">CommonParameters</span></span>
<span data-ttu-id="330a0-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="330a0-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="330a0-179">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="330a0-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="330a0-180">輸入</span><span class="sxs-lookup"><span data-stu-id="330a0-180">INPUTS</span></span>

### <span data-ttu-id="330a0-181">所有</span><span class="sxs-lookup"><span data-stu-id="330a0-181">None</span></span>

## <span data-ttu-id="330a0-182">輸出</span><span class="sxs-lookup"><span data-stu-id="330a0-182">OUTPUTS</span></span>

### <span data-ttu-id="330a0-183">AzureRMBackupRetentionPolicy 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="330a0-183">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy</span></span>

## <span data-ttu-id="330a0-184">筆記</span><span class="sxs-lookup"><span data-stu-id="330a0-184">NOTES</span></span>
* <span data-ttu-id="330a0-185">所有</span><span class="sxs-lookup"><span data-stu-id="330a0-185">None</span></span>

## <span data-ttu-id="330a0-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="330a0-186">RELATED LINKS</span></span>

[<span data-ttu-id="330a0-187">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="330a0-187">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="330a0-188">新-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="330a0-188">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)



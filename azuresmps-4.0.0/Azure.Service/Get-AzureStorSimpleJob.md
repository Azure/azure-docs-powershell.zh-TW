---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967004"
---
# <span data-ttu-id="3cfa4-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="3cfa4-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="3cfa4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3cfa4-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfa4-103">取得 StorSimple 作業。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="3cfa4-104">句法</span><span class="sxs-lookup"><span data-stu-id="3cfa4-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cfa4-105">說明</span><span class="sxs-lookup"><span data-stu-id="3cfa4-105">DESCRIPTION</span></span>
<span data-ttu-id="3cfa4-106">**AzureStorSimpleJob** Cmdlet 會取得 Azure StorSimple 作業。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="3cfa4-107">指定實例識別碼以取得特定作業。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="3cfa4-108">指定其他參數，以限制此 Cmdlet 取得的作業。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="3cfa4-109">這個 Cmdlet 會傳回200工作的最大值。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="3cfa4-110">如果有超過200個作業，請使用 *第一個* 和 [ *略過* ] 參數來取得剩餘作業。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="3cfa4-111">如果您為 *Skip* 指定的值是100，而 *第一次* 則是50，則此 Cmdlet 不會傳回第一個100結果。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="3cfa4-112">它會在跳過的100之後傳回接下來的50結果。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="3cfa4-113">示例</span><span class="sxs-lookup"><span data-stu-id="3cfa4-113">EXAMPLES</span></span>

### <span data-ttu-id="3cfa4-114">範例1：使用識別碼來取得作業</span><span class="sxs-lookup"><span data-stu-id="3cfa4-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="3cfa4-115">這個命令會取得具有指定識別碼之作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="3cfa4-116">範例2：使用裝置名稱取得工作</span><span class="sxs-lookup"><span data-stu-id="3cfa4-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="3cfa4-117">這個命令會取得名為 8600-Bravo 001 之裝置工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="3cfa4-118">此命令會取得裝置的前兩個作業。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="3cfa4-119">範例3：取得完成的工作</span><span class="sxs-lookup"><span data-stu-id="3cfa4-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="3cfa4-120">這個命令會取得已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-120">This command gets completed jobs.</span></span>
<span data-ttu-id="3cfa4-121">命令在跳過前十個作業之後，只會取得前兩個作業。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="3cfa4-122">範例4：取得手動備份作業</span><span class="sxs-lookup"><span data-stu-id="3cfa4-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="3cfa4-123">這個命令會取得手動備份類型的作業。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="3cfa4-124">範例5：在指定的時間之間取得作業</span><span class="sxs-lookup"><span data-stu-id="3cfa4-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="3cfa4-125">前兩個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="3cfa4-126">這些命令會將新的時間儲存在 $StartTime，並 $EndTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="3cfa4-127">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="3cfa4-128">最終命令會在 $StartTime 和 $EndTime 中所儲存的時間之間，取得名為 Device07 之裝置的工作。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="3cfa4-129">參數</span><span class="sxs-lookup"><span data-stu-id="3cfa4-129">PARAMETERS</span></span>

### <span data-ttu-id="3cfa4-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3cfa4-130">-DeviceName</span></span>
<span data-ttu-id="3cfa4-131">指定 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-131">Specifies the name of a StorSimple device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa4-132">-優先</span><span class="sxs-lookup"><span data-stu-id="3cfa4-132">-First</span></span>
<span data-ttu-id="3cfa4-133">只取得指定數目的物件。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="3cfa4-134">輸入要取得的物件數目。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-134">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa4-135">-從</span><span class="sxs-lookup"><span data-stu-id="3cfa4-135">-From</span></span>
<span data-ttu-id="3cfa4-136">指定此 Cmdlet 取得作業的開始日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa4-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3cfa4-137">-InstanceId</span></span>
<span data-ttu-id="3cfa4-138">指定要取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-138">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa4-139">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3cfa4-139">-Profile</span></span>
<span data-ttu-id="3cfa4-140">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3cfa4-141">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3cfa4-142">-略過</span><span class="sxs-lookup"><span data-stu-id="3cfa4-142">-Skip</span></span>
<span data-ttu-id="3cfa4-143">忽略指定的物件數目，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="3cfa4-144">輸入要略過的物件數目。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-144">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa4-145">-狀態</span><span class="sxs-lookup"><span data-stu-id="3cfa4-145">-Status</span></span>
<span data-ttu-id="3cfa4-146">指定狀態。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-146">Specifies the status.</span></span>
<span data-ttu-id="3cfa4-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3cfa4-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3cfa4-148">進行</span><span class="sxs-lookup"><span data-stu-id="3cfa4-148">Running</span></span>
- <span data-ttu-id="3cfa4-149">完畢</span><span class="sxs-lookup"><span data-stu-id="3cfa4-149">Completed</span></span>
- <span data-ttu-id="3cfa4-150">取消</span><span class="sxs-lookup"><span data-stu-id="3cfa4-150">Cancelled</span></span>
- <span data-ttu-id="3cfa4-151">成功</span><span class="sxs-lookup"><span data-stu-id="3cfa4-151">Failed</span></span>
- <span data-ttu-id="3cfa4-152">取消</span><span class="sxs-lookup"><span data-stu-id="3cfa4-152">Canceling</span></span>
- <span data-ttu-id="3cfa4-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="3cfa4-153">CompletedWithErrors</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa4-154">-To</span><span class="sxs-lookup"><span data-stu-id="3cfa4-154">-To</span></span>
<span data-ttu-id="3cfa4-155">指定此 Cmdlet 取得作業的結束日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa4-156">-類型</span><span class="sxs-lookup"><span data-stu-id="3cfa4-156">-Type</span></span>
<span data-ttu-id="3cfa4-157">指定作業類型。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-157">Specifies the job type.</span></span>
<span data-ttu-id="3cfa4-158">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3cfa4-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3cfa4-159">備份</span><span class="sxs-lookup"><span data-stu-id="3cfa4-159">Backup</span></span>
- <span data-ttu-id="3cfa4-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="3cfa4-160">ManualBackup</span></span>
- <span data-ttu-id="3cfa4-161">還原</span><span class="sxs-lookup"><span data-stu-id="3cfa4-161">Restore</span></span>
- <span data-ttu-id="3cfa4-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="3cfa4-162">CloneWorkflow</span></span>
- <span data-ttu-id="3cfa4-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="3cfa4-163">DeviceRestore</span></span>
- <span data-ttu-id="3cfa4-164">時更新</span><span class="sxs-lookup"><span data-stu-id="3cfa4-164">Update</span></span>
- <span data-ttu-id="3cfa4-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="3cfa4-165">SupportPackage</span></span>
- <span data-ttu-id="3cfa4-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="3cfa4-166">VirtualApplianceProvisioning</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa4-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfa4-167">CommonParameters</span></span>
<span data-ttu-id="3cfa4-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfa4-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfa4-170">輸入</span><span class="sxs-lookup"><span data-stu-id="3cfa4-170">INPUTS</span></span>

### <span data-ttu-id="3cfa4-171">所有</span><span class="sxs-lookup"><span data-stu-id="3cfa4-171">None</span></span>
<span data-ttu-id="3cfa4-172">您無法將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="3cfa4-173">輸出</span><span class="sxs-lookup"><span data-stu-id="3cfa4-173">OUTPUTS</span></span>

### <span data-ttu-id="3cfa4-174">IList \<DeviceJobDetails\> 、DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="3cfa4-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="3cfa4-175">這個 Cmdlet 會傳回作業詳細資料物件的清單，或者，如果您指定 *InstanceID* 參數，則會傳回單一作業詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="3cfa4-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="3cfa4-176">筆記</span><span class="sxs-lookup"><span data-stu-id="3cfa4-176">NOTES</span></span>

## <span data-ttu-id="3cfa4-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cfa4-177">RELATED LINKS</span></span>

[<span data-ttu-id="3cfa4-178">停止 AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="3cfa4-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)



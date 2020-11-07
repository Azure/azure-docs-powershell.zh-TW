---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967298"
---
# <span data-ttu-id="bcb09-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb09-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="bcb09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcb09-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb09-103">更新現有的備份原則。</span><span class="sxs-lookup"><span data-stu-id="bcb09-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="bcb09-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcb09-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bcb09-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcb09-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb09-106">**AzureStorSimpleDeviceBackupPolicy** Cmdlet 會更新現有的備份原則。</span><span class="sxs-lookup"><span data-stu-id="bcb09-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="bcb09-107">您可以重新命名原則、新增、更新或刪除排程，以及更新與原則相關聯的磁片。</span><span class="sxs-lookup"><span data-stu-id="bcb09-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="bcb09-108">示例</span><span class="sxs-lookup"><span data-stu-id="bcb09-108">EXAMPLES</span></span>

### <span data-ttu-id="bcb09-109">範例1：變更備份原則的名稱</span><span class="sxs-lookup"><span data-stu-id="bcb09-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="bcb09-110">這個命令會將具有指定識別碼的備份原則名稱變更為 UpdatedGeneralPolicy07。</span><span class="sxs-lookup"><span data-stu-id="bcb09-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="bcb09-111">這個命令會指定 *WaitForComplete* 參數，因此命令會完成任務，然後傳回工作的 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="bcb09-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="bcb09-112">範例2：更新備份原則的排程</span><span class="sxs-lookup"><span data-stu-id="bcb09-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="bcb09-113">第一個命令會使用 **AzureStorSimpleDeviceBackupScheduleUpdateConfig** Cmdlet 建立更新設定物件，然後將它儲存在 $UpdateConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="bcb09-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="bcb09-114">第二個命令會建立名為 $UpdateArray 的新陣列變數。</span><span class="sxs-lookup"><span data-stu-id="bcb09-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="bcb09-115">下一個命令會將儲存在 $UpdateConfig 的更新加到該陣列中。</span><span class="sxs-lookup"><span data-stu-id="bcb09-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="bcb09-116">您可以在陣列中新增一個以上的更新。</span><span class="sxs-lookup"><span data-stu-id="bcb09-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="bcb09-117">Final 命令會更新名為 Contoso63-AppVm 的裝置上具有指定識別碼的備份原則。</span><span class="sxs-lookup"><span data-stu-id="bcb09-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="bcb09-118">原則現在已將更新的排程儲存在 $UpdateArray 中。</span><span class="sxs-lookup"><span data-stu-id="bcb09-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="bcb09-119">參數</span><span class="sxs-lookup"><span data-stu-id="bcb09-119">PARAMETERS</span></span>

### <span data-ttu-id="bcb09-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="bcb09-120">-BackupPolicyId</span></span>
<span data-ttu-id="bcb09-121">指定要更新之 **BackupPolicy** 物件的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcb09-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb09-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="bcb09-122">-BackupPolicyName</span></span>
<span data-ttu-id="bcb09-123">指定備份原則的新名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb09-123">Specifies a new name for the backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb09-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="bcb09-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="bcb09-125">指定要刪除之 **BackupSchedule** 物件的實例識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="bcb09-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb09-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="bcb09-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="bcb09-127">指定要新增至原則的 **BackupScheduleBase** 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="bcb09-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="bcb09-128">若要取得 **BackupScheduleBase** 物件，請使用 **AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcb09-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb09-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="bcb09-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="bcb09-130">指定要更新的 **BackupScheduleUpdateRequest** 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="bcb09-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="bcb09-131">若要取得 **BackupScheduleUpdateRequest** 物件，請使用 **AzureStorSimpleDeviceBackupScheduleUpdateConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcb09-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb09-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bcb09-132">-DeviceName</span></span>
<span data-ttu-id="bcb09-133">指定要更新備份原則之 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb09-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb09-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="bcb09-134">-NewName</span></span>
<span data-ttu-id="bcb09-135">指定裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb09-135">Specifies a name for the device.</span></span>

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

### <span data-ttu-id="bcb09-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bcb09-136">-Profile</span></span>
<span data-ttu-id="bcb09-137">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bcb09-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bcb09-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="bcb09-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="bcb09-139">指定要更新備份原則之卷 Id 的陣列。</span><span class="sxs-lookup"><span data-stu-id="bcb09-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb09-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="bcb09-140">-WaitForComplete</span></span>
<span data-ttu-id="bcb09-141">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="bcb09-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb09-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb09-142">CommonParameters</span></span>
<span data-ttu-id="bcb09-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcb09-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb09-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcb09-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb09-145">輸入</span><span class="sxs-lookup"><span data-stu-id="bcb09-145">INPUTS</span></span>

### <span data-ttu-id="bcb09-146">所有</span><span class="sxs-lookup"><span data-stu-id="bcb09-146">None</span></span>

## <span data-ttu-id="bcb09-147">輸出</span><span class="sxs-lookup"><span data-stu-id="bcb09-147">OUTPUTS</span></span>

### <span data-ttu-id="bcb09-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="bcb09-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="bcb09-149">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="bcb09-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="bcb09-150">如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="bcb09-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="bcb09-151">筆記</span><span class="sxs-lookup"><span data-stu-id="bcb09-151">NOTES</span></span>

## <span data-ttu-id="bcb09-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcb09-152">RELATED LINKS</span></span>

[<span data-ttu-id="bcb09-153">AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb09-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="bcb09-154">新-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb09-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="bcb09-155">移除-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bcb09-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="bcb09-156">新-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="bcb09-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)



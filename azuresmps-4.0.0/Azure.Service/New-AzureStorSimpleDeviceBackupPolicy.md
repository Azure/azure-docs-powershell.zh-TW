---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967654"
---
# <span data-ttu-id="1099d-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1099d-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="1099d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1099d-102">SYNOPSIS</span></span>
<span data-ttu-id="1099d-103">建立備份原則。</span><span class="sxs-lookup"><span data-stu-id="1099d-103">Creates a backup policy.</span></span>

## <span data-ttu-id="1099d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1099d-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1099d-105">說明</span><span class="sxs-lookup"><span data-stu-id="1099d-105">DESCRIPTION</span></span>
<span data-ttu-id="1099d-106">**新的-AzureStorSimpleDeviceBackupPolicy** Cmdlet 會建立備份原則。</span><span class="sxs-lookup"><span data-stu-id="1099d-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="1099d-107">備份原則包含一或多個可以在一或多個卷上執行的備份排程。</span><span class="sxs-lookup"><span data-stu-id="1099d-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="1099d-108">若要建立備份排程，請使用 **AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1099d-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="1099d-109">示例</span><span class="sxs-lookup"><span data-stu-id="1099d-109">EXAMPLES</span></span>

### <span data-ttu-id="1099d-110">範例1：建立備份原則</span><span class="sxs-lookup"><span data-stu-id="1099d-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="1099d-111">第一個命令會使用 **新的 AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet 來建立備份排程設定物件，然後將該物件儲存在 $Schedule 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="1099d-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="1099d-112">第二個命令會使用 **新的 AzureStorSimpleDeviceBackupScheduleAddConfig** 建立另一個備份設定物件，然後將該物件儲存在 $Schedule 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="1099d-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="1099d-113">第三個命令會建立一個名為 $ScheduleArray 的空陣列變數。</span><span class="sxs-lookup"><span data-stu-id="1099d-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="1099d-114">接下來的兩個命令會將在前兩個命令中建立的物件新增到 $ScheduleArray。</span><span class="sxs-lookup"><span data-stu-id="1099d-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="1099d-115">第六個命令會使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet，透過名為 Contoso63-AppVm 的裝置取得體積容器，然後將該容器物件儲存在 $DeviceContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="1099d-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="1099d-116">第七個命令會使用 **AzureStorSimpleDeviceVolume** Cmdlet 來取得儲存在 $DeviceContainer 第一個成員中之卷容器的體積，然後將該體積條儲存在 $Volume 變數中。</span><span class="sxs-lookup"><span data-stu-id="1099d-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="1099d-117">第八個命令會建立一個名為 $VolumeArray 的空陣列變數。</span><span class="sxs-lookup"><span data-stu-id="1099d-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="1099d-118">下一個命令會將卷識別碼新增到 $VolumeArray。</span><span class="sxs-lookup"><span data-stu-id="1099d-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="1099d-119">此值會識別儲存在備份原則執行之 $Volume 的音量。</span><span class="sxs-lookup"><span data-stu-id="1099d-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="1099d-120">您可以將其他卷識別碼新增至 $VolumeArray。</span><span class="sxs-lookup"><span data-stu-id="1099d-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="1099d-121">最終命令會針對名為 Contoso63-AppVm 的裝置建立名為 GeneralPolicy07 的備份原則。</span><span class="sxs-lookup"><span data-stu-id="1099d-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="1099d-122">此命令會指定儲存在 $ScheduleArray 中的排程設定物件。</span><span class="sxs-lookup"><span data-stu-id="1099d-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="1099d-123">此命令會指定 $VolumeArray 中要套用原則的量或體積。</span><span class="sxs-lookup"><span data-stu-id="1099d-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="1099d-124">您可以使用 **AzureStorSimpleDeviceBackupPolicy** Cmdlet 來驗證備份原則。</span><span class="sxs-lookup"><span data-stu-id="1099d-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="1099d-125">參數</span><span class="sxs-lookup"><span data-stu-id="1099d-125">PARAMETERS</span></span>

### <span data-ttu-id="1099d-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="1099d-126">-BackupPolicyName</span></span>
<span data-ttu-id="1099d-127">指定備份原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="1099d-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="1099d-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="1099d-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="1099d-129">指定要新增至原則的 **BackupScheduleBase** 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="1099d-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="1099d-130">每個物件代表排程。</span><span class="sxs-lookup"><span data-stu-id="1099d-130">Each object represents a schedule.</span></span>
<span data-ttu-id="1099d-131">備份原則包含一或多個排程。</span><span class="sxs-lookup"><span data-stu-id="1099d-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="1099d-132">若要取得 **BackupScheduleBase** 物件，請使用 **AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1099d-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1099d-133">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1099d-133">-DeviceName</span></span>
<span data-ttu-id="1099d-134">指定要建立備份原則之 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="1099d-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="1099d-135">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1099d-135">-Profile</span></span>
<span data-ttu-id="1099d-136">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1099d-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="1099d-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="1099d-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="1099d-138">指定要新增至備份原則之卷識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="1099d-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1099d-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="1099d-139">-WaitForComplete</span></span>
<span data-ttu-id="1099d-140">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="1099d-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="1099d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1099d-141">CommonParameters</span></span>
<span data-ttu-id="1099d-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1099d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1099d-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1099d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1099d-144">輸入</span><span class="sxs-lookup"><span data-stu-id="1099d-144">INPUTS</span></span>

### <span data-ttu-id="1099d-145">所有</span><span class="sxs-lookup"><span data-stu-id="1099d-145">None</span></span>

## <span data-ttu-id="1099d-146">輸出</span><span class="sxs-lookup"><span data-stu-id="1099d-146">OUTPUTS</span></span>

### <span data-ttu-id="1099d-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1099d-147">BackupPolicy</span></span>
<span data-ttu-id="1099d-148">這個 Cmdlet 會傳回包含新排程和卷的 **BackupPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="1099d-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="1099d-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1099d-149">NOTES</span></span>

## <span data-ttu-id="1099d-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1099d-150">RELATED LINKS</span></span>

[<span data-ttu-id="1099d-151">AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1099d-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="1099d-152">AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="1099d-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="1099d-153">AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="1099d-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="1099d-154">移除-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1099d-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="1099d-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1099d-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="1099d-156">新-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="1099d-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)



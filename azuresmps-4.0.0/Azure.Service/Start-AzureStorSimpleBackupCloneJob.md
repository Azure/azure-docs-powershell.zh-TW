---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967194"
---
# <span data-ttu-id="f234b-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="f234b-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="f234b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f234b-102">SYNOPSIS</span></span>
<span data-ttu-id="f234b-103">啟動作業，在裝置上克隆備份。</span><span class="sxs-lookup"><span data-stu-id="f234b-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="f234b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f234b-104">SYNTAX</span></span>

### <span data-ttu-id="f234b-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="f234b-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f234b-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="f234b-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f234b-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="f234b-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f234b-108">說明</span><span class="sxs-lookup"><span data-stu-id="f234b-108">DESCRIPTION</span></span>
<span data-ttu-id="f234b-109">**AzureStorSimpleBackupCloneJob** Cmdlet 會啟動一個作業，在 StorSimple 裝置上克隆現有的備份。</span><span class="sxs-lookup"><span data-stu-id="f234b-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="f234b-110">示例</span><span class="sxs-lookup"><span data-stu-id="f234b-110">EXAMPLES</span></span>

### <span data-ttu-id="f234b-111">範例1：使用裝置名稱將備份克隆至不同的磁片卷</span><span class="sxs-lookup"><span data-stu-id="f234b-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="f234b-112">第一個命令會使用 **AzureStorSimpleDeviceBackup** Cmdlet，取得名為 ContosoDev07 之裝置的第一次備份。</span><span class="sxs-lookup"><span data-stu-id="f234b-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="f234b-113">該命令會將該備份儲存在 $Backup 變數中。</span><span class="sxs-lookup"><span data-stu-id="f234b-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="f234b-114">第二個命令會使用 **AzureStorSimpleAccessControlRecord** Cmdlet 取得存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="f234b-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="f234b-115">該命令會將結果儲存在 $Acrs 變數中。</span><span class="sxs-lookup"><span data-stu-id="f234b-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="f234b-116">最後一個命令會開始將裝置上的某個磁片卷的指定備份克隆到相同裝置上的不同卷的作業。</span><span class="sxs-lookup"><span data-stu-id="f234b-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="f234b-117">這個範例會依名稱指定裝置。</span><span class="sxs-lookup"><span data-stu-id="f234b-117">This example specifies the device by name.</span></span>
<span data-ttu-id="f234b-118">該命令會使用儲存在 $Backup 和 $Acrs 中的值。</span><span class="sxs-lookup"><span data-stu-id="f234b-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="f234b-119">此命令會傳回作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f234b-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="f234b-120">範例2：使用裝置識別碼將備份克隆至不同的卷</span><span class="sxs-lookup"><span data-stu-id="f234b-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="f234b-121">第一個命令會使用 **AzureStorSimpleDeviceBackup** Cmdlet，取得名為 ContosoDev07 之裝置的第一次備份。</span><span class="sxs-lookup"><span data-stu-id="f234b-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="f234b-122">該命令會將該備份儲存在 $Backup 變數中。</span><span class="sxs-lookup"><span data-stu-id="f234b-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="f234b-123">第二個命令會使用 **AzureStorSimpleAccessControlRecord** Cmdlet 取得存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="f234b-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="f234b-124">該命令會將結果儲存在 $Acrs 變數中。</span><span class="sxs-lookup"><span data-stu-id="f234b-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="f234b-125">最後一個命令會開始將裝置上的某個磁片卷的指定備份克隆到相同裝置上的不同卷的作業。</span><span class="sxs-lookup"><span data-stu-id="f234b-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="f234b-126">這個範例會依裝置識別碼來指定裝置。</span><span class="sxs-lookup"><span data-stu-id="f234b-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="f234b-127">該命令會使用儲存在 $Backup 和 $Acrs 中的值。</span><span class="sxs-lookup"><span data-stu-id="f234b-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="f234b-128">此命令會傳回作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f234b-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="f234b-129">範例3：使用裝置名稱將備份克隆到其他裝置上的卷</span><span class="sxs-lookup"><span data-stu-id="f234b-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="f234b-130">第一個命令會使用 **AzureStorSimpleDeviceBackup** Cmdlet，取得名為 ContosoDev07 之裝置的第一次備份。</span><span class="sxs-lookup"><span data-stu-id="f234b-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="f234b-131">該命令會將該備份儲存在 $Backup 變數中。</span><span class="sxs-lookup"><span data-stu-id="f234b-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="f234b-132">第二個命令會使用 **AzureStorSimpleAccessControlRecord** Cmdlet 取得存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="f234b-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="f234b-133">該命令會將結果儲存在 $Acrs 變數中。</span><span class="sxs-lookup"><span data-stu-id="f234b-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="f234b-134">最後一個命令會開始將裝置上的某個卷的指定備份克隆到另一個裝置上的某個卷的作業。</span><span class="sxs-lookup"><span data-stu-id="f234b-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="f234b-135">這個範例會依名稱指定裝置。</span><span class="sxs-lookup"><span data-stu-id="f234b-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="f234b-136">該命令會使用儲存在 $Backup 和 $Acrs 中的值。</span><span class="sxs-lookup"><span data-stu-id="f234b-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="f234b-137">此命令會傳回作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f234b-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="f234b-138">範例4：使用裝置名稱和管線運算子將備份克隆至不同的卷名</span><span class="sxs-lookup"><span data-stu-id="f234b-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="f234b-139">第一個命令會使用 **AzureStorSimpleDeviceBackup** Cmdlet，取得名為 ContosoDev07 之裝置的第一次備份。</span><span class="sxs-lookup"><span data-stu-id="f234b-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="f234b-140">該命令會將該備份儲存在 $Backup 變數中。</span><span class="sxs-lookup"><span data-stu-id="f234b-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="f234b-141">第二個命令會使用 **AzureStorSimpleAccessControlRecord** Cmdlet 取得存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="f234b-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="f234b-142">使用管線運算子，命令會將其結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f234b-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f234b-143">目前的 Cmdlet 會開始將裝置上的某個卷的指定備份克隆至相同裝置上的其他卷的作業。</span><span class="sxs-lookup"><span data-stu-id="f234b-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="f234b-144">這個範例會依名稱指定裝置。</span><span class="sxs-lookup"><span data-stu-id="f234b-144">This example specifies the device by name.</span></span>
<span data-ttu-id="f234b-145">命令會使用儲存在 $Backup 中的值。</span><span class="sxs-lookup"><span data-stu-id="f234b-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="f234b-146">此命令會從管線中取得 *TargetAccessControlRecords* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="f234b-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="f234b-147">此命令會傳回作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f234b-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="f234b-148">參數</span><span class="sxs-lookup"><span data-stu-id="f234b-148">PARAMETERS</span></span>

### <span data-ttu-id="f234b-149">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f234b-149">-BackupId</span></span>
<span data-ttu-id="f234b-150">指定要克隆之備份的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="f234b-150">Specifies the instance ID of the backup to clone.</span></span>

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

### <span data-ttu-id="f234b-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="f234b-151">-CloneVolumeName</span></span>
<span data-ttu-id="f234b-152">指定目標裝置上新的克隆卷名。</span><span class="sxs-lookup"><span data-stu-id="f234b-152">Specifies the name for the new cloned volume on the target device.</span></span>

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

### <span data-ttu-id="f234b-153">-Force</span><span class="sxs-lookup"><span data-stu-id="f234b-153">-Force</span></span>
<span data-ttu-id="f234b-154">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f234b-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f234b-155">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f234b-155">-Profile</span></span>
<span data-ttu-id="f234b-156">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f234b-156">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f234b-157">-快照</span><span class="sxs-lookup"><span data-stu-id="f234b-157">-Snapshot</span></span>
<span data-ttu-id="f234b-158">指定此 Cmdlet 克隆的快照物件。</span><span class="sxs-lookup"><span data-stu-id="f234b-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f234b-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="f234b-159">-SourceDeviceId</span></span>
<span data-ttu-id="f234b-160">指定來源裝置的 [實例識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f234b-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="f234b-161">這個 Cmdlet 會從來源裝置克隆回來。</span><span class="sxs-lookup"><span data-stu-id="f234b-161">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f234b-162">-SourceDeviceName</span><span class="sxs-lookup"><span data-stu-id="f234b-162">-SourceDeviceName</span></span>
<span data-ttu-id="f234b-163">指定來源裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f234b-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="f234b-164">這個 Cmdlet 會從來源裝置克隆回來。</span><span class="sxs-lookup"><span data-stu-id="f234b-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f234b-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="f234b-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="f234b-166">指定存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="f234b-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f234b-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="f234b-167">-TargetDeviceId</span></span>
<span data-ttu-id="f234b-168">指定目標裝置的 [實例識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f234b-168">Specifies the instance ID of the target device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f234b-169">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="f234b-169">-TargetDeviceName</span></span>
<span data-ttu-id="f234b-170">指定此 Cmdlet 將備份克隆到哪個裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f234b-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f234b-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f234b-171">CommonParameters</span></span>
<span data-ttu-id="f234b-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f234b-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f234b-173">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f234b-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f234b-174">輸入</span><span class="sxs-lookup"><span data-stu-id="f234b-174">INPUTS</span></span>

### <span data-ttu-id="f234b-175">快照、AccessControlRecord 清單</span><span class="sxs-lookup"><span data-stu-id="f234b-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="f234b-176">您可以將 **快照** 物件或 **AccessControlRecord** 物件的清單傳送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f234b-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="f234b-177">輸出</span><span class="sxs-lookup"><span data-stu-id="f234b-177">OUTPUTS</span></span>

## <span data-ttu-id="f234b-178">筆記</span><span class="sxs-lookup"><span data-stu-id="f234b-178">NOTES</span></span>

## <span data-ttu-id="f234b-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="f234b-179">RELATED LINKS</span></span>

[<span data-ttu-id="f234b-180">AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="f234b-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="f234b-181">AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f234b-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)



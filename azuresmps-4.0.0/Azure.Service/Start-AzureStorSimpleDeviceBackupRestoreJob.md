---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967193"
---
# <span data-ttu-id="999f3-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="999f3-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="999f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="999f3-102">SYNOPSIS</span></span>
<span data-ttu-id="999f3-103">啟動作業來還原 StorSimple 裝置上的備份。</span><span class="sxs-lookup"><span data-stu-id="999f3-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="999f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="999f3-104">SYNTAX</span></span>

### <span data-ttu-id="999f3-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="999f3-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="999f3-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="999f3-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="999f3-107">說明</span><span class="sxs-lookup"><span data-stu-id="999f3-107">DESCRIPTION</span></span>
<span data-ttu-id="999f3-108">**AzureStorSimpleDeviceBackupRestoreJob** Cmdlet 會啟動作業來還原 StorSimple 裝置上的備份。</span><span class="sxs-lookup"><span data-stu-id="999f3-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="999f3-109">指定備份識別碼與選用的快照識別碼。</span><span class="sxs-lookup"><span data-stu-id="999f3-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="999f3-110">示例</span><span class="sxs-lookup"><span data-stu-id="999f3-110">EXAMPLES</span></span>

### <span data-ttu-id="999f3-111">範例1：啟動作業來還原備份</span><span class="sxs-lookup"><span data-stu-id="999f3-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="999f3-112">這個命令會啟動一個作業，在名為 Contoso63-AppVm 的裝置上還原具有指定識別碼的備份物件及其相關聯的快照。</span><span class="sxs-lookup"><span data-stu-id="999f3-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="999f3-113">命令會指定 *WaitForComplete* 參數，因此在 Cmdlet 將控制權傳回給主機前，作業就完成了。</span><span class="sxs-lookup"><span data-stu-id="999f3-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="999f3-114">範例2：啟動作業來還原特定的快照</span><span class="sxs-lookup"><span data-stu-id="999f3-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="999f3-115">這個命令會啟動作業來還原具有指定識別碼的備份快照。</span><span class="sxs-lookup"><span data-stu-id="999f3-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="999f3-116">命令會透過名為 Contoso63-AppVm 的裝置上的識別碼來指定備份物件。</span><span class="sxs-lookup"><span data-stu-id="999f3-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="999f3-117">此命令會指定 *Force* 參數，因此它會啟動作業，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="999f3-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="999f3-118">參數</span><span class="sxs-lookup"><span data-stu-id="999f3-118">PARAMETERS</span></span>

### <span data-ttu-id="999f3-119">-BackupId</span><span class="sxs-lookup"><span data-stu-id="999f3-119">-BackupId</span></span>
<span data-ttu-id="999f3-120">指定要還原之備份的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="999f3-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="999f3-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="999f3-121">-DeviceName</span></span>
<span data-ttu-id="999f3-122">指定要在其上存在備份的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="999f3-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="999f3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="999f3-123">-Force</span></span>
<span data-ttu-id="999f3-124">表示此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="999f3-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="999f3-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="999f3-125">-Profile</span></span>
<span data-ttu-id="999f3-126">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="999f3-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="999f3-127">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="999f3-127">-SnapshotId</span></span>
<span data-ttu-id="999f3-128">指定要還原之快照的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="999f3-128">Specifies the instance ID of the snapshot to restore.</span></span>

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

### <span data-ttu-id="999f3-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="999f3-129">-WaitForComplete</span></span>
<span data-ttu-id="999f3-130">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="999f3-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="999f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999f3-131">CommonParameters</span></span>
<span data-ttu-id="999f3-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="999f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999f3-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="999f3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999f3-134">輸入</span><span class="sxs-lookup"><span data-stu-id="999f3-134">INPUTS</span></span>

### <span data-ttu-id="999f3-135">所有</span><span class="sxs-lookup"><span data-stu-id="999f3-135">None</span></span>

## <span data-ttu-id="999f3-136">輸出</span><span class="sxs-lookup"><span data-stu-id="999f3-136">OUTPUTS</span></span>

### <span data-ttu-id="999f3-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="999f3-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="999f3-138">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="999f3-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="999f3-139">如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="999f3-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="999f3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="999f3-140">NOTES</span></span>

## <span data-ttu-id="999f3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="999f3-141">RELATED LINKS</span></span>

[<span data-ttu-id="999f3-142">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="999f3-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="999f3-143">開始-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="999f3-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)



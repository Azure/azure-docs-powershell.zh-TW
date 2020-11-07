---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967910"
---
# <span data-ttu-id="97f5a-101">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="97f5a-101">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="97f5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="97f5a-103">移除現有的備份原則。</span><span class="sxs-lookup"><span data-stu-id="97f5a-103">Removes an existing backup policy.</span></span>

## <span data-ttu-id="97f5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="97f5a-104">SYNTAX</span></span>

### <span data-ttu-id="97f5a-105">IdentifyById (預設) </span><span class="sxs-lookup"><span data-stu-id="97f5a-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="97f5a-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="97f5a-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="97f5a-107">說明</span><span class="sxs-lookup"><span data-stu-id="97f5a-107">DESCRIPTION</span></span>
<span data-ttu-id="97f5a-108">**AzureStorSimpleDeviceBackupPolicy** Cmdlet 會移除現有的 **BackupPolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="97f5a-108">The **Remove-AzureStorSimpleDeviceBackupPolicy** cmdlet removes an existing **BackupPolicy** object.</span></span>
<span data-ttu-id="97f5a-109">移除備份原則之後，不會根據該原則進行進一步的備份。</span><span class="sxs-lookup"><span data-stu-id="97f5a-109">After you remove a backup policy, no further backups take place based on that policy.</span></span>
<span data-ttu-id="97f5a-110">這個 Cmdlet 也會刪除與刪除的原則相關的所有排程。</span><span class="sxs-lookup"><span data-stu-id="97f5a-110">This cmdlet also deletes all schedules associated with the deleted policy.</span></span>

## <span data-ttu-id="97f5a-111">示例</span><span class="sxs-lookup"><span data-stu-id="97f5a-111">EXAMPLES</span></span>

### <span data-ttu-id="97f5a-112">範例1：移除備份原則</span><span class="sxs-lookup"><span data-stu-id="97f5a-112">Example 1: Remove a backup policy</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

<span data-ttu-id="97f5a-113">這個命令會移除實例識別碼為03710b4c-82c1-40ca-be5c-40289dc49642 的 **BackupPolicy** ，因此不會根據此原則進行其他備份。</span><span class="sxs-lookup"><span data-stu-id="97f5a-113">This command removes the **BackupPolicy** that has the instance ID 03710b4c-82c1-40ca-be5c-40289dc49642, so that no more backups are made based on this policy.</span></span>
<span data-ttu-id="97f5a-114">此命令也會刪除與此原則相關的所有排程。</span><span class="sxs-lookup"><span data-stu-id="97f5a-114">The command also deletes all schedules associated with this policy.</span></span>
<span data-ttu-id="97f5a-115">命令會啟動移除 **BackupPolicy** 物件的作業，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="97f5a-115">The command starts the operation that removes the **BackupPolicy** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="97f5a-116">若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97f5a-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="97f5a-117">範例2：移除裝置的第一項備份原則</span><span class="sxs-lookup"><span data-stu-id="97f5a-117">Example 2: Remove the first of the backup policies for a device</span></span>
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

<span data-ttu-id="97f5a-118">第一個命令會取得名為 Contoso63-AppVm 之裝置的備份原則，然後將它們儲存在 $Policies 變數中。</span><span class="sxs-lookup"><span data-stu-id="97f5a-118">The first command gets the backup policies for the device named Contoso63-AppVm, and then stores them in the $Policies variable.</span></span>

<span data-ttu-id="97f5a-119">第二個命令會將第一個備份原則從 Contoso63-AppVm 中移除。</span><span class="sxs-lookup"><span data-stu-id="97f5a-119">The second command removes the first backup policy from Contoso63-AppVm.</span></span>
<span data-ttu-id="97f5a-120">此命令使用標準的點語法來識別 $Policies 中第一個專案的 **InstanceId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="97f5a-120">The command uses standard dot syntax to identify the **InstanceId** property of the first item in $Policies.</span></span>
<span data-ttu-id="97f5a-121">這個命令會指定 *WaitForComplete* 參數，因此命令會完成任務，然後傳回工作的 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="97f5a-121">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="97f5a-122">範例3：使用管線移除備份原則</span><span class="sxs-lookup"><span data-stu-id="97f5a-122">Example 3: Remove a backup policy by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

<span data-ttu-id="97f5a-123">這個命令會使用 **AzureStorSimpleDeviceBackupPolicy** 來取得 **BackupPolicyDetails** 物件，然後使用管線運算子將它傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97f5a-123">This command gets a **BackupPolicyDetails** object by using **Get-AzureStorSimpleDeviceBackupPolicy** , and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="97f5a-124">目前的 Cmdlet 會移除名為 TSQAVolume01_Default 的備份原則。</span><span class="sxs-lookup"><span data-stu-id="97f5a-124">The current cmdlet removes the backup policy named TSQAVolume01_Default.</span></span>

## <span data-ttu-id="97f5a-125">參數</span><span class="sxs-lookup"><span data-stu-id="97f5a-125">PARAMETERS</span></span>

### <span data-ttu-id="97f5a-126">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="97f5a-126">-BackupPolicy</span></span>
<span data-ttu-id="97f5a-127">指定要刪除的 **BackupPolicyDetails** 物件。</span><span class="sxs-lookup"><span data-stu-id="97f5a-127">Specifies the **BackupPolicyDetails** object to delete.</span></span>
<span data-ttu-id="97f5a-128">若要取得 **BackupPolicyDetails** 物件，請使用 **AzureStorSimpleDeviceBackupPolicy** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97f5a-128">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97f5a-129">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="97f5a-129">-BackupPolicyId</span></span>
<span data-ttu-id="97f5a-130">指定要刪除之 **BackupPolicy** 物件的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="97f5a-130">Specifies the instance ID of the **BackupPolicy** object to delete.</span></span>

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

### <span data-ttu-id="97f5a-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="97f5a-131">-DeviceName</span></span>
<span data-ttu-id="97f5a-132">指定要刪除備份原則之 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="97f5a-132">Specifies the name of the StorSimple device on which to delete the backup policy.</span></span>

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

### <span data-ttu-id="97f5a-133">-Force</span><span class="sxs-lookup"><span data-stu-id="97f5a-133">-Force</span></span>
<span data-ttu-id="97f5a-134">表示此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97f5a-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="97f5a-135">-設定檔</span><span class="sxs-lookup"><span data-stu-id="97f5a-135">-Profile</span></span>
<span data-ttu-id="97f5a-136">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="97f5a-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="97f5a-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="97f5a-137">-WaitForComplete</span></span>
<span data-ttu-id="97f5a-138">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="97f5a-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="97f5a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f5a-139">CommonParameters</span></span>
<span data-ttu-id="97f5a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97f5a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f5a-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97f5a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f5a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="97f5a-142">INPUTS</span></span>

### <span data-ttu-id="97f5a-143">BackupPolicyDetails</span><span class="sxs-lookup"><span data-stu-id="97f5a-143">BackupPolicyDetails</span></span>
<span data-ttu-id="97f5a-144">這個 Cmdlet 接受要刪除的 **BackupPolicyDetails** 物件。</span><span class="sxs-lookup"><span data-stu-id="97f5a-144">This cmdlet accepts a **BackupPolicyDetails** object to delete.</span></span>

## <span data-ttu-id="97f5a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="97f5a-145">OUTPUTS</span></span>

### <span data-ttu-id="97f5a-146">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="97f5a-146">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="97f5a-147">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="97f5a-147">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="97f5a-148">如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="97f5a-148">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="97f5a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="97f5a-149">NOTES</span></span>

## <span data-ttu-id="97f5a-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="97f5a-150">RELATED LINKS</span></span>

[<span data-ttu-id="97f5a-151">AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="97f5a-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="97f5a-152">新-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="97f5a-152">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="97f5a-153">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="97f5a-153">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="97f5a-154">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="97f5a-154">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)



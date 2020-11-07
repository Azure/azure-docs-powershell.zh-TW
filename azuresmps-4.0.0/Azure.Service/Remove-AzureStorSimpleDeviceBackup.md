---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967913"
---
# <span data-ttu-id="0cdb1-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="0cdb1-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="0cdb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0cdb1-102">SYNOPSIS</span></span>
<span data-ttu-id="0cdb1-103">刪除備份物件。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-103">Deletes a backup object.</span></span>

## <span data-ttu-id="0cdb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="0cdb1-104">SYNTAX</span></span>

### <span data-ttu-id="0cdb1-105">IdentifyById (預設) </span><span class="sxs-lookup"><span data-stu-id="0cdb1-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0cdb1-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="0cdb1-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0cdb1-107">說明</span><span class="sxs-lookup"><span data-stu-id="0cdb1-107">DESCRIPTION</span></span>
<span data-ttu-id="0cdb1-108">**AzureStorSimpleDeviceBackup** Cmdlet 會刪除單一備份物件。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="0cdb1-109">如果您嘗試刪除已經刪除的備份，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="0cdb1-110">示例</span><span class="sxs-lookup"><span data-stu-id="0cdb1-110">EXAMPLES</span></span>

### <span data-ttu-id="0cdb1-111">範例1：移除裝置的備份</span><span class="sxs-lookup"><span data-stu-id="0cdb1-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="0cdb1-112">這個命令會針對名稱為 Contoso63-AppVm 的裝置，移除具有指定識別碼的備份。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="0cdb1-113">命令會啟動移除 **備份** 物件的作業，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="0cdb1-114">若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="0cdb1-115">範例2：使用 ID 移除裝置的第一個備份</span><span class="sxs-lookup"><span data-stu-id="0cdb1-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="0cdb1-116">第一個命令會取得名為 Contoso63-AppVm 之裝置的備份，然後將它們儲存在 $Backup 變數中。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="0cdb1-117">第二個命令會從名為 Contoso63-AppVm 的裝置中刪除備份。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="0cdb1-118">此命令使用標準點符號來參照 $Backup 陣列第一個元素的 **InstanceId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="0cdb1-119">這個命令會指定 *WaitForComplete* 參數，因此命令會等到作業完成，然後傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="0cdb1-120">範例3：使用管線移除裝置的第一次備份</span><span class="sxs-lookup"><span data-stu-id="0cdb1-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="0cdb1-121">第一個命令會取得名為 Contoso63-AppVm 之裝置的備份，然後將它們儲存在 $Backup 變數中。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="0cdb1-122">第二個命令會將儲存在 $Backup 陣列中的第一個物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="0cdb1-123">這個 Cmdlet 會從名為 Contoso63-AppVm 的裝置中刪除該備份。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="0cdb1-124">這個命令會指定 *WaitForComplete* 參數，因此命令會等到作業完成，然後傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="0cdb1-125">參數</span><span class="sxs-lookup"><span data-stu-id="0cdb1-125">PARAMETERS</span></span>

### <span data-ttu-id="0cdb1-126">-備份</span><span class="sxs-lookup"><span data-stu-id="0cdb1-126">-Backup</span></span>
<span data-ttu-id="0cdb1-127">指定要刪除的 **備份** 物件。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="0cdb1-128">若要取得 **備份** 物件，請使用 **AzureStorSimpleDeviceBackup** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cdb1-129">-BackupId</span><span class="sxs-lookup"><span data-stu-id="0cdb1-129">-BackupId</span></span>
<span data-ttu-id="0cdb1-130">指定要刪除之備份的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="0cdb1-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0cdb1-131">-DeviceName</span></span>
<span data-ttu-id="0cdb1-132">指定要刪除備份之 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="0cdb1-133">-Force</span><span class="sxs-lookup"><span data-stu-id="0cdb1-133">-Force</span></span>
<span data-ttu-id="0cdb1-134">表示此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="0cdb1-135">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0cdb1-135">-Profile</span></span>
<span data-ttu-id="0cdb1-136">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0cdb1-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="0cdb1-137">-WaitForComplete</span></span>
<span data-ttu-id="0cdb1-138">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="0cdb1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cdb1-139">CommonParameters</span></span>
<span data-ttu-id="0cdb1-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cdb1-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cdb1-142">輸入</span><span class="sxs-lookup"><span data-stu-id="0cdb1-142">INPUTS</span></span>

### <span data-ttu-id="0cdb1-143">備份</span><span class="sxs-lookup"><span data-stu-id="0cdb1-143">Backup</span></span>

## <span data-ttu-id="0cdb1-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0cdb1-144">OUTPUTS</span></span>

### <span data-ttu-id="0cdb1-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="0cdb1-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="0cdb1-146">這個 Cmdlet 會傳回 **TaskStatusInfo** 物件如果您不指定 *該參數，* 則會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="0cdb1-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="0cdb1-147">筆記</span><span class="sxs-lookup"><span data-stu-id="0cdb1-147">NOTES</span></span>

## <span data-ttu-id="0cdb1-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cdb1-148">RELATED LINKS</span></span>

[<span data-ttu-id="0cdb1-149">AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="0cdb1-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)



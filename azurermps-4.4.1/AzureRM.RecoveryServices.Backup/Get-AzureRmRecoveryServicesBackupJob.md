---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456451"
---
# <span data-ttu-id="7df9d-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7df9d-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="7df9d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7df9d-102">SYNOPSIS</span></span>
<span data-ttu-id="7df9d-103">取得備份作業。</span><span class="sxs-lookup"><span data-stu-id="7df9d-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7df9d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7df9d-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7df9d-105">說明</span><span class="sxs-lookup"><span data-stu-id="7df9d-105">DESCRIPTION</span></span>
<span data-ttu-id="7df9d-106">**AzureRmRecoveryServicesBackupJob** Cmdlet 會針對特定的電子倉庫取得 Azure 備份作業。</span><span class="sxs-lookup"><span data-stu-id="7df9d-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="7df9d-107">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7df9d-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7df9d-108">示例</span><span class="sxs-lookup"><span data-stu-id="7df9d-108">EXAMPLES</span></span>

### <span data-ttu-id="7df9d-109">範例1：取得所有進行中的工作</span><span class="sxs-lookup"><span data-stu-id="7df9d-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="7df9d-110">第一個命令會以陣列形式取得進行中作業的狀態，然後將它儲存在 $Joblist 變數中。</span><span class="sxs-lookup"><span data-stu-id="7df9d-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="7df9d-111">第二個命令會顯示 $Joblist 陣列中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="7df9d-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="7df9d-112">範例2：在過去7天內取得所有失敗的工作</span><span class="sxs-lookup"><span data-stu-id="7df9d-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="7df9d-113">此命令會從 vault 中的最後一周取得失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="7df9d-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="7df9d-114">*From* 參數指定過去在 UTC 中指定的時間（以七天為單位）。</span><span class="sxs-lookup"><span data-stu-id="7df9d-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="7df9d-115">該命令不會指定 *To* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="7df9d-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="7df9d-116">因此，它會使用目前時間的預設值。</span><span class="sxs-lookup"><span data-stu-id="7df9d-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="7df9d-117">範例3：取得進行中的工作並等待完成</span><span class="sxs-lookup"><span data-stu-id="7df9d-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="7df9d-118">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="7df9d-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="7df9d-119">參數</span><span class="sxs-lookup"><span data-stu-id="7df9d-119">PARAMETERS</span></span>

### <span data-ttu-id="7df9d-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7df9d-120">-BackupManagementType</span></span>
<span data-ttu-id="7df9d-121">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="7df9d-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="7df9d-122">目前僅支援 Add-azurevm。</span><span class="sxs-lookup"><span data-stu-id="7df9d-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df9d-123">-從</span><span class="sxs-lookup"><span data-stu-id="7df9d-123">-From</span></span>
<span data-ttu-id="7df9d-124">指定此 Cmdlet 所取得作業之時間範圍的開始（以 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="7df9d-124">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7df9d-125">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7df9d-125">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="7df9d-126">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="7df9d-126">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="7df9d-127">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="7df9d-127">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df9d-128">-工作</span><span class="sxs-lookup"><span data-stu-id="7df9d-128">-Job</span></span>
<span data-ttu-id="7df9d-129">指定要取得的備份作業名稱。</span><span class="sxs-lookup"><span data-stu-id="7df9d-129">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df9d-130">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="7df9d-130">-JobId</span></span>
<span data-ttu-id="7df9d-131">指定此 Cmdlet 所取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7df9d-131">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="7df9d-132">識別碼是 **AzureRmRecoveryServicesBackupJob** 物件的 InstanceId 屬性。</span><span class="sxs-lookup"><span data-stu-id="7df9d-132">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="7df9d-133">若要取得 **AzureRmRecoveryServicesBackupJob** 物件，請使用 AzureRmRecoveryServicesBackupJob。</span><span class="sxs-lookup"><span data-stu-id="7df9d-133">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df9d-134">-操作</span><span class="sxs-lookup"><span data-stu-id="7df9d-134">-Operation</span></span>
<span data-ttu-id="7df9d-135">指定此 Cmdlet 取得作業的操作。</span><span class="sxs-lookup"><span data-stu-id="7df9d-135">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7df9d-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7df9d-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7df9d-137">備份</span><span class="sxs-lookup"><span data-stu-id="7df9d-137">Backup</span></span>
- <span data-ttu-id="7df9d-138">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="7df9d-138">ConfigureBackup</span></span>
- <span data-ttu-id="7df9d-139">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="7df9d-139">DeleteBackupData</span></span>
- <span data-ttu-id="7df9d-140">註冊表</span><span class="sxs-lookup"><span data-stu-id="7df9d-140">Register</span></span>
- <span data-ttu-id="7df9d-141">還原</span><span class="sxs-lookup"><span data-stu-id="7df9d-141">Restore</span></span>
- <span data-ttu-id="7df9d-142">對</span><span class="sxs-lookup"><span data-stu-id="7df9d-142">UnProtect</span></span>
- <span data-ttu-id="7df9d-143">登出</span><span class="sxs-lookup"><span data-stu-id="7df9d-143">Unregister</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df9d-144">-狀態</span><span class="sxs-lookup"><span data-stu-id="7df9d-144">-Status</span></span>
<span data-ttu-id="7df9d-145">指定此 Cmdlet 取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7df9d-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7df9d-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7df9d-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7df9d-147">正在</span><span class="sxs-lookup"><span data-stu-id="7df9d-147">InProgress</span></span>
- <span data-ttu-id="7df9d-148">成功</span><span class="sxs-lookup"><span data-stu-id="7df9d-148">Failed</span></span>
- <span data-ttu-id="7df9d-149">取消</span><span class="sxs-lookup"><span data-stu-id="7df9d-149">Cancelled</span></span>
- <span data-ttu-id="7df9d-150">正在</span><span class="sxs-lookup"><span data-stu-id="7df9d-150">Cancelling</span></span>
- <span data-ttu-id="7df9d-151">完畢</span><span class="sxs-lookup"><span data-stu-id="7df9d-151">Completed</span></span>
- <span data-ttu-id="7df9d-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="7df9d-152">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df9d-153">-To</span><span class="sxs-lookup"><span data-stu-id="7df9d-153">-To</span></span>
<span data-ttu-id="7df9d-154">指定此 Cmdlet 所取得作業之時間範圍的結尾（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="7df9d-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7df9d-155">預設值為目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="7df9d-155">The default value is the current system time.</span></span>
<span data-ttu-id="7df9d-156">如果您指定此參數，您也必須指定 *From* 參數。</span><span class="sxs-lookup"><span data-stu-id="7df9d-156">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="7df9d-157">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="7df9d-157">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df9d-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df9d-158">-DefaultProfile</span></span>
<span data-ttu-id="7df9d-159">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7df9d-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7df9d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df9d-160">CommonParameters</span></span>
<span data-ttu-id="7df9d-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7df9d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df9d-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7df9d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df9d-163">輸入</span><span class="sxs-lookup"><span data-stu-id="7df9d-163">INPUTS</span></span>

## <span data-ttu-id="7df9d-164">輸出</span><span class="sxs-lookup"><span data-stu-id="7df9d-164">OUTPUTS</span></span>

### <span data-ttu-id="7df9d-165">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="7df9d-165">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="7df9d-166">[System.object]. RecoveryServices [JobBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="7df9d-166">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="7df9d-167">筆記</span><span class="sxs-lookup"><span data-stu-id="7df9d-167">NOTES</span></span>

## <span data-ttu-id="7df9d-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="7df9d-168">RELATED LINKS</span></span>

[<span data-ttu-id="7df9d-169">AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="7df9d-169">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="7df9d-170">停止 AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7df9d-170">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="7df9d-171">稍候-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7df9d-171">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


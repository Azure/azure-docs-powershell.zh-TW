---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621152"
---
# <span data-ttu-id="bcd2b-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="bcd2b-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="bcd2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd2b-103">取得備份作業。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="bcd2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcd2b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcd2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcd2b-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd2b-106">**AzRecoveryServicesBackupJob** Cmdlet 會針對特定的電子倉庫取得 Azure 備份作業。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="bcd2b-107">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bcd2b-108">示例</span><span class="sxs-lookup"><span data-stu-id="bcd2b-108">EXAMPLES</span></span>

### <span data-ttu-id="bcd2b-109">範例1：取得所有進行中的工作</span><span class="sxs-lookup"><span data-stu-id="bcd2b-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="bcd2b-110">第一個命令會以陣列形式取得進行中作業的狀態，然後將它儲存在 $Joblist 變數中。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="bcd2b-111">第二個命令會顯示 $Joblist 陣列中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="bcd2b-112">範例2：在過去7天內取得所有失敗的工作</span><span class="sxs-lookup"><span data-stu-id="bcd2b-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="bcd2b-113">此命令會從 vault 中的最後一周取得失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="bcd2b-114">*From* 參數指定過去在 UTC 中指定的時間（以七天為單位）。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="bcd2b-115">該命令不會指定 *To* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="bcd2b-116">因此，它會使用目前時間的預設值。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="bcd2b-117">範例3：取得進行中的工作並等待完成</span><span class="sxs-lookup"><span data-stu-id="bcd2b-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="bcd2b-118">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="bcd2b-119">參數</span><span class="sxs-lookup"><span data-stu-id="bcd2b-119">PARAMETERS</span></span>

### <span data-ttu-id="bcd2b-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bcd2b-120">-BackupManagementType</span></span>
<span data-ttu-id="bcd2b-121">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="bcd2b-122">目前僅支援 Add-azurevm、AzureStorage。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcd2b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd2b-123">-DefaultProfile</span></span>
<span data-ttu-id="bcd2b-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcd2b-125">-從</span><span class="sxs-lookup"><span data-stu-id="bcd2b-125">-From</span></span>
<span data-ttu-id="bcd2b-126">指定此 Cmdlet 所取得作業之時間範圍的開始（以 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bcd2b-127">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="bcd2b-128">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="bcd2b-129">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="bcd2b-130">-工作</span><span class="sxs-lookup"><span data-stu-id="bcd2b-130">-Job</span></span>
<span data-ttu-id="bcd2b-131">指定要取得的備份作業名稱。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="bcd2b-132">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="bcd2b-132">-JobId</span></span>
<span data-ttu-id="bcd2b-133">指定此 Cmdlet 所取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="bcd2b-134">識別碼是 **AzureRmRecoveryServicesBackupJob** 物件的 InstanceId 屬性。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="bcd2b-135">若要取得 **AzureRmRecoveryServicesBackupJob** 物件，請使用 AzRecoveryServicesBackupJob。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="bcd2b-136">-操作</span><span class="sxs-lookup"><span data-stu-id="bcd2b-136">-Operation</span></span>
<span data-ttu-id="bcd2b-137">指定此 Cmdlet 取得作業的操作。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bcd2b-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bcd2b-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bcd2b-139">備份</span><span class="sxs-lookup"><span data-stu-id="bcd2b-139">Backup</span></span>
- <span data-ttu-id="bcd2b-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="bcd2b-140">ConfigureBackup</span></span>
- <span data-ttu-id="bcd2b-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="bcd2b-141">DeleteBackupData</span></span>
- <span data-ttu-id="bcd2b-142">註冊表</span><span class="sxs-lookup"><span data-stu-id="bcd2b-142">Register</span></span>
- <span data-ttu-id="bcd2b-143">還原</span><span class="sxs-lookup"><span data-stu-id="bcd2b-143">Restore</span></span>
- <span data-ttu-id="bcd2b-144">對</span><span class="sxs-lookup"><span data-stu-id="bcd2b-144">UnProtect</span></span>
- <span data-ttu-id="bcd2b-145">登出</span><span class="sxs-lookup"><span data-stu-id="bcd2b-145">Unregister</span></span>

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

### <span data-ttu-id="bcd2b-146">-狀態</span><span class="sxs-lookup"><span data-stu-id="bcd2b-146">-Status</span></span>
<span data-ttu-id="bcd2b-147">指定此 Cmdlet 取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bcd2b-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bcd2b-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bcd2b-149">正在</span><span class="sxs-lookup"><span data-stu-id="bcd2b-149">InProgress</span></span>
- <span data-ttu-id="bcd2b-150">成功</span><span class="sxs-lookup"><span data-stu-id="bcd2b-150">Failed</span></span>
- <span data-ttu-id="bcd2b-151">取消</span><span class="sxs-lookup"><span data-stu-id="bcd2b-151">Cancelled</span></span>
- <span data-ttu-id="bcd2b-152">正在</span><span class="sxs-lookup"><span data-stu-id="bcd2b-152">Cancelling</span></span>
- <span data-ttu-id="bcd2b-153">完畢</span><span class="sxs-lookup"><span data-stu-id="bcd2b-153">Completed</span></span>
- <span data-ttu-id="bcd2b-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="bcd2b-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="bcd2b-155">-To</span><span class="sxs-lookup"><span data-stu-id="bcd2b-155">-To</span></span>
<span data-ttu-id="bcd2b-156">指定此 Cmdlet 所取得作業之時間範圍的結尾（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bcd2b-157">預設值為目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-157">The default value is the current system time.</span></span>
<span data-ttu-id="bcd2b-158">如果您指定此參數，您也必須指定 *From* 參數。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="bcd2b-159">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="bcd2b-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bcd2b-160">-VaultId</span></span>
<span data-ttu-id="bcd2b-161">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-161">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd2b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd2b-162">CommonParameters</span></span>
<span data-ttu-id="bcd2b-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd2b-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcd2b-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd2b-165">輸入</span><span class="sxs-lookup"><span data-stu-id="bcd2b-165">INPUTS</span></span>

### <span data-ttu-id="bcd2b-166">System.object</span><span class="sxs-lookup"><span data-stu-id="bcd2b-166">System.String</span></span>

## <span data-ttu-id="bcd2b-167">輸出</span><span class="sxs-lookup"><span data-stu-id="bcd2b-167">OUTPUTS</span></span>

### <span data-ttu-id="bcd2b-168">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="bcd2b-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="bcd2b-169">筆記</span><span class="sxs-lookup"><span data-stu-id="bcd2b-169">NOTES</span></span>

## <span data-ttu-id="bcd2b-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcd2b-170">RELATED LINKS</span></span>

[<span data-ttu-id="bcd2b-171">AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="bcd2b-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="bcd2b-172">停止 AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="bcd2b-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="bcd2b-173">稍候-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="bcd2b-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)



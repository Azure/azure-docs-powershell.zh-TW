---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399816"
---
# <span data-ttu-id="a248a-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a248a-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="a248a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a248a-102">SYNOPSIS</span></span>
<span data-ttu-id="a248a-103">獲得備份工作。</span><span class="sxs-lookup"><span data-stu-id="a248a-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="a248a-104">語法</span><span class="sxs-lookup"><span data-stu-id="a248a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a248a-105">描述</span><span class="sxs-lookup"><span data-stu-id="a248a-105">DESCRIPTION</span></span>
<span data-ttu-id="a248a-106">**Get-AzRecoveryServicesBackupJob** Cmdlet 會取得特定儲存庫的 Azure 備份工作。</span><span class="sxs-lookup"><span data-stu-id="a248a-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="a248a-107">使用目前的 Cmdlet 之前，使用 Set-AzRecoveryServicesVaultContext Cmdlet 設定庫內容。</span><span class="sxs-lookup"><span data-stu-id="a248a-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a248a-108">例子</span><span class="sxs-lookup"><span data-stu-id="a248a-108">EXAMPLES</span></span>

### <span data-ttu-id="a248a-109">範例 1：取得所有進行中的工作</span><span class="sxs-lookup"><span data-stu-id="a248a-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="a248a-110">第一個命令會以陣列取得進行中工作的狀態，然後將它儲存在$Joblist變數中。</span><span class="sxs-lookup"><span data-stu-id="a248a-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="a248a-111">第二個命令會顯示陣列$Joblist專案。</span><span class="sxs-lookup"><span data-stu-id="a248a-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="a248a-112">範例 2：取得過去 7 天內的所有失敗工作</span><span class="sxs-lookup"><span data-stu-id="a248a-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="a248a-113">此命令會從儲存庫的最後一周開始，收到失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="a248a-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="a248a-114">From 參數會指定過去以 UTC 指定的七天時間。</span><span class="sxs-lookup"><span data-stu-id="a248a-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="a248a-115">命令不會指定 To *參數的值。*</span><span class="sxs-lookup"><span data-stu-id="a248a-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="a248a-116">因此，它會使用目前時間的預設值。</span><span class="sxs-lookup"><span data-stu-id="a248a-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="a248a-117">範例 3：取得進行中的工作並等待完成</span><span class="sxs-lookup"><span data-stu-id="a248a-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="a248a-118">此腳本會輪詢目前進行中的第一個工作，直到該工作完成為止。</span><span class="sxs-lookup"><span data-stu-id="a248a-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="a248a-119">參數</span><span class="sxs-lookup"><span data-stu-id="a248a-119">PARAMETERS</span></span>

### <span data-ttu-id="a248a-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a248a-120">-BackupManagementType</span></span>
<span data-ttu-id="a248a-121">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="a248a-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="a248a-122">目前僅支援 Azure%。AzureStorage。</span><span class="sxs-lookup"><span data-stu-id="a248a-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="a248a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a248a-123">-DefaultProfile</span></span>
<span data-ttu-id="a248a-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a248a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a248a-125">-從</span><span class="sxs-lookup"><span data-stu-id="a248a-125">-From</span></span>
<span data-ttu-id="a248a-126">指定此 **Cmdlet** 所獲得之工作的開始時間 ，做為 DateTime 物件。</span><span class="sxs-lookup"><span data-stu-id="a248a-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a248a-127">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a248a-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="a248a-128">有關 **DateTime** 物件的資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="a248a-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="a248a-129">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="a248a-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="a248a-130">-Job</span><span class="sxs-lookup"><span data-stu-id="a248a-130">-Job</span></span>
<span data-ttu-id="a248a-131">指定要取得之備份工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="a248a-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="a248a-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="a248a-132">-JobId</span></span>
<span data-ttu-id="a248a-133">指定此 Cmdlet 所獲得工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a248a-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="a248a-134">識別碼是 **AzureRmRecoveryServicesBackupJob** 物件的 InstanceId 屬性。</span><span class="sxs-lookup"><span data-stu-id="a248a-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="a248a-135">若要取得 **AzureRmRecoveryServicesBackupJob** 物件，請使用 Get-AzRecoveryServicesBackupJob。</span><span class="sxs-lookup"><span data-stu-id="a248a-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="a248a-136">-作業</span><span class="sxs-lookup"><span data-stu-id="a248a-136">-Operation</span></span>
<span data-ttu-id="a248a-137">指定此 Cmdlet 所獲得工作的作業。</span><span class="sxs-lookup"><span data-stu-id="a248a-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a248a-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a248a-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a248a-139">備份</span><span class="sxs-lookup"><span data-stu-id="a248a-139">Backup</span></span>
- <span data-ttu-id="a248a-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="a248a-140">ConfigureBackup</span></span>
- <span data-ttu-id="a248a-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="a248a-141">DeleteBackupData</span></span>
- <span data-ttu-id="a248a-142">註冊</span><span class="sxs-lookup"><span data-stu-id="a248a-142">Register</span></span>
- <span data-ttu-id="a248a-143">恢復</span><span class="sxs-lookup"><span data-stu-id="a248a-143">Restore</span></span>
- <span data-ttu-id="a248a-144">取消保護</span><span class="sxs-lookup"><span data-stu-id="a248a-144">UnProtect</span></span>
- <span data-ttu-id="a248a-145">登出</span><span class="sxs-lookup"><span data-stu-id="a248a-145">Unregister</span></span>

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

### <span data-ttu-id="a248a-146">-狀態</span><span class="sxs-lookup"><span data-stu-id="a248a-146">-Status</span></span>
<span data-ttu-id="a248a-147">指定此 Cmdlet 獲得的工作狀態。</span><span class="sxs-lookup"><span data-stu-id="a248a-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a248a-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a248a-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a248a-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="a248a-149">InProgress</span></span>
- <span data-ttu-id="a248a-150">失敗</span><span class="sxs-lookup"><span data-stu-id="a248a-150">Failed</span></span>
- <span data-ttu-id="a248a-151">取消</span><span class="sxs-lookup"><span data-stu-id="a248a-151">Cancelled</span></span>
- <span data-ttu-id="a248a-152">取消</span><span class="sxs-lookup"><span data-stu-id="a248a-152">Cancelling</span></span>
- <span data-ttu-id="a248a-153">完成</span><span class="sxs-lookup"><span data-stu-id="a248a-153">Completed</span></span>
- <span data-ttu-id="a248a-154">已完成的WithWarnings</span><span class="sxs-lookup"><span data-stu-id="a248a-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="a248a-155">-To</span><span class="sxs-lookup"><span data-stu-id="a248a-155">-To</span></span>
<span data-ttu-id="a248a-156">指定此 **Cmdlet** 所獲得之工作的結束時間範圍 ，做為 DateTime 物件。</span><span class="sxs-lookup"><span data-stu-id="a248a-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a248a-157">預設值為目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="a248a-157">The default value is the current system time.</span></span>
<span data-ttu-id="a248a-158">如果您指定此參數，您也必須指定 *From* 參數。</span><span class="sxs-lookup"><span data-stu-id="a248a-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="a248a-159">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="a248a-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="a248a-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a248a-160">-VaultId</span></span>
<span data-ttu-id="a248a-161">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="a248a-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a248a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a248a-162">CommonParameters</span></span>
<span data-ttu-id="a248a-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a248a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a248a-164">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a248a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a248a-165">輸入</span><span class="sxs-lookup"><span data-stu-id="a248a-165">INPUTS</span></span>

### <span data-ttu-id="a248a-166">System.String</span><span class="sxs-lookup"><span data-stu-id="a248a-166">System.String</span></span>

## <span data-ttu-id="a248a-167">輸出</span><span class="sxs-lookup"><span data-stu-id="a248a-167">OUTPUTS</span></span>

### <span data-ttu-id="a248a-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase</span><span class="sxs-lookup"><span data-stu-id="a248a-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a248a-169">筆記</span><span class="sxs-lookup"><span data-stu-id="a248a-169">NOTES</span></span>

## <span data-ttu-id="a248a-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="a248a-170">RELATED LINKS</span></span>


[<span data-ttu-id="a248a-171">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a248a-171">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="a248a-172">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a248a-172">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)



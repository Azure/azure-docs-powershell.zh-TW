---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970824"
---
# <span data-ttu-id="3ded5-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3ded5-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="3ded5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ded5-102">SYNOPSIS</span></span>

<span data-ttu-id="3ded5-103">取得備份作業。</span><span class="sxs-lookup"><span data-stu-id="3ded5-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="3ded5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ded5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ded5-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ded5-105">DESCRIPTION</span></span>

<span data-ttu-id="3ded5-106">**AzRecoveryServicesBackupJob** Cmdlet 會針對特定的電子倉庫取得 Azure 備份作業。</span><span class="sxs-lookup"><span data-stu-id="3ded5-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="3ded5-107">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="3ded5-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="3ded5-108">示例</span><span class="sxs-lookup"><span data-stu-id="3ded5-108">EXAMPLES</span></span>

### <span data-ttu-id="3ded5-109">範例1：取得所有進行中的工作</span><span class="sxs-lookup"><span data-stu-id="3ded5-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="3ded5-110">第一個命令會以陣列形式取得進行中作業的狀態，然後將它儲存在 $Joblist 變數中。</span><span class="sxs-lookup"><span data-stu-id="3ded5-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="3ded5-111">第二個命令會顯示 $Joblist 陣列中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="3ded5-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="3ded5-112">範例2：在過去7天內取得所有失敗的工作</span><span class="sxs-lookup"><span data-stu-id="3ded5-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="3ded5-113">此命令會從 vault 中的最後一周取得失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="3ded5-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="3ded5-114">*From* 參數指定過去在 UTC 中指定的時間（以七天為單位）。</span><span class="sxs-lookup"><span data-stu-id="3ded5-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="3ded5-115">該命令不會指定 *To* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="3ded5-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="3ded5-116">因此，它會使用目前時間的預設值。</span><span class="sxs-lookup"><span data-stu-id="3ded5-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="3ded5-117">範例3：取得進行中的工作並等待完成</span><span class="sxs-lookup"><span data-stu-id="3ded5-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="3ded5-118">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="3ded5-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="3ded5-119">注意：您可以使用 **AzRecoveryServicesBackupJob** Cmdlet 來等待 Azure 備份作業完成，而不是迴圈執行。</span><span class="sxs-lookup"><span data-stu-id="3ded5-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="3ded5-120">範例4：在最近2天中取得所有您成功完成的所有新工作</span><span class="sxs-lookup"><span data-stu-id="3ded5-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="3ded5-121">第一個 Cmdlet 會提取 vault 物件。</span><span class="sxs-lookup"><span data-stu-id="3ded5-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="3ded5-122">第二個 Cmdlet 會將所有在過去2天完成的所有在指定電子倉庫中的所有，都儲存到 $jobs。</span><span class="sxs-lookup"><span data-stu-id="3ded5-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="3ded5-123">將 BackupManagementType 參數的值變更為 MAB，以便取得 MAB 代理作業。</span><span class="sxs-lookup"><span data-stu-id="3ded5-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="3ded5-124">參數</span><span class="sxs-lookup"><span data-stu-id="3ded5-124">PARAMETERS</span></span>

### <span data-ttu-id="3ded5-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3ded5-125">-BackupManagementType</span></span>

<span data-ttu-id="3ded5-126">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="3ded5-126">The class of resources being protected.</span></span> <span data-ttu-id="3ded5-127">目前，此 Cmdlet 支援的值為 AzureStorage、AzureWorkload、MAB。</span><span class="sxs-lookup"><span data-stu-id="3ded5-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ded5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ded5-128">-DefaultProfile</span></span>

<span data-ttu-id="3ded5-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ded5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ded5-130">-從</span><span class="sxs-lookup"><span data-stu-id="3ded5-130">-From</span></span>

<span data-ttu-id="3ded5-131">指定此 Cmdlet 所取得作業之時間範圍的開始（以 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="3ded5-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="3ded5-132">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ded5-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="3ded5-133">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="3ded5-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="3ded5-134">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="3ded5-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="3ded5-135">-工作</span><span class="sxs-lookup"><span data-stu-id="3ded5-135">-Job</span></span>

<span data-ttu-id="3ded5-136">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="3ded5-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="3ded5-137">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="3ded5-137">-JobId</span></span>

<span data-ttu-id="3ded5-138">指定此 Cmdlet 所取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ded5-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="3ded5-139">[識別碼] 是 **RecoveryServices JobBase** 物件的 [JobId] 屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="3ded5-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="3ded5-140">-操作</span><span class="sxs-lookup"><span data-stu-id="3ded5-140">-Operation</span></span>

<span data-ttu-id="3ded5-141">指定此 Cmdlet 取得作業的操作。</span><span class="sxs-lookup"><span data-stu-id="3ded5-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="3ded5-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3ded5-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ded5-143">備份</span><span class="sxs-lookup"><span data-stu-id="3ded5-143">Backup</span></span>
- <span data-ttu-id="3ded5-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="3ded5-144">ConfigureBackup</span></span>
- <span data-ttu-id="3ded5-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="3ded5-145">DeleteBackupData</span></span>
- <span data-ttu-id="3ded5-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="3ded5-146">DisableBackup</span></span>
- <span data-ttu-id="3ded5-147">還原</span><span class="sxs-lookup"><span data-stu-id="3ded5-147">Restore</span></span>
- <span data-ttu-id="3ded5-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="3ded5-148">BackupDataMove</span></span>

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

### <span data-ttu-id="3ded5-149">-狀態</span><span class="sxs-lookup"><span data-stu-id="3ded5-149">-Status</span></span>

<span data-ttu-id="3ded5-150">指定此 Cmdlet 取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3ded5-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="3ded5-151">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3ded5-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ded5-152">正在</span><span class="sxs-lookup"><span data-stu-id="3ded5-152">InProgress</span></span>
- <span data-ttu-id="3ded5-153">成功</span><span class="sxs-lookup"><span data-stu-id="3ded5-153">Failed</span></span>
- <span data-ttu-id="3ded5-154">取消</span><span class="sxs-lookup"><span data-stu-id="3ded5-154">Cancelled</span></span>
- <span data-ttu-id="3ded5-155">正在</span><span class="sxs-lookup"><span data-stu-id="3ded5-155">Cancelling</span></span>
- <span data-ttu-id="3ded5-156">完畢</span><span class="sxs-lookup"><span data-stu-id="3ded5-156">Completed</span></span>
- <span data-ttu-id="3ded5-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="3ded5-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="3ded5-158">-To</span><span class="sxs-lookup"><span data-stu-id="3ded5-158">-To</span></span>

<span data-ttu-id="3ded5-159">指定此 Cmdlet 所取得作業之時間範圍的結尾（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="3ded5-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="3ded5-160">預設值為目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="3ded5-160">The default value is the current system time.</span></span>
<span data-ttu-id="3ded5-161">如果您指定此參數，您也必須指定 **-From** 參數。</span><span class="sxs-lookup"><span data-stu-id="3ded5-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="3ded5-162">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="3ded5-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="3ded5-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3ded5-163">-VaultId</span></span>

<span data-ttu-id="3ded5-164">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="3ded5-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3ded5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ded5-165">CommonParameters</span></span>
<span data-ttu-id="3ded5-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ded5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ded5-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ded5-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ded5-168">輸入</span><span class="sxs-lookup"><span data-stu-id="3ded5-168">INPUTS</span></span>

### <span data-ttu-id="3ded5-169">System.object</span><span class="sxs-lookup"><span data-stu-id="3ded5-169">System.String</span></span>

## <span data-ttu-id="3ded5-170">輸出</span><span class="sxs-lookup"><span data-stu-id="3ded5-170">OUTPUTS</span></span>

### <span data-ttu-id="3ded5-171">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="3ded5-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3ded5-172">筆記</span><span class="sxs-lookup"><span data-stu-id="3ded5-172">NOTES</span></span>

## <span data-ttu-id="3ded5-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ded5-173">RELATED LINKS</span></span>

[<span data-ttu-id="3ded5-174">AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="3ded5-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="3ded5-175">停止 AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3ded5-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="3ded5-176">稍候-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3ded5-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
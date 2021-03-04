---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 011b27cfff166173d485636a1e8890d917484651
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909982"
---
# <span data-ttu-id="f3f83-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f3f83-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f3f83-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3f83-102">SYNOPSIS</span></span>

<span data-ttu-id="f3f83-103">獲得備份工作。</span><span class="sxs-lookup"><span data-stu-id="f3f83-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="f3f83-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3f83-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3f83-105">描述</span><span class="sxs-lookup"><span data-stu-id="f3f83-105">DESCRIPTION</span></span>

<span data-ttu-id="f3f83-106">**Get-AzRecoveryServicesBackupJob** Cmdlet 會取得特定儲存庫的 Azure 備份工作。</span><span class="sxs-lookup"><span data-stu-id="f3f83-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="f3f83-107">使用 -VaultId 參數設定庫上下文。</span><span class="sxs-lookup"><span data-stu-id="f3f83-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f3f83-108">例子</span><span class="sxs-lookup"><span data-stu-id="f3f83-108">EXAMPLES</span></span>

### <span data-ttu-id="f3f83-109">範例 1：取得所有進行中的工作</span><span class="sxs-lookup"><span data-stu-id="f3f83-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="f3f83-110">第一個命令會以陣列取得進行中工作的狀態，然後將它儲存在$Joblist變數中。</span><span class="sxs-lookup"><span data-stu-id="f3f83-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="f3f83-111">第二個命令會顯示陣列$Joblist專案。</span><span class="sxs-lookup"><span data-stu-id="f3f83-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="f3f83-112">範例 2：過去 7 天內取得所有失敗的工作</span><span class="sxs-lookup"><span data-stu-id="f3f83-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="f3f83-113">此命令會從儲存庫的最後一周開始，收到失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="f3f83-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="f3f83-114">From 參數會指定過去以 UTC 指定的七天時間。</span><span class="sxs-lookup"><span data-stu-id="f3f83-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="f3f83-115">命令不會指定 To *參數的值。*</span><span class="sxs-lookup"><span data-stu-id="f3f83-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="f3f83-116">因此，它會使用目前時間的預設值。</span><span class="sxs-lookup"><span data-stu-id="f3f83-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="f3f83-117">範例 3：取得進行中的工作並等待完成</span><span class="sxs-lookup"><span data-stu-id="f3f83-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="f3f83-118">此腳本會輪詢目前進行中的第一個工作，直到該工作完成為止。</span><span class="sxs-lookup"><span data-stu-id="f3f83-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="f3f83-119">注意：您可以使用 **Wait-AzRecoveryServicesBackupJob** Cmdlet 來等待 Azure 備份工作完成，而不是 While 迴圈。</span><span class="sxs-lookup"><span data-stu-id="f3f83-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="f3f83-120">範例 4：取得過去 2 天內完成的所有 AzureMS 工作</span><span class="sxs-lookup"><span data-stu-id="f3f83-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="f3f83-121">第一個 Cmdlet 會抓取庫物件。</span><span class="sxs-lookup"><span data-stu-id="f3f83-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="f3f83-122">第二個 Cmdlet 會儲存在所給保存庫中的所有 AzureCM 工作，此工作于過去 2 天內完成，$jobs。</span><span class="sxs-lookup"><span data-stu-id="f3f83-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="f3f83-123">將 BackupManagementType 參數的值變更為 MAB，以抓取 MAB 代理程式工作。</span><span class="sxs-lookup"><span data-stu-id="f3f83-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="f3f83-124">參數</span><span class="sxs-lookup"><span data-stu-id="f3f83-124">PARAMETERS</span></span>

### <span data-ttu-id="f3f83-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f3f83-125">-BackupManagementType</span></span>

<span data-ttu-id="f3f83-126">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="f3f83-126">The class of resources being protected.</span></span> <span data-ttu-id="f3f83-127">此 Cmdlet 目前支援的值為 AzureCM、AzureStorage、AzureWorkload、MAB。</span><span class="sxs-lookup"><span data-stu-id="f3f83-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

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

### <span data-ttu-id="f3f83-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f83-128">-DefaultProfile</span></span>

<span data-ttu-id="f3f83-129">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3f83-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f83-130">-從</span><span class="sxs-lookup"><span data-stu-id="f3f83-130">-From</span></span>

<span data-ttu-id="f3f83-131">指定此 **Cmdlet** 所獲得之工作的開始時間 ，做為 DateTime 物件。</span><span class="sxs-lookup"><span data-stu-id="f3f83-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f3f83-132">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3f83-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="f3f83-133">有關 **DateTime** 物件的資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="f3f83-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f3f83-134">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="f3f83-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="f3f83-135">-Job</span><span class="sxs-lookup"><span data-stu-id="f3f83-135">-Job</span></span>

<span data-ttu-id="f3f83-136">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="f3f83-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="f3f83-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="f3f83-137">-JobId</span></span>

<span data-ttu-id="f3f83-138">指定此 Cmdlet 所獲得工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3f83-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="f3f83-139">識別碼是 **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase 物件的 JobId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f3f83-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="f3f83-140">-作業</span><span class="sxs-lookup"><span data-stu-id="f3f83-140">-Operation</span></span>

<span data-ttu-id="f3f83-141">指定此 Cmdlet 所獲得工作的作業。</span><span class="sxs-lookup"><span data-stu-id="f3f83-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f3f83-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f3f83-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3f83-143">備份</span><span class="sxs-lookup"><span data-stu-id="f3f83-143">Backup</span></span>
- <span data-ttu-id="f3f83-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="f3f83-144">ConfigureBackup</span></span>
- <span data-ttu-id="f3f83-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="f3f83-145">DeleteBackupData</span></span>
- <span data-ttu-id="f3f83-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="f3f83-146">DisableBackup</span></span>
- <span data-ttu-id="f3f83-147">恢復</span><span class="sxs-lookup"><span data-stu-id="f3f83-147">Restore</span></span>
- <span data-ttu-id="f3f83-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="f3f83-148">BackupDataMove</span></span>

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

### <span data-ttu-id="f3f83-149">-狀態</span><span class="sxs-lookup"><span data-stu-id="f3f83-149">-Status</span></span>

<span data-ttu-id="f3f83-150">指定此 Cmdlet 獲得的工作狀態。</span><span class="sxs-lookup"><span data-stu-id="f3f83-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f3f83-151">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f3f83-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3f83-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="f3f83-152">InProgress</span></span>
- <span data-ttu-id="f3f83-153">失敗</span><span class="sxs-lookup"><span data-stu-id="f3f83-153">Failed</span></span>
- <span data-ttu-id="f3f83-154">取消</span><span class="sxs-lookup"><span data-stu-id="f3f83-154">Cancelled</span></span>
- <span data-ttu-id="f3f83-155">取消</span><span class="sxs-lookup"><span data-stu-id="f3f83-155">Cancelling</span></span>
- <span data-ttu-id="f3f83-156">完成</span><span class="sxs-lookup"><span data-stu-id="f3f83-156">Completed</span></span>
- <span data-ttu-id="f3f83-157">已完成的WithWarnings</span><span class="sxs-lookup"><span data-stu-id="f3f83-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="f3f83-158">-To</span><span class="sxs-lookup"><span data-stu-id="f3f83-158">-To</span></span>

<span data-ttu-id="f3f83-159">指定此 **Cmdlet** 所獲得之工作的結束時間範圍 ，做為 DateTime 物件。</span><span class="sxs-lookup"><span data-stu-id="f3f83-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f3f83-160">預設值為目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="f3f83-160">The default value is the current system time.</span></span>
<span data-ttu-id="f3f83-161">如果您指定此參數，您也必須指定 **-From** 參數。</span><span class="sxs-lookup"><span data-stu-id="f3f83-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="f3f83-162">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="f3f83-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="f3f83-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f3f83-163">-VaultId</span></span>

<span data-ttu-id="f3f83-164">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3f83-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f3f83-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f83-165">CommonParameters</span></span>
<span data-ttu-id="f3f83-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3f83-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f83-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3f83-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f83-168">輸入</span><span class="sxs-lookup"><span data-stu-id="f3f83-168">INPUTS</span></span>

### <span data-ttu-id="f3f83-169">System.String</span><span class="sxs-lookup"><span data-stu-id="f3f83-169">System.String</span></span>

## <span data-ttu-id="f3f83-170">輸出</span><span class="sxs-lookup"><span data-stu-id="f3f83-170">OUTPUTS</span></span>

### <span data-ttu-id="f3f83-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase</span><span class="sxs-lookup"><span data-stu-id="f3f83-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f3f83-172">筆記</span><span class="sxs-lookup"><span data-stu-id="f3f83-172">NOTES</span></span>

## <span data-ttu-id="f3f83-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3f83-173">RELATED LINKS</span></span>

[<span data-ttu-id="f3f83-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="f3f83-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="f3f83-175">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f3f83-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="f3f83-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f3f83-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)

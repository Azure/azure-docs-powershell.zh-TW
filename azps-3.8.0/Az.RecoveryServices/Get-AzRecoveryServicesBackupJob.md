---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 4d5ec07e7a068e1ab96f485ee67db0c1dd43f388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956830"
---
# <span data-ttu-id="9a649-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9a649-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="9a649-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a649-102">SYNOPSIS</span></span>

<span data-ttu-id="9a649-103">取得備份作業。</span><span class="sxs-lookup"><span data-stu-id="9a649-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="9a649-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a649-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a649-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a649-105">DESCRIPTION</span></span>

<span data-ttu-id="9a649-106">**AzRecoveryServicesBackupJob** Cmdlet 會針對特定的電子倉庫取得 Azure 備份作業。</span><span class="sxs-lookup"><span data-stu-id="9a649-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="9a649-107">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="9a649-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="9a649-108">示例</span><span class="sxs-lookup"><span data-stu-id="9a649-108">EXAMPLES</span></span>

### <span data-ttu-id="9a649-109">範例1：取得所有進行中的工作</span><span class="sxs-lookup"><span data-stu-id="9a649-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="9a649-110">第一個命令會以陣列形式取得進行中作業的狀態，然後將它儲存在 $Joblist 變數中。</span><span class="sxs-lookup"><span data-stu-id="9a649-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="9a649-111">第二個命令會顯示 $Joblist 陣列中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="9a649-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="9a649-112">範例2：在過去7天內取得所有失敗的工作</span><span class="sxs-lookup"><span data-stu-id="9a649-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="9a649-113">此命令會從 vault 中的最後一周取得失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="9a649-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="9a649-114">*From* 參數指定過去在 UTC 中指定的時間（以七天為單位）。</span><span class="sxs-lookup"><span data-stu-id="9a649-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="9a649-115">該命令不會指定 *To* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="9a649-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="9a649-116">因此，它會使用目前時間的預設值。</span><span class="sxs-lookup"><span data-stu-id="9a649-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="9a649-117">範例3：取得進行中的工作並等待完成</span><span class="sxs-lookup"><span data-stu-id="9a649-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="9a649-118">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="9a649-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="9a649-119">注意：您可以使用 **AzRecoveryServicesBackupJob** Cmdlet 來等待 Azure 備份作業完成，而不是迴圈執行。</span><span class="sxs-lookup"><span data-stu-id="9a649-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="9a649-120">參數</span><span class="sxs-lookup"><span data-stu-id="9a649-120">PARAMETERS</span></span>

### <span data-ttu-id="9a649-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9a649-121">-BackupManagementType</span></span>

<span data-ttu-id="9a649-122">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="9a649-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="9a649-123">目前僅支援 Add-azurevm、AzureStorage。</span><span class="sxs-lookup"><span data-stu-id="9a649-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="9a649-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a649-124">-DefaultProfile</span></span>

<span data-ttu-id="9a649-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a649-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a649-126">-從</span><span class="sxs-lookup"><span data-stu-id="9a649-126">-From</span></span>

<span data-ttu-id="9a649-127">指定此 Cmdlet 所取得作業之時間範圍的開始（以 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="9a649-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9a649-128">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a649-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="9a649-129">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="9a649-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9a649-130">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="9a649-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="9a649-131">-工作</span><span class="sxs-lookup"><span data-stu-id="9a649-131">-Job</span></span>

<span data-ttu-id="9a649-132">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="9a649-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="9a649-133">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="9a649-133">-JobId</span></span>

<span data-ttu-id="9a649-134">指定此 Cmdlet 所取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a649-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="9a649-135">[識別碼] 是 **RecoveryServices JobBase** 物件的 [JobId] 屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="9a649-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="9a649-136">-操作</span><span class="sxs-lookup"><span data-stu-id="9a649-136">-Operation</span></span>

<span data-ttu-id="9a649-137">指定此 Cmdlet 取得作業的操作。</span><span class="sxs-lookup"><span data-stu-id="9a649-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9a649-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9a649-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a649-139">備份</span><span class="sxs-lookup"><span data-stu-id="9a649-139">Backup</span></span>
- <span data-ttu-id="9a649-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="9a649-140">ConfigureBackup</span></span>
- <span data-ttu-id="9a649-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="9a649-141">DeleteBackupData</span></span>
- <span data-ttu-id="9a649-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="9a649-142">DisableBackup</span></span>
- <span data-ttu-id="9a649-143">還原</span><span class="sxs-lookup"><span data-stu-id="9a649-143">Restore</span></span>

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

### <span data-ttu-id="9a649-144">-狀態</span><span class="sxs-lookup"><span data-stu-id="9a649-144">-Status</span></span>

<span data-ttu-id="9a649-145">指定此 Cmdlet 取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="9a649-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9a649-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9a649-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a649-147">正在</span><span class="sxs-lookup"><span data-stu-id="9a649-147">InProgress</span></span>
- <span data-ttu-id="9a649-148">成功</span><span class="sxs-lookup"><span data-stu-id="9a649-148">Failed</span></span>
- <span data-ttu-id="9a649-149">取消</span><span class="sxs-lookup"><span data-stu-id="9a649-149">Cancelled</span></span>
- <span data-ttu-id="9a649-150">正在</span><span class="sxs-lookup"><span data-stu-id="9a649-150">Cancelling</span></span>
- <span data-ttu-id="9a649-151">完畢</span><span class="sxs-lookup"><span data-stu-id="9a649-151">Completed</span></span>
- <span data-ttu-id="9a649-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="9a649-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="9a649-153">-To</span><span class="sxs-lookup"><span data-stu-id="9a649-153">-To</span></span>

<span data-ttu-id="9a649-154">指定此 Cmdlet 所取得作業之時間範圍的結尾（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="9a649-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9a649-155">預設值為目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="9a649-155">The default value is the current system time.</span></span>
<span data-ttu-id="9a649-156">如果您指定此參數，您也必須指定 **-From** 參數。</span><span class="sxs-lookup"><span data-stu-id="9a649-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="9a649-157">針對日期使用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="9a649-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="9a649-158">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9a649-158">-VaultId</span></span>

<span data-ttu-id="9a649-159">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="9a649-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9a649-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a649-160">CommonParameters</span></span>
<span data-ttu-id="9a649-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a649-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a649-162">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9a649-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a649-163">輸入</span><span class="sxs-lookup"><span data-stu-id="9a649-163">INPUTS</span></span>

### <span data-ttu-id="9a649-164">System.object</span><span class="sxs-lookup"><span data-stu-id="9a649-164">System.String</span></span>

## <span data-ttu-id="9a649-165">輸出</span><span class="sxs-lookup"><span data-stu-id="9a649-165">OUTPUTS</span></span>

### <span data-ttu-id="9a649-166">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="9a649-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9a649-167">筆記</span><span class="sxs-lookup"><span data-stu-id="9a649-167">NOTES</span></span>

## <span data-ttu-id="9a649-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a649-168">RELATED LINKS</span></span>

[<span data-ttu-id="9a649-169">AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="9a649-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="9a649-170">停止 AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9a649-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="9a649-171">稍候-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9a649-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)

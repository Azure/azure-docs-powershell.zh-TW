---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: cbdb60fb4ec139b1dae92b7dd8e2e54675ae1f90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448473"
---
# <span data-ttu-id="6084f-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6084f-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="6084f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6084f-102">SYNOPSIS</span></span>
<span data-ttu-id="6084f-103">取得備份作業。</span><span class="sxs-lookup"><span data-stu-id="6084f-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6084f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6084f-104">SYNTAX</span></span>

### <span data-ttu-id="6084f-105">FiltersSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6084f-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6084f-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="6084f-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6084f-107">說明</span><span class="sxs-lookup"><span data-stu-id="6084f-107">DESCRIPTION</span></span>
<span data-ttu-id="6084f-108">**AzureRmBackupJob** Cmdlet 會針對特定的電子倉庫取得 Azure 備份作業。</span><span class="sxs-lookup"><span data-stu-id="6084f-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="6084f-109">示例</span><span class="sxs-lookup"><span data-stu-id="6084f-109">EXAMPLES</span></span>

### <span data-ttu-id="6084f-110">範例1：取得備份保存庫中的所有工作</span><span class="sxs-lookup"><span data-stu-id="6084f-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="6084f-111">第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="6084f-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="6084f-112">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="6084f-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="6084f-113">第二個命令會在 $Vault 中取得 vault 的所有作業。</span><span class="sxs-lookup"><span data-stu-id="6084f-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="6084f-114">範例2：取得完成的工作</span><span class="sxs-lookup"><span data-stu-id="6084f-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="6084f-115">這個命令會在 $Vault 中從 vault 中取得已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="6084f-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="6084f-116">範例3：取得最後一周失敗的工作</span><span class="sxs-lookup"><span data-stu-id="6084f-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="6084f-117">此命令會從 $Vault 中的 [vault] 的最後一周取得失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="6084f-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="6084f-118">*From* 參數指定過去七天的時間。</span><span class="sxs-lookup"><span data-stu-id="6084f-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="6084f-119">該命令不會指定 *To* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="6084f-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="6084f-120">因此，它會使用目前時間的預設值。</span><span class="sxs-lookup"><span data-stu-id="6084f-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="6084f-121">範例4：輪詢備份完成的正在進行中的工作</span><span class="sxs-lookup"><span data-stu-id="6084f-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="6084f-122">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="6084f-122">This script polls the first job that is currently in progress until the job has completed.</span></span>
<span data-ttu-id="6084f-123">腳本的第一行會取得正在進行的 $Vault 中的所有工作，然後將這些作業儲存在 $Jobs 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="6084f-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>
<span data-ttu-id="6084f-124">第二行會將 $Jobs 陣列中的第一個工作儲存在 $Job 變數中。</span><span class="sxs-lookup"><span data-stu-id="6084f-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>
<span data-ttu-id="6084f-125">第三行會啟動一個 **while** 迴圈，以檢查作業的目前狀態，直到作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="6084f-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="6084f-126">如需有關 **while** 關鍵字的資訊，請輸入 `Get-Help about_While` 。</span><span class="sxs-lookup"><span data-stu-id="6084f-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>
<span data-ttu-id="6084f-127">**While** 迴圈會將訊息寫入主控台，並在十秒內休眠，然後更新 $Job 變數。</span><span class="sxs-lookup"><span data-stu-id="6084f-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="6084f-128">此腳本會使用 $Job 現有的值和目前的 Cmdlet 來更新 $Job 變數，以取得工作的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6084f-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="6084f-129">如需有關 Windows PowerShell Cmdlet 的詳細資訊，請輸入 `Get-Help Write-Host` 和 `Get-Help Start-Sleep` 。</span><span class="sxs-lookup"><span data-stu-id="6084f-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>
<span data-ttu-id="6084f-130">腳本的最後一行告訴您腳本已完成。</span><span class="sxs-lookup"><span data-stu-id="6084f-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="6084f-131">參數</span><span class="sxs-lookup"><span data-stu-id="6084f-131">PARAMETERS</span></span>

### <span data-ttu-id="6084f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6084f-132">-DefaultProfile</span></span>
<span data-ttu-id="6084f-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6084f-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6084f-134">-從</span><span class="sxs-lookup"><span data-stu-id="6084f-134">-From</span></span>
<span data-ttu-id="6084f-135">指定此 Cmdlet 所取得作業之時間範圍的開始（以 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="6084f-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6084f-136">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6084f-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="6084f-137">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="6084f-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6084f-138">-工作</span><span class="sxs-lookup"><span data-stu-id="6084f-138">-Job</span></span>
<span data-ttu-id="6084f-139">指定此 Cmdlet 取得的作業。</span><span class="sxs-lookup"><span data-stu-id="6084f-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="6084f-140">若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6084f-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6084f-141">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="6084f-141">-JobId</span></span>
<span data-ttu-id="6084f-142">指定此 Cmdlet 所取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6084f-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="6084f-143">識別碼是 **AzureRmBackupJob** 物件的 **InstanceId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6084f-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="6084f-144">若要取得 **AzureRmBackupJob** 物件，請使用 AzureRmBackupJob。</span><span class="sxs-lookup"><span data-stu-id="6084f-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6084f-145">-操作</span><span class="sxs-lookup"><span data-stu-id="6084f-145">-Operation</span></span>
<span data-ttu-id="6084f-146">指定此 Cmdlet 取得作業的操作。</span><span class="sxs-lookup"><span data-stu-id="6084f-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6084f-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6084f-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6084f-148">備份</span><span class="sxs-lookup"><span data-stu-id="6084f-148">Backup</span></span> 
- <span data-ttu-id="6084f-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="6084f-149">ConfigureBackup</span></span> 
- <span data-ttu-id="6084f-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="6084f-150">DeleteBackupData</span></span> 
- <span data-ttu-id="6084f-151">註冊表</span><span class="sxs-lookup"><span data-stu-id="6084f-151">Register</span></span> 
- <span data-ttu-id="6084f-152">還原</span><span class="sxs-lookup"><span data-stu-id="6084f-152">Restore</span></span> 
- <span data-ttu-id="6084f-153">對</span><span class="sxs-lookup"><span data-stu-id="6084f-153">UnProtect</span></span> 
- <span data-ttu-id="6084f-154">登出</span><span class="sxs-lookup"><span data-stu-id="6084f-154">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6084f-155">-狀態</span><span class="sxs-lookup"><span data-stu-id="6084f-155">-Status</span></span>
<span data-ttu-id="6084f-156">指定此 Cmdlet 取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="6084f-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6084f-157">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6084f-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6084f-158">正在</span><span class="sxs-lookup"><span data-stu-id="6084f-158">InProgress</span></span>
- <span data-ttu-id="6084f-159">成功</span><span class="sxs-lookup"><span data-stu-id="6084f-159">Failed</span></span>
- <span data-ttu-id="6084f-160">取消</span><span class="sxs-lookup"><span data-stu-id="6084f-160">Cancelled</span></span>
- <span data-ttu-id="6084f-161">正在</span><span class="sxs-lookup"><span data-stu-id="6084f-161">Cancelling</span></span>
- <span data-ttu-id="6084f-162">完畢</span><span class="sxs-lookup"><span data-stu-id="6084f-162">Completed</span></span>
- <span data-ttu-id="6084f-163">CompletedWithWarnings 您可以指定此參數來尋找所有正在進行中的作業或所有失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="6084f-163">CompletedWithWarnings You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6084f-164">-To</span><span class="sxs-lookup"><span data-stu-id="6084f-164">-To</span></span>
<span data-ttu-id="6084f-165">指定此 Cmdlet 所取得作業之時間範圍的結尾（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="6084f-165">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6084f-166">預設值為目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="6084f-166">The default value is the current system time.</span></span>
<span data-ttu-id="6084f-167">如果您指定此參數，您也必須指定 *From* 參數。</span><span class="sxs-lookup"><span data-stu-id="6084f-167">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6084f-168">-類型</span><span class="sxs-lookup"><span data-stu-id="6084f-168">-Type</span></span>
<span data-ttu-id="6084f-169">指定此 Cmdlet 取得備份作業的容器類型。</span><span class="sxs-lookup"><span data-stu-id="6084f-169">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="6084f-170">目前唯一支援的值為 Add-azurevm。</span><span class="sxs-lookup"><span data-stu-id="6084f-170">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6084f-171">-保存庫</span><span class="sxs-lookup"><span data-stu-id="6084f-171">-Vault</span></span>
<span data-ttu-id="6084f-172">指定此 Cmdlet 取得作業的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="6084f-172">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="6084f-173">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6084f-173">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6084f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6084f-174">CommonParameters</span></span>
<span data-ttu-id="6084f-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6084f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6084f-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6084f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6084f-177">輸入</span><span class="sxs-lookup"><span data-stu-id="6084f-177">INPUTS</span></span>

### <span data-ttu-id="6084f-178">AzureRMBackupVault 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="6084f-178">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="6084f-179">參數：保存庫 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6084f-179">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="6084f-180">輸出</span><span class="sxs-lookup"><span data-stu-id="6084f-180">OUTPUTS</span></span>

### <span data-ttu-id="6084f-181">AzureRMBackupJob 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="6084f-181">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="6084f-182">筆記</span><span class="sxs-lookup"><span data-stu-id="6084f-182">NOTES</span></span>
* <span data-ttu-id="6084f-183">所有</span><span class="sxs-lookup"><span data-stu-id="6084f-183">None</span></span>

## <span data-ttu-id="6084f-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="6084f-184">RELATED LINKS</span></span>

[<span data-ttu-id="6084f-185">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="6084f-185">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="6084f-186">停止 AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6084f-186">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="6084f-187">稍候-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6084f-187">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)



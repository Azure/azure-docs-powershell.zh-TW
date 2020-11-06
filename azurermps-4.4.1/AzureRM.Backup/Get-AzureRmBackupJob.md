---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446879"
---
# <span data-ttu-id="1e3b7-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="1e3b7-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="1e3b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3b7-103">取得備份作業。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e3b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e3b7-104">SYNTAX</span></span>

### <span data-ttu-id="1e3b7-105">FiltersSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1e3b7-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e3b7-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="1e3b7-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e3b7-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e3b7-107">DESCRIPTION</span></span>
<span data-ttu-id="1e3b7-108">**AzureRmBackupJob** Cmdlet 會針對特定的電子倉庫取得 Azure 備份作業。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="1e3b7-109">示例</span><span class="sxs-lookup"><span data-stu-id="1e3b7-109">EXAMPLES</span></span>

### <span data-ttu-id="1e3b7-110">範例1：取得備份保存庫中的所有工作</span><span class="sxs-lookup"><span data-stu-id="1e3b7-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="1e3b7-111">第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="1e3b7-112">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="1e3b7-113">第二個命令會在 $Vault 中取得 vault 的所有作業。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="1e3b7-114">範例2：取得完成的工作</span><span class="sxs-lookup"><span data-stu-id="1e3b7-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="1e3b7-115">這個命令會在 $Vault 中從 vault 中取得已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="1e3b7-116">範例3：取得最後一周失敗的工作</span><span class="sxs-lookup"><span data-stu-id="1e3b7-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="1e3b7-117">此命令會從 $Vault 中的 [vault] 的最後一周取得失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="1e3b7-118">*From* 參數指定過去七天的時間。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="1e3b7-119">該命令不會指定 *To* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="1e3b7-120">因此，它會使用目前時間的預設值。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="1e3b7-121">範例4：輪詢備份完成的正在進行中的工作</span><span class="sxs-lookup"><span data-stu-id="1e3b7-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
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

<span data-ttu-id="1e3b7-122">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="1e3b7-123">腳本的第一行會取得正在進行的 $Vault 中的所有工作，然後將這些作業儲存在 $Jobs 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="1e3b7-124">第二行會將 $Jobs 陣列中的第一個工作儲存在 $Job 變數中。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="1e3b7-125">第三行會啟動一個 **while** 迴圈，以檢查作業的目前狀態，直到作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="1e3b7-126">如需有關 **while** 關鍵字的資訊，請輸入 `Get-Help about_While` 。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="1e3b7-127">**While** 迴圈會將訊息寫入主控台，並在十秒內休眠，然後更新 $Job 變數。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="1e3b7-128">此腳本會使用 $Job 現有的值和目前的 Cmdlet 來更新 $Job 變數，以取得工作的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="1e3b7-129">如需有關 Windows PowerShell Cmdlet 的詳細資訊，請輸入 `Get-Help Write-Host` 和 `Get-Help Start-Sleep` 。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="1e3b7-130">腳本的最後一行告訴您腳本已完成。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="1e3b7-131">參數</span><span class="sxs-lookup"><span data-stu-id="1e3b7-131">PARAMETERS</span></span>

### <span data-ttu-id="1e3b7-132">-從</span><span class="sxs-lookup"><span data-stu-id="1e3b7-132">-From</span></span>
<span data-ttu-id="1e3b7-133">指定此 Cmdlet 所取得作業之時間範圍的開始（以 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-133">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="1e3b7-134">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-134">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="1e3b7-135">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-135">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="1e3b7-136">-工作</span><span class="sxs-lookup"><span data-stu-id="1e3b7-136">-Job</span></span>
<span data-ttu-id="1e3b7-137">指定此 Cmdlet 取得的作業。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-137">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="1e3b7-138">若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-138">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="1e3b7-139">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="1e3b7-139">-JobId</span></span>
<span data-ttu-id="1e3b7-140">指定此 Cmdlet 所取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-140">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="1e3b7-141">識別碼是 **AzureRmBackupJob** 物件的 **InstanceId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-141">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="1e3b7-142">若要取得 **AzureRmBackupJob** 物件，請使用 AzureRmBackupJob。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-142">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

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

### <span data-ttu-id="1e3b7-143">-操作</span><span class="sxs-lookup"><span data-stu-id="1e3b7-143">-Operation</span></span>
<span data-ttu-id="1e3b7-144">指定此 Cmdlet 取得作業的操作。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-144">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="1e3b7-145">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1e3b7-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e3b7-146">備份</span><span class="sxs-lookup"><span data-stu-id="1e3b7-146">Backup</span></span> 
- <span data-ttu-id="1e3b7-147">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="1e3b7-147">ConfigureBackup</span></span> 
- <span data-ttu-id="1e3b7-148">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="1e3b7-148">DeleteBackupData</span></span> 
- <span data-ttu-id="1e3b7-149">註冊表</span><span class="sxs-lookup"><span data-stu-id="1e3b7-149">Register</span></span> 
- <span data-ttu-id="1e3b7-150">還原</span><span class="sxs-lookup"><span data-stu-id="1e3b7-150">Restore</span></span> 
- <span data-ttu-id="1e3b7-151">對</span><span class="sxs-lookup"><span data-stu-id="1e3b7-151">UnProtect</span></span> 
- <span data-ttu-id="1e3b7-152">登出</span><span class="sxs-lookup"><span data-stu-id="1e3b7-152">Unregister</span></span>

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

### <span data-ttu-id="1e3b7-153">-狀態</span><span class="sxs-lookup"><span data-stu-id="1e3b7-153">-Status</span></span>
<span data-ttu-id="1e3b7-154">指定此 Cmdlet 取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-154">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="1e3b7-155">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1e3b7-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e3b7-156">正在</span><span class="sxs-lookup"><span data-stu-id="1e3b7-156">InProgress</span></span>
- <span data-ttu-id="1e3b7-157">成功</span><span class="sxs-lookup"><span data-stu-id="1e3b7-157">Failed</span></span>
- <span data-ttu-id="1e3b7-158">取消</span><span class="sxs-lookup"><span data-stu-id="1e3b7-158">Cancelled</span></span>
- <span data-ttu-id="1e3b7-159">正在</span><span class="sxs-lookup"><span data-stu-id="1e3b7-159">Cancelling</span></span>
- <span data-ttu-id="1e3b7-160">完畢</span><span class="sxs-lookup"><span data-stu-id="1e3b7-160">Completed</span></span>
- <span data-ttu-id="1e3b7-161">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="1e3b7-161">CompletedWithWarnings</span></span> 

<span data-ttu-id="1e3b7-162">您可以指定此參數來尋找所有正在進行中的作業或所有失敗的工作。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-162">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

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

### <span data-ttu-id="1e3b7-163">-To</span><span class="sxs-lookup"><span data-stu-id="1e3b7-163">-To</span></span>
<span data-ttu-id="1e3b7-164">指定此 Cmdlet 所取得作業之時間範圍的結尾（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-164">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="1e3b7-165">預設值為目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-165">The default value is the current system time.</span></span>
<span data-ttu-id="1e3b7-166">如果您指定此參數，您也必須指定 *From* 參數。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-166">If you specify this parameter, you must also specify the *From* parameter.</span></span>

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

### <span data-ttu-id="1e3b7-167">-類型</span><span class="sxs-lookup"><span data-stu-id="1e3b7-167">-Type</span></span>
<span data-ttu-id="1e3b7-168">指定此 Cmdlet 取得備份作業的容器類型。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-168">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="1e3b7-169">目前唯一支援的值為 Add-azurevm。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-169">Currently, the only supported value is AzureVM.</span></span>

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

### <span data-ttu-id="1e3b7-170">-保存庫</span><span class="sxs-lookup"><span data-stu-id="1e3b7-170">-Vault</span></span>
<span data-ttu-id="1e3b7-171">指定此 Cmdlet 取得作業的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-171">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="1e3b7-172">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-172">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="1e3b7-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3b7-173">-DefaultProfile</span></span>
<span data-ttu-id="1e3b7-174">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e3b7-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3b7-175">CommonParameters</span></span>
<span data-ttu-id="1e3b7-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3b7-177">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3b7-178">輸入</span><span class="sxs-lookup"><span data-stu-id="1e3b7-178">INPUTS</span></span>

### <span data-ttu-id="1e3b7-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="1e3b7-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="1e3b7-180">輸出</span><span class="sxs-lookup"><span data-stu-id="1e3b7-180">OUTPUTS</span></span>

### <span data-ttu-id="1e3b7-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="1e3b7-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="1e3b7-182">這個 Cmdlet 會傳回一或多個備份作業。</span><span class="sxs-lookup"><span data-stu-id="1e3b7-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="1e3b7-183">筆記</span><span class="sxs-lookup"><span data-stu-id="1e3b7-183">NOTES</span></span>
* <span data-ttu-id="1e3b7-184">所有</span><span class="sxs-lookup"><span data-stu-id="1e3b7-184">None</span></span>

## <span data-ttu-id="1e3b7-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e3b7-185">RELATED LINKS</span></span>

[<span data-ttu-id="1e3b7-186">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="1e3b7-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="1e3b7-187">停止 AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="1e3b7-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="1e3b7-188">稍候-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="1e3b7-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)



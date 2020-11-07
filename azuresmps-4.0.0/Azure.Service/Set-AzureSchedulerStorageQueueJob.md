---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967496"
---
# <span data-ttu-id="c439e-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c439e-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="c439e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c439e-102">SYNOPSIS</span></span>
<span data-ttu-id="c439e-103">更新具有儲存動作的排程作業。</span><span class="sxs-lookup"><span data-stu-id="c439e-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="c439e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c439e-104">SYNTAX</span></span>

### <span data-ttu-id="c439e-105">必填</span><span class="sxs-lookup"><span data-stu-id="c439e-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c439e-106">週期性</span><span class="sxs-lookup"><span data-stu-id="c439e-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c439e-107">說明</span><span class="sxs-lookup"><span data-stu-id="c439e-107">DESCRIPTION</span></span>
<span data-ttu-id="c439e-108">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c439e-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c439e-109">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="c439e-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c439e-110">**AzureSchedulerStorageQueueJob** Cmdlet 會更新具有 Azure 儲存空間動作的排程作業。</span><span class="sxs-lookup"><span data-stu-id="c439e-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="c439e-111">示例</span><span class="sxs-lookup"><span data-stu-id="c439e-111">EXAMPLES</span></span>

### <span data-ttu-id="c439e-112">範例1：更新儲存佇列訊息</span><span class="sxs-lookup"><span data-stu-id="c439e-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="c439e-113">這個命令會更新名為 Job12 的儲存作業的佇列訊息。</span><span class="sxs-lookup"><span data-stu-id="c439e-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="c439e-114">命令會指定作業集合名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="c439e-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="c439e-115">範例2：啟用儲存佇列作業</span><span class="sxs-lookup"><span data-stu-id="c439e-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="c439e-116">這個命令會啟用名為 Job16 的作業。</span><span class="sxs-lookup"><span data-stu-id="c439e-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="c439e-117">此命令會透過指定 *JobState* 參數的值，將作業的狀態變更為 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="c439e-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="c439e-118">參數</span><span class="sxs-lookup"><span data-stu-id="c439e-118">PARAMETERS</span></span>

### <span data-ttu-id="c439e-119">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c439e-119">-EndTime</span></span>
<span data-ttu-id="c439e-120">指定時間（作為 **DateTime** 物件），讓排程程式停止啟動作業。</span><span class="sxs-lookup"><span data-stu-id="c439e-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="c439e-121">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c439e-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="c439e-122">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="c439e-122">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="c439e-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="c439e-124">指定標頭做為雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c439e-124">Specifies headers as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="c439e-125">-ErrorActionMethod</span></span>
<span data-ttu-id="c439e-126">指定 HTTP 和 HTTPS 動作類型的方法。</span><span class="sxs-lookup"><span data-stu-id="c439e-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="c439e-127">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c439e-127">Valid values are:</span></span> 

- <span data-ttu-id="c439e-128">獲取</span><span class="sxs-lookup"><span data-stu-id="c439e-128">GET</span></span>
- <span data-ttu-id="c439e-129">將</span><span class="sxs-lookup"><span data-stu-id="c439e-129">PUT</span></span>
- <span data-ttu-id="c439e-130">發佈</span><span class="sxs-lookup"><span data-stu-id="c439e-130">POST</span></span>
- <span data-ttu-id="c439e-131">螺絲刀</span><span class="sxs-lookup"><span data-stu-id="c439e-131">HEAD</span></span>
- <span data-ttu-id="c439e-132">DELETE</span><span class="sxs-lookup"><span data-stu-id="c439e-132">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="c439e-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="c439e-134">指定儲存作業作業動作的主體。</span><span class="sxs-lookup"><span data-stu-id="c439e-134">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="c439e-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="c439e-136">指定放入和張貼作業動作的本文。</span><span class="sxs-lookup"><span data-stu-id="c439e-136">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="c439e-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="c439e-138">指定儲存佇列 (SAS) 標記的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="c439e-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c439e-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="c439e-140">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c439e-140">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c439e-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="c439e-142">指定儲存佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="c439e-142">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="c439e-143">-ErrorActionURI</span></span>
<span data-ttu-id="c439e-144">指定錯誤作業動作的 URI。</span><span class="sxs-lookup"><span data-stu-id="c439e-144">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="c439e-145">-ExecutionCount</span></span>
<span data-ttu-id="c439e-146">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="c439e-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="c439e-147">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="c439e-147">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-148">頻率</span><span class="sxs-lookup"><span data-stu-id="c439e-148">-Frequency</span></span>
<span data-ttu-id="c439e-149">指定此排程作業的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="c439e-149">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-150">間隔</span><span class="sxs-lookup"><span data-stu-id="c439e-150">-Interval</span></span>
<span data-ttu-id="c439e-151">使用 *frequency* 參數指定的頻率來指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="c439e-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c439e-152">-JobCollectionName</span></span>
<span data-ttu-id="c439e-153">指定要包含排程作業之集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="c439e-153">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-154">-JobName</span><span class="sxs-lookup"><span data-stu-id="c439e-154">-JobName</span></span>
<span data-ttu-id="c439e-155">指定要更新的排程作業名稱。</span><span class="sxs-lookup"><span data-stu-id="c439e-155">Specifies the name of the scheduler job to update.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="c439e-156">-JobState</span></span>
<span data-ttu-id="c439e-157">指定排程作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="c439e-157">Specifies the state for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-158">-位置</span><span class="sxs-lookup"><span data-stu-id="c439e-158">-Location</span></span>
<span data-ttu-id="c439e-159">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="c439e-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="c439e-160">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c439e-160">Valid values are:</span></span> 

- <span data-ttu-id="c439e-161">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="c439e-161">Anywhere Asia</span></span>
- <span data-ttu-id="c439e-162">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="c439e-162">Anywhere Europe</span></span>
- <span data-ttu-id="c439e-163">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="c439e-163">Anywhere US</span></span>
- <span data-ttu-id="c439e-164">東亞</span><span class="sxs-lookup"><span data-stu-id="c439e-164">East Asia</span></span>
- <span data-ttu-id="c439e-165">東美國</span><span class="sxs-lookup"><span data-stu-id="c439e-165">East US</span></span>
- <span data-ttu-id="c439e-166">美國中北部</span><span class="sxs-lookup"><span data-stu-id="c439e-166">North Central US</span></span>
- <span data-ttu-id="c439e-167">北歐</span><span class="sxs-lookup"><span data-stu-id="c439e-167">North Europe</span></span>
- <span data-ttu-id="c439e-168">美國中南部</span><span class="sxs-lookup"><span data-stu-id="c439e-168">South Central US</span></span>
- <span data-ttu-id="c439e-169">東南亞</span><span class="sxs-lookup"><span data-stu-id="c439e-169">Southeast Asia</span></span>
- <span data-ttu-id="c439e-170">西歐</span><span class="sxs-lookup"><span data-stu-id="c439e-170">West Europe</span></span>
- <span data-ttu-id="c439e-171">美國西部</span><span class="sxs-lookup"><span data-stu-id="c439e-171">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c439e-172">-PassThru</span></span>
<span data-ttu-id="c439e-173">表示此 Cmdlet 會傳回代表其操作專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c439e-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="c439e-174">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c439e-174">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c439e-175">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c439e-175">-Profile</span></span>
<span data-ttu-id="c439e-176">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c439e-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c439e-177">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c439e-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c439e-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="c439e-178">-SASToken</span></span>
<span data-ttu-id="c439e-179">指定儲存佇列的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="c439e-179">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-180">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c439e-180">-StartTime</span></span>
<span data-ttu-id="c439e-181">指定要啟動作業的時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="c439e-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="c439e-182">-StorageQueueAccount</span></span>
<span data-ttu-id="c439e-183">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c439e-183">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="c439e-184">-StorageQueueMessage</span></span>
<span data-ttu-id="c439e-185">指定儲存作業的佇列訊息。</span><span class="sxs-lookup"><span data-stu-id="c439e-185">Specifies the queue message for the Storage job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="c439e-186">-StorageQueueName</span></span>
<span data-ttu-id="c439e-187">指定儲存佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="c439e-187">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c439e-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c439e-188">CommonParameters</span></span>
<span data-ttu-id="c439e-189">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c439e-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c439e-190">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c439e-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c439e-191">輸入</span><span class="sxs-lookup"><span data-stu-id="c439e-191">INPUTS</span></span>

## <span data-ttu-id="c439e-192">輸出</span><span class="sxs-lookup"><span data-stu-id="c439e-192">OUTPUTS</span></span>

## <span data-ttu-id="c439e-193">筆記</span><span class="sxs-lookup"><span data-stu-id="c439e-193">NOTES</span></span>

## <span data-ttu-id="c439e-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="c439e-194">RELATED LINKS</span></span>

[<span data-ttu-id="c439e-195">新-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c439e-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)



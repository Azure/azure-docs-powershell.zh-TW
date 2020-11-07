---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967348"
---
# <span data-ttu-id="edb3c-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="edb3c-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="edb3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="edb3c-103">建立具有儲存動作的排程作業。</span><span class="sxs-lookup"><span data-stu-id="edb3c-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="edb3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="edb3c-104">SYNTAX</span></span>

### <span data-ttu-id="edb3c-105">必填</span><span class="sxs-lookup"><span data-stu-id="edb3c-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="edb3c-106">週期性</span><span class="sxs-lookup"><span data-stu-id="edb3c-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="edb3c-107">說明</span><span class="sxs-lookup"><span data-stu-id="edb3c-107">DESCRIPTION</span></span>
<span data-ttu-id="edb3c-108">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edb3c-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="edb3c-109">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="edb3c-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="edb3c-110">**新的-AzureSchedulerStorageQueueJob** Cmdlet 會建立具有 Azure 儲存空間動作的排程作業。</span><span class="sxs-lookup"><span data-stu-id="edb3c-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="edb3c-111">示例</span><span class="sxs-lookup"><span data-stu-id="edb3c-111">EXAMPLES</span></span>

### <span data-ttu-id="edb3c-112">範例1：建立一次執行的儲存作業</span><span class="sxs-lookup"><span data-stu-id="edb3c-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="edb3c-113">這個命令會建立一個排程儲存作業，作為名為 JobCollection01 的集合的一部分。</span><span class="sxs-lookup"><span data-stu-id="edb3c-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="edb3c-114">此命令會指定儲存空間帳戶、佇列名稱和 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="edb3c-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="edb3c-115">作業會立即執行一次。</span><span class="sxs-lookup"><span data-stu-id="edb3c-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="edb3c-116">範例2：建立執行指定次數的儲存作業</span><span class="sxs-lookup"><span data-stu-id="edb3c-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="edb3c-117">這個命令會建立一個排程儲存作業，作為名為 JobCollection01 的集合的一部分。</span><span class="sxs-lookup"><span data-stu-id="edb3c-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="edb3c-118">此命令會指定儲存空間帳戶、佇列名稱和 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="edb3c-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="edb3c-119">作業總共每小時執行20次。</span><span class="sxs-lookup"><span data-stu-id="edb3c-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="edb3c-120">參數</span><span class="sxs-lookup"><span data-stu-id="edb3c-120">PARAMETERS</span></span>

### <span data-ttu-id="edb3c-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="edb3c-121">-EndTime</span></span>
<span data-ttu-id="edb3c-122">指定時間（作為 **DateTime** 物件），讓排程程式停止啟動作業。</span><span class="sxs-lookup"><span data-stu-id="edb3c-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="edb3c-123">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edb3c-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="edb3c-124">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="edb3c-124">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="edb3c-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="edb3c-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="edb3c-126">指定標頭做為雜湊表。</span><span class="sxs-lookup"><span data-stu-id="edb3c-126">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="edb3c-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="edb3c-127">-ErrorActionMethod</span></span>
<span data-ttu-id="edb3c-128">指定 HTTP 和 HTTPS 動作類型的方法。</span><span class="sxs-lookup"><span data-stu-id="edb3c-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="edb3c-129">有效值為：</span><span class="sxs-lookup"><span data-stu-id="edb3c-129">Valid values are:</span></span> 

- <span data-ttu-id="edb3c-130">獲取</span><span class="sxs-lookup"><span data-stu-id="edb3c-130">GET</span></span>
- <span data-ttu-id="edb3c-131">將</span><span class="sxs-lookup"><span data-stu-id="edb3c-131">PUT</span></span>
- <span data-ttu-id="edb3c-132">發佈</span><span class="sxs-lookup"><span data-stu-id="edb3c-132">POST</span></span>
- <span data-ttu-id="edb3c-133">螺絲刀</span><span class="sxs-lookup"><span data-stu-id="edb3c-133">HEAD</span></span>
- <span data-ttu-id="edb3c-134">DELETE</span><span class="sxs-lookup"><span data-stu-id="edb3c-134">DELETE</span></span>

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

### <span data-ttu-id="edb3c-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="edb3c-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="edb3c-136">指定儲存作業作業動作的主體。</span><span class="sxs-lookup"><span data-stu-id="edb3c-136">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="edb3c-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="edb3c-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="edb3c-138">指定放入和張貼作業動作的本文。</span><span class="sxs-lookup"><span data-stu-id="edb3c-138">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="edb3c-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="edb3c-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="edb3c-140">指定儲存佇列 (SAS) 標記的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="edb3c-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="edb3c-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edb3c-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="edb3c-142">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="edb3c-142">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="edb3c-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="edb3c-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="edb3c-144">指定儲存佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="edb3c-144">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="edb3c-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="edb3c-145">-ErrorActionURI</span></span>
<span data-ttu-id="edb3c-146">指定錯誤作業動作的 URI。</span><span class="sxs-lookup"><span data-stu-id="edb3c-146">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="edb3c-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="edb3c-147">-ExecutionCount</span></span>
<span data-ttu-id="edb3c-148">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="edb3c-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="edb3c-149">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="edb3c-149">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="edb3c-150">頻率</span><span class="sxs-lookup"><span data-stu-id="edb3c-150">-Frequency</span></span>
<span data-ttu-id="edb3c-151">指定此排程作業的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="edb3c-151">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="edb3c-152">間隔</span><span class="sxs-lookup"><span data-stu-id="edb3c-152">-Interval</span></span>
<span data-ttu-id="edb3c-153">使用 *frequency* 參數指定的頻率來指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="edb3c-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="edb3c-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="edb3c-154">-JobCollectionName</span></span>
<span data-ttu-id="edb3c-155">指定要包含排程作業之集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="edb3c-155">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="edb3c-156">-JobName</span><span class="sxs-lookup"><span data-stu-id="edb3c-156">-JobName</span></span>
<span data-ttu-id="edb3c-157">指定排程作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="edb3c-157">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="edb3c-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="edb3c-158">-JobState</span></span>
<span data-ttu-id="edb3c-159">指定排程作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="edb3c-159">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="edb3c-160">-位置</span><span class="sxs-lookup"><span data-stu-id="edb3c-160">-Location</span></span>
<span data-ttu-id="edb3c-161">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="edb3c-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="edb3c-162">有效值為：</span><span class="sxs-lookup"><span data-stu-id="edb3c-162">Valid values are:</span></span> 

- <span data-ttu-id="edb3c-163">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="edb3c-163">Anywhere Asia</span></span>
- <span data-ttu-id="edb3c-164">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="edb3c-164">Anywhere Europe</span></span>
- <span data-ttu-id="edb3c-165">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="edb3c-165">Anywhere US</span></span>
- <span data-ttu-id="edb3c-166">東亞</span><span class="sxs-lookup"><span data-stu-id="edb3c-166">East Asia</span></span>
- <span data-ttu-id="edb3c-167">東美國</span><span class="sxs-lookup"><span data-stu-id="edb3c-167">East US</span></span>
- <span data-ttu-id="edb3c-168">美國中北部</span><span class="sxs-lookup"><span data-stu-id="edb3c-168">North Central US</span></span>
- <span data-ttu-id="edb3c-169">北歐</span><span class="sxs-lookup"><span data-stu-id="edb3c-169">North Europe</span></span>
- <span data-ttu-id="edb3c-170">美國中南部</span><span class="sxs-lookup"><span data-stu-id="edb3c-170">South Central US</span></span>
- <span data-ttu-id="edb3c-171">東南亞</span><span class="sxs-lookup"><span data-stu-id="edb3c-171">Southeast Asia</span></span>
- <span data-ttu-id="edb3c-172">西歐</span><span class="sxs-lookup"><span data-stu-id="edb3c-172">West Europe</span></span>
- <span data-ttu-id="edb3c-173">美國西部</span><span class="sxs-lookup"><span data-stu-id="edb3c-173">West US</span></span>

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

### <span data-ttu-id="edb3c-174">-設定檔</span><span class="sxs-lookup"><span data-stu-id="edb3c-174">-Profile</span></span>
<span data-ttu-id="edb3c-175">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="edb3c-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="edb3c-176">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="edb3c-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="edb3c-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="edb3c-177">-SASToken</span></span>
<span data-ttu-id="edb3c-178">指定儲存佇列的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="edb3c-178">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="edb3c-179">-StartTime</span><span class="sxs-lookup"><span data-stu-id="edb3c-179">-StartTime</span></span>
<span data-ttu-id="edb3c-180">指定要啟動作業的時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="edb3c-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="edb3c-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="edb3c-181">-StorageQueueAccount</span></span>
<span data-ttu-id="edb3c-182">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="edb3c-182">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="edb3c-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="edb3c-183">-StorageQueueMessage</span></span>
<span data-ttu-id="edb3c-184">指定 [儲存作業] 的 [佇列] 訊息。</span><span class="sxs-lookup"><span data-stu-id="edb3c-184">Specifies the queue message for Storage job.</span></span>

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

### <span data-ttu-id="edb3c-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="edb3c-185">-StorageQueueName</span></span>
<span data-ttu-id="edb3c-186">指定儲存佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="edb3c-186">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="edb3c-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb3c-187">CommonParameters</span></span>
<span data-ttu-id="edb3c-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edb3c-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb3c-189">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="edb3c-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb3c-190">輸入</span><span class="sxs-lookup"><span data-stu-id="edb3c-190">INPUTS</span></span>

## <span data-ttu-id="edb3c-191">輸出</span><span class="sxs-lookup"><span data-stu-id="edb3c-191">OUTPUTS</span></span>

## <span data-ttu-id="edb3c-192">筆記</span><span class="sxs-lookup"><span data-stu-id="edb3c-192">NOTES</span></span>

## <span data-ttu-id="edb3c-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="edb3c-193">RELATED LINKS</span></span>

[<span data-ttu-id="edb3c-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="edb3c-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)



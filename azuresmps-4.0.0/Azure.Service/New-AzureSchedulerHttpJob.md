---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967350"
---
# <span data-ttu-id="85972-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="85972-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="85972-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85972-102">SYNOPSIS</span></span>
<span data-ttu-id="85972-103">建立具有 HTTP 動作的排程作業。</span><span class="sxs-lookup"><span data-stu-id="85972-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="85972-104">句法</span><span class="sxs-lookup"><span data-stu-id="85972-104">SYNTAX</span></span>

### <span data-ttu-id="85972-105">必填</span><span class="sxs-lookup"><span data-stu-id="85972-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="85972-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="85972-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="85972-107">週期性</span><span class="sxs-lookup"><span data-stu-id="85972-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="85972-108">Authentication</span><span class="sxs-lookup"><span data-stu-id="85972-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="85972-109">說明</span><span class="sxs-lookup"><span data-stu-id="85972-109">DESCRIPTION</span></span>
<span data-ttu-id="85972-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85972-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="85972-111">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="85972-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="85972-112">**新的-AzureSchedulerHttpJob** Cmdlet 會建立一個具有 HTTP 動作的排程作業。</span><span class="sxs-lookup"><span data-stu-id="85972-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="85972-113">示例</span><span class="sxs-lookup"><span data-stu-id="85972-113">EXAMPLES</span></span>

### <span data-ttu-id="85972-114">範例1：建立 HTTP 作業</span><span class="sxs-lookup"><span data-stu-id="85972-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="85972-115">這個命令會在名為 JobCollection01 的作業集合中建立排程程式 HTTP 作業。</span><span class="sxs-lookup"><span data-stu-id="85972-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="85972-116">此命令會指定 URI 並指定 [取得為] 方法。</span><span class="sxs-lookup"><span data-stu-id="85972-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="85972-117">範例2：建立特定執行計數的 HTTP 作業</span><span class="sxs-lookup"><span data-stu-id="85972-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="85972-118">這個命令會在名為 JobCollection01 的作業集合中建立排程程式 HTTP 作業。</span><span class="sxs-lookup"><span data-stu-id="85972-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="85972-119">此命令會指定 URI 並指定 [取得為] 方法。</span><span class="sxs-lookup"><span data-stu-id="85972-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="85972-120">這個命令會導致作業執行20次。</span><span class="sxs-lookup"><span data-stu-id="85972-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="85972-121">參數</span><span class="sxs-lookup"><span data-stu-id="85972-121">PARAMETERS</span></span>

### <span data-ttu-id="85972-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="85972-122">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="85972-123">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="85972-124">-EndTime</span></span>
<span data-ttu-id="85972-125">指定時間（作為 **DateTime** 物件），以讓排程停止啟動作業。</span><span class="sxs-lookup"><span data-stu-id="85972-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="85972-126">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85972-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="85972-127">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="85972-127">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="85972-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="85972-129">指定 [標題] 做為 hashtable。</span><span class="sxs-lookup"><span data-stu-id="85972-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="85972-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="85972-130">-ErrorActionMethod</span></span>
<span data-ttu-id="85972-131">指定 HTTP 和 HTTPS 動作類型的方法。</span><span class="sxs-lookup"><span data-stu-id="85972-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="85972-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="85972-132">Valid values are:</span></span> 

- <span data-ttu-id="85972-133">獲取</span><span class="sxs-lookup"><span data-stu-id="85972-133">GET</span></span>
- <span data-ttu-id="85972-134">將</span><span class="sxs-lookup"><span data-stu-id="85972-134">PUT</span></span>
- <span data-ttu-id="85972-135">發佈</span><span class="sxs-lookup"><span data-stu-id="85972-135">POST</span></span>
- <span data-ttu-id="85972-136">螺絲刀</span><span class="sxs-lookup"><span data-stu-id="85972-136">HEAD</span></span>
- <span data-ttu-id="85972-137">DELETE</span><span class="sxs-lookup"><span data-stu-id="85972-137">DELETE</span></span>

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

### <span data-ttu-id="85972-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="85972-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="85972-139">指定儲存作業作業動作的主體。</span><span class="sxs-lookup"><span data-stu-id="85972-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="85972-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="85972-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="85972-141">指定放入和張貼作業動作的本文。</span><span class="sxs-lookup"><span data-stu-id="85972-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="85972-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="85972-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="85972-143">指定儲存佇列 (SAS) 標記的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="85972-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="85972-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85972-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="85972-145">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="85972-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="85972-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="85972-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="85972-147">指定儲存佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="85972-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="85972-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="85972-148">-ErrorActionURI</span></span>
<span data-ttu-id="85972-149">指定錯誤作業動作的 URI。</span><span class="sxs-lookup"><span data-stu-id="85972-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="85972-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="85972-150">-ExecutionCount</span></span>
<span data-ttu-id="85972-151">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="85972-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="85972-152">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="85972-152">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-153">頻率</span><span class="sxs-lookup"><span data-stu-id="85972-153">-Frequency</span></span>
<span data-ttu-id="85972-154">指定此排程作業的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="85972-154">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-155">-標題</span><span class="sxs-lookup"><span data-stu-id="85972-155">-Headers</span></span>
<span data-ttu-id="85972-156">指定要作為 hashtable 的標頭。</span><span class="sxs-lookup"><span data-stu-id="85972-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="85972-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="85972-157">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-158">間隔</span><span class="sxs-lookup"><span data-stu-id="85972-158">-Interval</span></span>
<span data-ttu-id="85972-159">使用 *frequency* 參數指定的頻率來指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="85972-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="85972-160">-JobCollectionName</span></span>
<span data-ttu-id="85972-161">指定要包含排程作業之集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="85972-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="85972-162">-JobName</span><span class="sxs-lookup"><span data-stu-id="85972-162">-JobName</span></span>
<span data-ttu-id="85972-163">指定排程作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="85972-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="85972-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="85972-164">-JobState</span></span>
<span data-ttu-id="85972-165">指定排程作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="85972-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="85972-166">-位置</span><span class="sxs-lookup"><span data-stu-id="85972-166">-Location</span></span>
<span data-ttu-id="85972-167">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="85972-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="85972-168">有效值為：</span><span class="sxs-lookup"><span data-stu-id="85972-168">Valid values are:</span></span> 

- <span data-ttu-id="85972-169">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="85972-169">Anywhere Asia</span></span>
- <span data-ttu-id="85972-170">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="85972-170">Anywhere Europe</span></span>
- <span data-ttu-id="85972-171">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="85972-171">Anywhere US</span></span>
- <span data-ttu-id="85972-172">東亞</span><span class="sxs-lookup"><span data-stu-id="85972-172">East Asia</span></span>
- <span data-ttu-id="85972-173">東美國</span><span class="sxs-lookup"><span data-stu-id="85972-173">East US</span></span>
- <span data-ttu-id="85972-174">美國中北部</span><span class="sxs-lookup"><span data-stu-id="85972-174">North Central US</span></span>
- <span data-ttu-id="85972-175">北歐</span><span class="sxs-lookup"><span data-stu-id="85972-175">North Europe</span></span>
- <span data-ttu-id="85972-176">美國中南部</span><span class="sxs-lookup"><span data-stu-id="85972-176">South Central US</span></span>
- <span data-ttu-id="85972-177">東南亞</span><span class="sxs-lookup"><span data-stu-id="85972-177">Southeast Asia</span></span>
- <span data-ttu-id="85972-178">西歐</span><span class="sxs-lookup"><span data-stu-id="85972-178">West Europe</span></span>
- <span data-ttu-id="85972-179">美國西部</span><span class="sxs-lookup"><span data-stu-id="85972-179">West US</span></span>

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

### <span data-ttu-id="85972-180">-方法</span><span class="sxs-lookup"><span data-stu-id="85972-180">-Method</span></span>
<span data-ttu-id="85972-181">指定 HTTP 和 HTTPS 動作類型的方法。</span><span class="sxs-lookup"><span data-stu-id="85972-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="85972-182">有效值為：</span><span class="sxs-lookup"><span data-stu-id="85972-182">Valid values are:</span></span> 

- <span data-ttu-id="85972-183">獲取</span><span class="sxs-lookup"><span data-stu-id="85972-183">GET</span></span>
- <span data-ttu-id="85972-184">將</span><span class="sxs-lookup"><span data-stu-id="85972-184">PUT</span></span>
- <span data-ttu-id="85972-185">發佈</span><span class="sxs-lookup"><span data-stu-id="85972-185">POST</span></span>
- <span data-ttu-id="85972-186">螺絲刀</span><span class="sxs-lookup"><span data-stu-id="85972-186">HEAD</span></span>
- <span data-ttu-id="85972-187">DELETE</span><span class="sxs-lookup"><span data-stu-id="85972-187">DELETE</span></span>

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

### <span data-ttu-id="85972-188">-設定檔</span><span class="sxs-lookup"><span data-stu-id="85972-188">-Profile</span></span>
<span data-ttu-id="85972-189">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="85972-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="85972-190">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="85972-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85972-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="85972-191">-RequestBody</span></span>
<span data-ttu-id="85972-192">指定放入和張貼作業動作的本文。</span><span class="sxs-lookup"><span data-stu-id="85972-192">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-193">-StartTime</span><span class="sxs-lookup"><span data-stu-id="85972-193">-StartTime</span></span>
<span data-ttu-id="85972-194">指定要啟動作業的時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="85972-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="85972-195">-URI</span><span class="sxs-lookup"><span data-stu-id="85972-195">-URI</span></span>
<span data-ttu-id="85972-196">指定作業動作的 URI。</span><span class="sxs-lookup"><span data-stu-id="85972-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85972-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85972-197">CommonParameters</span></span>
<span data-ttu-id="85972-198">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85972-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85972-199">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85972-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85972-200">輸入</span><span class="sxs-lookup"><span data-stu-id="85972-200">INPUTS</span></span>

## <span data-ttu-id="85972-201">輸出</span><span class="sxs-lookup"><span data-stu-id="85972-201">OUTPUTS</span></span>

## <span data-ttu-id="85972-202">筆記</span><span class="sxs-lookup"><span data-stu-id="85972-202">NOTES</span></span>

## <span data-ttu-id="85972-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="85972-203">RELATED LINKS</span></span>

[<span data-ttu-id="85972-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="85972-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)



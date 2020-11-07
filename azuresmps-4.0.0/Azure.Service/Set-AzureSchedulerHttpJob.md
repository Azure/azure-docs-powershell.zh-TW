---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967245"
---
# <span data-ttu-id="b4e37-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="b4e37-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="b4e37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4e37-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e37-103">更新具有 HTTP 動作的排程作業。</span><span class="sxs-lookup"><span data-stu-id="b4e37-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="b4e37-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4e37-104">SYNTAX</span></span>

### <span data-ttu-id="b4e37-105">必填</span><span class="sxs-lookup"><span data-stu-id="b4e37-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e37-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="b4e37-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b4e37-107">週期性</span><span class="sxs-lookup"><span data-stu-id="b4e37-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b4e37-108">Authentication</span><span class="sxs-lookup"><span data-stu-id="b4e37-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b4e37-109">說明</span><span class="sxs-lookup"><span data-stu-id="b4e37-109">DESCRIPTION</span></span>
<span data-ttu-id="b4e37-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4e37-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b4e37-111">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="b4e37-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b4e37-112">**AzureSchedulerHttpJob** Cmdlet 會更新具有 HTTP 動作的排程作業。</span><span class="sxs-lookup"><span data-stu-id="b4e37-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="b4e37-113">示例</span><span class="sxs-lookup"><span data-stu-id="b4e37-113">EXAMPLES</span></span>

### <span data-ttu-id="b4e37-114">範例1：將作業狀態變更為 [已停用]</span><span class="sxs-lookup"><span data-stu-id="b4e37-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="b4e37-115">這個命令會將名為 Job01 的作業狀態變更為 [已停用]。</span><span class="sxs-lookup"><span data-stu-id="b4e37-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="b4e37-116">該作業是指定位置中名為 JobColleciton01 的作業集合的一部分。</span><span class="sxs-lookup"><span data-stu-id="b4e37-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="b4e37-117">範例2：更新作業的 URI</span><span class="sxs-lookup"><span data-stu-id="b4e37-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="b4e37-118">這個命令會將名為 Job01 的工作 URI 更新為 http://www.contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="b4e37-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="b4e37-119">參數</span><span class="sxs-lookup"><span data-stu-id="b4e37-119">PARAMETERS</span></span>

### <span data-ttu-id="b4e37-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b4e37-120">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="b4e37-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="b4e37-121">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="b4e37-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b4e37-122">-EndTime</span></span>
<span data-ttu-id="b4e37-123">指定時間（作為 **DateTime** 物件），以讓排程停止啟動作業。</span><span class="sxs-lookup"><span data-stu-id="b4e37-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="b4e37-124">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4e37-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="b4e37-125">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="b4e37-125">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="b4e37-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="b4e37-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="b4e37-127">指定 [標題] 做為 hashtable。</span><span class="sxs-lookup"><span data-stu-id="b4e37-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="b4e37-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="b4e37-128">-ErrorActionMethod</span></span>
<span data-ttu-id="b4e37-129">指定 HTTP 和 HTTPS 動作類型的方法。</span><span class="sxs-lookup"><span data-stu-id="b4e37-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="b4e37-130">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b4e37-130">Valid values are:</span></span> 

- <span data-ttu-id="b4e37-131">獲取</span><span class="sxs-lookup"><span data-stu-id="b4e37-131">GET</span></span>
- <span data-ttu-id="b4e37-132">將</span><span class="sxs-lookup"><span data-stu-id="b4e37-132">PUT</span></span>
- <span data-ttu-id="b4e37-133">發佈</span><span class="sxs-lookup"><span data-stu-id="b4e37-133">POST</span></span>
- <span data-ttu-id="b4e37-134">螺絲刀</span><span class="sxs-lookup"><span data-stu-id="b4e37-134">HEAD</span></span>
- <span data-ttu-id="b4e37-135">DELETE</span><span class="sxs-lookup"><span data-stu-id="b4e37-135">DELETE</span></span>

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

### <span data-ttu-id="b4e37-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="b4e37-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="b4e37-137">指定儲存作業作業動作的主體。</span><span class="sxs-lookup"><span data-stu-id="b4e37-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="b4e37-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="b4e37-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="b4e37-139">指定放入和張貼作業動作的本文。</span><span class="sxs-lookup"><span data-stu-id="b4e37-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="b4e37-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="b4e37-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="b4e37-141">指定儲存佇列 (SAS) 標記的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="b4e37-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="b4e37-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4e37-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="b4e37-143">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e37-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="b4e37-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b4e37-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="b4e37-145">指定儲存佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e37-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="b4e37-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="b4e37-146">-ErrorActionURI</span></span>
<span data-ttu-id="b4e37-147">指定錯誤作業動作的 URI。</span><span class="sxs-lookup"><span data-stu-id="b4e37-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="b4e37-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="b4e37-148">-ExecutionCount</span></span>
<span data-ttu-id="b4e37-149">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="b4e37-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="b4e37-150">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="b4e37-150">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="b4e37-151">頻率</span><span class="sxs-lookup"><span data-stu-id="b4e37-151">-Frequency</span></span>
<span data-ttu-id="b4e37-152">指定此排程作業的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="b4e37-152">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="b4e37-153">-標題</span><span class="sxs-lookup"><span data-stu-id="b4e37-153">-Headers</span></span>
<span data-ttu-id="b4e37-154">將標頭指定為雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b4e37-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="b4e37-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b4e37-155">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="b4e37-156">間隔</span><span class="sxs-lookup"><span data-stu-id="b4e37-156">-Interval</span></span>
<span data-ttu-id="b4e37-157">使用 *frequency* 參數指定的頻率來指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="b4e37-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="b4e37-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b4e37-158">-JobCollectionName</span></span>
<span data-ttu-id="b4e37-159">指定包含要修改之排程作業之集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e37-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="b4e37-160">-JobName</span><span class="sxs-lookup"><span data-stu-id="b4e37-160">-JobName</span></span>
<span data-ttu-id="b4e37-161">指定要修改的排程作業名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e37-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="b4e37-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="b4e37-162">-JobState</span></span>
<span data-ttu-id="b4e37-163">指定排程作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b4e37-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="b4e37-164">-位置</span><span class="sxs-lookup"><span data-stu-id="b4e37-164">-Location</span></span>
<span data-ttu-id="b4e37-165">指定託管雲端服務的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e37-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="b4e37-166">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b4e37-166">Valid values are:</span></span> 

- <span data-ttu-id="b4e37-167">亞洲任何地方</span><span class="sxs-lookup"><span data-stu-id="b4e37-167">Anywhere Asia</span></span>
- <span data-ttu-id="b4e37-168">歐洲任何地方</span><span class="sxs-lookup"><span data-stu-id="b4e37-168">Anywhere Europe</span></span>
- <span data-ttu-id="b4e37-169">美國任何地方</span><span class="sxs-lookup"><span data-stu-id="b4e37-169">Anywhere US</span></span>
- <span data-ttu-id="b4e37-170">東亞</span><span class="sxs-lookup"><span data-stu-id="b4e37-170">East Asia</span></span>
- <span data-ttu-id="b4e37-171">東美國</span><span class="sxs-lookup"><span data-stu-id="b4e37-171">East US</span></span>
- <span data-ttu-id="b4e37-172">美國中北部</span><span class="sxs-lookup"><span data-stu-id="b4e37-172">North Central US</span></span>
- <span data-ttu-id="b4e37-173">北歐</span><span class="sxs-lookup"><span data-stu-id="b4e37-173">North Europe</span></span>
- <span data-ttu-id="b4e37-174">美國中南部</span><span class="sxs-lookup"><span data-stu-id="b4e37-174">South Central US</span></span>
- <span data-ttu-id="b4e37-175">東南亞</span><span class="sxs-lookup"><span data-stu-id="b4e37-175">Southeast Asia</span></span>
- <span data-ttu-id="b4e37-176">西歐</span><span class="sxs-lookup"><span data-stu-id="b4e37-176">West Europe</span></span>
- <span data-ttu-id="b4e37-177">美國西部</span><span class="sxs-lookup"><span data-stu-id="b4e37-177">West US</span></span>

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

### <span data-ttu-id="b4e37-178">-方法</span><span class="sxs-lookup"><span data-stu-id="b4e37-178">-Method</span></span>
<span data-ttu-id="b4e37-179">指定 HTTP 和 HTTPS 動作類型的方法。</span><span class="sxs-lookup"><span data-stu-id="b4e37-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="b4e37-180">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b4e37-180">Valid values are:</span></span> 

- <span data-ttu-id="b4e37-181">獲取</span><span class="sxs-lookup"><span data-stu-id="b4e37-181">GET</span></span>
- <span data-ttu-id="b4e37-182">將</span><span class="sxs-lookup"><span data-stu-id="b4e37-182">PUT</span></span>
- <span data-ttu-id="b4e37-183">發佈</span><span class="sxs-lookup"><span data-stu-id="b4e37-183">POST</span></span>
- <span data-ttu-id="b4e37-184">螺絲刀</span><span class="sxs-lookup"><span data-stu-id="b4e37-184">HEAD</span></span>
- <span data-ttu-id="b4e37-185">DELETE</span><span class="sxs-lookup"><span data-stu-id="b4e37-185">DELETE</span></span>

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

### <span data-ttu-id="b4e37-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4e37-186">-PassThru</span></span>
<span data-ttu-id="b4e37-187">表示此 Cmdlet 會傳回代表其操作專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b4e37-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="b4e37-188">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b4e37-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4e37-189">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b4e37-189">-Profile</span></span>
<span data-ttu-id="b4e37-190">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b4e37-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4e37-191">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b4e37-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4e37-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="b4e37-192">-RequestBody</span></span>
<span data-ttu-id="b4e37-193">指定放入和張貼作業動作的本文。</span><span class="sxs-lookup"><span data-stu-id="b4e37-193">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="b4e37-194">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b4e37-194">-StartTime</span></span>
<span data-ttu-id="b4e37-195">指定要啟動作業的時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="b4e37-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="b4e37-196">-URI</span><span class="sxs-lookup"><span data-stu-id="b4e37-196">-URI</span></span>
<span data-ttu-id="b4e37-197">指定作業動作的 URI。</span><span class="sxs-lookup"><span data-stu-id="b4e37-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="b4e37-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e37-198">CommonParameters</span></span>
<span data-ttu-id="b4e37-199">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4e37-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e37-200">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b4e37-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e37-201">輸入</span><span class="sxs-lookup"><span data-stu-id="b4e37-201">INPUTS</span></span>

## <span data-ttu-id="b4e37-202">輸出</span><span class="sxs-lookup"><span data-stu-id="b4e37-202">OUTPUTS</span></span>

## <span data-ttu-id="b4e37-203">筆記</span><span class="sxs-lookup"><span data-stu-id="b4e37-203">NOTES</span></span>

## <span data-ttu-id="b4e37-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4e37-204">RELATED LINKS</span></span>

[<span data-ttu-id="b4e37-205">新-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="b4e37-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)



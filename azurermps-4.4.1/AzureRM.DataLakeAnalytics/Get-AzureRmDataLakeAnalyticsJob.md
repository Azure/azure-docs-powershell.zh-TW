---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456728"
---
# <span data-ttu-id="e3f3b-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3f3b-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="e3f3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f3b-103">取得資料 Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3f3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3f3b-104">SYNTAX</span></span>

### <span data-ttu-id="e3f3b-105">[資源群組] 和 [帳戶] 中的 [全部] (預設) </span><span class="sxs-lookup"><span data-stu-id="e3f3b-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3f3b-106">特定 JobInformation</span><span class="sxs-lookup"><span data-stu-id="e3f3b-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3f3b-107">說明</span><span class="sxs-lookup"><span data-stu-id="e3f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="e3f3b-108">**AzureRmDataLakeAnalyticsJob** Cmdlet 會取得 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="e3f3b-109">如果您沒有指定作業，此 Cmdlet 會取得所有作業。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="e3f3b-110">示例</span><span class="sxs-lookup"><span data-stu-id="e3f3b-110">EXAMPLES</span></span>

### <span data-ttu-id="e3f3b-111">範例1：取得指定的工作</span><span class="sxs-lookup"><span data-stu-id="e3f3b-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="e3f3b-112">這個命令會取得具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="e3f3b-113">範例2：取得上周提交的工作</span><span class="sxs-lookup"><span data-stu-id="e3f3b-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="e3f3b-114">此命令會取得上周提交的工作。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="e3f3b-115">參數</span><span class="sxs-lookup"><span data-stu-id="e3f3b-115">PARAMETERS</span></span>

### <span data-ttu-id="e3f3b-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e3f3b-116">-Account</span></span>
<span data-ttu-id="e3f3b-117">指定資料 Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-118">-包含</span><span class="sxs-lookup"><span data-stu-id="e3f3b-118">-Include</span></span>
<span data-ttu-id="e3f3b-119">指定選項，以指示要取得工作的其他資訊類型。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="e3f3b-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e3f3b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3f3b-121">所有</span><span class="sxs-lookup"><span data-stu-id="e3f3b-121">None</span></span>
- <span data-ttu-id="e3f3b-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="e3f3b-122">DebugInfo</span></span>
- <span data-ttu-id="e3f3b-123">Statistics</span><span class="sxs-lookup"><span data-stu-id="e3f3b-123">Statistics</span></span>
- <span data-ttu-id="e3f3b-124">同時</span><span class="sxs-lookup"><span data-stu-id="e3f3b-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-125">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="e3f3b-125">-JobId</span></span>
<span data-ttu-id="e3f3b-126">指定要取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3f3b-127">-Name</span></span>
<span data-ttu-id="e3f3b-128">指定要用來篩選工作清單結果的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="e3f3b-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e3f3b-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3f3b-130">所有</span><span class="sxs-lookup"><span data-stu-id="e3f3b-130">None</span></span>
- <span data-ttu-id="e3f3b-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="e3f3b-131">DebugInfo</span></span>
- <span data-ttu-id="e3f3b-132">Statistics</span><span class="sxs-lookup"><span data-stu-id="e3f3b-132">Statistics</span></span>
- <span data-ttu-id="e3f3b-133">同時</span><span class="sxs-lookup"><span data-stu-id="e3f3b-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-134">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="e3f3b-134">-PipelineId</span></span>
<span data-ttu-id="e3f3b-135">一個選用的識別碼，只指示應傳回指定管線的工作部分。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-136">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="e3f3b-136">-RecurrenceId</span></span>
<span data-ttu-id="e3f3b-137">一個選用的識別碼，只指示應該傳回指定的定期作業部分。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-138">-結果</span><span class="sxs-lookup"><span data-stu-id="e3f3b-138">-Result</span></span>
<span data-ttu-id="e3f3b-139">指定作業結果的結果篩選器。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="e3f3b-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e3f3b-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3f3b-141">所有</span><span class="sxs-lookup"><span data-stu-id="e3f3b-141">None</span></span>
- <span data-ttu-id="e3f3b-142">取消</span><span class="sxs-lookup"><span data-stu-id="e3f3b-142">Cancelled</span></span>
- <span data-ttu-id="e3f3b-143">成功</span><span class="sxs-lookup"><span data-stu-id="e3f3b-143">Failed</span></span>
- <span data-ttu-id="e3f3b-144">成功</span><span class="sxs-lookup"><span data-stu-id="e3f3b-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-145">-State</span><span class="sxs-lookup"><span data-stu-id="e3f3b-145">-State</span></span>
<span data-ttu-id="e3f3b-146">指定作業結果的狀態篩選器。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="e3f3b-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e3f3b-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3f3b-148">認可</span><span class="sxs-lookup"><span data-stu-id="e3f3b-148">Accepted</span></span>
- <span data-ttu-id="e3f3b-149">新增功能</span><span class="sxs-lookup"><span data-stu-id="e3f3b-149">New</span></span>
- <span data-ttu-id="e3f3b-150">編譯</span><span class="sxs-lookup"><span data-stu-id="e3f3b-150">Compiling</span></span>
- <span data-ttu-id="e3f3b-151">排程</span><span class="sxs-lookup"><span data-stu-id="e3f3b-151">Scheduling</span></span>
- <span data-ttu-id="e3f3b-152">排</span><span class="sxs-lookup"><span data-stu-id="e3f3b-152">Queued</span></span>
- <span data-ttu-id="e3f3b-153">入門</span><span class="sxs-lookup"><span data-stu-id="e3f3b-153">Starting</span></span>
- <span data-ttu-id="e3f3b-154">處於</span><span class="sxs-lookup"><span data-stu-id="e3f3b-154">Paused</span></span>
- <span data-ttu-id="e3f3b-155">進行</span><span class="sxs-lookup"><span data-stu-id="e3f3b-155">Running</span></span>
- <span data-ttu-id="e3f3b-156">截至</span><span class="sxs-lookup"><span data-stu-id="e3f3b-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="e3f3b-157">-SubmittedAfter</span></span>
<span data-ttu-id="e3f3b-158">指定日期篩選。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-158">Specifies a date filter.</span></span>
<span data-ttu-id="e3f3b-159">使用此參數可將作業清單結果篩選為在指定日期之後提交的作業。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-160">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="e3f3b-160">-SubmittedBefore</span></span>
<span data-ttu-id="e3f3b-161">指定日期篩選。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-161">Specifies a date filter.</span></span>
<span data-ttu-id="e3f3b-162">使用此參數可將作業清單結果篩選為在指定日期前提交的作業。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-163">-提交者</span><span class="sxs-lookup"><span data-stu-id="e3f3b-163">-Submitter</span></span>
<span data-ttu-id="e3f3b-164">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="e3f3b-165">使用此參數可將作業清單結果篩選為指定使用者所提交的工作。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-166">-上方</span><span class="sxs-lookup"><span data-stu-id="e3f3b-166">-Top</span></span>
<span data-ttu-id="e3f3b-167">指明要傳回的作業數的選用值。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="e3f3b-168">預設值為500</span><span class="sxs-lookup"><span data-stu-id="e3f3b-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f3b-169">-DefaultProfile</span></span>
<span data-ttu-id="e3f3b-170">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f3b-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f3b-171">CommonParameters</span></span>
<span data-ttu-id="e3f3b-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f3b-173">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f3b-174">輸入</span><span class="sxs-lookup"><span data-stu-id="e3f3b-174">INPUTS</span></span>

### <span data-ttu-id="e3f3b-175">Guid</span><span class="sxs-lookup"><span data-stu-id="e3f3b-175">Guid</span></span>
<span data-ttu-id="e3f3b-176">形參 "JobId" 接受管線中 "Guid" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e3f3b-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="e3f3b-177">輸出</span><span class="sxs-lookup"><span data-stu-id="e3f3b-177">OUTPUTS</span></span>

### <span data-ttu-id="e3f3b-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="e3f3b-178">JobInformation</span></span>
<span data-ttu-id="e3f3b-179">指定的工作資訊詳細資料</span><span class="sxs-lookup"><span data-stu-id="e3f3b-179">The specified job information details</span></span>

### <span data-ttu-id="e3f3b-180">清單<JobInformation></span><span class="sxs-lookup"><span data-stu-id="e3f3b-180">List<JobInformation></span></span>
<span data-ttu-id="e3f3b-181">指定資料 Lake Analytics 帳戶中的作業清單。</span><span class="sxs-lookup"><span data-stu-id="e3f3b-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="e3f3b-182">筆記</span><span class="sxs-lookup"><span data-stu-id="e3f3b-182">NOTES</span></span>

## <span data-ttu-id="e3f3b-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3f3b-183">RELATED LINKS</span></span>

[<span data-ttu-id="e3f3b-184">停止 AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3f3b-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="e3f3b-185">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3f3b-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="e3f3b-186">稍候-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3f3b-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)



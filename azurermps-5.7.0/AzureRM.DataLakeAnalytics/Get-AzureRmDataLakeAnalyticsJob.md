---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444556"
---
# <span data-ttu-id="a60b2-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a60b2-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="a60b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a60b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a60b2-103">取得資料 Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="a60b2-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a60b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a60b2-104">SYNTAX</span></span>

### <span data-ttu-id="a60b2-105">GetAllInResourceGroupAndAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="a60b2-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a60b2-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="a60b2-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a60b2-107">說明</span><span class="sxs-lookup"><span data-stu-id="a60b2-107">DESCRIPTION</span></span>
<span data-ttu-id="a60b2-108">**AzureRmDataLakeAnalyticsJob** Cmdlet 會取得 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="a60b2-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="a60b2-109">如果您沒有指定作業，此 Cmdlet 會取得所有作業。</span><span class="sxs-lookup"><span data-stu-id="a60b2-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="a60b2-110">示例</span><span class="sxs-lookup"><span data-stu-id="a60b2-110">EXAMPLES</span></span>

### <span data-ttu-id="a60b2-111">範例1：取得指定的工作</span><span class="sxs-lookup"><span data-stu-id="a60b2-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="a60b2-112">這個命令會取得具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="a60b2-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="a60b2-113">範例2：取得上周提交的工作</span><span class="sxs-lookup"><span data-stu-id="a60b2-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="a60b2-114">此命令會取得上周提交的工作。</span><span class="sxs-lookup"><span data-stu-id="a60b2-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="a60b2-115">參數</span><span class="sxs-lookup"><span data-stu-id="a60b2-115">PARAMETERS</span></span>

### <span data-ttu-id="a60b2-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a60b2-116">-Account</span></span>
<span data-ttu-id="a60b2-117">指定資料 Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a60b2-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60b2-118">-DefaultProfile</span></span>
<span data-ttu-id="a60b2-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a60b2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-120">-包含</span><span class="sxs-lookup"><span data-stu-id="a60b2-120">-Include</span></span>
<span data-ttu-id="a60b2-121">指定選項，以指示要取得工作的其他資訊類型。</span><span class="sxs-lookup"><span data-stu-id="a60b2-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="a60b2-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a60b2-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a60b2-123">所有</span><span class="sxs-lookup"><span data-stu-id="a60b2-123">None</span></span>
- <span data-ttu-id="a60b2-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="a60b2-124">DebugInfo</span></span>
- <span data-ttu-id="a60b2-125">Statistics</span><span class="sxs-lookup"><span data-stu-id="a60b2-125">Statistics</span></span>
- <span data-ttu-id="a60b2-126">同時</span><span class="sxs-lookup"><span data-stu-id="a60b2-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-127">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="a60b2-127">-JobId</span></span>
<span data-ttu-id="a60b2-128">指定要取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="a60b2-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="a60b2-129">-Name</span></span>
<span data-ttu-id="a60b2-130">指定要用來篩選工作清單結果的名稱。</span><span class="sxs-lookup"><span data-stu-id="a60b2-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="a60b2-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a60b2-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a60b2-132">所有</span><span class="sxs-lookup"><span data-stu-id="a60b2-132">None</span></span>
- <span data-ttu-id="a60b2-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="a60b2-133">DebugInfo</span></span>
- <span data-ttu-id="a60b2-134">Statistics</span><span class="sxs-lookup"><span data-stu-id="a60b2-134">Statistics</span></span>
- <span data-ttu-id="a60b2-135">同時</span><span class="sxs-lookup"><span data-stu-id="a60b2-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="a60b2-136">-PipelineId</span></span>
<span data-ttu-id="a60b2-137">一個選用的識別碼，只指示應傳回指定管線的工作部分。</span><span class="sxs-lookup"><span data-stu-id="a60b2-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="a60b2-138">-RecurrenceId</span></span>
<span data-ttu-id="a60b2-139">一個選用的識別碼，只指示應該傳回指定的定期作業部分。</span><span class="sxs-lookup"><span data-stu-id="a60b2-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-140">-結果</span><span class="sxs-lookup"><span data-stu-id="a60b2-140">-Result</span></span>
<span data-ttu-id="a60b2-141">指定作業結果的結果篩選器。</span><span class="sxs-lookup"><span data-stu-id="a60b2-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="a60b2-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a60b2-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a60b2-143">所有</span><span class="sxs-lookup"><span data-stu-id="a60b2-143">None</span></span>
- <span data-ttu-id="a60b2-144">取消</span><span class="sxs-lookup"><span data-stu-id="a60b2-144">Cancelled</span></span>
- <span data-ttu-id="a60b2-145">成功</span><span class="sxs-lookup"><span data-stu-id="a60b2-145">Failed</span></span>
- <span data-ttu-id="a60b2-146">成功</span><span class="sxs-lookup"><span data-stu-id="a60b2-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-147">-State</span><span class="sxs-lookup"><span data-stu-id="a60b2-147">-State</span></span>
<span data-ttu-id="a60b2-148">指定作業結果的狀態篩選器。</span><span class="sxs-lookup"><span data-stu-id="a60b2-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="a60b2-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a60b2-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a60b2-150">認可</span><span class="sxs-lookup"><span data-stu-id="a60b2-150">Accepted</span></span>
- <span data-ttu-id="a60b2-151">新增功能</span><span class="sxs-lookup"><span data-stu-id="a60b2-151">New</span></span>
- <span data-ttu-id="a60b2-152">編譯</span><span class="sxs-lookup"><span data-stu-id="a60b2-152">Compiling</span></span>
- <span data-ttu-id="a60b2-153">排程</span><span class="sxs-lookup"><span data-stu-id="a60b2-153">Scheduling</span></span>
- <span data-ttu-id="a60b2-154">排</span><span class="sxs-lookup"><span data-stu-id="a60b2-154">Queued</span></span>
- <span data-ttu-id="a60b2-155">入門</span><span class="sxs-lookup"><span data-stu-id="a60b2-155">Starting</span></span>
- <span data-ttu-id="a60b2-156">處於</span><span class="sxs-lookup"><span data-stu-id="a60b2-156">Paused</span></span>
- <span data-ttu-id="a60b2-157">進行</span><span class="sxs-lookup"><span data-stu-id="a60b2-157">Running</span></span>
- <span data-ttu-id="a60b2-158">截至</span><span class="sxs-lookup"><span data-stu-id="a60b2-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="a60b2-159">-SubmittedAfter</span></span>
<span data-ttu-id="a60b2-160">指定日期篩選。</span><span class="sxs-lookup"><span data-stu-id="a60b2-160">Specifies a date filter.</span></span>
<span data-ttu-id="a60b2-161">使用此參數可將作業清單結果篩選為在指定日期之後提交的作業。</span><span class="sxs-lookup"><span data-stu-id="a60b2-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="a60b2-162">-SubmittedBefore</span></span>
<span data-ttu-id="a60b2-163">指定日期篩選。</span><span class="sxs-lookup"><span data-stu-id="a60b2-163">Specifies a date filter.</span></span>
<span data-ttu-id="a60b2-164">使用此參數可將作業清單結果篩選為在指定日期前提交的作業。</span><span class="sxs-lookup"><span data-stu-id="a60b2-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-165">-提交者</span><span class="sxs-lookup"><span data-stu-id="a60b2-165">-Submitter</span></span>
<span data-ttu-id="a60b2-166">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="a60b2-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="a60b2-167">使用此參數可將作業清單結果篩選為指定使用者所提交的工作。</span><span class="sxs-lookup"><span data-stu-id="a60b2-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-168">-上方</span><span class="sxs-lookup"><span data-stu-id="a60b2-168">-Top</span></span>
<span data-ttu-id="a60b2-169">指明要傳回的作業數的選用值。</span><span class="sxs-lookup"><span data-stu-id="a60b2-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="a60b2-170">預設值為500</span><span class="sxs-lookup"><span data-stu-id="a60b2-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60b2-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60b2-171">CommonParameters</span></span>
<span data-ttu-id="a60b2-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a60b2-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60b2-173">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a60b2-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60b2-174">輸入</span><span class="sxs-lookup"><span data-stu-id="a60b2-174">INPUTS</span></span>

### <span data-ttu-id="a60b2-175">Guid</span><span class="sxs-lookup"><span data-stu-id="a60b2-175">Guid</span></span>
<span data-ttu-id="a60b2-176">形參 "JobId" 接受管線中 "Guid" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a60b2-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="a60b2-177">輸出</span><span class="sxs-lookup"><span data-stu-id="a60b2-177">OUTPUTS</span></span>

### <span data-ttu-id="a60b2-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="a60b2-178">JobInformation</span></span>
<span data-ttu-id="a60b2-179">指定的工作資訊詳細資料</span><span class="sxs-lookup"><span data-stu-id="a60b2-179">The specified job information details</span></span>

### <span data-ttu-id="a60b2-180">清單<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="a60b2-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="a60b2-181">指定資料 Lake Analytics 帳戶中的作業清單。</span><span class="sxs-lookup"><span data-stu-id="a60b2-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="a60b2-182">筆記</span><span class="sxs-lookup"><span data-stu-id="a60b2-182">NOTES</span></span>

## <span data-ttu-id="a60b2-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="a60b2-183">RELATED LINKS</span></span>

[<span data-ttu-id="a60b2-184">停止 AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a60b2-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a60b2-185">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a60b2-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a60b2-186">稍候-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a60b2-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)



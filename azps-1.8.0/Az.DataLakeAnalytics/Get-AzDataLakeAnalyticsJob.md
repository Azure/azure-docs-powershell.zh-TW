---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 73a9325ea4f1bc45eaaf2fb81796d526c7b95fea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788050"
---
# <span data-ttu-id="232ca-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="232ca-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="232ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="232ca-102">SYNOPSIS</span></span>
<span data-ttu-id="232ca-103">取得資料 Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="232ca-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="232ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="232ca-104">SYNTAX</span></span>

### <span data-ttu-id="232ca-105">GetAllInResourceGroupAndAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="232ca-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="232ca-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="232ca-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="232ca-107">說明</span><span class="sxs-lookup"><span data-stu-id="232ca-107">DESCRIPTION</span></span>
<span data-ttu-id="232ca-108">**AzDataLakeAnalyticsJob** Cmdlet 會取得 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="232ca-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="232ca-109">如果您沒有指定作業，此 Cmdlet 會取得所有作業。</span><span class="sxs-lookup"><span data-stu-id="232ca-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="232ca-110">示例</span><span class="sxs-lookup"><span data-stu-id="232ca-110">EXAMPLES</span></span>

### <span data-ttu-id="232ca-111">範例1：取得指定的工作</span><span class="sxs-lookup"><span data-stu-id="232ca-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="232ca-112">這個命令會取得具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="232ca-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="232ca-113">範例2：取得上周提交的工作</span><span class="sxs-lookup"><span data-stu-id="232ca-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="232ca-114">此命令會取得上周提交的工作。</span><span class="sxs-lookup"><span data-stu-id="232ca-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="232ca-115">參數</span><span class="sxs-lookup"><span data-stu-id="232ca-115">PARAMETERS</span></span>

### <span data-ttu-id="232ca-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="232ca-116">-Account</span></span>
<span data-ttu-id="232ca-117">指定資料 Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="232ca-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="232ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232ca-118">-DefaultProfile</span></span>
<span data-ttu-id="232ca-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="232ca-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="232ca-120">-包含</span><span class="sxs-lookup"><span data-stu-id="232ca-120">-Include</span></span>
<span data-ttu-id="232ca-121">指定選項，以指示要取得工作的其他資訊類型。</span><span class="sxs-lookup"><span data-stu-id="232ca-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="232ca-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="232ca-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="232ca-123">所有</span><span class="sxs-lookup"><span data-stu-id="232ca-123">None</span></span>
- <span data-ttu-id="232ca-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="232ca-124">DebugInfo</span></span>
- <span data-ttu-id="232ca-125">Statistics</span><span class="sxs-lookup"><span data-stu-id="232ca-125">Statistics</span></span>
- <span data-ttu-id="232ca-126">同時</span><span class="sxs-lookup"><span data-stu-id="232ca-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-127">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="232ca-127">-JobId</span></span>
<span data-ttu-id="232ca-128">指定要取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="232ca-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="232ca-129">-Name</span></span>
<span data-ttu-id="232ca-130">指定要用來篩選工作清單結果的名稱。</span><span class="sxs-lookup"><span data-stu-id="232ca-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="232ca-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="232ca-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="232ca-132">所有</span><span class="sxs-lookup"><span data-stu-id="232ca-132">None</span></span>
- <span data-ttu-id="232ca-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="232ca-133">DebugInfo</span></span>
- <span data-ttu-id="232ca-134">Statistics</span><span class="sxs-lookup"><span data-stu-id="232ca-134">Statistics</span></span>
- <span data-ttu-id="232ca-135">同時</span><span class="sxs-lookup"><span data-stu-id="232ca-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="232ca-136">-PipelineId</span></span>
<span data-ttu-id="232ca-137">一個選用的識別碼，只指示應傳回指定管線的工作部分。</span><span class="sxs-lookup"><span data-stu-id="232ca-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="232ca-138">-RecurrenceId</span></span>
<span data-ttu-id="232ca-139">一個選用的識別碼，只指示應該傳回指定的定期作業部分。</span><span class="sxs-lookup"><span data-stu-id="232ca-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-140">-結果</span><span class="sxs-lookup"><span data-stu-id="232ca-140">-Result</span></span>
<span data-ttu-id="232ca-141">指定作業結果的結果篩選器。</span><span class="sxs-lookup"><span data-stu-id="232ca-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="232ca-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="232ca-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="232ca-143">所有</span><span class="sxs-lookup"><span data-stu-id="232ca-143">None</span></span>
- <span data-ttu-id="232ca-144">取消</span><span class="sxs-lookup"><span data-stu-id="232ca-144">Cancelled</span></span>
- <span data-ttu-id="232ca-145">成功</span><span class="sxs-lookup"><span data-stu-id="232ca-145">Failed</span></span>
- <span data-ttu-id="232ca-146">成功</span><span class="sxs-lookup"><span data-stu-id="232ca-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-147">-State</span><span class="sxs-lookup"><span data-stu-id="232ca-147">-State</span></span>
<span data-ttu-id="232ca-148">指定作業結果的狀態篩選器。</span><span class="sxs-lookup"><span data-stu-id="232ca-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="232ca-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="232ca-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="232ca-150">認可</span><span class="sxs-lookup"><span data-stu-id="232ca-150">Accepted</span></span>
- <span data-ttu-id="232ca-151">新增功能</span><span class="sxs-lookup"><span data-stu-id="232ca-151">New</span></span>
- <span data-ttu-id="232ca-152">編譯</span><span class="sxs-lookup"><span data-stu-id="232ca-152">Compiling</span></span>
- <span data-ttu-id="232ca-153">排程</span><span class="sxs-lookup"><span data-stu-id="232ca-153">Scheduling</span></span>
- <span data-ttu-id="232ca-154">排</span><span class="sxs-lookup"><span data-stu-id="232ca-154">Queued</span></span>
- <span data-ttu-id="232ca-155">入門</span><span class="sxs-lookup"><span data-stu-id="232ca-155">Starting</span></span>
- <span data-ttu-id="232ca-156">處於</span><span class="sxs-lookup"><span data-stu-id="232ca-156">Paused</span></span>
- <span data-ttu-id="232ca-157">進行</span><span class="sxs-lookup"><span data-stu-id="232ca-157">Running</span></span>
- <span data-ttu-id="232ca-158">截至</span><span class="sxs-lookup"><span data-stu-id="232ca-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="232ca-159">-SubmittedAfter</span></span>
<span data-ttu-id="232ca-160">指定日期篩選。</span><span class="sxs-lookup"><span data-stu-id="232ca-160">Specifies a date filter.</span></span>
<span data-ttu-id="232ca-161">使用此參數可將作業清單結果篩選為在指定日期之後提交的作業。</span><span class="sxs-lookup"><span data-stu-id="232ca-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="232ca-162">-SubmittedBefore</span></span>
<span data-ttu-id="232ca-163">指定日期篩選。</span><span class="sxs-lookup"><span data-stu-id="232ca-163">Specifies a date filter.</span></span>
<span data-ttu-id="232ca-164">使用此參數可將作業清單結果篩選為在指定日期前提交的作業。</span><span class="sxs-lookup"><span data-stu-id="232ca-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-165">-提交者</span><span class="sxs-lookup"><span data-stu-id="232ca-165">-Submitter</span></span>
<span data-ttu-id="232ca-166">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="232ca-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="232ca-167">使用此參數可將作業清單結果篩選為指定使用者所提交的工作。</span><span class="sxs-lookup"><span data-stu-id="232ca-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-168">-上方</span><span class="sxs-lookup"><span data-stu-id="232ca-168">-Top</span></span>
<span data-ttu-id="232ca-169">指明要傳回的作業數的選用值。</span><span class="sxs-lookup"><span data-stu-id="232ca-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="232ca-170">預設值為500</span><span class="sxs-lookup"><span data-stu-id="232ca-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ca-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232ca-171">CommonParameters</span></span>
<span data-ttu-id="232ca-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="232ca-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232ca-173">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="232ca-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232ca-174">輸入</span><span class="sxs-lookup"><span data-stu-id="232ca-174">INPUTS</span></span>

### <span data-ttu-id="232ca-175">System.object</span><span class="sxs-lookup"><span data-stu-id="232ca-175">System.String</span></span>

### <span data-ttu-id="232ca-176">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="232ca-176">System.Guid</span></span>

### <span data-ttu-id="232ca-177">DataLakeAnalyticsEnums + ExtendedJobData （DataLakeAnalytics）。</span><span class="sxs-lookup"><span data-stu-id="232ca-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="232ca-178">"CoreLib" 1 [（System.object，System.object，，版本 = 4.0.0.0，Culture = 中立，</span><span class="sxs-lookup"><span data-stu-id="232ca-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="232ca-179">JobState [] DataLake. []</span><span class="sxs-lookup"><span data-stu-id="232ca-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="232ca-180">JobResult [] DataLake. []</span><span class="sxs-lookup"><span data-stu-id="232ca-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="232ca-181">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="232ca-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="232ca-182">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="232ca-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="232ca-183">輸出</span><span class="sxs-lookup"><span data-stu-id="232ca-183">OUTPUTS</span></span>

### <span data-ttu-id="232ca-184">[DataLake. JobInformation]。</span><span class="sxs-lookup"><span data-stu-id="232ca-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="232ca-185">筆記</span><span class="sxs-lookup"><span data-stu-id="232ca-185">NOTES</span></span>

## <span data-ttu-id="232ca-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="232ca-186">RELATED LINKS</span></span>

[<span data-ttu-id="232ca-187">停止 AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="232ca-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="232ca-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="232ca-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="232ca-189">稍候-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="232ca-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 0078196d8b06ae791fa0855345eec02d1f2eb59c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907661"
---
# <span data-ttu-id="4ffbd-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4ffbd-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="4ffbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ffbd-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffbd-103">獲得 Data Lake Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="4ffbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ffbd-104">SYNTAX</span></span>

### <span data-ttu-id="4ffbd-105">GetAllInResourceGroupAndAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="4ffbd-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ffbd-106">GetByS0ificJobInformation</span><span class="sxs-lookup"><span data-stu-id="4ffbd-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ffbd-107">描述</span><span class="sxs-lookup"><span data-stu-id="4ffbd-107">DESCRIPTION</span></span>
<span data-ttu-id="4ffbd-108">**Get-AzDataLakeAnalyticsJob** Cmdlet 會取得 Azure Data Lake Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="4ffbd-109">如果您未指定工作，此 Cmdlet 會獲得所有工作。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="4ffbd-110">例子</span><span class="sxs-lookup"><span data-stu-id="4ffbd-110">EXAMPLES</span></span>

### <span data-ttu-id="4ffbd-111">範例 1：取得指定的工作</span><span class="sxs-lookup"><span data-stu-id="4ffbd-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="4ffbd-112">此命令會以指定的識別碼獲得工作。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="4ffbd-113">範例 2：取得過去一周提交的工作</span><span class="sxs-lookup"><span data-stu-id="4ffbd-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="4ffbd-114">此命令會獲得過去一周提交的工作。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="4ffbd-115">參數</span><span class="sxs-lookup"><span data-stu-id="4ffbd-115">PARAMETERS</span></span>

### <span data-ttu-id="4ffbd-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="4ffbd-116">-Account</span></span>
<span data-ttu-id="4ffbd-117">指定 Data Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="4ffbd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffbd-118">-DefaultProfile</span></span>
<span data-ttu-id="4ffbd-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4ffbd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ffbd-120">-包含</span><span class="sxs-lookup"><span data-stu-id="4ffbd-120">-Include</span></span>
<span data-ttu-id="4ffbd-121">指定選項，指出要取回有關工作的其他資訊類型。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="4ffbd-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4ffbd-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ffbd-123">沒有</span><span class="sxs-lookup"><span data-stu-id="4ffbd-123">None</span></span>
- <span data-ttu-id="4ffbd-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="4ffbd-124">DebugInfo</span></span>
- <span data-ttu-id="4ffbd-125">統計</span><span class="sxs-lookup"><span data-stu-id="4ffbd-125">Statistics</span></span>
- <span data-ttu-id="4ffbd-126">所有</span><span class="sxs-lookup"><span data-stu-id="4ffbd-126">All</span></span>

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

### <span data-ttu-id="4ffbd-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="4ffbd-127">-JobId</span></span>
<span data-ttu-id="4ffbd-128">指定要取得的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="4ffbd-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ffbd-129">-Name</span></span>
<span data-ttu-id="4ffbd-130">指定要用於篩選工作清單結果的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="4ffbd-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4ffbd-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ffbd-132">沒有</span><span class="sxs-lookup"><span data-stu-id="4ffbd-132">None</span></span>
- <span data-ttu-id="4ffbd-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="4ffbd-133">DebugInfo</span></span>
- <span data-ttu-id="4ffbd-134">統計</span><span class="sxs-lookup"><span data-stu-id="4ffbd-134">Statistics</span></span>
- <span data-ttu-id="4ffbd-135">所有</span><span class="sxs-lookup"><span data-stu-id="4ffbd-135">All</span></span>

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

### <span data-ttu-id="4ffbd-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="4ffbd-136">-PipelineId</span></span>
<span data-ttu-id="4ffbd-137">應僅指出指定管線中工作部分的選擇性識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="4ffbd-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="4ffbd-138">-RecurrenceId</span></span>
<span data-ttu-id="4ffbd-139">應僅指出指定週期中工作部分的選擇性識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="4ffbd-140">-結果</span><span class="sxs-lookup"><span data-stu-id="4ffbd-140">-Result</span></span>
<span data-ttu-id="4ffbd-141">指定工作結果的結果篩選。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="4ffbd-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4ffbd-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ffbd-143">沒有</span><span class="sxs-lookup"><span data-stu-id="4ffbd-143">None</span></span>
- <span data-ttu-id="4ffbd-144">取消</span><span class="sxs-lookup"><span data-stu-id="4ffbd-144">Cancelled</span></span>
- <span data-ttu-id="4ffbd-145">失敗</span><span class="sxs-lookup"><span data-stu-id="4ffbd-145">Failed</span></span>
- <span data-ttu-id="4ffbd-146">成功</span><span class="sxs-lookup"><span data-stu-id="4ffbd-146">Succeeded</span></span>

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

### <span data-ttu-id="4ffbd-147">-State</span><span class="sxs-lookup"><span data-stu-id="4ffbd-147">-State</span></span>
<span data-ttu-id="4ffbd-148">指定工作結果的狀態篩選。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="4ffbd-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4ffbd-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ffbd-150">接受</span><span class="sxs-lookup"><span data-stu-id="4ffbd-150">Accepted</span></span>
- <span data-ttu-id="4ffbd-151">新增功能</span><span class="sxs-lookup"><span data-stu-id="4ffbd-151">New</span></span>
- <span data-ttu-id="4ffbd-152">編譯</span><span class="sxs-lookup"><span data-stu-id="4ffbd-152">Compiling</span></span>
- <span data-ttu-id="4ffbd-153">調度</span><span class="sxs-lookup"><span data-stu-id="4ffbd-153">Scheduling</span></span>
- <span data-ttu-id="4ffbd-154">排隊</span><span class="sxs-lookup"><span data-stu-id="4ffbd-154">Queued</span></span>
- <span data-ttu-id="4ffbd-155">開始</span><span class="sxs-lookup"><span data-stu-id="4ffbd-155">Starting</span></span>
- <span data-ttu-id="4ffbd-156">暫停</span><span class="sxs-lookup"><span data-stu-id="4ffbd-156">Paused</span></span>
- <span data-ttu-id="4ffbd-157">運行</span><span class="sxs-lookup"><span data-stu-id="4ffbd-157">Running</span></span>
- <span data-ttu-id="4ffbd-158">結束</span><span class="sxs-lookup"><span data-stu-id="4ffbd-158">Ended</span></span>

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

### <span data-ttu-id="4ffbd-159">-提交之後</span><span class="sxs-lookup"><span data-stu-id="4ffbd-159">-SubmittedAfter</span></span>
<span data-ttu-id="4ffbd-160">指定日期篩選。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-160">Specifies a date filter.</span></span>
<span data-ttu-id="4ffbd-161">使用此參數將工作清單結果篩選為指定日期之後提交的工作。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="4ffbd-162">-提交Before</span><span class="sxs-lookup"><span data-stu-id="4ffbd-162">-SubmittedBefore</span></span>
<span data-ttu-id="4ffbd-163">指定日期篩選。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-163">Specifies a date filter.</span></span>
<span data-ttu-id="4ffbd-164">使用此參數來篩選工作清單結果至指定日期之前提交的工作。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="4ffbd-165">-提交者</span><span class="sxs-lookup"><span data-stu-id="4ffbd-165">-Submitter</span></span>
<span data-ttu-id="4ffbd-166">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="4ffbd-167">使用此參數，將工作清單結果篩選為指定使用者提交的工作。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="4ffbd-168">-頂端</span><span class="sxs-lookup"><span data-stu-id="4ffbd-168">-Top</span></span>
<span data-ttu-id="4ffbd-169">這是一個可指出要退回之工作數目的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="4ffbd-170">預設值為 500</span><span class="sxs-lookup"><span data-stu-id="4ffbd-170">Default value is 500</span></span>

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

### <span data-ttu-id="4ffbd-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffbd-171">CommonParameters</span></span>
<span data-ttu-id="4ffbd-172">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffbd-173">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4ffbd-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffbd-174">輸入</span><span class="sxs-lookup"><span data-stu-id="4ffbd-174">INPUTS</span></span>

### <span data-ttu-id="4ffbd-175">System.String</span><span class="sxs-lookup"><span data-stu-id="4ffbd-175">System.String</span></span>

### <span data-ttu-id="4ffbd-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4ffbd-176">System.Guid</span></span>

### <span data-ttu-id="4ffbd-177">Microsoft.Azure.Commands.DataLakeAnalytics.models.DataLakeAnalyticsEnums+ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="4ffbd-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="4ffbd-178">System.Nullable'1[[System.DateTimeOffset， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ffbd-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ffbd-179">Microsoft.Azure.management.DataLake.Analytics.models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="4ffbd-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="4ffbd-180">Microsoft.Azure.management.DataLake.Analytics.models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="4ffbd-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="4ffbd-181">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ffbd-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ffbd-182">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ffbd-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4ffbd-183">輸出</span><span class="sxs-lookup"><span data-stu-id="4ffbd-183">OUTPUTS</span></span>

### <span data-ttu-id="4ffbd-184">Microsoft.Azure.management.DataLake.Analytics.models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="4ffbd-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="4ffbd-185">筆記</span><span class="sxs-lookup"><span data-stu-id="4ffbd-185">NOTES</span></span>

## <span data-ttu-id="4ffbd-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ffbd-186">RELATED LINKS</span></span>

[<span data-ttu-id="4ffbd-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4ffbd-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="4ffbd-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4ffbd-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="4ffbd-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4ffbd-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)



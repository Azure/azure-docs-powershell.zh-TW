---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451724"
---
# <span data-ttu-id="c509a-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c509a-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="c509a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c509a-102">SYNOPSIS</span></span>
<span data-ttu-id="c509a-103">提交作業。</span><span class="sxs-lookup"><span data-stu-id="c509a-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c509a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c509a-104">SYNTAX</span></span>

### <span data-ttu-id="c509a-105">含雙 SQL 腳本路徑的提交作業</span><span class="sxs-lookup"><span data-stu-id="c509a-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c509a-106">提交 U-SQL 作業</span><span class="sxs-lookup"><span data-stu-id="c509a-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c509a-107">含有含 reucurrence 資訊之雙 SQL 腳本路徑的提交作業</span><span class="sxs-lookup"><span data-stu-id="c509a-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c509a-108">使用定期資訊提交 U-SQL 作業</span><span class="sxs-lookup"><span data-stu-id="c509a-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c509a-109">使用含有 reucurrence 和管線資訊的雙 SQL 腳本路徑提交作業</span><span class="sxs-lookup"><span data-stu-id="c509a-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c509a-110">使用週期及管線資訊提交 U-SQL 作業</span><span class="sxs-lookup"><span data-stu-id="c509a-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c509a-111">說明</span><span class="sxs-lookup"><span data-stu-id="c509a-111">DESCRIPTION</span></span>
<span data-ttu-id="c509a-112">**AzureRmDataLakeAnalyticsJob** Cmdlet 會提交 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="c509a-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="c509a-113">示例</span><span class="sxs-lookup"><span data-stu-id="c509a-113">EXAMPLES</span></span>

### <span data-ttu-id="c509a-114">範例1：提交作業</span><span class="sxs-lookup"><span data-stu-id="c509a-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="c509a-115">這個命令會提交資料 Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="c509a-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="c509a-116">參數</span><span class="sxs-lookup"><span data-stu-id="c509a-116">PARAMETERS</span></span>

### <span data-ttu-id="c509a-117">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c509a-117">-Account</span></span>
<span data-ttu-id="c509a-118">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c509a-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c509a-119">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="c509a-119">-CompileMode</span></span>
<span data-ttu-id="c509a-120">指定作業的編譯模式。</span><span class="sxs-lookup"><span data-stu-id="c509a-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="c509a-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c509a-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c509a-122">語義</span><span class="sxs-lookup"><span data-stu-id="c509a-122">Semantic</span></span>
- <span data-ttu-id="c509a-123">填</span><span class="sxs-lookup"><span data-stu-id="c509a-123">Full</span></span>
- <span data-ttu-id="c509a-124">SingleBox</span><span class="sxs-lookup"><span data-stu-id="c509a-124">SingleBox</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="c509a-125">-CompileOnly</span></span>
<span data-ttu-id="c509a-126">表示此 Cmdlet 編譯作業而不執行它。</span><span class="sxs-lookup"><span data-stu-id="c509a-126">Indicates that this cmdlet compiles the job without running it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="c509a-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="c509a-128">指定作業的資料 Lake Analytics 單位 (DLAU) ，指出作業允許的最大並行度。</span><span class="sxs-lookup"><span data-stu-id="c509a-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="c509a-129">-Name</span></span>
<span data-ttu-id="c509a-130">指定作業名稱。</span><span class="sxs-lookup"><span data-stu-id="c509a-130">Specifies the job name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-131">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="c509a-131">-PipelineId</span></span>
<span data-ttu-id="c509a-132">代表此作業提交的識別碼，是一組週期性作業的一部分，也是與作業管線相關聯。</span><span class="sxs-lookup"><span data-stu-id="c509a-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-133">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="c509a-133">-PipelineName</span></span>
<span data-ttu-id="c509a-134">與此工作相關聯之管線的選擇性易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c509a-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="c509a-135">-PipelineUri</span></span>
<span data-ttu-id="c509a-136">連結至與此管線關聯之來源服務的可選 uri。</span><span class="sxs-lookup"><span data-stu-id="c509a-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-137">-優先順序</span><span class="sxs-lookup"><span data-stu-id="c509a-137">-Priority</span></span>
<span data-ttu-id="c509a-138">指定作業的優先順序。</span><span class="sxs-lookup"><span data-stu-id="c509a-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="c509a-139">如果未指定，優先順序為1000。</span><span class="sxs-lookup"><span data-stu-id="c509a-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="c509a-140">較低的數位表示較高的作業優先順序。</span><span class="sxs-lookup"><span data-stu-id="c509a-140">A low number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-141">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="c509a-141">-RecurrenceId</span></span>
<span data-ttu-id="c509a-142">代表此作業提交的識別碼，是一組具有相同週期 ID 的週期性作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="c509a-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-143">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="c509a-143">-RecurrenceName</span></span>
<span data-ttu-id="c509a-144">作業間定期關聯的選擇性易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c509a-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="c509a-145">-RunId</span></span>
<span data-ttu-id="c509a-146">識別管線的此特定執行小程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c509a-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-147">-執行時間</span><span class="sxs-lookup"><span data-stu-id="c509a-147">-Runtime</span></span>
<span data-ttu-id="c509a-148">指定作業的執行時間版本。</span><span class="sxs-lookup"><span data-stu-id="c509a-148">Specifies the runtime version of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-149">-腳本</span><span class="sxs-lookup"><span data-stu-id="c509a-149">-Script</span></span>
<span data-ttu-id="c509a-150">指定要執行的腳本內容。</span><span class="sxs-lookup"><span data-stu-id="c509a-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="c509a-151">-ScriptPath</span></span>
<span data-ttu-id="c509a-152">指定要執行之腳本的本機檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="c509a-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509a-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c509a-153">-DefaultProfile</span></span>
<span data-ttu-id="c509a-154">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c509a-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c509a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c509a-155">CommonParameters</span></span>
<span data-ttu-id="c509a-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c509a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c509a-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c509a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c509a-158">輸入</span><span class="sxs-lookup"><span data-stu-id="c509a-158">INPUTS</span></span>

### <span data-ttu-id="c509a-159">字串</span><span class="sxs-lookup"><span data-stu-id="c509a-159">String</span></span>
<span data-ttu-id="c509a-160">形參 "Script" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c509a-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c509a-161">輸出</span><span class="sxs-lookup"><span data-stu-id="c509a-161">OUTPUTS</span></span>

### <span data-ttu-id="c509a-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="c509a-162">JobInformation</span></span>
<span data-ttu-id="c509a-163">已提交作業的初始作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c509a-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="c509a-164">筆記</span><span class="sxs-lookup"><span data-stu-id="c509a-164">NOTES</span></span>

## <span data-ttu-id="c509a-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="c509a-165">RELATED LINKS</span></span>

[<span data-ttu-id="c509a-166">AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c509a-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c509a-167">停止 AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c509a-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c509a-168">稍候-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c509a-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)



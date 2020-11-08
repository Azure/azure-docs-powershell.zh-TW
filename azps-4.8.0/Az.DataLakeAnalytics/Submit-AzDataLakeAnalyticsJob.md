---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969307"
---
# <span data-ttu-id="5e5a3-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5e5a3-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="5e5a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5a3-103">提交作業。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-103">Submits a job.</span></span>

## <span data-ttu-id="5e5a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e5a3-104">SYNTAX</span></span>

### <span data-ttu-id="5e5a3-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="5e5a3-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e5a3-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="5e5a3-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e5a3-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="5e5a3-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e5a3-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="5e5a3-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e5a3-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="5e5a3-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e5a3-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="5e5a3-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e5a3-111">說明</span><span class="sxs-lookup"><span data-stu-id="5e5a3-111">DESCRIPTION</span></span>
<span data-ttu-id="5e5a3-112">**AzDataLakeAnalyticsJob** Cmdlet 會提交 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="5e5a3-113">示例</span><span class="sxs-lookup"><span data-stu-id="5e5a3-113">EXAMPLES</span></span>

### <span data-ttu-id="5e5a3-114">範例1：提交作業</span><span class="sxs-lookup"><span data-stu-id="5e5a3-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="5e5a3-115">這個命令會提交資料 Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="5e5a3-116">範例2：使用腳本參數提交作業</span><span class="sxs-lookup"><span data-stu-id="5e5a3-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="5e5a3-117">U-SQL 腳本參數會在主要腳本內容的前面加上，例如： DECLARE @Department 字串 = "Sales";宣告 @NumRecords int = 1000;宣告 @StartDateTime datetime = New datetime (2017、12、6、0、0、0、0) ;</span><span class="sxs-lookup"><span data-stu-id="5e5a3-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="5e5a3-118">參數</span><span class="sxs-lookup"><span data-stu-id="5e5a3-118">PARAMETERS</span></span>

### <span data-ttu-id="5e5a3-119">-帳戶</span><span class="sxs-lookup"><span data-stu-id="5e5a3-119">-Account</span></span>
<span data-ttu-id="5e5a3-120">要在其中提交作業的 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="5e5a3-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="5e5a3-121">-AnalyticsUnits</span></span>
<span data-ttu-id="5e5a3-122">要用於此作業的分析單元。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-122">The analytics units to use for this job.</span></span> <span data-ttu-id="5e5a3-123">通常，專門針對腳本的更多分析單元，會使腳本執行時間變得更快。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="5e5a3-124">-CompileMode</span></span>
<span data-ttu-id="5e5a3-125">要針對此作業執行的編譯類型。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="5e5a3-126">有效值：</span><span class="sxs-lookup"><span data-stu-id="5e5a3-126">Valid values:</span></span> 
- <span data-ttu-id="5e5a3-127">語義 (只會執行語義檢查和必要的健全檢查) </span><span class="sxs-lookup"><span data-stu-id="5e5a3-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="5e5a3-128">完整 (完全編譯) </span><span class="sxs-lookup"><span data-stu-id="5e5a3-128">Full (Full compilation)</span></span>
- <span data-ttu-id="5e5a3-129">在本機執行完整編譯 SingleBox () </span><span class="sxs-lookup"><span data-stu-id="5e5a3-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="5e5a3-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="5e5a3-130">-CompileOnly</span></span>
<span data-ttu-id="5e5a3-131">表示提交只應建立作業，而如果設定為 true，則不會執行。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="5e5a3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e5a3-132">-DefaultProfile</span></span>
<span data-ttu-id="5e5a3-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5e5a3-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e5a3-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e5a3-134">-Name</span></span>
<span data-ttu-id="5e5a3-135">要提交之作業的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="5e5a3-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="5e5a3-136">-PipelineId</span></span>
<span data-ttu-id="5e5a3-137">代表此作業提交的識別碼，是一組週期性作業的一部分，也是與作業管線相關聯。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="5e5a3-138">-PipelineName</span></span>
<span data-ttu-id="5e5a3-139">與此工作相關聯之管線的選擇性易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="5e5a3-140">-PipelineUri</span></span>
<span data-ttu-id="5e5a3-141">連結至與此管線關聯之來源服務的可選 uri。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-142">-優先順序</span><span class="sxs-lookup"><span data-stu-id="5e5a3-142">-Priority</span></span>
<span data-ttu-id="5e5a3-143">作業的優先順序。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-143">The priority of the job.</span></span> <span data-ttu-id="5e5a3-144">如果未指定，優先順序為1000。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="5e5a3-145">較小的數位表示較高的作業優先順序。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="5e5a3-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="5e5a3-146">-RecurrenceId</span></span>
<span data-ttu-id="5e5a3-147">代表此作業提交的識別碼，是一組具有相同週期 ID 的週期性作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="5e5a3-148">-RecurrenceName</span></span>
<span data-ttu-id="5e5a3-149">作業間定期關聯的選擇性易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="5e5a3-150">-RunId</span></span>
<span data-ttu-id="5e5a3-151">識別管線的此特定執行小程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-152">-執行時間</span><span class="sxs-lookup"><span data-stu-id="5e5a3-152">-Runtime</span></span>
<span data-ttu-id="5e5a3-153">或者，您也可以設定要用於工作的執行時間版本。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="5e5a3-154">如果不是，則會使用預設執行時間。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="5e5a3-155">-腳本</span><span class="sxs-lookup"><span data-stu-id="5e5a3-155">-Script</span></span>
<span data-ttu-id="5e5a3-156">[腳本]，以執行 (寫入的內嵌) 。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="5e5a3-157">-ScriptParameter</span></span>
<span data-ttu-id="5e5a3-158">此作業的腳本參數，做為參數名稱的字典， (字串) 到值 (任何位元組、sbyte、int、uint (或 uint32) 、長型、雙引號 (或 uint64) 、float、double、decimal、short (或 int16) 、，ushort (或 uint16) 、char、string、DateTime、bool、Guid 或 byte [] ) 。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="5e5a3-159">-ScriptPath</span></span>
<span data-ttu-id="5e5a3-160">要提交的腳本檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5a3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5a3-161">CommonParameters</span></span>
<span data-ttu-id="5e5a3-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5a3-163">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5a3-164">輸入</span><span class="sxs-lookup"><span data-stu-id="5e5a3-164">INPUTS</span></span>

### <span data-ttu-id="5e5a3-165">System.object</span><span class="sxs-lookup"><span data-stu-id="5e5a3-165">System.String</span></span>

### <span data-ttu-id="5e5a3-166">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5e5a3-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5e5a3-167">System.object</span><span class="sxs-lookup"><span data-stu-id="5e5a3-167">System.Int32</span></span>

### <span data-ttu-id="5e5a3-168">System.object</span><span class="sxs-lookup"><span data-stu-id="5e5a3-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="5e5a3-169">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="5e5a3-169">System.Guid</span></span>

### <span data-ttu-id="5e5a3-170">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5e5a3-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5e5a3-171">輸出</span><span class="sxs-lookup"><span data-stu-id="5e5a3-171">OUTPUTS</span></span>

### <span data-ttu-id="5e5a3-172">[DataLake. JobInformation]。</span><span class="sxs-lookup"><span data-stu-id="5e5a3-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="5e5a3-173">筆記</span><span class="sxs-lookup"><span data-stu-id="5e5a3-173">NOTES</span></span>

## <span data-ttu-id="5e5a3-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e5a3-174">RELATED LINKS</span></span>

[<span data-ttu-id="5e5a3-175">AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5e5a3-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="5e5a3-176">停止 AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5e5a3-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="5e5a3-177">稍候-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5e5a3-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)



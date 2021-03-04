---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 429b0a6cec9c7a3f27019e950e5497eac961c81f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910518"
---
# <span data-ttu-id="22bfa-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="22bfa-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="22bfa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="22bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="22bfa-103">提交工作。</span><span class="sxs-lookup"><span data-stu-id="22bfa-103">Submits a job.</span></span>

## <span data-ttu-id="22bfa-104">語法</span><span class="sxs-lookup"><span data-stu-id="22bfa-104">SYNTAX</span></span>

### <span data-ttu-id="22bfa-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="22bfa-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22bfa-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="22bfa-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22bfa-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="22bfa-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22bfa-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="22bfa-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22bfa-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="22bfa-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22bfa-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="22bfa-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22bfa-111">描述</span><span class="sxs-lookup"><span data-stu-id="22bfa-111">DESCRIPTION</span></span>
<span data-ttu-id="22bfa-112">**Submit-AzDataLakeAnalyticsJob** Cmdlet 會提交 Azure Data Lake Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="22bfa-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="22bfa-113">例子</span><span class="sxs-lookup"><span data-stu-id="22bfa-113">EXAMPLES</span></span>

### <span data-ttu-id="22bfa-114">範例 1：提交工作</span><span class="sxs-lookup"><span data-stu-id="22bfa-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="22bfa-115">此命令會提交 Data Lake Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="22bfa-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="22bfa-116">範例 2：使用腳本參數提交工作</span><span class="sxs-lookup"><span data-stu-id="22bfa-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="22bfa-117">U-SQL 腳本參數會位於主要腳本內容的上方，例如：DECLARE @Department 字串 = "Sales";DECLARE @NumRecords int = 1000;DECLARE @StartDateTime DateTime = 新的 DateTime (2017， 12， 6， 0， 0， 0， 0) ;</span><span class="sxs-lookup"><span data-stu-id="22bfa-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="22bfa-118">參數</span><span class="sxs-lookup"><span data-stu-id="22bfa-118">PARAMETERS</span></span>

### <span data-ttu-id="22bfa-119">-帳戶</span><span class="sxs-lookup"><span data-stu-id="22bfa-119">-Account</span></span>
<span data-ttu-id="22bfa-120">提交工作之 Data Lake Analytics 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="22bfa-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="22bfa-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="22bfa-121">-AnalyticsUnits</span></span>
<span data-ttu-id="22bfa-122">此工作使用的分析單位。</span><span class="sxs-lookup"><span data-stu-id="22bfa-122">The analytics units to use for this job.</span></span> <span data-ttu-id="22bfa-123">一般來說，更專注于腳本的分析單位會加快腳本的執行時間。</span><span class="sxs-lookup"><span data-stu-id="22bfa-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="22bfa-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="22bfa-124">-CompileMode</span></span>
<span data-ttu-id="22bfa-125">此工作要完成之編譯的類型。</span><span class="sxs-lookup"><span data-stu-id="22bfa-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="22bfa-126">有效的值：</span><span class="sxs-lookup"><span data-stu-id="22bfa-126">Valid values:</span></span> 
- <span data-ttu-id="22bfa-127">語 (詞只會執行語性檢查和必要的性向檢查) </span><span class="sxs-lookup"><span data-stu-id="22bfa-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="22bfa-128">完整 (完整編譯) </span><span class="sxs-lookup"><span data-stu-id="22bfa-128">Full (Full compilation)</span></span>
- <span data-ttu-id="22bfa-129">在 (執行完整編譯的單一Box) </span><span class="sxs-lookup"><span data-stu-id="22bfa-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="22bfa-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="22bfa-130">-CompileOnly</span></span>
<span data-ttu-id="22bfa-131">表示提交應只建立工作，如果設定為 True，則不執行。</span><span class="sxs-lookup"><span data-stu-id="22bfa-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="22bfa-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22bfa-132">-DefaultProfile</span></span>
<span data-ttu-id="22bfa-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="22bfa-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22bfa-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="22bfa-134">-Name</span></span>
<span data-ttu-id="22bfa-135">要提交之工作的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="22bfa-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="22bfa-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="22bfa-136">-PipelineId</span></span>
<span data-ttu-id="22bfa-137">指出提交此工作的識別碼是一組週期性工作的一部分，也與工作管道相關聯。</span><span class="sxs-lookup"><span data-stu-id="22bfa-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="22bfa-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="22bfa-138">-PipelineName</span></span>
<span data-ttu-id="22bfa-139">與此工作相關聯的管線的選擇性好用名稱。</span><span class="sxs-lookup"><span data-stu-id="22bfa-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="22bfa-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="22bfa-140">-PipelineUri</span></span>
<span data-ttu-id="22bfa-141">連結到與此管線相關聯的原始服務的選擇性 uri。</span><span class="sxs-lookup"><span data-stu-id="22bfa-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="22bfa-142">-優先順序</span><span class="sxs-lookup"><span data-stu-id="22bfa-142">-Priority</span></span>
<span data-ttu-id="22bfa-143">工作的優先順序。</span><span class="sxs-lookup"><span data-stu-id="22bfa-143">The priority of the job.</span></span> <span data-ttu-id="22bfa-144">如果未指定，優先順序為 1000。</span><span class="sxs-lookup"><span data-stu-id="22bfa-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="22bfa-145">數位越低，代表工作優先順序越高。</span><span class="sxs-lookup"><span data-stu-id="22bfa-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="22bfa-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="22bfa-146">-RecurrenceId</span></span>
<span data-ttu-id="22bfa-147">指出提交此工作的識別碼是具有相同週期識別碼的一組週期性工作的一部分。</span><span class="sxs-lookup"><span data-stu-id="22bfa-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="22bfa-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="22bfa-148">-RecurrenceName</span></span>
<span data-ttu-id="22bfa-149">工作之間週期相互關聯性選擇性的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="22bfa-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="22bfa-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="22bfa-150">-RunId</span></span>
<span data-ttu-id="22bfa-151">識別管線此特定執行反覆運算的識別碼。</span><span class="sxs-lookup"><span data-stu-id="22bfa-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="22bfa-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="22bfa-152">-Runtime</span></span>
<span data-ttu-id="22bfa-153">選擇性地設定要用於工作的執行時間版本。</span><span class="sxs-lookup"><span data-stu-id="22bfa-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="22bfa-154">如果取消集區，則使用預設執行時間。</span><span class="sxs-lookup"><span data-stu-id="22bfa-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="22bfa-155">-腳本</span><span class="sxs-lookup"><span data-stu-id="22bfa-155">-Script</span></span>
<span data-ttu-id="22bfa-156">腳本以執行 (內嵌或) 。</span><span class="sxs-lookup"><span data-stu-id="22bfa-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="22bfa-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="22bfa-157">-ScriptParameter</span></span>
<span data-ttu-id="22bfa-158">此工作的腳本參數做為參數名稱的字典 (字串) 位元組 (值， sbyte、int、uint (或 uint32) 、long、ulong (或 uint64) 、float、double、decimal、short (或 int16) 、ushort (或 uint16) 、char、string、DateTime、bool、Guid 或 byte[]) 。</span><span class="sxs-lookup"><span data-stu-id="22bfa-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="22bfa-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="22bfa-159">-ScriptPath</span></span>
<span data-ttu-id="22bfa-160">要提交之腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="22bfa-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="22bfa-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22bfa-161">CommonParameters</span></span>
<span data-ttu-id="22bfa-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="22bfa-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22bfa-163">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="22bfa-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22bfa-164">輸入</span><span class="sxs-lookup"><span data-stu-id="22bfa-164">INPUTS</span></span>

### <span data-ttu-id="22bfa-165">System.String</span><span class="sxs-lookup"><span data-stu-id="22bfa-165">System.String</span></span>

### <span data-ttu-id="22bfa-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22bfa-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="22bfa-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="22bfa-167">System.Int32</span></span>

### <span data-ttu-id="22bfa-168">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="22bfa-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="22bfa-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="22bfa-169">System.Guid</span></span>

### <span data-ttu-id="22bfa-170">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="22bfa-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="22bfa-171">輸出</span><span class="sxs-lookup"><span data-stu-id="22bfa-171">OUTPUTS</span></span>

### <span data-ttu-id="22bfa-172">Microsoft.Azure.management.DataLake.Analytics.models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="22bfa-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="22bfa-173">筆記</span><span class="sxs-lookup"><span data-stu-id="22bfa-173">NOTES</span></span>

## <span data-ttu-id="22bfa-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="22bfa-174">RELATED LINKS</span></span>

[<span data-ttu-id="22bfa-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="22bfa-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="22bfa-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="22bfa-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="22bfa-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="22bfa-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)



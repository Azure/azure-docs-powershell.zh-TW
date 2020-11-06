---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: fc09560bca0d825cc65d8a4f964119cd50898190
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446280"
---
# <span data-ttu-id="f2568-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f2568-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="f2568-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2568-102">SYNOPSIS</span></span>
<span data-ttu-id="f2568-103">提交作業。</span><span class="sxs-lookup"><span data-stu-id="f2568-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2568-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2568-104">SYNTAX</span></span>

### <span data-ttu-id="f2568-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="f2568-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2568-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="f2568-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2568-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="f2568-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2568-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="f2568-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2568-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="f2568-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2568-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="f2568-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2568-111">說明</span><span class="sxs-lookup"><span data-stu-id="f2568-111">DESCRIPTION</span></span>
<span data-ttu-id="f2568-112">**AzureRmDataLakeAnalyticsJob** Cmdlet 會提交 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="f2568-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="f2568-113">示例</span><span class="sxs-lookup"><span data-stu-id="f2568-113">EXAMPLES</span></span>

### <span data-ttu-id="f2568-114">範例1：提交作業</span><span class="sxs-lookup"><span data-stu-id="f2568-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="f2568-115">這個命令會提交資料 Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="f2568-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="f2568-116">範例2：使用腳本參數提交作業</span><span class="sxs-lookup"><span data-stu-id="f2568-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="f2568-117">U-SQL 腳本參數會在主要腳本內容的前面加上，例如：</span><span class="sxs-lookup"><span data-stu-id="f2568-117">U-SQL script parameters are prepended above the main script contents, e.g.:</span></span>

<span data-ttu-id="f2568-118">宣告 @Department 字串 = "Sales";宣告 @NumRecords int = 1000;宣告 @StartDateTime datetime = New datetime (2017、12、6、0、0、0、0) ;</span><span class="sxs-lookup"><span data-stu-id="f2568-118">DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="f2568-119">參數</span><span class="sxs-lookup"><span data-stu-id="f2568-119">PARAMETERS</span></span>

### <span data-ttu-id="f2568-120">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f2568-120">-Account</span></span>
<span data-ttu-id="f2568-121">要在其中提交作業的 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f2568-121">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="f2568-122">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="f2568-122">-CompileMode</span></span>
<span data-ttu-id="f2568-123">要針對此作業執行的編譯類型。</span><span class="sxs-lookup"><span data-stu-id="f2568-123">The type of compilation to be done on this job.</span></span> <span data-ttu-id="f2568-124">有效值：</span><span class="sxs-lookup"><span data-stu-id="f2568-124">Valid values:</span></span> 

- <span data-ttu-id="f2568-125">語義 (只會執行語義檢查和必要的健全檢查) </span><span class="sxs-lookup"><span data-stu-id="f2568-125">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="f2568-126">完整 (完全編譯) </span><span class="sxs-lookup"><span data-stu-id="f2568-126">Full (Full compilation)</span></span>
- <span data-ttu-id="f2568-127">在本機執行完整編譯 SingleBox () </span><span class="sxs-lookup"><span data-stu-id="f2568-127">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-128">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="f2568-128">-CompileOnly</span></span>
<span data-ttu-id="f2568-129">表示提交只應建立作業，而如果設定為 true，則不會執行。</span><span class="sxs-lookup"><span data-stu-id="f2568-129">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2568-130">-DefaultProfile</span></span>
<span data-ttu-id="f2568-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f2568-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2568-132">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="f2568-132">-AnalyticsUnits</span></span>
<span data-ttu-id="f2568-133">要用於此作業的分析單元。</span><span class="sxs-lookup"><span data-stu-id="f2568-133">The analytics units to use for this job.</span></span> <span data-ttu-id="f2568-134">通常，專門針對腳本的更多分析單元，會使腳本執行時間變得更快。</span><span class="sxs-lookup"><span data-stu-id="f2568-134">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2568-135">-Name</span></span>
<span data-ttu-id="f2568-136">要提交之作業的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="f2568-136">The friendly name of the job to submit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-137">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="f2568-137">-PipelineId</span></span>
<span data-ttu-id="f2568-138">代表此作業提交的識別碼，是一組週期性作業的一部分，也是與作業管線相關聯。</span><span class="sxs-lookup"><span data-stu-id="f2568-138">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-139">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f2568-139">-PipelineName</span></span>
<span data-ttu-id="f2568-140">與此工作相關聯之管線的選擇性易記名稱。</span><span class="sxs-lookup"><span data-stu-id="f2568-140">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-141">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="f2568-141">-PipelineUri</span></span>
<span data-ttu-id="f2568-142">連結至與此管線關聯之來源服務的可選 uri。</span><span class="sxs-lookup"><span data-stu-id="f2568-142">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-143">-優先順序</span><span class="sxs-lookup"><span data-stu-id="f2568-143">-Priority</span></span>
<span data-ttu-id="f2568-144">作業的優先順序。</span><span class="sxs-lookup"><span data-stu-id="f2568-144">The priority of the job.</span></span> <span data-ttu-id="f2568-145">如果未指定，優先順序為1000。</span><span class="sxs-lookup"><span data-stu-id="f2568-145">If not specified, the priority is 1000.</span></span> <span data-ttu-id="f2568-146">較小的數位表示較高的作業優先順序。</span><span class="sxs-lookup"><span data-stu-id="f2568-146">A lower number indicates a higher job priority.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-147">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="f2568-147">-RecurrenceId</span></span>
<span data-ttu-id="f2568-148">代表此作業提交的識別碼，是一組具有相同週期 ID 的週期性作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="f2568-148">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-149">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="f2568-149">-RecurrenceName</span></span>
<span data-ttu-id="f2568-150">作業間定期關聯的選擇性易記名稱。</span><span class="sxs-lookup"><span data-stu-id="f2568-150">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-151">-RunId</span><span class="sxs-lookup"><span data-stu-id="f2568-151">-RunId</span></span>
<span data-ttu-id="f2568-152">識別管線的此特定執行小程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2568-152">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-153">-執行時間</span><span class="sxs-lookup"><span data-stu-id="f2568-153">-Runtime</span></span>
<span data-ttu-id="f2568-154">或者，您也可以設定要用於工作的執行時間版本。</span><span class="sxs-lookup"><span data-stu-id="f2568-154">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="f2568-155">如果不是，則會使用預設執行時間。</span><span class="sxs-lookup"><span data-stu-id="f2568-155">If left unset, the default runtime is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-156">-腳本</span><span class="sxs-lookup"><span data-stu-id="f2568-156">-Script</span></span>
<span data-ttu-id="f2568-157">[腳本]，以執行 (寫入的內嵌) 。</span><span class="sxs-lookup"><span data-stu-id="f2568-157">Script to execute (written inline).</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-158">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="f2568-158">-ScriptParameter</span></span>
<span data-ttu-id="f2568-159">此作業的腳本參數，做為參數名稱的字典， (字串) 到值 (任何位元組、sbyte、int、uint (或 uint32) 、長型、雙引號 (或 uint64) 、float、double、decimal、short (或 int16) 、，ushort (或 uint16) 、char、string、DateTime、bool、Guid 或 byte [] ) 。</span><span class="sxs-lookup"><span data-stu-id="f2568-159">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-160">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="f2568-160">-ScriptPath</span></span>
<span data-ttu-id="f2568-161">要提交的腳本檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f2568-161">Path to the script file to submit.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2568-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2568-162">CommonParameters</span></span>
<span data-ttu-id="f2568-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2568-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2568-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2568-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2568-165">輸入</span><span class="sxs-lookup"><span data-stu-id="f2568-165">INPUTS</span></span>

### <span data-ttu-id="f2568-166">字串</span><span class="sxs-lookup"><span data-stu-id="f2568-166">String</span></span>
<span data-ttu-id="f2568-167">形參 "Script" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f2568-167">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f2568-168">輸出</span><span class="sxs-lookup"><span data-stu-id="f2568-168">OUTPUTS</span></span>

### <span data-ttu-id="f2568-169">JobInformation</span><span class="sxs-lookup"><span data-stu-id="f2568-169">JobInformation</span></span>
<span data-ttu-id="f2568-170">已提交作業的初始作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f2568-170">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="f2568-171">筆記</span><span class="sxs-lookup"><span data-stu-id="f2568-171">NOTES</span></span>

## <span data-ttu-id="f2568-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2568-172">RELATED LINKS</span></span>

[<span data-ttu-id="f2568-173">AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f2568-173">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="f2568-174">停止 AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f2568-174">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="f2568-175">稍候-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f2568-175">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)



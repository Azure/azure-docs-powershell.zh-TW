---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: fb01af87d28323e3e25c46868f94e892b835afc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454431"
---
# <span data-ttu-id="96067-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="96067-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="96067-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96067-102">SYNOPSIS</span></span>
<span data-ttu-id="96067-103">取得作業的批次工作。</span><span class="sxs-lookup"><span data-stu-id="96067-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96067-104">句法</span><span class="sxs-lookup"><span data-stu-id="96067-104">SYNTAX</span></span>

### <span data-ttu-id="96067-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="96067-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96067-106">標識號</span><span class="sxs-lookup"><span data-stu-id="96067-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96067-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="96067-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96067-108">說明</span><span class="sxs-lookup"><span data-stu-id="96067-108">DESCRIPTION</span></span>
<span data-ttu-id="96067-109">**AzureBatchTask** Cmdlet 會取得批次作業的 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="96067-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="96067-110">使用 *JobId* 參數或 *作業* 參數指定作業。</span><span class="sxs-lookup"><span data-stu-id="96067-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="96067-111">若要取得單一任務，請指定 *Id* 參數。</span><span class="sxs-lookup"><span data-stu-id="96067-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="96067-112">您可以指定 *篩選* 參數，以取得符合開啟資料通訊協定 (OData) 篩選的任務。</span><span class="sxs-lookup"><span data-stu-id="96067-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="96067-113">示例</span><span class="sxs-lookup"><span data-stu-id="96067-113">EXAMPLES</span></span>

### <span data-ttu-id="96067-114">範例1：依識別碼取得任務</span><span class="sxs-lookup"><span data-stu-id="96067-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 : 
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="96067-115">這個命令會取得 [作業 Job01] 底下的 [識別碼 Task03] 任務。</span><span class="sxs-lookup"><span data-stu-id="96067-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="96067-116">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="96067-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="96067-117">範例2：從指定的工作取得所有已完成的任務</span><span class="sxs-lookup"><span data-stu-id="96067-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         : 
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               : 
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="96067-118">這個命令會從具有識別碼 Job02 的作業中取得已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="96067-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="96067-119">參數</span><span class="sxs-lookup"><span data-stu-id="96067-119">PARAMETERS</span></span>

### <span data-ttu-id="96067-120">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="96067-120">-BatchContext</span></span>
<span data-ttu-id="96067-121">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="96067-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="96067-122">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96067-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96067-123">-展開</span><span class="sxs-lookup"><span data-stu-id="96067-123">-Expand</span></span>
<span data-ttu-id="96067-124">指定 OData expand 子句。</span><span class="sxs-lookup"><span data-stu-id="96067-124">Specifies an OData expand clause.</span></span>
<span data-ttu-id="96067-125">指定此參數的值，以取得要取得之主要實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="96067-125">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96067-126">-篩選</span><span class="sxs-lookup"><span data-stu-id="96067-126">-Filter</span></span>
<span data-ttu-id="96067-127">指定任務的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="96067-127">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="96067-128">如果您沒有指定篩選，這個 Cmdlet 會傳回批次帳戶或工作的所有任務。</span><span class="sxs-lookup"><span data-stu-id="96067-128">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96067-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="96067-129">-Id</span></span>
<span data-ttu-id="96067-130">指定此 Cmdlet 所取得之任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96067-130">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="96067-131">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="96067-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96067-132">-工作</span><span class="sxs-lookup"><span data-stu-id="96067-132">-Job</span></span>
<span data-ttu-id="96067-133">指定包含此 Cmdlet 所取得之任務的工作。</span><span class="sxs-lookup"><span data-stu-id="96067-133">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="96067-134">若要取得 **PSCloudJob** 物件，請使用 Get-AzureBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96067-134">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96067-135">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="96067-135">-JobId</span></span>
<span data-ttu-id="96067-136">指定包含此 Cmdlet 所取得之任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="96067-136">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96067-137">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="96067-137">-MaxCount</span></span>
<span data-ttu-id="96067-138">指定要傳回的最大任務數。</span><span class="sxs-lookup"><span data-stu-id="96067-138">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="96067-139">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="96067-139">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="96067-140">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="96067-140">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96067-141">-選取</span><span class="sxs-lookup"><span data-stu-id="96067-141">-Select</span></span>
<span data-ttu-id="96067-142">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="96067-142">Specifies an OData select clause.</span></span>
<span data-ttu-id="96067-143">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="96067-143">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96067-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96067-144">-DefaultProfile</span></span>
<span data-ttu-id="96067-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96067-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96067-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96067-146">CommonParameters</span></span>
<span data-ttu-id="96067-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96067-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96067-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96067-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96067-149">輸入</span><span class="sxs-lookup"><span data-stu-id="96067-149">INPUTS</span></span>

### <span data-ttu-id="96067-150">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="96067-150">BatchAccountContext</span></span>
<span data-ttu-id="96067-151">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="96067-151">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="96067-152">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="96067-152">PSCloudJob</span></span>
<span data-ttu-id="96067-153">參數「作業」接受管道中類型 ' PSCloudJob」的值</span><span class="sxs-lookup"><span data-stu-id="96067-153">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="96067-154">輸出</span><span class="sxs-lookup"><span data-stu-id="96067-154">OUTPUTS</span></span>

### <span data-ttu-id="96067-155">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="96067-155">PSCloudTask</span></span>

## <span data-ttu-id="96067-156">筆記</span><span class="sxs-lookup"><span data-stu-id="96067-156">NOTES</span></span>

## <span data-ttu-id="96067-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="96067-157">RELATED LINKS</span></span>

[<span data-ttu-id="96067-158">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="96067-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="96067-159">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="96067-159">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="96067-160">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="96067-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="96067-161">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="96067-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="96067-162">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="96067-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="96067-163">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="96067-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



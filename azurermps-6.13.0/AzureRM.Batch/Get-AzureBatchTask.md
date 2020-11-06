---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: 0229a44512aecc52b16650740d74ff177f83b9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453883"
---
# <span data-ttu-id="486eb-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="486eb-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="486eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="486eb-102">SYNOPSIS</span></span>
<span data-ttu-id="486eb-103">取得作業的批次工作。</span><span class="sxs-lookup"><span data-stu-id="486eb-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="486eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="486eb-104">SYNTAX</span></span>

### <span data-ttu-id="486eb-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="486eb-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="486eb-106">標識號</span><span class="sxs-lookup"><span data-stu-id="486eb-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="486eb-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="486eb-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="486eb-108">說明</span><span class="sxs-lookup"><span data-stu-id="486eb-108">DESCRIPTION</span></span>
<span data-ttu-id="486eb-109">**AzureBatchTask** Cmdlet 會取得批次作業的 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="486eb-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="486eb-110">使用 *JobId* 參數或 *作業* 參數指定作業。</span><span class="sxs-lookup"><span data-stu-id="486eb-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="486eb-111">若要取得單一任務，請指定 *Id* 參數。</span><span class="sxs-lookup"><span data-stu-id="486eb-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="486eb-112">您可以指定 *篩選* 參數，以取得符合開啟資料通訊協定 (OData) 篩選的任務。</span><span class="sxs-lookup"><span data-stu-id="486eb-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="486eb-113">示例</span><span class="sxs-lookup"><span data-stu-id="486eb-113">EXAMPLES</span></span>

### <span data-ttu-id="486eb-114">範例1：依識別碼取得任務</span><span class="sxs-lookup"><span data-stu-id="486eb-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="486eb-115">這個命令會取得 [作業 Job01] 底下的 [識別碼 Task03] 任務。</span><span class="sxs-lookup"><span data-stu-id="486eb-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="486eb-116">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="486eb-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="486eb-117">範例2：從指定的工作取得所有已完成的任務</span><span class="sxs-lookup"><span data-stu-id="486eb-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="486eb-118">這個命令會從具有識別碼 Job02 的作業中取得已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="486eb-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="486eb-119">參數</span><span class="sxs-lookup"><span data-stu-id="486eb-119">PARAMETERS</span></span>

### <span data-ttu-id="486eb-120">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="486eb-120">-BatchContext</span></span>
<span data-ttu-id="486eb-121">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="486eb-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="486eb-122">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="486eb-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="486eb-123">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="486eb-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="486eb-124">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="486eb-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="486eb-125">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="486eb-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="486eb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486eb-126">-DefaultProfile</span></span>
<span data-ttu-id="486eb-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="486eb-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="486eb-128">-展開</span><span class="sxs-lookup"><span data-stu-id="486eb-128">-Expand</span></span>
<span data-ttu-id="486eb-129">指定 OData expand 子句。</span><span class="sxs-lookup"><span data-stu-id="486eb-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="486eb-130">指定此參數的值，以取得要取得之主要實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="486eb-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="486eb-131">-篩選</span><span class="sxs-lookup"><span data-stu-id="486eb-131">-Filter</span></span>
<span data-ttu-id="486eb-132">指定任務的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="486eb-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="486eb-133">如果您沒有指定篩選，這個 Cmdlet 會傳回批次帳戶或工作的所有任務。</span><span class="sxs-lookup"><span data-stu-id="486eb-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="486eb-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="486eb-134">-Id</span></span>
<span data-ttu-id="486eb-135">指定此 Cmdlet 所取得之任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="486eb-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="486eb-136">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="486eb-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="486eb-137">-工作</span><span class="sxs-lookup"><span data-stu-id="486eb-137">-Job</span></span>
<span data-ttu-id="486eb-138">指定包含此 Cmdlet 所取得之任務的工作。</span><span class="sxs-lookup"><span data-stu-id="486eb-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="486eb-139">若要取得 **PSCloudJob** 物件，請使用 Get-AzureBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="486eb-139">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="486eb-140">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="486eb-140">-JobId</span></span>
<span data-ttu-id="486eb-141">指定包含此 Cmdlet 所取得之任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="486eb-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="486eb-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="486eb-142">-MaxCount</span></span>
<span data-ttu-id="486eb-143">指定要傳回的最大任務數。</span><span class="sxs-lookup"><span data-stu-id="486eb-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="486eb-144">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="486eb-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="486eb-145">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="486eb-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="486eb-146">-選取</span><span class="sxs-lookup"><span data-stu-id="486eb-146">-Select</span></span>
<span data-ttu-id="486eb-147">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="486eb-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="486eb-148">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="486eb-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="486eb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486eb-149">CommonParameters</span></span>
<span data-ttu-id="486eb-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="486eb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486eb-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="486eb-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486eb-152">輸入</span><span class="sxs-lookup"><span data-stu-id="486eb-152">INPUTS</span></span>

### <span data-ttu-id="486eb-153">System.object</span><span class="sxs-lookup"><span data-stu-id="486eb-153">System.String</span></span>

### <span data-ttu-id="486eb-154">Microsoft.Azure.Commands.Batch。PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="486eb-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="486eb-155">參數：作業 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="486eb-155">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="486eb-156">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="486eb-156">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="486eb-157">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="486eb-157">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="486eb-158">輸出</span><span class="sxs-lookup"><span data-stu-id="486eb-158">OUTPUTS</span></span>

### <span data-ttu-id="486eb-159">Microsoft.Azure.Commands.Batch。PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="486eb-159">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="486eb-160">筆記</span><span class="sxs-lookup"><span data-stu-id="486eb-160">NOTES</span></span>

## <span data-ttu-id="486eb-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="486eb-161">RELATED LINKS</span></span>

[<span data-ttu-id="486eb-162">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="486eb-162">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="486eb-163">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="486eb-163">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="486eb-164">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="486eb-164">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="486eb-165">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="486eb-165">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="486eb-166">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="486eb-166">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="486eb-167">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="486eb-167">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



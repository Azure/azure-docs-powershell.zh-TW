---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: 214ee3b030757da9acf632b2768a94b1ab026cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917102"
---
# <span data-ttu-id="30b2d-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="30b2d-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="30b2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="30b2d-103">獲得工作的批次工作。</span><span class="sxs-lookup"><span data-stu-id="30b2d-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="30b2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="30b2d-104">SYNTAX</span></span>

### <span data-ttu-id="30b2d-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="30b2d-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30b2d-106">Id</span><span class="sxs-lookup"><span data-stu-id="30b2d-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30b2d-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="30b2d-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30b2d-108">描述</span><span class="sxs-lookup"><span data-stu-id="30b2d-108">DESCRIPTION</span></span>
<span data-ttu-id="30b2d-109">**Get-AzBatchTask** Cmdlet 會取得批次工作的 Azure 批次處理工作。</span><span class="sxs-lookup"><span data-stu-id="30b2d-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="30b2d-110">使用 *JobId* 參數或 Job 參數 *指定* 工作。</span><span class="sxs-lookup"><span data-stu-id="30b2d-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="30b2d-111">若要取得單一工作，請指定 *Id* 參數。</span><span class="sxs-lookup"><span data-stu-id="30b2d-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="30b2d-112">您可以指定 *Filter* 參數，以取得符合 OData (開啟資料通訊協定) 的工作。</span><span class="sxs-lookup"><span data-stu-id="30b2d-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="30b2d-113">例子</span><span class="sxs-lookup"><span data-stu-id="30b2d-113">EXAMPLES</span></span>

### <span data-ttu-id="30b2d-114">範例 1：以識別碼取得工作</span><span class="sxs-lookup"><span data-stu-id="30b2d-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
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

<span data-ttu-id="30b2d-115">此命令會獲得 Job Job01 下具有 ID Task03 的工作。</span><span class="sxs-lookup"><span data-stu-id="30b2d-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="30b2d-116">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="30b2d-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="30b2d-117">範例 2：從指定的工作取得所有已完成的工作</span><span class="sxs-lookup"><span data-stu-id="30b2d-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
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

<span data-ttu-id="30b2d-118">此命令會從具有識別碼 Job02 的工作中，獲得已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="30b2d-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="30b2d-119">參數</span><span class="sxs-lookup"><span data-stu-id="30b2d-119">PARAMETERS</span></span>

### <span data-ttu-id="30b2d-120">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="30b2d-120">-BatchContext</span></span>
<span data-ttu-id="30b2d-121">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="30b2d-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="30b2d-122">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="30b2d-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="30b2d-123">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="30b2d-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="30b2d-124">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="30b2d-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="30b2d-125">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="30b2d-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="30b2d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b2d-126">-DefaultProfile</span></span>
<span data-ttu-id="30b2d-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30b2d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30b2d-128">-展開</span><span class="sxs-lookup"><span data-stu-id="30b2d-128">-Expand</span></span>
<span data-ttu-id="30b2d-129">指定 OData expand 子句。</span><span class="sxs-lookup"><span data-stu-id="30b2d-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="30b2d-130">指定此參數的值，以取得要取得之主實體的相關實體。</span><span class="sxs-lookup"><span data-stu-id="30b2d-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="30b2d-131">-篩選</span><span class="sxs-lookup"><span data-stu-id="30b2d-131">-Filter</span></span>
<span data-ttu-id="30b2d-132">指定任務的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="30b2d-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="30b2d-133">如果您未指定篩選，此 Cmdlet 會針對批次帳戶或工作，會返回所有工作。</span><span class="sxs-lookup"><span data-stu-id="30b2d-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="30b2d-134">-Id</span><span class="sxs-lookup"><span data-stu-id="30b2d-134">-Id</span></span>
<span data-ttu-id="30b2d-135">指定此 Cmdlet 所獲得之任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="30b2d-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="30b2d-136">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="30b2d-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="30b2d-137">-Job</span><span class="sxs-lookup"><span data-stu-id="30b2d-137">-Job</span></span>
<span data-ttu-id="30b2d-138">指定包含此 Cmdlet 所獲得之工作的作業。</span><span class="sxs-lookup"><span data-stu-id="30b2d-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="30b2d-139">若要取得 **PSCloudJob 物件** ，請使用 Get-AzBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30b2d-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="30b2d-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="30b2d-140">-JobId</span></span>
<span data-ttu-id="30b2d-141">指定包含此 Cmdlet 所獲得之工作的工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="30b2d-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="30b2d-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="30b2d-142">-MaxCount</span></span>
<span data-ttu-id="30b2d-143">指定要退回的任務數上限。</span><span class="sxs-lookup"><span data-stu-id="30b2d-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="30b2d-144">如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="30b2d-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="30b2d-145">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="30b2d-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="30b2d-146">-選取</span><span class="sxs-lookup"><span data-stu-id="30b2d-146">-Select</span></span>
<span data-ttu-id="30b2d-147">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="30b2d-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="30b2d-148">指定此參數的值以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="30b2d-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="30b2d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b2d-149">CommonParameters</span></span>
<span data-ttu-id="30b2d-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30b2d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b2d-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30b2d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b2d-152">輸入</span><span class="sxs-lookup"><span data-stu-id="30b2d-152">INPUTS</span></span>

### <span data-ttu-id="30b2d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="30b2d-153">System.String</span></span>

### <span data-ttu-id="30b2d-154">Microsoft.Azure.Commands.Batch。Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="30b2d-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="30b2d-155">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="30b2d-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="30b2d-156">輸出</span><span class="sxs-lookup"><span data-stu-id="30b2d-156">OUTPUTS</span></span>

### <span data-ttu-id="30b2d-157">Microsoft.Azure.Commands.Batch。Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="30b2d-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="30b2d-158">筆記</span><span class="sxs-lookup"><span data-stu-id="30b2d-158">NOTES</span></span>

## <span data-ttu-id="30b2d-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="30b2d-159">RELATED LINKS</span></span>

[<span data-ttu-id="30b2d-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="30b2d-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="30b2d-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="30b2d-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="30b2d-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="30b2d-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="30b2d-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="30b2d-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="30b2d-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="30b2d-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="30b2d-165">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="30b2d-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

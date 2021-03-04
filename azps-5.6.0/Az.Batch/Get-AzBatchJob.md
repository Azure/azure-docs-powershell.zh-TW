---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 4b570f78ddb73c7f0ab6dedcd4eca3ac26ff12df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910549"
---
# <span data-ttu-id="c0ec2-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c0ec2-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="c0ec2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ec2-103">獲得批次帳戶或工作排程的批次工作。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="c0ec2-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0ec2-104">SYNTAX</span></span>

### <span data-ttu-id="c0ec2-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="c0ec2-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0ec2-106">Id</span><span class="sxs-lookup"><span data-stu-id="c0ec2-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ec2-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="c0ec2-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0ec2-108">描述</span><span class="sxs-lookup"><span data-stu-id="c0ec2-108">DESCRIPTION</span></span>
<span data-ttu-id="c0ec2-109">**Get-AzBatchJob** Cmdlet 會取得 Batch 帳戶的 Azure Batch 工作，此工作由 *BatchAccountCoNtext* 參數指定。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="c0ec2-110">您可以使用 *Id* 參數取得單一工作。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="c0ec2-111">您可以使用 Filter參數來取得符合 OData 和 OData (的) 工作。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="c0ec2-112">如果您提供工作排程識別碼或 **PSCloudJobSchedule** 實例，此 Cmdlet 只會會回回該工作排程的工作。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="c0ec2-113">例子</span><span class="sxs-lookup"><span data-stu-id="c0ec2-113">EXAMPLES</span></span>

### <span data-ttu-id="c0ec2-114">範例 1：以識別碼取得批次工作</span><span class="sxs-lookup"><span data-stu-id="c0ec2-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 :
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="c0ec2-115">此命令會獲得具有識別碼 Job01 的工作。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="c0ec2-116">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c0ec2-117">範例 2：取得工作排程的所有使用中工作</span><span class="sxs-lookup"><span data-stu-id="c0ec2-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="c0ec2-118">此命令會針對具有 ID JobSchedule27 的工作排程，獲得使用中工作。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="c0ec2-119">範例 3：使用管線在工作排程下獲得所有工作</span><span class="sxs-lookup"><span data-stu-id="c0ec2-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="c0ec2-120">此命令會使用 Cmdlet，獲得具有 ID JobSchedule27 的工作排Get-AzBatchJobSchedule排程。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="c0ec2-121">該命令會使用管線運算子，將該工作排程傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0ec2-122">命令會獲得該工作排程的所有工作。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="c0ec2-123">參數</span><span class="sxs-lookup"><span data-stu-id="c0ec2-123">PARAMETERS</span></span>

### <span data-ttu-id="c0ec2-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="c0ec2-124">-BatchContext</span></span>
<span data-ttu-id="c0ec2-125">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c0ec2-126">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c0ec2-127">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c0ec2-128">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c0ec2-129">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c0ec2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ec2-130">-DefaultProfile</span></span>
<span data-ttu-id="c0ec2-131">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0ec2-132">-展開</span><span class="sxs-lookup"><span data-stu-id="c0ec2-132">-Expand</span></span>
<span data-ttu-id="c0ec2-133">指定 Open Data Protocol (OData) expand 子句。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="c0ec2-134">指定此參數的值，以取得您取得之主實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="c0ec2-135">-篩選</span><span class="sxs-lookup"><span data-stu-id="c0ec2-135">-Filter</span></span>
<span data-ttu-id="c0ec2-136">指定工作的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="c0ec2-137">如果您未指定篩選，此 Cmdlet 會針對批次帳戶或工作排程，會返回所有工作。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="c0ec2-138">-Id</span><span class="sxs-lookup"><span data-stu-id="c0ec2-138">-Id</span></span>
<span data-ttu-id="c0ec2-139">指定此 Cmdlet 所獲得工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="c0ec2-140">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-140">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec2-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0ec2-141">-JobSchedule</span></span>
<span data-ttu-id="c0ec2-142">指定 **PSCloudJobSchedule** 物件，代表包含工作的工作排程。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="c0ec2-143">若要取得 **PSCloudJobSchedule** 物件，請使用 Get-AzBatchJobSchedule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec2-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="c0ec2-144">-JobScheduleId</span></span>
<span data-ttu-id="c0ec2-145">指定包含工作的工作排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec2-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c0ec2-146">-MaxCount</span></span>
<span data-ttu-id="c0ec2-147">指定要退回的工作數量上限。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="c0ec2-148">如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c0ec2-149">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="c0ec2-150">-選取</span><span class="sxs-lookup"><span data-stu-id="c0ec2-150">-Select</span></span>
<span data-ttu-id="c0ec2-151">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="c0ec2-152">指定此參數的值以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="c0ec2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ec2-153">CommonParameters</span></span>
<span data-ttu-id="c0ec2-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0ec2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ec2-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0ec2-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ec2-156">輸入</span><span class="sxs-lookup"><span data-stu-id="c0ec2-156">INPUTS</span></span>

### <span data-ttu-id="c0ec2-157">System.String</span><span class="sxs-lookup"><span data-stu-id="c0ec2-157">System.String</span></span>

### <span data-ttu-id="c0ec2-158">Microsoft.Azure.Commands.Batch。Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0ec2-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="c0ec2-159">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="c0ec2-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c0ec2-160">輸出</span><span class="sxs-lookup"><span data-stu-id="c0ec2-160">OUTPUTS</span></span>

### <span data-ttu-id="c0ec2-161">Microsoft.Azure.Commands.Batch。Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="c0ec2-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="c0ec2-162">筆記</span><span class="sxs-lookup"><span data-stu-id="c0ec2-162">NOTES</span></span>

## <span data-ttu-id="c0ec2-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0ec2-163">RELATED LINKS</span></span>

[<span data-ttu-id="c0ec2-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c0ec2-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="c0ec2-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c0ec2-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="c0ec2-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c0ec2-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c0ec2-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0ec2-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="c0ec2-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c0ec2-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="c0ec2-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c0ec2-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="c0ec2-170">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c0ec2-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="c0ec2-171">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0ec2-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

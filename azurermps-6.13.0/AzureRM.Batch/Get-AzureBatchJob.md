---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: 1a5f971e52da27eb2abeca02c4362eee9b9755c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450296"
---
# <span data-ttu-id="43684-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43684-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="43684-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43684-102">SYNOPSIS</span></span>
<span data-ttu-id="43684-103">取得批次帳戶或作業排程的批次作業。</span><span class="sxs-lookup"><span data-stu-id="43684-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43684-104">句法</span><span class="sxs-lookup"><span data-stu-id="43684-104">SYNTAX</span></span>

### <span data-ttu-id="43684-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="43684-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43684-106">標識號</span><span class="sxs-lookup"><span data-stu-id="43684-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43684-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="43684-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43684-108">說明</span><span class="sxs-lookup"><span data-stu-id="43684-108">DESCRIPTION</span></span>
<span data-ttu-id="43684-109">**AzureBatchJob** Cmdlet 會針對 *BatchAccountCoNtext* 參數所指定的批次帳戶取得 Azure Batch 作業。</span><span class="sxs-lookup"><span data-stu-id="43684-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="43684-110">您可以使用 *識別碼* 參數來取得單一作業。</span><span class="sxs-lookup"><span data-stu-id="43684-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="43684-111">您可以使用 *Filter* 參數，以取得符合開放式資料通訊協定 (OData) 篩選的作業。</span><span class="sxs-lookup"><span data-stu-id="43684-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="43684-112">如果您提供作業排程 ID 或 **PSCloudJobSchedule** 實例，這個 Cmdlet 只會傳回該作業排程的工作。</span><span class="sxs-lookup"><span data-stu-id="43684-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="43684-113">示例</span><span class="sxs-lookup"><span data-stu-id="43684-113">EXAMPLES</span></span>

### <span data-ttu-id="43684-114">範例1：透過識別碼取得批次作業</span><span class="sxs-lookup"><span data-stu-id="43684-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
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

<span data-ttu-id="43684-115">這個命令會取得 ID 為 Job01 的作業。</span><span class="sxs-lookup"><span data-stu-id="43684-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="43684-116">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="43684-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="43684-117">範例2：取得作業排程的所有活動作業</span><span class="sxs-lookup"><span data-stu-id="43684-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="43684-118">這個命令會取得具有識別碼 JobSchedule27 之作業排程的作用中作業。</span><span class="sxs-lookup"><span data-stu-id="43684-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="43684-119">範例3：使用管線在作業排程下取得所有作業</span><span class="sxs-lookup"><span data-stu-id="43684-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
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

<span data-ttu-id="43684-120">這個命令會透過使用 Get-AzureBatchJobSchedule Cmdlet 來取得 ID 為 JobSchedule27 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="43684-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="43684-121">透過使用管線運算子，命令會將作業排程傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43684-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43684-122">此命令會取得該作業排程的所有作業。</span><span class="sxs-lookup"><span data-stu-id="43684-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="43684-123">參數</span><span class="sxs-lookup"><span data-stu-id="43684-123">PARAMETERS</span></span>

### <span data-ttu-id="43684-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="43684-124">-BatchContext</span></span>
<span data-ttu-id="43684-125">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="43684-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="43684-126">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="43684-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="43684-127">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="43684-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="43684-128">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="43684-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="43684-129">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="43684-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="43684-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43684-130">-DefaultProfile</span></span>
<span data-ttu-id="43684-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43684-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43684-132">-展開</span><span class="sxs-lookup"><span data-stu-id="43684-132">-Expand</span></span>
<span data-ttu-id="43684-133">指定 (OData) expand 子句中的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="43684-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="43684-134">指定此參數的值，以取得您所取得之主要實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="43684-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="43684-135">-篩選</span><span class="sxs-lookup"><span data-stu-id="43684-135">-Filter</span></span>
<span data-ttu-id="43684-136">指定作業的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="43684-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="43684-137">如果您沒有指定篩選，此 Cmdlet 會傳回批次帳戶或作業排程的所有作業。</span><span class="sxs-lookup"><span data-stu-id="43684-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="43684-138">-識別碼</span><span class="sxs-lookup"><span data-stu-id="43684-138">-Id</span></span>
<span data-ttu-id="43684-139">指定此 Cmdlet 所取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="43684-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="43684-140">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="43684-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="43684-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="43684-141">-JobSchedule</span></span>
<span data-ttu-id="43684-142">指定代表包含工作之作業排程的 **PSCloudJobSchedule** 物件。</span><span class="sxs-lookup"><span data-stu-id="43684-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="43684-143">若要取得 **PSCloudJobSchedule** 物件，請使用 Get-AzureBatchJobSchedule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43684-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="43684-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="43684-144">-JobScheduleId</span></span>
<span data-ttu-id="43684-145">指定包含工作的作業排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="43684-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="43684-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="43684-146">-MaxCount</span></span>
<span data-ttu-id="43684-147">指定要傳回的作業數目上限。</span><span class="sxs-lookup"><span data-stu-id="43684-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="43684-148">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="43684-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="43684-149">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="43684-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="43684-150">-選取</span><span class="sxs-lookup"><span data-stu-id="43684-150">-Select</span></span>
<span data-ttu-id="43684-151">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="43684-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="43684-152">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="43684-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="43684-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43684-153">CommonParameters</span></span>
<span data-ttu-id="43684-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43684-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43684-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43684-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43684-156">輸入</span><span class="sxs-lookup"><span data-stu-id="43684-156">INPUTS</span></span>

### <span data-ttu-id="43684-157">System.object</span><span class="sxs-lookup"><span data-stu-id="43684-157">System.String</span></span>

### <span data-ttu-id="43684-158">Microsoft.Azure.Commands.Batch。PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="43684-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="43684-159">參數： JobSchedule (ByValue) </span><span class="sxs-lookup"><span data-stu-id="43684-159">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="43684-160">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="43684-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="43684-161">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="43684-161">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="43684-162">輸出</span><span class="sxs-lookup"><span data-stu-id="43684-162">OUTPUTS</span></span>

### <span data-ttu-id="43684-163">Microsoft.Azure.Commands.Batch。PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="43684-163">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="43684-164">筆記</span><span class="sxs-lookup"><span data-stu-id="43684-164">NOTES</span></span>

## <span data-ttu-id="43684-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="43684-165">RELATED LINKS</span></span>

[<span data-ttu-id="43684-166">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43684-166">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="43684-167">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43684-167">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="43684-168">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="43684-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="43684-169">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="43684-169">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="43684-170">新-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43684-170">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="43684-171">移除-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43684-171">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="43684-172">停止 AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43684-172">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="43684-173">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="43684-173">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: dcfbfe698889b4e918fddb54bfdce41e73cd5e5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450295"
---
# <span data-ttu-id="9489f-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="9489f-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="9489f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9489f-102">SYNOPSIS</span></span>
<span data-ttu-id="9489f-103">取得批次工作準備與發行任務狀態。</span><span class="sxs-lookup"><span data-stu-id="9489f-103">Gets Batch job preparation and release task status.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9489f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9489f-104">SYNTAX</span></span>

### <span data-ttu-id="9489f-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="9489f-105">Id (Default)</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9489f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9489f-106">InputObject</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9489f-107">說明</span><span class="sxs-lookup"><span data-stu-id="9489f-107">DESCRIPTION</span></span>
<span data-ttu-id="9489f-108">**AzureBatchJobPreparationAndReleaseTaskStatus** Cmdlet 會取得批次作業的 Azure Batch 作業準備與釋放工作狀態。</span><span class="sxs-lookup"><span data-stu-id="9489f-108">The **Get-AzureBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="9489f-109">您必須將 *識別碼* 參數或 **PSCloudJob** 實例提供給這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9489f-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="9489f-110">示例</span><span class="sxs-lookup"><span data-stu-id="9489f-110">EXAMPLES</span></span>

### <span data-ttu-id="9489f-111">範例1：取得工作的工作準備與發行狀態</span><span class="sxs-lookup"><span data-stu-id="9489f-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="9489f-112">這個命令會取得作業「Test」的工作準備與發行任務狀態。</span><span class="sxs-lookup"><span data-stu-id="9489f-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="9489f-113">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="9489f-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9489f-114">範例2：使用篩選來取得工作的工作準備與發行狀態，並選取 [已指定]</span><span class="sxs-lookup"><span data-stu-id="9489f-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="9489f-115">這個命令會在節點「tvm-2316545714_1-20170613t201733z」上取得作業「Test」的工作準備與發行任務狀態，並使用 Select 子句指定僅傳回 JobPreparationTaskExecutionInformation 資訊</span><span class="sxs-lookup"><span data-stu-id="9489f-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="9489f-116">參數</span><span class="sxs-lookup"><span data-stu-id="9489f-116">PARAMETERS</span></span>

### <span data-ttu-id="9489f-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9489f-117">-BatchContext</span></span>
<span data-ttu-id="9489f-118">與批次服務互動時要使用的 BatchAccountCoNtext 實例。</span><span class="sxs-lookup"><span data-stu-id="9489f-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="9489f-119">使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="9489f-119">Use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="9489f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9489f-120">-DefaultProfile</span></span>
<span data-ttu-id="9489f-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9489f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9489f-122">-展開</span><span class="sxs-lookup"><span data-stu-id="9489f-122">-Expand</span></span>
<span data-ttu-id="9489f-123">指定 (OData) expand 子句中的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9489f-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="9489f-124">指定此參數的值，以取得您所取得之主要實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="9489f-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="9489f-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="9489f-125">-Filter</span></span>
<span data-ttu-id="9489f-126">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="9489f-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="9489f-127">如果您沒有指定篩選，此 Cmdlet 會傳回作業的所有工作準備與發行任務狀態。</span><span class="sxs-lookup"><span data-stu-id="9489f-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="9489f-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9489f-128">-Id</span></span>
<span data-ttu-id="9489f-129">指定要檢索其準備與發行工作的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="9489f-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="9489f-130">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="9489f-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9489f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9489f-131">-InputObject</span></span>
<span data-ttu-id="9489f-132">指定代表作業的 **PSCloudJob** 物件，以取得準備與發行任務狀態。</span><span class="sxs-lookup"><span data-stu-id="9489f-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="9489f-133">若要取得 **PSCloudJob** 物件，請使用 Get-AzureBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9489f-133">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9489f-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9489f-134">-MaxCount</span></span>
<span data-ttu-id="9489f-135">指定要傳回的工作準備與發行任務狀態的數目上限。</span><span class="sxs-lookup"><span data-stu-id="9489f-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="9489f-136">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="9489f-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="9489f-137">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="9489f-137">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9489f-138">-選取</span><span class="sxs-lookup"><span data-stu-id="9489f-138">-Select</span></span>
<span data-ttu-id="9489f-139">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="9489f-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="9489f-140">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="9489f-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="9489f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9489f-141">CommonParameters</span></span>
<span data-ttu-id="9489f-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9489f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9489f-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9489f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9489f-144">輸入</span><span class="sxs-lookup"><span data-stu-id="9489f-144">INPUTS</span></span>

### <span data-ttu-id="9489f-145">Microsoft.Azure.Commands.Batch。PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="9489f-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="9489f-146">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9489f-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9489f-147">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9489f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="9489f-148">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9489f-148">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="9489f-149">輸出</span><span class="sxs-lookup"><span data-stu-id="9489f-149">OUTPUTS</span></span>

### <span data-ttu-id="9489f-150">Microsoft.Azure.Commands.Batch。PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="9489f-150">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="9489f-151">筆記</span><span class="sxs-lookup"><span data-stu-id="9489f-151">NOTES</span></span>

## <span data-ttu-id="9489f-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9489f-152">RELATED LINKS</span></span>

[<span data-ttu-id="9489f-153">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9489f-153">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="9489f-154">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9489f-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
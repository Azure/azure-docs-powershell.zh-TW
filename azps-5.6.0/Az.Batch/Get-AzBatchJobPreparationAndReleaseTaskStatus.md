---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: e85976b4d4b5de508e1a4f25338b21abdb0c097f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909789"
---
# <span data-ttu-id="6d182-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="6d182-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="6d182-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6d182-102">SYNOPSIS</span></span>
<span data-ttu-id="6d182-103">獲得批次工作準備和釋出工作狀態。</span><span class="sxs-lookup"><span data-stu-id="6d182-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="6d182-104">語法</span><span class="sxs-lookup"><span data-stu-id="6d182-104">SYNTAX</span></span>

### <span data-ttu-id="6d182-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="6d182-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d182-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6d182-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d182-107">描述</span><span class="sxs-lookup"><span data-stu-id="6d182-107">DESCRIPTION</span></span>
<span data-ttu-id="6d182-108">**Get-AzBatchJobPreparationAndReleaseTaskStatus** Cmdlet 會取得批次工作的 Azure Batch 工作準備和發行工作狀態。</span><span class="sxs-lookup"><span data-stu-id="6d182-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="6d182-109">您必須為此 *Cmdlet* 提供 Id 參數或 **PSCloudJob** 實例。</span><span class="sxs-lookup"><span data-stu-id="6d182-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="6d182-110">例子</span><span class="sxs-lookup"><span data-stu-id="6d182-110">EXAMPLES</span></span>

### <span data-ttu-id="6d182-111">範例 1：取得工作的準備工作和釋出狀態</span><span class="sxs-lookup"><span data-stu-id="6d182-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="6d182-112">此命令會針對工作「測試」獲得工作準備和釋出工作狀態。</span><span class="sxs-lookup"><span data-stu-id="6d182-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="6d182-113">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="6d182-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6d182-114">範例 2：使用指定篩選和選取來取得工作的工作準備和發行狀態</span><span class="sxs-lookup"><span data-stu-id="6d182-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="6d182-115">此命令會獲得節點 "tvm-2316545714_1-20170613t201733z" 上的工作準備和發行工作狀態，並使用 Select 子句指定只傳回 JobPreparationTaskExecutionInformation 資訊</span><span class="sxs-lookup"><span data-stu-id="6d182-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="6d182-116">參數</span><span class="sxs-lookup"><span data-stu-id="6d182-116">PARAMETERS</span></span>

### <span data-ttu-id="6d182-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="6d182-117">-BatchContext</span></span>
<span data-ttu-id="6d182-118">BatchAccountCoNtext 實例，用於與批次處理服務互動。</span><span class="sxs-lookup"><span data-stu-id="6d182-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="6d182-119">使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="6d182-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="6d182-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d182-120">-DefaultProfile</span></span>
<span data-ttu-id="6d182-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d182-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d182-122">-展開</span><span class="sxs-lookup"><span data-stu-id="6d182-122">-Expand</span></span>
<span data-ttu-id="6d182-123">指定 Open Data Protocol (OData) expand 子句。</span><span class="sxs-lookup"><span data-stu-id="6d182-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="6d182-124">指定此參數的值，以取得您取得之主實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="6d182-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="6d182-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="6d182-125">-Filter</span></span>
<span data-ttu-id="6d182-126">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="6d182-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="6d182-127">如果您未指定篩選，此 Cmdlet 會針對該工作，會返回所有工作準備和釋出工作狀態。</span><span class="sxs-lookup"><span data-stu-id="6d182-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="6d182-128">-Id</span><span class="sxs-lookup"><span data-stu-id="6d182-128">-Id</span></span>
<span data-ttu-id="6d182-129">指定應取回準備和釋出工作的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d182-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="6d182-130">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="6d182-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="6d182-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d182-131">-InputObject</span></span>
<span data-ttu-id="6d182-132">指定 **PSCloudJob 物件** ，代表工作以取得準備和釋出工作狀態。</span><span class="sxs-lookup"><span data-stu-id="6d182-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="6d182-133">若要取得 **PSCloudJob 物件** ，請使用 Get-AzBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d182-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="6d182-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6d182-134">-MaxCount</span></span>
<span data-ttu-id="6d182-135">指定要退回的工作準備和釋出工作狀態數量上限。</span><span class="sxs-lookup"><span data-stu-id="6d182-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="6d182-136">如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="6d182-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6d182-137">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="6d182-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="6d182-138">-選取</span><span class="sxs-lookup"><span data-stu-id="6d182-138">-Select</span></span>
<span data-ttu-id="6d182-139">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="6d182-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="6d182-140">指定此參數的值以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="6d182-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="6d182-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d182-141">CommonParameters</span></span>
<span data-ttu-id="6d182-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6d182-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d182-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d182-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d182-144">輸入</span><span class="sxs-lookup"><span data-stu-id="6d182-144">INPUTS</span></span>

### <span data-ttu-id="6d182-145">Microsoft.Azure.Commands.Batch。Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="6d182-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="6d182-146">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="6d182-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6d182-147">輸出</span><span class="sxs-lookup"><span data-stu-id="6d182-147">OUTPUTS</span></span>

### <span data-ttu-id="6d182-148">Microsoft.Azure.Commands.Batch。Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="6d182-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="6d182-149">筆記</span><span class="sxs-lookup"><span data-stu-id="6d182-149">NOTES</span></span>

## <span data-ttu-id="6d182-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d182-150">RELATED LINKS</span></span>

[<span data-ttu-id="6d182-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6d182-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="6d182-152">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6d182-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 294669fe5b9e5aeb01dfbfa7ab538a0f6d411cca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917425"
---
# <span data-ttu-id="3636d-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="3636d-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="3636d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3636d-102">SYNOPSIS</span></span>
<span data-ttu-id="3636d-103">獲得指定工作的任務計數。</span><span class="sxs-lookup"><span data-stu-id="3636d-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="3636d-104">語法</span><span class="sxs-lookup"><span data-stu-id="3636d-104">SYNTAX</span></span>

### <span data-ttu-id="3636d-105">Id</span><span class="sxs-lookup"><span data-stu-id="3636d-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3636d-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="3636d-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3636d-107">描述</span><span class="sxs-lookup"><span data-stu-id="3636d-107">DESCRIPTION</span></span>
<span data-ttu-id="3636d-108">**Get-AzBatchTaskCount** Cmdlet 會取得批次工作的 Azure 批次工作計數。</span><span class="sxs-lookup"><span data-stu-id="3636d-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="3636d-109">使用 *JobId* 參數或 Job 參數 *指定* 工作。</span><span class="sxs-lookup"><span data-stu-id="3636d-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="3636d-110">任務計數會根據進行中、執行或已完成的任務狀態提供工作計數，以及成功或失敗的任務計數。</span><span class="sxs-lookup"><span data-stu-id="3636d-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="3636d-111">準備狀態中的工作會計算為執行中。</span><span class="sxs-lookup"><span data-stu-id="3636d-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="3636d-112">如果 validationStatus 未驗證，則批次服務無法根據清單工作 API 中報告的工作狀態檢查狀態計數。</span><span class="sxs-lookup"><span data-stu-id="3636d-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="3636d-113">如果工作包含超過 200，000 個任務，則 validationStatus 可能未驗證。</span><span class="sxs-lookup"><span data-stu-id="3636d-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="3636d-114">例子</span><span class="sxs-lookup"><span data-stu-id="3636d-114">EXAMPLES</span></span>

### <span data-ttu-id="3636d-115">範例 1：根據識別碼取得任務計數</span><span class="sxs-lookup"><span data-stu-id="3636d-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="3636d-116">此命令會計算 Job Job01 的工作計數。</span><span class="sxs-lookup"><span data-stu-id="3636d-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="3636d-117">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="3636d-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="3636d-118">參數</span><span class="sxs-lookup"><span data-stu-id="3636d-118">PARAMETERS</span></span>

### <span data-ttu-id="3636d-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="3636d-119">-BatchContext</span></span>
<span data-ttu-id="3636d-120">BatchAccountCoNtext 實例，用於與批次處理服務互動。</span><span class="sxs-lookup"><span data-stu-id="3636d-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="3636d-121">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="3636d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="3636d-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="3636d-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="3636d-123">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3636d-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="3636d-124">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="3636d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3636d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3636d-125">-DefaultProfile</span></span>
<span data-ttu-id="3636d-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3636d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3636d-127">-Job</span><span class="sxs-lookup"><span data-stu-id="3636d-127">-Job</span></span>
<span data-ttu-id="3636d-128">指定包含此 Cmdlet 所獲得之工作的作業。</span><span class="sxs-lookup"><span data-stu-id="3636d-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="3636d-129">若要取得 **PSCloudJob 物件** ，請使用 Get-AzBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3636d-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="3636d-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="3636d-130">-JobId</span></span>
<span data-ttu-id="3636d-131">要取得工作計數的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="3636d-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3636d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3636d-132">CommonParameters</span></span>
<span data-ttu-id="3636d-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3636d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3636d-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3636d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3636d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3636d-135">INPUTS</span></span>

### <span data-ttu-id="3636d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3636d-136">System.String</span></span>

### <span data-ttu-id="3636d-137">Microsoft.Azure.Commands.Batch。Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="3636d-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="3636d-138">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="3636d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3636d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="3636d-139">OUTPUTS</span></span>

### <span data-ttu-id="3636d-140">Microsoft.Azure.Commands.Batch。Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="3636d-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="3636d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="3636d-141">NOTES</span></span>

## <span data-ttu-id="3636d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="3636d-142">RELATED LINKS</span></span>

[<span data-ttu-id="3636d-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3636d-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3636d-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3636d-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="3636d-145">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3636d-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129647"
---
# <span data-ttu-id="f3a0d-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="f3a0d-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="f3a0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a0d-103">取得指定工作的任務計數。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="f3a0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3a0d-104">SYNTAX</span></span>

### <span data-ttu-id="f3a0d-105">標識號</span><span class="sxs-lookup"><span data-stu-id="f3a0d-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a0d-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="f3a0d-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3a0d-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3a0d-107">DESCRIPTION</span></span>
<span data-ttu-id="f3a0d-108">**AzBatchTaskCount** Cmdlet 會取得批次作業的 Azure Batch 任務計數。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="f3a0d-109">使用 *JobId* 參數或 *作業* 參數指定作業。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="f3a0d-110">[任務計數]：依活動、執行或已完成的任務狀態，以及成功或失敗的任務計數，提供任務的計數。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="f3a0d-111">準備狀態中的工作會計算為正在執行。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="f3a0d-112">如果 validationStatus 是 unvalidated，則批次服務無法針對清單任務 API 中所報告的任務狀態檢查狀態計數。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="f3a0d-113">如果工作包含200000以上的任務，可能會 unvalidated validationStatus。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="f3a0d-114">示例</span><span class="sxs-lookup"><span data-stu-id="f3a0d-114">EXAMPLES</span></span>

### <span data-ttu-id="f3a0d-115">範例1：依識別碼取得任務計數</span><span class="sxs-lookup"><span data-stu-id="f3a0d-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="f3a0d-116">這個命令會取得工作 Job01 的任務計數。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="f3a0d-117">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f3a0d-118">參數</span><span class="sxs-lookup"><span data-stu-id="f3a0d-118">PARAMETERS</span></span>

### <span data-ttu-id="f3a0d-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="f3a0d-119">-BatchContext</span></span>
<span data-ttu-id="f3a0d-120">與批次服務互動時要使用的 BatchAccountCoNtext 實例。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="f3a0d-121">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="f3a0d-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="f3a0d-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="f3a0d-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f3a0d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a0d-125">-DefaultProfile</span></span>
<span data-ttu-id="f3a0d-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3a0d-127">-工作</span><span class="sxs-lookup"><span data-stu-id="f3a0d-127">-Job</span></span>
<span data-ttu-id="f3a0d-128">指定包含此 Cmdlet 所取得之任務的工作。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="f3a0d-129">若要取得 **PSCloudJob** 物件，請使用 Get-AzBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="f3a0d-130">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="f3a0d-130">-JobId</span></span>
<span data-ttu-id="f3a0d-131">要取得其任務計數的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="f3a0d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a0d-132">CommonParameters</span></span>
<span data-ttu-id="f3a0d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a0d-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f3a0d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a0d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f3a0d-135">INPUTS</span></span>

### <span data-ttu-id="f3a0d-136">System.object</span><span class="sxs-lookup"><span data-stu-id="f3a0d-136">System.String</span></span>

### <span data-ttu-id="f3a0d-137">Microsoft.Azure.Commands.Batch。PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="f3a0d-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="f3a0d-138">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="f3a0d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f3a0d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f3a0d-139">OUTPUTS</span></span>

### <span data-ttu-id="f3a0d-140">Microsoft.Azure.Commands.Batch。PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="f3a0d-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="f3a0d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f3a0d-141">NOTES</span></span>

## <span data-ttu-id="f3a0d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3a0d-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3a0d-143">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f3a0d-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f3a0d-144">AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f3a0d-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="f3a0d-145">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f3a0d-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
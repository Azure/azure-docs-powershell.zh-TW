---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446511"
---
# <span data-ttu-id="9cb62-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="9cb62-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="9cb62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cb62-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb62-103">取得指定工作的任務計數。</span><span class="sxs-lookup"><span data-stu-id="9cb62-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cb62-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cb62-104">SYNTAX</span></span>

### <span data-ttu-id="9cb62-105">標識號</span><span class="sxs-lookup"><span data-stu-id="9cb62-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="9cb62-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="9cb62-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="9cb62-107">說明</span><span class="sxs-lookup"><span data-stu-id="9cb62-107">DESCRIPTION</span></span>
<span data-ttu-id="9cb62-108">**AzureBatchTaskCounts** Cmdlet 會取得批次作業的 Azure Batch 任務計數。</span><span class="sxs-lookup"><span data-stu-id="9cb62-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="9cb62-109">使用 *JobId* 參數或 *作業* 參數指定作業。</span><span class="sxs-lookup"><span data-stu-id="9cb62-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="9cb62-110">[任務計數]：依活動、執行或已完成的任務狀態，以及成功或失敗的任務計數，提供任務的計數。</span><span class="sxs-lookup"><span data-stu-id="9cb62-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="9cb62-111">準備狀態中的工作會計算為正在執行。</span><span class="sxs-lookup"><span data-stu-id="9cb62-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="9cb62-112">如果 validationStatus 是 unvalidated，則批次服務無法針對清單任務 API 中所報告的任務狀態檢查狀態計數。</span><span class="sxs-lookup"><span data-stu-id="9cb62-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="9cb62-113">如果工作包含200000以上的任務，可能會 unvalidated validationStatus。</span><span class="sxs-lookup"><span data-stu-id="9cb62-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="9cb62-114">示例</span><span class="sxs-lookup"><span data-stu-id="9cb62-114">EXAMPLES</span></span>

### <span data-ttu-id="9cb62-115">範例1：依識別碼取得任務計數</span><span class="sxs-lookup"><span data-stu-id="9cb62-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="9cb62-116">這個命令會取得工作 Job01 的任務計數。</span><span class="sxs-lookup"><span data-stu-id="9cb62-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="9cb62-117">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="9cb62-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9cb62-118">參數</span><span class="sxs-lookup"><span data-stu-id="9cb62-118">PARAMETERS</span></span>

### <span data-ttu-id="9cb62-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9cb62-119">-BatchContext</span></span>
<span data-ttu-id="9cb62-120">與批次服務互動時要使用的 BatchAccountCoNtext 實例。</span><span class="sxs-lookup"><span data-stu-id="9cb62-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="9cb62-121">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="9cb62-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="9cb62-122">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="9cb62-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="9cb62-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9cb62-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="9cb62-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="9cb62-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb62-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb62-125">-DefaultProfile</span></span>
<span data-ttu-id="9cb62-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cb62-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cb62-127">-工作</span><span class="sxs-lookup"><span data-stu-id="9cb62-127">-Job</span></span>
<span data-ttu-id="9cb62-128">指定包含此 Cmdlet 所取得之任務的工作。</span><span class="sxs-lookup"><span data-stu-id="9cb62-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="9cb62-129">若要取得 **PSCloudJob** 物件，請使用 Get-AzureBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cb62-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb62-130">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="9cb62-130">-JobId</span></span>
<span data-ttu-id="9cb62-131">要取得其任務計數的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="9cb62-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="9cb62-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9cb62-132">INPUTS</span></span>

### <span data-ttu-id="9cb62-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9cb62-133">System.String</span></span>
<span data-ttu-id="9cb62-134">Microsoft.Azure.Commands.Batch。PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9cb62-134">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>


## <span data-ttu-id="9cb62-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9cb62-135">OUTPUTS</span></span>

### <span data-ttu-id="9cb62-136">Microsoft.Azure.Commands.Batch。PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="9cb62-136">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>


## <span data-ttu-id="9cb62-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9cb62-137">NOTES</span></span>

## <span data-ttu-id="9cb62-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cb62-138">RELATED LINKS</span></span>

[<span data-ttu-id="9cb62-139">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9cb62-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9cb62-140">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9cb62-140">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="9cb62-141">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9cb62-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
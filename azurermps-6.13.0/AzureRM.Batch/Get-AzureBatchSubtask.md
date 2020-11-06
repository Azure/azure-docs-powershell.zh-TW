---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 5aa0ccc7da257cf20deb4a79d2b5415aa4c45885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453887"
---
# <span data-ttu-id="6f3f0-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="6f3f0-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="6f3f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f3f0-102">SYNOPSIS</span></span>
<span data-ttu-id="6f3f0-103">取得指定工作的子任務資訊。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f3f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f3f0-104">SYNTAX</span></span>

### <span data-ttu-id="6f3f0-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="6f3f0-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f3f0-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="6f3f0-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f3f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="6f3f0-107">DESCRIPTION</span></span>
<span data-ttu-id="6f3f0-108">**AzureBatchSubtask** Cmdlet 會檢索指定工作的子任務資訊。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="6f3f0-109">子任務為個別工作提供並行處理，並啟用任務執行與進度的精確監視。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="6f3f0-110">示例</span><span class="sxs-lookup"><span data-stu-id="6f3f0-110">EXAMPLES</span></span>

### <span data-ttu-id="6f3f0-111">範例1：傳回指定工作的所有子任務</span><span class="sxs-lookup"><span data-stu-id="6f3f0-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="6f3f0-112">這些命令會傳回具有識別碼 myTask 之工作的所有子任務。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="6f3f0-113">若要這樣做，範例中的第一個命令會針對批次帳戶 contosobatchaccount 建立帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="6f3f0-114">這個物件參照會儲存在名為 $coNtext 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="6f3f0-115">然後，第二個命令會使用該物件參照和 **AzureBatchSubtask** Cmdlet 傳回 myTask 的所有子任務，該工作是作為作業作業-01 的一部分執行。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="6f3f0-116">參數</span><span class="sxs-lookup"><span data-stu-id="6f3f0-116">PARAMETERS</span></span>

### <span data-ttu-id="6f3f0-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="6f3f0-117">-BatchContext</span></span>
<span data-ttu-id="6f3f0-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6f3f0-119">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6f3f0-120">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6f3f0-121">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6f3f0-122">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6f3f0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f3f0-123">-DefaultProfile</span></span>
<span data-ttu-id="6f3f0-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f3f0-125">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="6f3f0-125">-JobId</span></span>
<span data-ttu-id="6f3f0-126">指定包含此 Cmdlet 所取得之子任務之工作的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f3f0-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6f3f0-127">-MaxCount</span></span>
<span data-ttu-id="6f3f0-128">指定要傳回的子任務數上限。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="6f3f0-129">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6f3f0-130">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="6f3f0-131">-任務</span><span class="sxs-lookup"><span data-stu-id="6f3f0-131">-Task</span></span>
<span data-ttu-id="6f3f0-132">指定包含此 Cmdlet 傳回之子任務之工作的物件參照。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="6f3f0-133">這個物件參照是使用 Get-AzureBatchTask Cmdlet 建立，並將傳回的物件儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-133">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f3f0-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="6f3f0-134">-TaskId</span></span>
<span data-ttu-id="6f3f0-135">指定此 Cmdlet 傳回之子任務的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f3f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f3f0-136">CommonParameters</span></span>
<span data-ttu-id="6f3f0-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f3f0-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f3f0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f3f0-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6f3f0-139">INPUTS</span></span>

### <span data-ttu-id="6f3f0-140">System.object</span><span class="sxs-lookup"><span data-stu-id="6f3f0-140">System.String</span></span>

### <span data-ttu-id="6f3f0-141">Microsoft.Azure.Commands.Batch。PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6f3f0-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="6f3f0-142">參數： Task (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6f3f0-142">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="6f3f0-143">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="6f3f0-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6f3f0-144">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6f3f0-144">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6f3f0-145">輸出</span><span class="sxs-lookup"><span data-stu-id="6f3f0-145">OUTPUTS</span></span>

### <span data-ttu-id="6f3f0-146">Microsoft.Azure.Commands.Batch。PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="6f3f0-146">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="6f3f0-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6f3f0-147">NOTES</span></span>

## <span data-ttu-id="6f3f0-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f3f0-148">RELATED LINKS</span></span>

[<span data-ttu-id="6f3f0-149">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6f3f0-149">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


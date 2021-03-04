---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 622b25a4cd84fcdd6ffb8179b3990ac786733e06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911761"
---
# <span data-ttu-id="bbbc3-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="bbbc3-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="bbbc3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bbbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="bbbc3-103">獲得指定任務的子任務資訊。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="bbbc3-104">語法</span><span class="sxs-lookup"><span data-stu-id="bbbc3-104">SYNTAX</span></span>

### <span data-ttu-id="bbbc3-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="bbbc3-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbbc3-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="bbbc3-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbbc3-107">描述</span><span class="sxs-lookup"><span data-stu-id="bbbc3-107">DESCRIPTION</span></span>
<span data-ttu-id="bbbc3-108">**Get-AzBatchSubtask** Cmdlet 會取得指定工作之子任務資訊。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="bbbc3-109">子任務可提供個別任務的平行處理，並啟用任務執行與進度的精確監控。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="bbbc3-110">例子</span><span class="sxs-lookup"><span data-stu-id="bbbc3-110">EXAMPLES</span></span>

### <span data-ttu-id="bbbc3-111">範例 1：針對指定任務返回所有子任務</span><span class="sxs-lookup"><span data-stu-id="bbbc3-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="bbbc3-112">這些命令會以 ID myTask 來返回工作的所有子任務。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="bbbc3-113">若要這麼做，範例中的第一個命令會建立批次帳戶 contosobatchaccount 帳戶金鑰的物件參照。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="bbbc3-114">此物件參照會儲存在名為 $coNtext 的$coNtext。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="bbbc3-115">接著，第二個命令會使用該物件參照和 **Get-AzBatchSubtask** Cmdlet，以返回 myTask 的所有子任務，此工作會做為 Job-01 的一部分執行。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="bbbc3-116">參數</span><span class="sxs-lookup"><span data-stu-id="bbbc3-116">PARAMETERS</span></span>

### <span data-ttu-id="bbbc3-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="bbbc3-117">-BatchContext</span></span>
<span data-ttu-id="bbbc3-118">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bbbc3-119">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bbbc3-120">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bbbc3-121">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bbbc3-122">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bbbc3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbbc3-123">-DefaultProfile</span></span>
<span data-ttu-id="bbbc3-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbbc3-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="bbbc3-125">-JobId</span></span>
<span data-ttu-id="bbbc3-126">指定包含此 Cmdlet 子任務之工作的工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="bbbc3-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bbbc3-127">-MaxCount</span></span>
<span data-ttu-id="bbbc3-128">指定要退回的子任務數上限。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="bbbc3-129">如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="bbbc3-130">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="bbbc3-131">-工作</span><span class="sxs-lookup"><span data-stu-id="bbbc3-131">-Task</span></span>
<span data-ttu-id="bbbc3-132">指定包含此 Cmdlet 所返回之子任務之工作的物件參照。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="bbbc3-133">此物件參照是使用 Cmdlet Get-AzBatchTask將所返回的物件儲存于變數中來建立。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="bbbc3-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="bbbc3-134">-TaskId</span></span>
<span data-ttu-id="bbbc3-135">指定此 Cmdlet 會返回其子任務的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="bbbc3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbbc3-136">CommonParameters</span></span>
<span data-ttu-id="bbbc3-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bbbc3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbbc3-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbbc3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbbc3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bbbc3-139">INPUTS</span></span>

### <span data-ttu-id="bbbc3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bbbc3-140">System.String</span></span>

### <span data-ttu-id="bbbc3-141">Microsoft.Azure.Commands.Batch。Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bbbc3-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="bbbc3-142">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="bbbc3-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bbbc3-143">輸出</span><span class="sxs-lookup"><span data-stu-id="bbbc3-143">OUTPUTS</span></span>

### <span data-ttu-id="bbbc3-144">Microsoft.Azure.Commands.Batch。Models.PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="bbbc3-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="bbbc3-145">筆記</span><span class="sxs-lookup"><span data-stu-id="bbbc3-145">NOTES</span></span>

## <span data-ttu-id="bbbc3-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbbc3-146">RELATED LINKS</span></span>

[<span data-ttu-id="bbbc3-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bbbc3-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)



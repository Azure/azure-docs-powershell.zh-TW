---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 1e7438195b0749dabc5206238a32bc00be03ea31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912913"
---
# <span data-ttu-id="f53a8-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="f53a8-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="f53a8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f53a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f53a8-103">停用指定計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="f53a8-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="f53a8-104">語法</span><span class="sxs-lookup"><span data-stu-id="f53a8-104">SYNTAX</span></span>

### <span data-ttu-id="f53a8-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="f53a8-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f53a8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f53a8-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f53a8-107">描述</span><span class="sxs-lookup"><span data-stu-id="f53a8-107">DESCRIPTION</span></span>
<span data-ttu-id="f53a8-108">**Disable-AzBatchComputeNodeScheduling** Cmdlet 會停用指定計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="f53a8-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="f53a8-109">計算節點是專屬於特定應用程式工作負載的 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f53a8-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="f53a8-110">當您停用計算節點上的任務排程時，您也可以選擇決定對節點工作佇列中目前的工作執行什麼處理。</span><span class="sxs-lookup"><span data-stu-id="f53a8-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="f53a8-111">**Disable-AzBatchComputeNodeScheduling** 可讓您執行下列操作：</span><span class="sxs-lookup"><span data-stu-id="f53a8-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="f53a8-112">終止工作並放回工作佇列。</span><span class="sxs-lookup"><span data-stu-id="f53a8-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="f53a8-113">這可讓這些任務在另一個計算節點上重新排期。</span><span class="sxs-lookup"><span data-stu-id="f53a8-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="f53a8-114">終止工作，並從工作佇列移除工作。</span><span class="sxs-lookup"><span data-stu-id="f53a8-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="f53a8-115">以這種方式停止的工作將不會重新排期。</span><span class="sxs-lookup"><span data-stu-id="f53a8-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="f53a8-116">等待目前執行的所有工作完成，然後停用計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="f53a8-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="f53a8-117">等待所有執行中的工作完成，所有資料保留期間到期，然後停用計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="f53a8-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="f53a8-118">例子</span><span class="sxs-lookup"><span data-stu-id="f53a8-118">EXAMPLES</span></span>

### <span data-ttu-id="f53a8-119">範例 1：停用計算節點上的任務排程</span><span class="sxs-lookup"><span data-stu-id="f53a8-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="f53a8-120">這些命令會停用計算節點 tvm-1783593343_34-20151117t222514z 上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="f53a8-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="f53a8-121">若要這麼做，範例中的第一個命令會建立批次帳戶 contosobatchaccount 帳戶金鑰的物件參照。</span><span class="sxs-lookup"><span data-stu-id="f53a8-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="f53a8-122">此物件參照會儲存在名為 $coNtext 的$coNtext。</span><span class="sxs-lookup"><span data-stu-id="f53a8-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="f53a8-123">接著，第二個命令會使用此物件參照和 **Disable-AzBatchComputeNodeScheduling** Cmdlet 連線到 myPool 資料庫，並停用節點 tvm-1783593343_34-20151117t222514z 上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="f53a8-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="f53a8-124">由於 *DisableComputeNodeSchedulingOptions* 參數並未包含任何目前在計算節點上執行的工作，因此將會重新叫用。</span><span class="sxs-lookup"><span data-stu-id="f53a8-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="f53a8-125">範例 2：停用資料集中所有計算節點上的任務排程</span><span class="sxs-lookup"><span data-stu-id="f53a8-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="f53a8-126">這些命令會停用批次處理集區集區 06 中所有電腦節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="f53a8-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="f53a8-127">若要執行這項工作，範例中的第一個命令會建立批次帳戶 contosobatchaccount 帳戶金鑰的物件參照。</span><span class="sxs-lookup"><span data-stu-id="f53a8-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="f53a8-128">此物件參照會儲存在名為 $coNtext 的$coNtext。</span><span class="sxs-lookup"><span data-stu-id="f53a8-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="f53a8-129">接著，範例中的第二個命令會使用此物件參照和 **Get-AzBatchComputeNode，** 以返回 Pool06 中找到的所有計算節點集合。</span><span class="sxs-lookup"><span data-stu-id="f53a8-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="f53a8-130">然後，該集合會傳輸至 **Disable-AzBatchComputeNodeScheduling** Cmdlet，以停用集合中每個計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="f53a8-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="f53a8-131">由於 *DisableComputeNodeSchedulingOptions* 參數並未包含任何目前在計算節點上執行的工作，因此將會重新叫用。</span><span class="sxs-lookup"><span data-stu-id="f53a8-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="f53a8-132">參數</span><span class="sxs-lookup"><span data-stu-id="f53a8-132">PARAMETERS</span></span>

### <span data-ttu-id="f53a8-133">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="f53a8-133">-BatchContext</span></span>
<span data-ttu-id="f53a8-134">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="f53a8-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f53a8-135">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="f53a8-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f53a8-136">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="f53a8-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f53a8-137">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f53a8-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f53a8-138">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="f53a8-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f53a8-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="f53a8-139">-ComputeNode</span></span>
<span data-ttu-id="f53a8-140">指定停用任務排程之計算節點的物件參照。</span><span class="sxs-lookup"><span data-stu-id="f53a8-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="f53a8-141">此物件參照是使用 Get-AzBatchComputeNode Cmdlet，並儲存于變數中所返回的計算節點物件所建立。</span><span class="sxs-lookup"><span data-stu-id="f53a8-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f53a8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53a8-142">-DefaultProfile</span></span>
<span data-ttu-id="f53a8-143">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f53a8-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f53a8-144">-停用SchedulingOption</span><span class="sxs-lookup"><span data-stu-id="f53a8-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="f53a8-145">指定此 Cmdlet 如何處理正在停用排程的電腦節點上執行的任何工作。</span><span class="sxs-lookup"><span data-stu-id="f53a8-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="f53a8-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f53a8-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f53a8-147">重新叫出。</span><span class="sxs-lookup"><span data-stu-id="f53a8-147">Requeue.</span></span>
<span data-ttu-id="f53a8-148">工作會立即停止，並返回工作佇列。</span><span class="sxs-lookup"><span data-stu-id="f53a8-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="f53a8-149">這可讓任務重新排在另一個計算節點上。</span><span class="sxs-lookup"><span data-stu-id="f53a8-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="f53a8-150">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="f53a8-150">This is the default value.</span></span> 
- <span data-ttu-id="f53a8-151">終止。</span><span class="sxs-lookup"><span data-stu-id="f53a8-151">Terminate.</span></span>
<span data-ttu-id="f53a8-152">工作會立即停止，並且從工作佇列移除。</span><span class="sxs-lookup"><span data-stu-id="f53a8-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="f53a8-153">這些工作將不會重新排期。</span><span class="sxs-lookup"><span data-stu-id="f53a8-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="f53a8-154">任務完成。</span><span class="sxs-lookup"><span data-stu-id="f53a8-154">TaskCompletion.</span></span>
<span data-ttu-id="f53a8-155">在計算節點上停用任務排程之前，目前執行的工作將能夠完成。</span><span class="sxs-lookup"><span data-stu-id="f53a8-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="f53a8-156">此節點上不會排程任何新工作。</span><span class="sxs-lookup"><span data-stu-id="f53a8-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="f53a8-157">RetainedData。</span><span class="sxs-lookup"><span data-stu-id="f53a8-157">RetainedData.</span></span>
<span data-ttu-id="f53a8-158">目前執行的工作將能夠完成，而資料保留期間在計算節點上停用任務排程之前，也會過期。</span><span class="sxs-lookup"><span data-stu-id="f53a8-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="f53a8-159">此節點上不會排程任何新工作。</span><span class="sxs-lookup"><span data-stu-id="f53a8-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53a8-160">-Id</span><span class="sxs-lookup"><span data-stu-id="f53a8-160">-Id</span></span>
<span data-ttu-id="f53a8-161">指定停用任務排程的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="f53a8-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53a8-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f53a8-162">-PoolId</span></span>
<span data-ttu-id="f53a8-163">指定包含已停用任務排程之計算節點的批次集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="f53a8-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="f53a8-164">如果您使用 *PoolId* 參數，請勿在同一個命令中使用 *ComputeNode* 參數。</span><span class="sxs-lookup"><span data-stu-id="f53a8-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="f53a8-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53a8-165">CommonParameters</span></span>
<span data-ttu-id="f53a8-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f53a8-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53a8-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f53a8-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53a8-168">輸入</span><span class="sxs-lookup"><span data-stu-id="f53a8-168">INPUTS</span></span>

### <span data-ttu-id="f53a8-169">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="f53a8-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="f53a8-170">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="f53a8-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f53a8-171">輸出</span><span class="sxs-lookup"><span data-stu-id="f53a8-171">OUTPUTS</span></span>

### <span data-ttu-id="f53a8-172">System.Void</span><span class="sxs-lookup"><span data-stu-id="f53a8-172">System.Void</span></span>

## <span data-ttu-id="f53a8-173">筆記</span><span class="sxs-lookup"><span data-stu-id="f53a8-173">NOTES</span></span>

## <span data-ttu-id="f53a8-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="f53a8-174">RELATED LINKS</span></span>

[<span data-ttu-id="f53a8-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f53a8-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f53a8-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="f53a8-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)



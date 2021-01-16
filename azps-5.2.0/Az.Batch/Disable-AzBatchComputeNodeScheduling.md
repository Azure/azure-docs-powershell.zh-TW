---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280844"
---
# <span data-ttu-id="d85a6-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="d85a6-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="d85a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d85a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d85a6-103">停用指定計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="d85a6-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="d85a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="d85a6-104">SYNTAX</span></span>

### <span data-ttu-id="d85a6-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="d85a6-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d85a6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d85a6-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d85a6-107">說明</span><span class="sxs-lookup"><span data-stu-id="d85a6-107">DESCRIPTION</span></span>
<span data-ttu-id="d85a6-108">**Disable AzBatchComputeNodeScheduling** Cmdlet 會在指定的計算節點上停用工作排程。</span><span class="sxs-lookup"><span data-stu-id="d85a6-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="d85a6-109">計算節點是專用於特定應用程式工作負載的 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d85a6-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="d85a6-110">當您在 [計算] 節點上停用任務排程時，您也可以決定如何處理目前在節點任務佇列中的工作。</span><span class="sxs-lookup"><span data-stu-id="d85a6-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="d85a6-111">**停用-AzBatchComputeNodeScheduling** 可讓您執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d85a6-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="d85a6-112">終止工作並將其放回作業佇列中。</span><span class="sxs-lookup"><span data-stu-id="d85a6-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="d85a6-113">這樣可將這些工作重新安排在另一個計算節點上。</span><span class="sxs-lookup"><span data-stu-id="d85a6-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="d85a6-114">終止工作並將其從作業佇列中移除。</span><span class="sxs-lookup"><span data-stu-id="d85a6-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="d85a6-115">以這種方式停止的工作不會重新排定日程。</span><span class="sxs-lookup"><span data-stu-id="d85a6-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="d85a6-116">等待目前執行的所有工作完成，然後在 [計算] 節點上停用 [任務排程]。</span><span class="sxs-lookup"><span data-stu-id="d85a6-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="d85a6-117">等待所有執行中的工作完成，並將所有資料保持期到期，然後在 [計算] 節點上停用 [任務排程]。</span><span class="sxs-lookup"><span data-stu-id="d85a6-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="d85a6-118">示例</span><span class="sxs-lookup"><span data-stu-id="d85a6-118">EXAMPLES</span></span>

### <span data-ttu-id="d85a6-119">範例1：停用計算節點上的任務排程</span><span class="sxs-lookup"><span data-stu-id="d85a6-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="d85a6-120">這些命令會在 compute 節點 tvm-1783593343_34-20151117t222514z 上停用 [任務排程]。</span><span class="sxs-lookup"><span data-stu-id="d85a6-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="d85a6-121">若要這樣做，範例中的第一個命令會針對批次帳戶 contosobatchaccount 建立帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="d85a6-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="d85a6-122">這個物件參照會儲存在名為 $coNtext 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d85a6-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="d85a6-123">然後，第二個命令會使用這個物件參照和 **Disable AzBatchComputeNodeScheduling** Cmdlet 來連線至 [pool myPool]，並在節點 tvm 上停用 [任務排程]-1783593343_34-20151117t222514z。</span><span class="sxs-lookup"><span data-stu-id="d85a6-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="d85a6-124">因為未包含 *DisableComputeNodeSchedulingOptions* 參數，所以任何目前在計算節點上執行的工作都會重新排隊。</span><span class="sxs-lookup"><span data-stu-id="d85a6-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="d85a6-125">範例2：在池中的所有計算節點上停用任務排程</span><span class="sxs-lookup"><span data-stu-id="d85a6-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="d85a6-126">這些命令會在批次池中 Pool06 的所有電腦節點上停用 [任務排程]。</span><span class="sxs-lookup"><span data-stu-id="d85a6-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="d85a6-127">若要執行這項工作，範例中的第一個命令會建立一個物件參考，以取得批次帳戶 contosobatchaccount 的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="d85a6-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="d85a6-128">這個物件參照會儲存在名為 $coNtext 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d85a6-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="d85a6-129">接著，這個範例中的第二個命令會使用這個物件參考，並 **取得 AzBatchComputeNode** ，以傳回在 Pool06 中找到的所有計算節點集合。</span><span class="sxs-lookup"><span data-stu-id="d85a6-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="d85a6-130">然後，該集合會輸送成管道，然後 **Disable AzBatchComputeNodeScheduling** Cmdlet，即可在集合中的每個計算節點上停用任務排程。</span><span class="sxs-lookup"><span data-stu-id="d85a6-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="d85a6-131">因為未包含 *DisableComputeNodeSchedulingOptions* 參數，所以任何目前在計算節點上執行的工作都會重新排隊。</span><span class="sxs-lookup"><span data-stu-id="d85a6-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="d85a6-132">參數</span><span class="sxs-lookup"><span data-stu-id="d85a6-132">PARAMETERS</span></span>

### <span data-ttu-id="d85a6-133">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d85a6-133">-BatchContext</span></span>
<span data-ttu-id="d85a6-134">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d85a6-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d85a6-135">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="d85a6-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d85a6-136">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="d85a6-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d85a6-137">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d85a6-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d85a6-138">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="d85a6-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d85a6-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d85a6-139">-ComputeNode</span></span>
<span data-ttu-id="d85a6-140">指定任務排程停用之計算節點的物件參照。</span><span class="sxs-lookup"><span data-stu-id="d85a6-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="d85a6-141">這個物件參照是使用 Get-AzBatchComputeNode Cmdlet 建立，並將傳回的計算節點物件儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="d85a6-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="d85a6-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85a6-142">-DefaultProfile</span></span>
<span data-ttu-id="d85a6-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d85a6-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d85a6-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="d85a6-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="d85a6-145">指定此 Cmdlet 處理正在停用排程之電腦節點上執行的任何工作的方式。</span><span class="sxs-lookup"><span data-stu-id="d85a6-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="d85a6-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d85a6-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d85a6-147">Requeue.</span><span class="sxs-lookup"><span data-stu-id="d85a6-147">Requeue.</span></span>
<span data-ttu-id="d85a6-148">任務會立即停止並傳回作業佇列。</span><span class="sxs-lookup"><span data-stu-id="d85a6-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="d85a6-149">這可讓任務在另一個計算節點上重新排定。</span><span class="sxs-lookup"><span data-stu-id="d85a6-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="d85a6-150">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="d85a6-150">This is the default value.</span></span> 
- <span data-ttu-id="d85a6-151">終結.</span><span class="sxs-lookup"><span data-stu-id="d85a6-151">Terminate.</span></span>
<span data-ttu-id="d85a6-152">工作會立即停止並從作業佇列中移除。</span><span class="sxs-lookup"><span data-stu-id="d85a6-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="d85a6-153">將不會重新安排這些工作。</span><span class="sxs-lookup"><span data-stu-id="d85a6-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="d85a6-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="d85a6-154">TaskCompletion.</span></span>
<span data-ttu-id="d85a6-155">在計算節點上停用任務排程前，目前執行中的工作將能完成。</span><span class="sxs-lookup"><span data-stu-id="d85a6-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="d85a6-156">此節點上將不會排程任何新工作。</span><span class="sxs-lookup"><span data-stu-id="d85a6-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="d85a6-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="d85a6-157">RetainedData.</span></span>
<span data-ttu-id="d85a6-158">在計算節點上停用任務排程前，目前執行中的工作將能完成，且資料保留期間將能到期。</span><span class="sxs-lookup"><span data-stu-id="d85a6-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="d85a6-159">此節點上將不會排程任何新工作。</span><span class="sxs-lookup"><span data-stu-id="d85a6-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="d85a6-160">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d85a6-160">-Id</span></span>
<span data-ttu-id="d85a6-161">指定 [任務排程] 停用的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="d85a6-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="d85a6-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d85a6-162">-PoolId</span></span>
<span data-ttu-id="d85a6-163">指定包含已停用任務排程之計算節點的批次池的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d85a6-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="d85a6-164">如果您使用 *PoolId* 參數，請勿在相同的命令中使用 *ComputeNode* 參數。</span><span class="sxs-lookup"><span data-stu-id="d85a6-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="d85a6-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85a6-165">CommonParameters</span></span>
<span data-ttu-id="d85a6-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d85a6-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85a6-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d85a6-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85a6-168">輸入</span><span class="sxs-lookup"><span data-stu-id="d85a6-168">INPUTS</span></span>

### <span data-ttu-id="d85a6-169">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d85a6-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d85a6-170">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d85a6-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d85a6-171">輸出</span><span class="sxs-lookup"><span data-stu-id="d85a6-171">OUTPUTS</span></span>

### <span data-ttu-id="d85a6-172">System.void</span><span class="sxs-lookup"><span data-stu-id="d85a6-172">System.Void</span></span>

## <span data-ttu-id="d85a6-173">筆記</span><span class="sxs-lookup"><span data-stu-id="d85a6-173">NOTES</span></span>

## <span data-ttu-id="d85a6-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="d85a6-174">RELATED LINKS</span></span>

[<span data-ttu-id="d85a6-175">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d85a6-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d85a6-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="d85a6-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446808"
---
# <span data-ttu-id="94c67-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="94c67-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="94c67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94c67-102">SYNOPSIS</span></span>
<span data-ttu-id="94c67-103">開始調整池子的大小。</span><span class="sxs-lookup"><span data-stu-id="94c67-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="94c67-104">句法</span><span class="sxs-lookup"><span data-stu-id="94c67-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94c67-105">說明</span><span class="sxs-lookup"><span data-stu-id="94c67-105">DESCRIPTION</span></span>
<span data-ttu-id="94c67-106">**AzBatchPoolResize** Cmdlet 會在池中啟動 Azure Batch 調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="94c67-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="94c67-107">示例</span><span class="sxs-lookup"><span data-stu-id="94c67-107">EXAMPLES</span></span>

### <span data-ttu-id="94c67-108">範例1：將池大小調整成12個節點</span><span class="sxs-lookup"><span data-stu-id="94c67-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="94c67-109">這個命令會在具有識別碼 ContosoPool06 的池中啟動調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="94c67-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="94c67-110">操作的目標是12個專用的計算節點。</span><span class="sxs-lookup"><span data-stu-id="94c67-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="94c67-111">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="94c67-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="94c67-112">範例2：使用解除配置選項調整池子的大小</span><span class="sxs-lookup"><span data-stu-id="94c67-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="94c67-113">這個 Cmdlet 會將一個池大小調整為五個專用的計算節點。</span><span class="sxs-lookup"><span data-stu-id="94c67-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="94c67-114">命令會使用 Get-AzBatchPool Cmdlet 來取得具有識別碼 ContosoPool06 的 pool。</span><span class="sxs-lookup"><span data-stu-id="94c67-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="94c67-115">透過使用管線運算子，命令會將該 pool 物件傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94c67-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94c67-116">命令會在該文檔池中啟動調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="94c67-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="94c67-117">目標是五個專用的計算節點。</span><span class="sxs-lookup"><span data-stu-id="94c67-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="94c67-118">此命令指定一個小時的超時時間。</span><span class="sxs-lookup"><span data-stu-id="94c67-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="94c67-119">命令會指定 [終止] 的解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="94c67-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="94c67-120">參數</span><span class="sxs-lookup"><span data-stu-id="94c67-120">PARAMETERS</span></span>

### <span data-ttu-id="94c67-121">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="94c67-121">-BatchContext</span></span>
<span data-ttu-id="94c67-122">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="94c67-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="94c67-123">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="94c67-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="94c67-124">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="94c67-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="94c67-125">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="94c67-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="94c67-126">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="94c67-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="94c67-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="94c67-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="94c67-128">指定此 Cmdlet 啟動之大小調整作業的解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="94c67-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c67-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c67-129">-DefaultProfile</span></span>
<span data-ttu-id="94c67-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94c67-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94c67-131">-識別碼</span><span class="sxs-lookup"><span data-stu-id="94c67-131">-Id</span></span>
<span data-ttu-id="94c67-132">指定此 Cmdlet 調整大小的池 ID。</span><span class="sxs-lookup"><span data-stu-id="94c67-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94c67-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="94c67-133">-ResizeTimeout</span></span>
<span data-ttu-id="94c67-134">指定調整大小作業的超時週期。</span><span class="sxs-lookup"><span data-stu-id="94c67-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="94c67-135">如果此時間池未達到目標大小，則會停止調整大小操作。</span><span class="sxs-lookup"><span data-stu-id="94c67-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c67-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="94c67-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="94c67-137">目標專用計算節點的數目。</span><span class="sxs-lookup"><span data-stu-id="94c67-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c67-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="94c67-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="94c67-139">目標低優先順序計算節點的數目。</span><span class="sxs-lookup"><span data-stu-id="94c67-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c67-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c67-140">CommonParameters</span></span>
<span data-ttu-id="94c67-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94c67-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c67-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="94c67-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c67-143">輸入</span><span class="sxs-lookup"><span data-stu-id="94c67-143">INPUTS</span></span>

### <span data-ttu-id="94c67-144">System.object</span><span class="sxs-lookup"><span data-stu-id="94c67-144">System.String</span></span>

### <span data-ttu-id="94c67-145">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="94c67-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="94c67-146">輸出</span><span class="sxs-lookup"><span data-stu-id="94c67-146">OUTPUTS</span></span>

### <span data-ttu-id="94c67-147">System.void</span><span class="sxs-lookup"><span data-stu-id="94c67-147">System.Void</span></span>

## <span data-ttu-id="94c67-148">筆記</span><span class="sxs-lookup"><span data-stu-id="94c67-148">NOTES</span></span>

## <span data-ttu-id="94c67-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="94c67-149">RELATED LINKS</span></span>

[<span data-ttu-id="94c67-150">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="94c67-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="94c67-151">AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="94c67-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="94c67-152">停止 AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="94c67-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="94c67-153">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94c67-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

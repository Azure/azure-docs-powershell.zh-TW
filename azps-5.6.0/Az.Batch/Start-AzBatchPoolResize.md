---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: b312a94a971a5ff17a153a8a9b0112e14886fe12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905606"
---
# <span data-ttu-id="4927b-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="4927b-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="4927b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4927b-102">SYNOPSIS</span></span>
<span data-ttu-id="4927b-103">開始調整資源庫的大小。</span><span class="sxs-lookup"><span data-stu-id="4927b-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="4927b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4927b-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4927b-105">描述</span><span class="sxs-lookup"><span data-stu-id="4927b-105">DESCRIPTION</span></span>
<span data-ttu-id="4927b-106">**Start-AzBatchPoolResize Cmdlet** 會啟動資料庫上的 Azure 批次調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="4927b-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="4927b-107">例子</span><span class="sxs-lookup"><span data-stu-id="4927b-107">EXAMPLES</span></span>

### <span data-ttu-id="4927b-108">範例 1：將共用區調整大小為 12 個節點</span><span class="sxs-lookup"><span data-stu-id="4927b-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="4927b-109">此命令在具有 ID ContosoPool06 的集中開始調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="4927b-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="4927b-110">作業的目標是 12 個專用計算節點。</span><span class="sxs-lookup"><span data-stu-id="4927b-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="4927b-111">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="4927b-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="4927b-112">範例 2：使用主機代管選項調整資料庫大小</span><span class="sxs-lookup"><span data-stu-id="4927b-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="4927b-113">此 Cmdlet 將計算區的大小調整為五個專用計算節點。</span><span class="sxs-lookup"><span data-stu-id="4927b-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="4927b-114">命令會使用 Cmdlet 的識別碼 ContosoPool06 來Get-AzBatchPool。</span><span class="sxs-lookup"><span data-stu-id="4927b-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="4927b-115">該命令會使用管線運算子，將該 Pool 物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4927b-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4927b-116">命令會啟動在資料表上調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="4927b-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="4927b-117">目標為五個專用計算節點。</span><span class="sxs-lookup"><span data-stu-id="4927b-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="4927b-118">命令會指定一小時的時數。</span><span class="sxs-lookup"><span data-stu-id="4927b-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="4927b-119">命令會指定終止的代管選項。</span><span class="sxs-lookup"><span data-stu-id="4927b-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="4927b-120">參數</span><span class="sxs-lookup"><span data-stu-id="4927b-120">PARAMETERS</span></span>

### <span data-ttu-id="4927b-121">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="4927b-121">-BatchContext</span></span>
<span data-ttu-id="4927b-122">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="4927b-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4927b-123">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="4927b-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4927b-124">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="4927b-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4927b-125">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4927b-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4927b-126">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="4927b-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4927b-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="4927b-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="4927b-128">指定此 Cmdlet 啟動之重大小作業的轉寄選項。</span><span class="sxs-lookup"><span data-stu-id="4927b-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="4927b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4927b-129">-DefaultProfile</span></span>
<span data-ttu-id="4927b-130">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4927b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4927b-131">-Id</span><span class="sxs-lookup"><span data-stu-id="4927b-131">-Id</span></span>
<span data-ttu-id="4927b-132">指定此 Cmdlet 調整大小之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4927b-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="4927b-133">-調整大小時間</span><span class="sxs-lookup"><span data-stu-id="4927b-133">-ResizeTimeout</span></span>
<span data-ttu-id="4927b-134">指定重重大小作業的一個時段。</span><span class="sxs-lookup"><span data-stu-id="4927b-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="4927b-135">如果此時資料庫未到達目標大小，調整大小作業會停止。</span><span class="sxs-lookup"><span data-stu-id="4927b-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="4927b-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="4927b-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="4927b-137">目標專用計算節點的數量。</span><span class="sxs-lookup"><span data-stu-id="4927b-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="4927b-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="4927b-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="4927b-139">目標低優先順序計算節點的數量。</span><span class="sxs-lookup"><span data-stu-id="4927b-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="4927b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4927b-140">CommonParameters</span></span>
<span data-ttu-id="4927b-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4927b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4927b-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4927b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4927b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="4927b-143">INPUTS</span></span>

### <span data-ttu-id="4927b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4927b-144">System.String</span></span>

### <span data-ttu-id="4927b-145">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="4927b-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4927b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="4927b-146">OUTPUTS</span></span>

### <span data-ttu-id="4927b-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="4927b-147">System.Void</span></span>

## <span data-ttu-id="4927b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="4927b-148">NOTES</span></span>

## <span data-ttu-id="4927b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="4927b-149">RELATED LINKS</span></span>

[<span data-ttu-id="4927b-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4927b-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4927b-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4927b-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="4927b-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="4927b-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="4927b-153">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4927b-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

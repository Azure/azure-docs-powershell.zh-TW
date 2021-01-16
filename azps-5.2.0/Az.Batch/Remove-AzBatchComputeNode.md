---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281102"
---
# <span data-ttu-id="8d74e-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8d74e-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="8d74e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d74e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d74e-103">從池中移除計算節點。</span><span class="sxs-lookup"><span data-stu-id="8d74e-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="8d74e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d74e-104">SYNTAX</span></span>

### <span data-ttu-id="8d74e-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="8d74e-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d74e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8d74e-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d74e-107">說明</span><span class="sxs-lookup"><span data-stu-id="8d74e-107">DESCRIPTION</span></span>
<span data-ttu-id="8d74e-108">**AzBatchComputeNode** Cmdlet 會從池中移除 Azure 批次計算節點。</span><span class="sxs-lookup"><span data-stu-id="8d74e-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="8d74e-109">示例</span><span class="sxs-lookup"><span data-stu-id="8d74e-109">EXAMPLES</span></span>

### <span data-ttu-id="8d74e-110">範例1：移除計算節點</span><span class="sxs-lookup"><span data-stu-id="8d74e-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="8d74e-111">這個命令會從擁有識別碼 Pool07 的池中移除具有指定識別碼的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="8d74e-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="8d74e-112">命令會指定終止解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="8d74e-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="8d74e-113">重新調整超時的時間為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="8d74e-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="8d74e-114">範例2：使用管線移除計算節點</span><span class="sxs-lookup"><span data-stu-id="8d74e-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="8d74e-115">這個命令會透過使用 Get-AzBatchComputeNode Cmdlet，從擁有識別碼 Pool07 的 pool 中取得具有指定 ID 的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="8d74e-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="8d74e-116">命令會使用管線將該節點傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d74e-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="8d74e-117">目前的 Cmdlet 會移除 [計算] 節點。</span><span class="sxs-lookup"><span data-stu-id="8d74e-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="8d74e-118">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="8d74e-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8d74e-119">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d74e-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8d74e-120">範例3：移除多個節點</span><span class="sxs-lookup"><span data-stu-id="8d74e-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="8d74e-121">這個命令會從擁有識別碼 Pool07 的池中移除兩個計算節點。</span><span class="sxs-lookup"><span data-stu-id="8d74e-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="8d74e-122">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d74e-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8d74e-123">參數</span><span class="sxs-lookup"><span data-stu-id="8d74e-123">PARAMETERS</span></span>

### <span data-ttu-id="8d74e-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="8d74e-124">-BatchContext</span></span>
<span data-ttu-id="8d74e-125">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="8d74e-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8d74e-126">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="8d74e-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8d74e-127">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="8d74e-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8d74e-128">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8d74e-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8d74e-129">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d74e-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8d74e-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="8d74e-130">-ComputeNode</span></span>
<span data-ttu-id="8d74e-131">指定代表此 Cmdlet 移除之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="8d74e-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8d74e-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="8d74e-132">-DeallocationOption</span></span>
<span data-ttu-id="8d74e-133">指定此 Cmdlet 啟動之移除作業的解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="8d74e-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="8d74e-134">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="8d74e-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="8d74e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d74e-135">-DefaultProfile</span></span>
<span data-ttu-id="8d74e-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d74e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d74e-137">-Force</span><span class="sxs-lookup"><span data-stu-id="8d74e-137">-Force</span></span>
<span data-ttu-id="8d74e-138">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8d74e-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d74e-139">-識別碼</span><span class="sxs-lookup"><span data-stu-id="8d74e-139">-Ids</span></span>
<span data-ttu-id="8d74e-140">指定此 Cmdlet 從池中移除之計算節點的 Id 陣列。</span><span class="sxs-lookup"><span data-stu-id="8d74e-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d74e-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="8d74e-141">-PoolId</span></span>
<span data-ttu-id="8d74e-142">指定包含此 Cmdlet 移除之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="8d74e-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8d74e-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="8d74e-143">-ResizeTimeout</span></span>
<span data-ttu-id="8d74e-144">指定從池中移除計算節點的超時間隔。</span><span class="sxs-lookup"><span data-stu-id="8d74e-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="8d74e-145">預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="8d74e-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="8d74e-146">[最小值] 為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="8d74e-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="8d74e-147">-確認</span><span class="sxs-lookup"><span data-stu-id="8d74e-147">-Confirm</span></span>
<span data-ttu-id="8d74e-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d74e-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d74e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d74e-149">-WhatIf</span></span>
<span data-ttu-id="8d74e-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d74e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d74e-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d74e-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d74e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d74e-152">CommonParameters</span></span>
<span data-ttu-id="8d74e-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d74e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d74e-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d74e-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d74e-155">輸入</span><span class="sxs-lookup"><span data-stu-id="8d74e-155">INPUTS</span></span>

### <span data-ttu-id="8d74e-156">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8d74e-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="8d74e-157">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="8d74e-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8d74e-158">輸出</span><span class="sxs-lookup"><span data-stu-id="8d74e-158">OUTPUTS</span></span>

### <span data-ttu-id="8d74e-159">System.void</span><span class="sxs-lookup"><span data-stu-id="8d74e-159">System.Void</span></span>

## <span data-ttu-id="8d74e-160">筆記</span><span class="sxs-lookup"><span data-stu-id="8d74e-160">NOTES</span></span>

## <span data-ttu-id="8d74e-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d74e-161">RELATED LINKS</span></span>

[<span data-ttu-id="8d74e-162">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8d74e-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8d74e-163">AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8d74e-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="8d74e-164">重新開機-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8d74e-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)



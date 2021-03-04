---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 7e2b2bca042573ec96fefdf85e5077ec1138d1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902929"
---
# <span data-ttu-id="ea02b-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ea02b-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="ea02b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea02b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea02b-103">從資料庫移除計算節點。</span><span class="sxs-lookup"><span data-stu-id="ea02b-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="ea02b-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea02b-104">SYNTAX</span></span>

### <span data-ttu-id="ea02b-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="ea02b-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea02b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ea02b-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea02b-107">描述</span><span class="sxs-lookup"><span data-stu-id="ea02b-107">DESCRIPTION</span></span>
<span data-ttu-id="ea02b-108">**Remove-AzBatchComputeNode** Cmdlet 會從資料庫移除 Azure Batch 計算節點。</span><span class="sxs-lookup"><span data-stu-id="ea02b-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="ea02b-109">例子</span><span class="sxs-lookup"><span data-stu-id="ea02b-109">EXAMPLES</span></span>

### <span data-ttu-id="ea02b-110">範例 1：移除計算節點</span><span class="sxs-lookup"><span data-stu-id="ea02b-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="ea02b-111">此命令會從具有識別碼 Pool07 的集中移除具有指定識別碼的計算節點。</span><span class="sxs-lookup"><span data-stu-id="ea02b-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="ea02b-112">命令會指定終止解除代管選項。</span><span class="sxs-lookup"><span data-stu-id="ea02b-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="ea02b-113">調整大小會超過 10 分鐘。</span><span class="sxs-lookup"><span data-stu-id="ea02b-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="ea02b-114">範例 2：使用管線移除計算節點</span><span class="sxs-lookup"><span data-stu-id="ea02b-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="ea02b-115">此命令會使用 Get-AzBatchComputeNode let，從具有識別碼 Pool07 的集中獲得具有指定識別碼的計算節點。</span><span class="sxs-lookup"><span data-stu-id="ea02b-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="ea02b-116">該命令會使用管線，將節點傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea02b-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="ea02b-117">目前的 Cmdlet 會移除計算節點。</span><span class="sxs-lookup"><span data-stu-id="ea02b-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="ea02b-118">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="ea02b-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ea02b-119">因此，命令不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ea02b-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ea02b-120">範例 3：移除多個節點</span><span class="sxs-lookup"><span data-stu-id="ea02b-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="ea02b-121">此命令會從具有識別碼 Pool07 的集中移除兩個計算節點。</span><span class="sxs-lookup"><span data-stu-id="ea02b-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="ea02b-122">命令不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ea02b-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ea02b-123">參數</span><span class="sxs-lookup"><span data-stu-id="ea02b-123">PARAMETERS</span></span>

### <span data-ttu-id="ea02b-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="ea02b-124">-BatchContext</span></span>
<span data-ttu-id="ea02b-125">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="ea02b-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ea02b-126">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="ea02b-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ea02b-127">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="ea02b-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ea02b-128">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ea02b-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ea02b-129">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="ea02b-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ea02b-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ea02b-130">-ComputeNode</span></span>
<span data-ttu-id="ea02b-131">指定 **PSComputeNode 物件** ，代表此 Cmdlet 移除的計算節點。</span><span class="sxs-lookup"><span data-stu-id="ea02b-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea02b-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="ea02b-132">-DeallocationOption</span></span>
<span data-ttu-id="ea02b-133">指定此 Cmdlet 啟動之移除作業的移轉選項。</span><span class="sxs-lookup"><span data-stu-id="ea02b-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="ea02b-134">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="ea02b-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="ea02b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea02b-135">-DefaultProfile</span></span>
<span data-ttu-id="ea02b-136">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea02b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea02b-137">-強制</span><span class="sxs-lookup"><span data-stu-id="ea02b-137">-Force</span></span>
<span data-ttu-id="ea02b-138">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ea02b-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea02b-139">-Ids</span><span class="sxs-lookup"><span data-stu-id="ea02b-139">-Ids</span></span>
<span data-ttu-id="ea02b-140">指定此 Cmdlet 從計算節點移除之計算節點的陣列。</span><span class="sxs-lookup"><span data-stu-id="ea02b-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="ea02b-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ea02b-141">-PoolId</span></span>
<span data-ttu-id="ea02b-142">指定包含此 Cmdlet 移除之計算節點之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea02b-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea02b-143">-調整大小時間</span><span class="sxs-lookup"><span data-stu-id="ea02b-143">-ResizeTimeout</span></span>
<span data-ttu-id="ea02b-144">指定從資料組移除計算節點的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="ea02b-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="ea02b-145">預設值為 10 分鐘。</span><span class="sxs-lookup"><span data-stu-id="ea02b-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="ea02b-146">最小值為 5 分鐘。</span><span class="sxs-lookup"><span data-stu-id="ea02b-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="ea02b-147">-確認</span><span class="sxs-lookup"><span data-stu-id="ea02b-147">-Confirm</span></span>
<span data-ttu-id="ea02b-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ea02b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea02b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea02b-149">-WhatIf</span></span>
<span data-ttu-id="ea02b-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea02b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea02b-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea02b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea02b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea02b-152">CommonParameters</span></span>
<span data-ttu-id="ea02b-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea02b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea02b-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea02b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea02b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="ea02b-155">INPUTS</span></span>

### <span data-ttu-id="ea02b-156">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ea02b-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ea02b-157">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="ea02b-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ea02b-158">輸出</span><span class="sxs-lookup"><span data-stu-id="ea02b-158">OUTPUTS</span></span>

### <span data-ttu-id="ea02b-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="ea02b-159">System.Void</span></span>

## <span data-ttu-id="ea02b-160">筆記</span><span class="sxs-lookup"><span data-stu-id="ea02b-160">NOTES</span></span>

## <span data-ttu-id="ea02b-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea02b-161">RELATED LINKS</span></span>

[<span data-ttu-id="ea02b-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ea02b-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ea02b-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ea02b-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ea02b-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ea02b-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)



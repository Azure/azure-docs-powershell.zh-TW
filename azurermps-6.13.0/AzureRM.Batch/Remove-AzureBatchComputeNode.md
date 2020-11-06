---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 39bbc9102d72c469730fe494869bffe5f726b41a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450290"
---
# <span data-ttu-id="ad662-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad662-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="ad662-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad662-102">SYNOPSIS</span></span>
<span data-ttu-id="ad662-103">從池中移除計算節點。</span><span class="sxs-lookup"><span data-stu-id="ad662-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad662-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad662-104">SYNTAX</span></span>

### <span data-ttu-id="ad662-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="ad662-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad662-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad662-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad662-107">說明</span><span class="sxs-lookup"><span data-stu-id="ad662-107">DESCRIPTION</span></span>
<span data-ttu-id="ad662-108">**AzureBatchComputeNode** Cmdlet 會從池中移除 Azure 批次計算節點。</span><span class="sxs-lookup"><span data-stu-id="ad662-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="ad662-109">示例</span><span class="sxs-lookup"><span data-stu-id="ad662-109">EXAMPLES</span></span>

### <span data-ttu-id="ad662-110">範例1：移除計算節點</span><span class="sxs-lookup"><span data-stu-id="ad662-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="ad662-111">這個命令會從擁有識別碼 Pool07 的池中移除具有指定識別碼的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="ad662-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="ad662-112">命令會指定終止解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="ad662-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="ad662-113">重新調整超時的時間為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="ad662-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="ad662-114">範例2：使用管線移除計算節點</span><span class="sxs-lookup"><span data-stu-id="ad662-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="ad662-115">這個命令會透過使用 Get-AzureBatchComputeNode Cmdlet，從擁有識別碼 Pool07 的 pool 中取得具有指定 ID 的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="ad662-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="ad662-116">命令會使用管線將該節點傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad662-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="ad662-117">目前的 Cmdlet 會移除 [計算] 節點。</span><span class="sxs-lookup"><span data-stu-id="ad662-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="ad662-118">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="ad662-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ad662-119">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad662-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ad662-120">範例3：移除多個節點</span><span class="sxs-lookup"><span data-stu-id="ad662-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="ad662-121">這個命令會從擁有識別碼 Pool07 的池中移除兩個計算節點。</span><span class="sxs-lookup"><span data-stu-id="ad662-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="ad662-122">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad662-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ad662-123">參數</span><span class="sxs-lookup"><span data-stu-id="ad662-123">PARAMETERS</span></span>

### <span data-ttu-id="ad662-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="ad662-124">-BatchContext</span></span>
<span data-ttu-id="ad662-125">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="ad662-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ad662-126">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="ad662-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ad662-127">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="ad662-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ad662-128">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ad662-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ad662-129">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad662-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ad662-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad662-130">-ComputeNode</span></span>
<span data-ttu-id="ad662-131">指定代表此 Cmdlet 移除之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="ad662-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad662-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="ad662-132">-DeallocationOption</span></span>
<span data-ttu-id="ad662-133">指定此 Cmdlet 啟動之移除作業的解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="ad662-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="ad662-134">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="ad662-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="ad662-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad662-135">-DefaultProfile</span></span>
<span data-ttu-id="ad662-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad662-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad662-137">-Force</span><span class="sxs-lookup"><span data-stu-id="ad662-137">-Force</span></span>
<span data-ttu-id="ad662-138">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ad662-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad662-139">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ad662-139">-Ids</span></span>
<span data-ttu-id="ad662-140">指定此 Cmdlet 從池中移除之計算節點的 Id 陣列。</span><span class="sxs-lookup"><span data-stu-id="ad662-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="ad662-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ad662-141">-PoolId</span></span>
<span data-ttu-id="ad662-142">指定包含此 Cmdlet 移除之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="ad662-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad662-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="ad662-143">-ResizeTimeout</span></span>
<span data-ttu-id="ad662-144">指定從池中移除計算節點的超時間隔。</span><span class="sxs-lookup"><span data-stu-id="ad662-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="ad662-145">預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="ad662-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="ad662-146">[最小值] 為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="ad662-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="ad662-147">-確認</span><span class="sxs-lookup"><span data-stu-id="ad662-147">-Confirm</span></span>
<span data-ttu-id="ad662-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad662-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad662-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad662-149">-WhatIf</span></span>
<span data-ttu-id="ad662-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad662-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad662-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad662-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad662-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad662-152">CommonParameters</span></span>
<span data-ttu-id="ad662-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad662-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad662-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad662-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad662-155">輸入</span><span class="sxs-lookup"><span data-stu-id="ad662-155">INPUTS</span></span>

### <span data-ttu-id="ad662-156">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad662-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="ad662-157">參數： ComputeNode (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ad662-157">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="ad662-158">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="ad662-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ad662-159">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ad662-159">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ad662-160">輸出</span><span class="sxs-lookup"><span data-stu-id="ad662-160">OUTPUTS</span></span>

### <span data-ttu-id="ad662-161">System.void</span><span class="sxs-lookup"><span data-stu-id="ad662-161">System.Void</span></span>

## <span data-ttu-id="ad662-162">筆記</span><span class="sxs-lookup"><span data-stu-id="ad662-162">NOTES</span></span>

## <span data-ttu-id="ad662-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad662-163">RELATED LINKS</span></span>

[<span data-ttu-id="ad662-164">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ad662-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ad662-165">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad662-165">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="ad662-166">重新開機-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ad662-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)



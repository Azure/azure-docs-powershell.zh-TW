---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: b134a59a2335eaa3ee95eaddb6b76148739569bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625231"
---
# <span data-ttu-id="d0610-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0610-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="d0610-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0610-102">SYNOPSIS</span></span>
<span data-ttu-id="d0610-103">從池中移除計算節點。</span><span class="sxs-lookup"><span data-stu-id="d0610-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0610-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0610-104">SYNTAX</span></span>

### <span data-ttu-id="d0610-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="d0610-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0610-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d0610-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0610-107">說明</span><span class="sxs-lookup"><span data-stu-id="d0610-107">DESCRIPTION</span></span>
<span data-ttu-id="d0610-108">**AzureBatchComputeNode** Cmdlet 會從池中移除 Azure 批次計算節點。</span><span class="sxs-lookup"><span data-stu-id="d0610-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="d0610-109">示例</span><span class="sxs-lookup"><span data-stu-id="d0610-109">EXAMPLES</span></span>

### <span data-ttu-id="d0610-110">範例1：移除計算節點</span><span class="sxs-lookup"><span data-stu-id="d0610-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="d0610-111">這個命令會從擁有識別碼 Pool07 的池中移除具有指定識別碼的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="d0610-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="d0610-112">命令會指定終止解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="d0610-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="d0610-113">重新調整超時的時間為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="d0610-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="d0610-114">範例2：使用管線移除計算節點</span><span class="sxs-lookup"><span data-stu-id="d0610-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="d0610-115">這個命令會透過使用 Get-AzureBatchComputeNode Cmdlet，從擁有識別碼 Pool07 的 pool 中取得具有指定 ID 的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="d0610-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="d0610-116">命令會使用管線將該節點傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0610-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="d0610-117">目前的 Cmdlet 會移除 [計算] 節點。</span><span class="sxs-lookup"><span data-stu-id="d0610-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="d0610-118">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="d0610-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d0610-119">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0610-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="d0610-120">範例3：移除多個節點</span><span class="sxs-lookup"><span data-stu-id="d0610-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="d0610-121">這個命令會從擁有識別碼 Pool07 的池中移除兩個計算節點。</span><span class="sxs-lookup"><span data-stu-id="d0610-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="d0610-122">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0610-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d0610-123">參數</span><span class="sxs-lookup"><span data-stu-id="d0610-123">PARAMETERS</span></span>

### <span data-ttu-id="d0610-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d0610-124">-BatchContext</span></span>
<span data-ttu-id="d0610-125">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d0610-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d0610-126">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0610-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d0610-127">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0610-127">-ComputeNode</span></span>
<span data-ttu-id="d0610-128">指定代表此 Cmdlet 移除之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0610-128">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0610-129">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="d0610-129">-DeallocationOption</span></span>
<span data-ttu-id="d0610-130">指定此 Cmdlet 啟動之移除作業的解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="d0610-130">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="d0610-131">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="d0610-131">The default value is Requeue.</span></span>

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

### <span data-ttu-id="d0610-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d0610-132">-Force</span></span>
<span data-ttu-id="d0610-133">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d0610-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0610-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d0610-134">-Ids</span></span>
<span data-ttu-id="d0610-135">指定此 Cmdlet 從池中移除之計算節點的 Id 陣列。</span><span class="sxs-lookup"><span data-stu-id="d0610-135">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="d0610-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d0610-136">-PoolId</span></span>
<span data-ttu-id="d0610-137">指定包含此 Cmdlet 移除之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="d0610-137">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0610-138">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="d0610-138">-ResizeTimeout</span></span>
<span data-ttu-id="d0610-139">指定從池中移除計算節點的超時間隔。</span><span class="sxs-lookup"><span data-stu-id="d0610-139">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="d0610-140">預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="d0610-140">The default value is 10 minutes.</span></span>
<span data-ttu-id="d0610-141">[最小值] 為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="d0610-141">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="d0610-142">-確認</span><span class="sxs-lookup"><span data-stu-id="d0610-142">-Confirm</span></span>
<span data-ttu-id="d0610-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0610-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0610-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0610-144">-WhatIf</span></span>
<span data-ttu-id="d0610-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0610-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0610-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0610-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0610-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0610-147">-DefaultProfile</span></span>
<span data-ttu-id="d0610-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0610-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0610-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0610-149">CommonParameters</span></span>
<span data-ttu-id="d0610-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0610-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0610-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0610-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0610-152">輸入</span><span class="sxs-lookup"><span data-stu-id="d0610-152">INPUTS</span></span>

### <span data-ttu-id="d0610-153">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d0610-153">BatchAccountContext</span></span>
<span data-ttu-id="d0610-154">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d0610-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d0610-155">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0610-155">PSComputeNode</span></span>
<span data-ttu-id="d0610-156">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d0610-156">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="d0610-157">輸出</span><span class="sxs-lookup"><span data-stu-id="d0610-157">OUTPUTS</span></span>

## <span data-ttu-id="d0610-158">筆記</span><span class="sxs-lookup"><span data-stu-id="d0610-158">NOTES</span></span>

## <span data-ttu-id="d0610-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0610-159">RELATED LINKS</span></span>

[<span data-ttu-id="d0610-160">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d0610-160">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d0610-161">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0610-161">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="d0610-162">重新開機-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0610-162">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)



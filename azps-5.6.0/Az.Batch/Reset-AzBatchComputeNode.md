---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: c6ad25e5c6ba327ddcd5b4877cbac39937ec4feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910297"
---
# <span data-ttu-id="34de3-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="34de3-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="34de3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="34de3-102">SYNOPSIS</span></span>
<span data-ttu-id="34de3-103">重新安裝指定計算節點上的作業系統。</span><span class="sxs-lookup"><span data-stu-id="34de3-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="34de3-104">語法</span><span class="sxs-lookup"><span data-stu-id="34de3-104">SYNTAX</span></span>

### <span data-ttu-id="34de3-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="34de3-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34de3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="34de3-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34de3-107">描述</span><span class="sxs-lookup"><span data-stu-id="34de3-107">DESCRIPTION</span></span>
<span data-ttu-id="34de3-108">**Reset-AzBatchComputeNode** Cmdlet 會重新安裝指定計算節點上的作業系統。</span><span class="sxs-lookup"><span data-stu-id="34de3-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="34de3-109">例子</span><span class="sxs-lookup"><span data-stu-id="34de3-109">EXAMPLES</span></span>

### <span data-ttu-id="34de3-110">範例 1：重新製作節點的動畫</span><span class="sxs-lookup"><span data-stu-id="34de3-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="34de3-111">此命令在名為 MyPool 的集中使用 ID "tvm-3257026573_2-20150813t200938z" 重新映射計算節點。</span><span class="sxs-lookup"><span data-stu-id="34de3-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="34de3-112">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="34de3-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="34de3-113">範例 2：重新映射一個資料集中的所有節點</span><span class="sxs-lookup"><span data-stu-id="34de3-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="34de3-114">此命令會重新映射處理名為 MyPool 之資料集中的每一個計算節點。</span><span class="sxs-lookup"><span data-stu-id="34de3-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="34de3-115">參數</span><span class="sxs-lookup"><span data-stu-id="34de3-115">PARAMETERS</span></span>

### <span data-ttu-id="34de3-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="34de3-116">-BatchContext</span></span>
<span data-ttu-id="34de3-117">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="34de3-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="34de3-118">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="34de3-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="34de3-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="34de3-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="34de3-120">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="34de3-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="34de3-121">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="34de3-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="34de3-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="34de3-122">-ComputeNode</span></span>
<span data-ttu-id="34de3-123">指定代表要重新映射之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="34de3-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="34de3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34de3-124">-DefaultProfile</span></span>
<span data-ttu-id="34de3-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="34de3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34de3-126">-Id</span><span class="sxs-lookup"><span data-stu-id="34de3-126">-Id</span></span>
<span data-ttu-id="34de3-127">指定要重新映射的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="34de3-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="34de3-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="34de3-128">-PoolId</span></span>
<span data-ttu-id="34de3-129">指定包含計算節點之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="34de3-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="34de3-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="34de3-130">-ReimageOption</span></span>
<span data-ttu-id="34de3-131">指定何時重新製作節點的映射，以及處理目前執行的工作。</span><span class="sxs-lookup"><span data-stu-id="34de3-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="34de3-132">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="34de3-132">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34de3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34de3-133">CommonParameters</span></span>
<span data-ttu-id="34de3-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="34de3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34de3-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34de3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34de3-136">輸入</span><span class="sxs-lookup"><span data-stu-id="34de3-136">INPUTS</span></span>

### <span data-ttu-id="34de3-137">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="34de3-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="34de3-138">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="34de3-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="34de3-139">輸出</span><span class="sxs-lookup"><span data-stu-id="34de3-139">OUTPUTS</span></span>

### <span data-ttu-id="34de3-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="34de3-140">System.Void</span></span>

## <span data-ttu-id="34de3-141">筆記</span><span class="sxs-lookup"><span data-stu-id="34de3-141">NOTES</span></span>

## <span data-ttu-id="34de3-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="34de3-142">RELATED LINKS</span></span>

[<span data-ttu-id="34de3-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="34de3-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="34de3-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="34de3-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="34de3-145">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="34de3-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 998d559265aaa590cb62f72c9e6b9ec9dc5914df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445708"
---
# <span data-ttu-id="ec001-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ec001-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="ec001-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec001-102">SYNOPSIS</span></span>
<span data-ttu-id="ec001-103">在指定的計算節點上重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="ec001-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec001-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec001-104">SYNTAX</span></span>

### <span data-ttu-id="ec001-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="ec001-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec001-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ec001-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec001-107">說明</span><span class="sxs-lookup"><span data-stu-id="ec001-107">DESCRIPTION</span></span>
<span data-ttu-id="ec001-108">**Reset AzureBatchComputeNode** Cmdlet 會在指定的計算節點上重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="ec001-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="ec001-109">示例</span><span class="sxs-lookup"><span data-stu-id="ec001-109">EXAMPLES</span></span>

### <span data-ttu-id="ec001-110">範例1：重新鏡像節點</span><span class="sxs-lookup"><span data-stu-id="ec001-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="ec001-111">這個命令會 reimages 命名為 MyPool 的池中 ID 為「tvm-3257026573_2-20150813t200938z」的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="ec001-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="ec001-112">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="ec001-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ec001-113">範例2：重新鏡像池中的所有節點</span><span class="sxs-lookup"><span data-stu-id="ec001-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="ec001-114">這個命令會 reimages 名為 MyPool 的池中的每個計算節點。</span><span class="sxs-lookup"><span data-stu-id="ec001-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="ec001-115">參數</span><span class="sxs-lookup"><span data-stu-id="ec001-115">PARAMETERS</span></span>

### <span data-ttu-id="ec001-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="ec001-116">-BatchContext</span></span>
<span data-ttu-id="ec001-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="ec001-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ec001-118">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="ec001-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ec001-119">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="ec001-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ec001-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ec001-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ec001-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="ec001-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ec001-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ec001-122">-ComputeNode</span></span>
<span data-ttu-id="ec001-123">指定代表要重新鏡像之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="ec001-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="ec001-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec001-124">-DefaultProfile</span></span>
<span data-ttu-id="ec001-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec001-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec001-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ec001-126">-Id</span></span>
<span data-ttu-id="ec001-127">指定要重新鏡像的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec001-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="ec001-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ec001-128">-PoolId</span></span>
<span data-ttu-id="ec001-129">指定包含計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="ec001-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="ec001-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="ec001-130">-ReimageOption</span></span>
<span data-ttu-id="ec001-131">指定何時要重新鏡像節點，以及如何處理目前執行中的任務。</span><span class="sxs-lookup"><span data-stu-id="ec001-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="ec001-132">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="ec001-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="ec001-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec001-133">CommonParameters</span></span>
<span data-ttu-id="ec001-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec001-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec001-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec001-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec001-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ec001-136">INPUTS</span></span>

### <span data-ttu-id="ec001-137">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ec001-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="ec001-138">參數： ComputeNode (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ec001-138">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="ec001-139">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="ec001-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ec001-140">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ec001-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ec001-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ec001-141">OUTPUTS</span></span>

### <span data-ttu-id="ec001-142">System.void</span><span class="sxs-lookup"><span data-stu-id="ec001-142">System.Void</span></span>

## <span data-ttu-id="ec001-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ec001-143">NOTES</span></span>

## <span data-ttu-id="ec001-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec001-144">RELATED LINKS</span></span>

[<span data-ttu-id="ec001-145">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ec001-145">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="ec001-146">重新開機-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ec001-146">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="ec001-147">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ec001-147">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



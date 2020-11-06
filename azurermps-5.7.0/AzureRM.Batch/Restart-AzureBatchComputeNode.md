---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 5f32963630769dc25ed62f47d93fe47e56abda91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448774"
---
# <span data-ttu-id="07098-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="07098-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="07098-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07098-102">SYNOPSIS</span></span>
<span data-ttu-id="07098-103">重新開機指定的計算節點。</span><span class="sxs-lookup"><span data-stu-id="07098-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07098-104">句法</span><span class="sxs-lookup"><span data-stu-id="07098-104">SYNTAX</span></span>

### <span data-ttu-id="07098-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="07098-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07098-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="07098-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07098-107">說明</span><span class="sxs-lookup"><span data-stu-id="07098-107">DESCRIPTION</span></span>
<span data-ttu-id="07098-108">**Restart AzureBatchComputeNode** Cmdlet 會重新開機指定的計算節點。</span><span class="sxs-lookup"><span data-stu-id="07098-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="07098-109">示例</span><span class="sxs-lookup"><span data-stu-id="07098-109">EXAMPLES</span></span>

### <span data-ttu-id="07098-110">範例1：重新開機計算節點</span><span class="sxs-lookup"><span data-stu-id="07098-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="07098-111">這個命令會在 pool MyPool 中重新開機 ID 為「tvm-3257026573_2-20150813t200938z」的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="07098-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="07098-112">範例2：重新開機池中的每個計算節點</span><span class="sxs-lookup"><span data-stu-id="07098-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="07098-113">這個命令會重新開機 [池 MyPool] 中的每個計算節點。</span><span class="sxs-lookup"><span data-stu-id="07098-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="07098-114">參數</span><span class="sxs-lookup"><span data-stu-id="07098-114">PARAMETERS</span></span>

### <span data-ttu-id="07098-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="07098-115">-BatchContext</span></span>
<span data-ttu-id="07098-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="07098-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="07098-117">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="07098-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="07098-118">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="07098-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="07098-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="07098-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="07098-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="07098-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07098-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="07098-121">-ComputeNode</span></span>
<span data-ttu-id="07098-122">指定代表要重新開機之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="07098-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07098-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07098-123">-DefaultProfile</span></span>
<span data-ttu-id="07098-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07098-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07098-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="07098-125">-Id</span></span>
<span data-ttu-id="07098-126">指定要重新開機的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="07098-126">Specifies the ID of the compute node to reboot.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07098-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="07098-127">-PoolId</span></span>
<span data-ttu-id="07098-128">指定包含計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="07098-128">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07098-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="07098-129">-RebootOption</span></span>
<span data-ttu-id="07098-130">指定何時重新開機節點，以及如何處理目前執行的工作。</span><span class="sxs-lookup"><span data-stu-id="07098-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="07098-131">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="07098-131">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeRebootOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07098-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07098-132">CommonParameters</span></span>
<span data-ttu-id="07098-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07098-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07098-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07098-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07098-135">輸入</span><span class="sxs-lookup"><span data-stu-id="07098-135">INPUTS</span></span>

### <span data-ttu-id="07098-136">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="07098-136">BatchAccountContext</span></span>
<span data-ttu-id="07098-137">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="07098-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="07098-138">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="07098-138">PSComputeNode</span></span>
<span data-ttu-id="07098-139">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="07098-139">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="07098-140">輸出</span><span class="sxs-lookup"><span data-stu-id="07098-140">OUTPUTS</span></span>

## <span data-ttu-id="07098-141">筆記</span><span class="sxs-lookup"><span data-stu-id="07098-141">NOTES</span></span>

## <span data-ttu-id="07098-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="07098-142">RELATED LINKS</span></span>

[<span data-ttu-id="07098-143">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="07098-143">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="07098-144">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="07098-144">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="07098-145">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07098-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



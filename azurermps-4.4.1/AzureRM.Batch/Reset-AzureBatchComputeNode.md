---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624328"
---
# <span data-ttu-id="81dbc-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="81dbc-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="81dbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="81dbc-103">在指定的計算節點上重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="81dbc-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81dbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="81dbc-104">SYNTAX</span></span>

### <span data-ttu-id="81dbc-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="81dbc-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81dbc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="81dbc-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81dbc-107">說明</span><span class="sxs-lookup"><span data-stu-id="81dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="81dbc-108">**Reset AzureBatchComputeNode** Cmdlet 會在指定的計算節點上重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="81dbc-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="81dbc-109">示例</span><span class="sxs-lookup"><span data-stu-id="81dbc-109">EXAMPLES</span></span>

### <span data-ttu-id="81dbc-110">範例1：重新鏡像節點</span><span class="sxs-lookup"><span data-stu-id="81dbc-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="81dbc-111">這個命令會 reimages 命名為 MyPool 的池中 ID 為「tvm-3257026573_2-20150813t200938z」的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="81dbc-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="81dbc-112">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="81dbc-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="81dbc-113">範例2：重新鏡像池中的所有節點</span><span class="sxs-lookup"><span data-stu-id="81dbc-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="81dbc-114">這個命令會 reimages 名為 MyPool 的池中的每個計算節點。</span><span class="sxs-lookup"><span data-stu-id="81dbc-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="81dbc-115">參數</span><span class="sxs-lookup"><span data-stu-id="81dbc-115">PARAMETERS</span></span>

### <span data-ttu-id="81dbc-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="81dbc-116">-BatchContext</span></span>
<span data-ttu-id="81dbc-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="81dbc-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="81dbc-118">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81dbc-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="81dbc-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="81dbc-119">-ComputeNode</span></span>
<span data-ttu-id="81dbc-120">指定代表要重新鏡像之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="81dbc-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="81dbc-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="81dbc-121">-Id</span></span>
<span data-ttu-id="81dbc-122">指定要重新鏡像的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="81dbc-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="81dbc-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="81dbc-123">-PoolId</span></span>
<span data-ttu-id="81dbc-124">指定包含計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="81dbc-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="81dbc-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="81dbc-125">-ReimageOption</span></span>
<span data-ttu-id="81dbc-126">指定何時要重新鏡像節點，以及如何處理目前執行中的任務。</span><span class="sxs-lookup"><span data-stu-id="81dbc-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="81dbc-127">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="81dbc-127">The default is Requeue.</span></span>

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

### <span data-ttu-id="81dbc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81dbc-128">-DefaultProfile</span></span>
<span data-ttu-id="81dbc-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81dbc-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81dbc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81dbc-130">CommonParameters</span></span>
<span data-ttu-id="81dbc-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81dbc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81dbc-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81dbc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81dbc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="81dbc-133">INPUTS</span></span>

### <span data-ttu-id="81dbc-134">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="81dbc-134">BatchAccountContext</span></span>
<span data-ttu-id="81dbc-135">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="81dbc-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="81dbc-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="81dbc-136">PSComputeNode</span></span>
<span data-ttu-id="81dbc-137">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="81dbc-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="81dbc-138">輸出</span><span class="sxs-lookup"><span data-stu-id="81dbc-138">OUTPUTS</span></span>

## <span data-ttu-id="81dbc-139">筆記</span><span class="sxs-lookup"><span data-stu-id="81dbc-139">NOTES</span></span>

## <span data-ttu-id="81dbc-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="81dbc-140">RELATED LINKS</span></span>

[<span data-ttu-id="81dbc-141">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="81dbc-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="81dbc-142">重新開機-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="81dbc-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="81dbc-143">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81dbc-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



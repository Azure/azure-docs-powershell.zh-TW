---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452595"
---
# <span data-ttu-id="381b1-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="381b1-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="381b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="381b1-102">SYNOPSIS</span></span>
<span data-ttu-id="381b1-103">重新開機指定的計算節點。</span><span class="sxs-lookup"><span data-stu-id="381b1-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="381b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="381b1-104">SYNTAX</span></span>

### <span data-ttu-id="381b1-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="381b1-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="381b1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="381b1-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="381b1-107">說明</span><span class="sxs-lookup"><span data-stu-id="381b1-107">DESCRIPTION</span></span>
<span data-ttu-id="381b1-108">**Restart AzureBatchComputeNode** Cmdlet 會重新開機指定的計算節點。</span><span class="sxs-lookup"><span data-stu-id="381b1-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="381b1-109">示例</span><span class="sxs-lookup"><span data-stu-id="381b1-109">EXAMPLES</span></span>

### <span data-ttu-id="381b1-110">範例1：重新開機計算節點</span><span class="sxs-lookup"><span data-stu-id="381b1-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="381b1-111">這個命令會在 pool MyPool 中重新開機 ID 為「tvm-3257026573_2-20150813t200938z」的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="381b1-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="381b1-112">範例2：重新開機池中的每個計算節點</span><span class="sxs-lookup"><span data-stu-id="381b1-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="381b1-113">這個命令會重新開機 [池 MyPool] 中的每個計算節點。</span><span class="sxs-lookup"><span data-stu-id="381b1-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="381b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="381b1-114">PARAMETERS</span></span>

### <span data-ttu-id="381b1-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="381b1-115">-BatchContext</span></span>
<span data-ttu-id="381b1-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="381b1-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="381b1-117">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="381b1-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="381b1-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="381b1-118">-ComputeNode</span></span>
<span data-ttu-id="381b1-119">指定代表要重新開機之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="381b1-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="381b1-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="381b1-120">-Id</span></span>
<span data-ttu-id="381b1-121">指定要重新開機的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="381b1-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="381b1-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="381b1-122">-PoolId</span></span>
<span data-ttu-id="381b1-123">指定包含計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="381b1-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="381b1-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="381b1-124">-RebootOption</span></span>
<span data-ttu-id="381b1-125">指定何時重新開機節點，以及如何處理目前執行的工作。</span><span class="sxs-lookup"><span data-stu-id="381b1-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="381b1-126">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="381b1-126">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381b1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381b1-127">-DefaultProfile</span></span>
<span data-ttu-id="381b1-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="381b1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="381b1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381b1-129">CommonParameters</span></span>
<span data-ttu-id="381b1-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="381b1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381b1-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="381b1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381b1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="381b1-132">INPUTS</span></span>

### <span data-ttu-id="381b1-133">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="381b1-133">BatchAccountContext</span></span>
<span data-ttu-id="381b1-134">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="381b1-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="381b1-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="381b1-135">PSComputeNode</span></span>
<span data-ttu-id="381b1-136">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="381b1-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="381b1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="381b1-137">OUTPUTS</span></span>

## <span data-ttu-id="381b1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="381b1-138">NOTES</span></span>

## <span data-ttu-id="381b1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="381b1-139">RELATED LINKS</span></span>

[<span data-ttu-id="381b1-140">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="381b1-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="381b1-141">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="381b1-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="381b1-142">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="381b1-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



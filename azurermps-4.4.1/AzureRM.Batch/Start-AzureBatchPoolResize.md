---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450852"
---
# <span data-ttu-id="868af-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="868af-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="868af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="868af-102">SYNOPSIS</span></span>
<span data-ttu-id="868af-103">開始調整池子的大小。</span><span class="sxs-lookup"><span data-stu-id="868af-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="868af-104">句法</span><span class="sxs-lookup"><span data-stu-id="868af-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="868af-105">說明</span><span class="sxs-lookup"><span data-stu-id="868af-105">DESCRIPTION</span></span>
<span data-ttu-id="868af-106">**AzureBatchPoolResize** Cmdlet 會在池中啟動 Azure Batch 調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="868af-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="868af-107">示例</span><span class="sxs-lookup"><span data-stu-id="868af-107">EXAMPLES</span></span>

### <span data-ttu-id="868af-108">範例1：將池大小調整成12個節點</span><span class="sxs-lookup"><span data-stu-id="868af-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="868af-109">這個命令會在具有識別碼 ContosoPool06 的池中啟動調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="868af-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="868af-110">操作的目標是12個專用的計算節點。</span><span class="sxs-lookup"><span data-stu-id="868af-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="868af-111">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="868af-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="868af-112">範例2：使用解除配置選項調整池子的大小</span><span class="sxs-lookup"><span data-stu-id="868af-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="868af-113">這個 Cmdlet 會將一個池大小調整為五個專用的計算節點。</span><span class="sxs-lookup"><span data-stu-id="868af-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="868af-114">命令會使用 Get-AzureBatchPool Cmdlet 來取得具有識別碼 ContosoPool06 的 pool。</span><span class="sxs-lookup"><span data-stu-id="868af-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="868af-115">透過使用管線運算子，命令會將該 pool 物件傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="868af-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="868af-116">命令會在該文檔池中啟動調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="868af-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="868af-117">目標是五個專用的計算節點。</span><span class="sxs-lookup"><span data-stu-id="868af-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="868af-118">此命令指定一個小時的超時時間。</span><span class="sxs-lookup"><span data-stu-id="868af-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="868af-119">命令會指定 [終止] 的解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="868af-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="868af-120">參數</span><span class="sxs-lookup"><span data-stu-id="868af-120">PARAMETERS</span></span>

### <span data-ttu-id="868af-121">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="868af-121">-BatchContext</span></span>
<span data-ttu-id="868af-122">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="868af-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="868af-123">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="868af-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="868af-124">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="868af-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="868af-125">指定此 Cmdlet 啟動之大小調整作業的解除配置選項。</span><span class="sxs-lookup"><span data-stu-id="868af-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="868af-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="868af-126">-Id</span></span>
<span data-ttu-id="868af-127">指定此 Cmdlet 調整大小的池 ID。</span><span class="sxs-lookup"><span data-stu-id="868af-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="868af-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="868af-128">-ResizeTimeout</span></span>
<span data-ttu-id="868af-129">指定調整大小作業的超時週期。</span><span class="sxs-lookup"><span data-stu-id="868af-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="868af-130">如果此時間池未達到目標大小，則會停止調整大小操作。</span><span class="sxs-lookup"><span data-stu-id="868af-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="868af-131">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="868af-131">-TargetDedicated</span></span>
<span data-ttu-id="868af-132">指定專用計算節點的目標數目。</span><span class="sxs-lookup"><span data-stu-id="868af-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="868af-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="868af-133">-DefaultProfile</span></span>
<span data-ttu-id="868af-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="868af-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="868af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868af-135">CommonParameters</span></span>
<span data-ttu-id="868af-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="868af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868af-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="868af-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868af-138">輸入</span><span class="sxs-lookup"><span data-stu-id="868af-138">INPUTS</span></span>

### <span data-ttu-id="868af-139">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="868af-139">BatchAccountContext</span></span>
<span data-ttu-id="868af-140">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="868af-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="868af-141">字串</span><span class="sxs-lookup"><span data-stu-id="868af-141">String</span></span>
<span data-ttu-id="868af-142">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="868af-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="868af-143">輸出</span><span class="sxs-lookup"><span data-stu-id="868af-143">OUTPUTS</span></span>

## <span data-ttu-id="868af-144">筆記</span><span class="sxs-lookup"><span data-stu-id="868af-144">NOTES</span></span>

## <span data-ttu-id="868af-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="868af-145">RELATED LINKS</span></span>

[<span data-ttu-id="868af-146">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="868af-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="868af-147">AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="868af-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="868af-148">停止 AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="868af-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="868af-149">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="868af-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



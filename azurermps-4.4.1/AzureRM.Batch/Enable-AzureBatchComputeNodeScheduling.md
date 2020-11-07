---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 6c890836d8ca22e617fdc88788a6809cbce8581c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625534"
---
# <span data-ttu-id="899db-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="899db-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="899db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="899db-102">SYNOPSIS</span></span>
<span data-ttu-id="899db-103">在指定的計算節點上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="899db-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="899db-104">句法</span><span class="sxs-lookup"><span data-stu-id="899db-104">SYNTAX</span></span>

### <span data-ttu-id="899db-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="899db-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="899db-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="899db-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="899db-107">說明</span><span class="sxs-lookup"><span data-stu-id="899db-107">DESCRIPTION</span></span>
<span data-ttu-id="899db-108">**Enable-AzureBatchComputeNodeScheduling** Cmdlet 可在指定的計算節點上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="899db-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="899db-109">計算節點是專用於特定應用程式工作負載的 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="899db-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="899db-110">示例</span><span class="sxs-lookup"><span data-stu-id="899db-110">EXAMPLES</span></span>

### <span data-ttu-id="899db-111">範例1：在計算節點上啟用任務排程</span><span class="sxs-lookup"><span data-stu-id="899db-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="899db-112">這些命令會在 compute 節點 tvm-1783593343_34-20151117t222514z 上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="899db-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="899db-113">若要這樣做，範例中的第一個命令會建立包含批次帳戶 contosobatchaccount 之帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="899db-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="899db-114">這個物件參照會儲存在名為 $coNtext 的變數中。</span><span class="sxs-lookup"><span data-stu-id="899db-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="899db-115">然後，第二個命令會使用這個物件參照和 **enable-AzureBatchComputeNodeScheduling** Cmdlet 來連線至 [pool myPool]，並在 tvm-1783593343_34-20151117t222514z 上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="899db-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="899db-116">範例2：在池中的計算節點上啟用任務排程</span><span class="sxs-lookup"><span data-stu-id="899db-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="899db-117">這些命令會在 [pool Pool06] 中的所有計算節點上啟用 [任務排程]。</span><span class="sxs-lookup"><span data-stu-id="899db-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="899db-118">若要執行這項工作，範例中的第一個命令會建立包含批次帳戶 contosobatchaccount 之帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="899db-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="899db-119">這個物件參照會儲存在名為 $coNtext 的變數中。</span><span class="sxs-lookup"><span data-stu-id="899db-119">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="899db-120">接著，這個範例中的第二個命令會使用這個物件參考，並 **取得 AzureBatchComputeNode** ，以傳回在 Pool06 中找到的所有計算節點集合。</span><span class="sxs-lookup"><span data-stu-id="899db-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="899db-121">然後，該集合會輸送成 **AzureBatchComputeNodeScheduling** Cmdlet，這會在集合中的每個計算節點上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="899db-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="899db-122">參數</span><span class="sxs-lookup"><span data-stu-id="899db-122">PARAMETERS</span></span>

### <span data-ttu-id="899db-123">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="899db-123">-BatchContext</span></span>
<span data-ttu-id="899db-124">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="899db-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="899db-125">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="899db-125">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="899db-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="899db-126">-ComputeNode</span></span>
<span data-ttu-id="899db-127">指定要啟用任務排程的計算節點物件參照。</span><span class="sxs-lookup"><span data-stu-id="899db-127">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="899db-128">這個物件參照是使用 Get-AzureBatchComputeNode Cmdlet 建立，並將傳回的計算節點物件儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="899db-128">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="899db-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="899db-129">-Id</span></span>
<span data-ttu-id="899db-130">指定啟用 [任務排程] 的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="899db-130">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="899db-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="899db-131">-PoolId</span></span>
<span data-ttu-id="899db-132">指定包含已啟用任務排程之計算節點的批次池識別碼。</span><span class="sxs-lookup"><span data-stu-id="899db-132">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="899db-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899db-133">-DefaultProfile</span></span>
<span data-ttu-id="899db-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="899db-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="899db-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899db-135">CommonParameters</span></span>
<span data-ttu-id="899db-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="899db-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899db-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="899db-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899db-138">輸入</span><span class="sxs-lookup"><span data-stu-id="899db-138">INPUTS</span></span>

### <span data-ttu-id="899db-139">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="899db-139">BatchAccountContext</span></span>
<span data-ttu-id="899db-140">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="899db-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="899db-141">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="899db-141">PSComputeNode</span></span>
<span data-ttu-id="899db-142">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="899db-142">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="899db-143">輸出</span><span class="sxs-lookup"><span data-stu-id="899db-143">OUTPUTS</span></span>

## <span data-ttu-id="899db-144">筆記</span><span class="sxs-lookup"><span data-stu-id="899db-144">NOTES</span></span>

## <span data-ttu-id="899db-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="899db-145">RELATED LINKS</span></span>

[<span data-ttu-id="899db-146">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="899db-146">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)



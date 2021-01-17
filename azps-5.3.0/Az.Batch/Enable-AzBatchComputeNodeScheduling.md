---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447027"
---
# <span data-ttu-id="30550-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="30550-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="30550-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30550-102">SYNOPSIS</span></span>
<span data-ttu-id="30550-103">在指定的計算節點上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="30550-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="30550-104">句法</span><span class="sxs-lookup"><span data-stu-id="30550-104">SYNTAX</span></span>

### <span data-ttu-id="30550-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="30550-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30550-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="30550-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30550-107">說明</span><span class="sxs-lookup"><span data-stu-id="30550-107">DESCRIPTION</span></span>
<span data-ttu-id="30550-108">**Enable-AzBatchComputeNodeScheduling** Cmdlet 可在指定的計算節點上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="30550-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="30550-109">計算節點是專用於特定應用程式工作負載的 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="30550-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="30550-110">示例</span><span class="sxs-lookup"><span data-stu-id="30550-110">EXAMPLES</span></span>

### <span data-ttu-id="30550-111">範例1：在計算節點上啟用任務排程</span><span class="sxs-lookup"><span data-stu-id="30550-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="30550-112">這些命令會在 compute 節點 tvm-1783593343_34-20151117t222514z 上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="30550-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="30550-113">若要這樣做，範例中的第一個命令會建立包含批次帳戶 contosobatchaccount 之帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="30550-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="30550-114">這個物件參照會儲存在名為 $coNtext 的變數中。</span><span class="sxs-lookup"><span data-stu-id="30550-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="30550-115">然後，第二個命令會使用這個物件參照和 **enable-AzBatchComputeNodeScheduling** Cmdlet 來連線至 [pool myPool]，並在 tvm-1783593343_34-20151117t222514z 上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="30550-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="30550-116">範例2：在池中的計算節點上啟用任務排程</span><span class="sxs-lookup"><span data-stu-id="30550-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="30550-117">這些命令會在 [pool Pool06] 中的所有計算節點上啟用 [任務排程]。</span><span class="sxs-lookup"><span data-stu-id="30550-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="30550-118">若要執行這項工作，範例中的第一個命令會建立包含批次帳戶 contosobatchaccount 之帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="30550-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="30550-119">這個物件參照會儲存在名為 $coNtext 的變數中。</span><span class="sxs-lookup"><span data-stu-id="30550-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="30550-120">接著，這個範例中的第二個命令會使用這個物件參考，並 **取得 AzBatchComputeNode** ，以傳回在 Pool06 中找到的所有計算節點集合。</span><span class="sxs-lookup"><span data-stu-id="30550-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="30550-121">然後，該集合會輸送成 **AzBatchComputeNodeScheduling** Cmdlet，這會在集合中的每個計算節點上啟用任務排程。</span><span class="sxs-lookup"><span data-stu-id="30550-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="30550-122">參數</span><span class="sxs-lookup"><span data-stu-id="30550-122">PARAMETERS</span></span>

### <span data-ttu-id="30550-123">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="30550-123">-BatchContext</span></span>
<span data-ttu-id="30550-124">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="30550-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="30550-125">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="30550-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="30550-126">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="30550-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="30550-127">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="30550-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="30550-128">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="30550-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="30550-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="30550-129">-ComputeNode</span></span>
<span data-ttu-id="30550-130">指定要啟用任務排程的計算節點物件參照。</span><span class="sxs-lookup"><span data-stu-id="30550-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="30550-131">這個物件參照是使用 Get-AzBatchComputeNode Cmdlet 建立，並將傳回的計算節點物件儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="30550-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="30550-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30550-132">-DefaultProfile</span></span>
<span data-ttu-id="30550-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30550-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30550-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="30550-134">-Id</span></span>
<span data-ttu-id="30550-135">指定啟用 [任務排程] 的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="30550-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="30550-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="30550-136">-PoolId</span></span>
<span data-ttu-id="30550-137">指定包含已啟用任務排程之計算節點的批次池識別碼。</span><span class="sxs-lookup"><span data-stu-id="30550-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="30550-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30550-138">CommonParameters</span></span>
<span data-ttu-id="30550-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30550-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30550-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="30550-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30550-141">輸入</span><span class="sxs-lookup"><span data-stu-id="30550-141">INPUTS</span></span>

### <span data-ttu-id="30550-142">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="30550-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="30550-143">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="30550-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="30550-144">輸出</span><span class="sxs-lookup"><span data-stu-id="30550-144">OUTPUTS</span></span>

### <span data-ttu-id="30550-145">System.void</span><span class="sxs-lookup"><span data-stu-id="30550-145">System.Void</span></span>

## <span data-ttu-id="30550-146">筆記</span><span class="sxs-lookup"><span data-stu-id="30550-146">NOTES</span></span>

## <span data-ttu-id="30550-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="30550-147">RELATED LINKS</span></span>

[<span data-ttu-id="30550-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="30550-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913258"
---
# <span data-ttu-id="37115-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="37115-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="37115-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37115-102">SYNOPSIS</span></span>
<span data-ttu-id="37115-103">啟用指定計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="37115-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="37115-104">語法</span><span class="sxs-lookup"><span data-stu-id="37115-104">SYNTAX</span></span>

### <span data-ttu-id="37115-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="37115-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37115-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="37115-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37115-107">描述</span><span class="sxs-lookup"><span data-stu-id="37115-107">DESCRIPTION</span></span>
<span data-ttu-id="37115-108">**Enable-AzBatchComputeNodeScheduling** Cmdlet 可啟用指定計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="37115-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="37115-109">計算節點是專屬於特定應用程式工作負載的 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="37115-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="37115-110">例子</span><span class="sxs-lookup"><span data-stu-id="37115-110">EXAMPLES</span></span>

### <span data-ttu-id="37115-111">範例 1：啟用計算節點上的任務排程</span><span class="sxs-lookup"><span data-stu-id="37115-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="37115-112">這些命令可啟用計算節點 tvm-1783593343_34-20151117t222514z 上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="37115-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="37115-113">若要這麼做，範例中的第一個命令會建立一個物件參照，其中包含批次帳戶 contosobatchaccount的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="37115-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="37115-114">此物件參照會儲存在名為 $coNtext 的$coNtext。</span><span class="sxs-lookup"><span data-stu-id="37115-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="37115-115">接著，第二個命令會使用此物件參照和 **Enable-AzBatchComputeNodeScheduling** Cmdlet 來連接到 myPool 的資料庫，並啟用 tvm-1783593343_34-20151117t222514z 上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="37115-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="37115-116">範例 2：啟用資料集中計算節點上的任務排程</span><span class="sxs-lookup"><span data-stu-id="37115-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="37115-117">這些命令可啟用在集區集區 06 中所有計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="37115-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="37115-118">若要執行這項工作，範例中的第一個命令會建立一個物件參照，其中包含批次帳戶 contosobatchaccount的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="37115-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="37115-119">此物件參照會儲存在名為 $coNtext 的$coNtext。</span><span class="sxs-lookup"><span data-stu-id="37115-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="37115-120">接著，範例中的第二個命令會使用此物件參照和 **Get-AzBatchComputeNode，** 以返回 Pool06 中找到的所有計算節點集合。</span><span class="sxs-lookup"><span data-stu-id="37115-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="37115-121">該集合接著會傳輸至 **Enable-AzBatchComputeNodeScheduling** Cmdlet，這可讓集合中的每個計算節點上的任務排程。</span><span class="sxs-lookup"><span data-stu-id="37115-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="37115-122">參數</span><span class="sxs-lookup"><span data-stu-id="37115-122">PARAMETERS</span></span>

### <span data-ttu-id="37115-123">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="37115-123">-BatchContext</span></span>
<span data-ttu-id="37115-124">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="37115-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="37115-125">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="37115-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="37115-126">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="37115-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="37115-127">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="37115-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="37115-128">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="37115-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="37115-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="37115-129">-ComputeNode</span></span>
<span data-ttu-id="37115-130">指定啟用任務排程之計算節點的物件參照。</span><span class="sxs-lookup"><span data-stu-id="37115-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="37115-131">此物件參照是使用 Get-AzBatchComputeNode Cmdlet，並儲存于變數中所返回的計算節點物件所建立。</span><span class="sxs-lookup"><span data-stu-id="37115-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="37115-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37115-132">-DefaultProfile</span></span>
<span data-ttu-id="37115-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37115-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37115-134">-Id</span><span class="sxs-lookup"><span data-stu-id="37115-134">-Id</span></span>
<span data-ttu-id="37115-135">指定啟用任務排程的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="37115-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="37115-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="37115-136">-PoolId</span></span>
<span data-ttu-id="37115-137">指定包含啟用任務排程之計算節點的批次集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="37115-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="37115-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37115-138">CommonParameters</span></span>
<span data-ttu-id="37115-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37115-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37115-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37115-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37115-141">輸入</span><span class="sxs-lookup"><span data-stu-id="37115-141">INPUTS</span></span>

### <span data-ttu-id="37115-142">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="37115-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="37115-143">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="37115-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="37115-144">輸出</span><span class="sxs-lookup"><span data-stu-id="37115-144">OUTPUTS</span></span>

### <span data-ttu-id="37115-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="37115-145">System.Void</span></span>

## <span data-ttu-id="37115-146">筆記</span><span class="sxs-lookup"><span data-stu-id="37115-146">NOTES</span></span>

## <span data-ttu-id="37115-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="37115-147">RELATED LINKS</span></span>

[<span data-ttu-id="37115-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="37115-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)



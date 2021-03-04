---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: daf89fec73ed18cf5b67c4100556d490795708d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910293"
---
# <span data-ttu-id="05361-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="05361-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="05361-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05361-102">SYNOPSIS</span></span>
<span data-ttu-id="05361-103">重新開機指定的計算節點。</span><span class="sxs-lookup"><span data-stu-id="05361-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="05361-104">語法</span><span class="sxs-lookup"><span data-stu-id="05361-104">SYNTAX</span></span>

### <span data-ttu-id="05361-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="05361-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05361-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="05361-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05361-107">描述</span><span class="sxs-lookup"><span data-stu-id="05361-107">DESCRIPTION</span></span>
<span data-ttu-id="05361-108">**Restart-AzBatchComputeNode** Cmdlet 會重新開機指定的計算節點。</span><span class="sxs-lookup"><span data-stu-id="05361-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="05361-109">例子</span><span class="sxs-lookup"><span data-stu-id="05361-109">EXAMPLES</span></span>

### <span data-ttu-id="05361-110">範例 1：重新開機計算節點</span><span class="sxs-lookup"><span data-stu-id="05361-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="05361-111">此命令會重新開機計算節點，其識別碼為 "tvm-3257026573_2-20150813t200938z" 的 MyPool。</span><span class="sxs-lookup"><span data-stu-id="05361-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="05361-112">範例 2：重新開機資料集中的每一個計算節點</span><span class="sxs-lookup"><span data-stu-id="05361-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="05361-113">此命令會重新開機 MyPool 資料集中的每一個計算節點。</span><span class="sxs-lookup"><span data-stu-id="05361-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="05361-114">參數</span><span class="sxs-lookup"><span data-stu-id="05361-114">PARAMETERS</span></span>

### <span data-ttu-id="05361-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="05361-115">-BatchContext</span></span>
<span data-ttu-id="05361-116">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="05361-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="05361-117">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="05361-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="05361-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="05361-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="05361-119">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="05361-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="05361-120">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="05361-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="05361-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="05361-121">-ComputeNode</span></span>
<span data-ttu-id="05361-122">指定代表要重新開機之計算節點的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="05361-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="05361-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05361-123">-DefaultProfile</span></span>
<span data-ttu-id="05361-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="05361-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05361-125">-Id</span><span class="sxs-lookup"><span data-stu-id="05361-125">-Id</span></span>
<span data-ttu-id="05361-126">指定要重新開機的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="05361-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="05361-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="05361-127">-PoolId</span></span>
<span data-ttu-id="05361-128">指定包含計算節點之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="05361-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="05361-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="05361-129">-RebootOption</span></span>
<span data-ttu-id="05361-130">指定何時重新開機節點，以及處理目前執行的工作。</span><span class="sxs-lookup"><span data-stu-id="05361-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="05361-131">預設值為 Requeue。</span><span class="sxs-lookup"><span data-stu-id="05361-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="05361-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05361-132">CommonParameters</span></span>
<span data-ttu-id="05361-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05361-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05361-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05361-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05361-135">輸入</span><span class="sxs-lookup"><span data-stu-id="05361-135">INPUTS</span></span>

### <span data-ttu-id="05361-136">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="05361-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="05361-137">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="05361-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="05361-138">輸出</span><span class="sxs-lookup"><span data-stu-id="05361-138">OUTPUTS</span></span>

### <span data-ttu-id="05361-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="05361-139">System.Void</span></span>

## <span data-ttu-id="05361-140">筆記</span><span class="sxs-lookup"><span data-stu-id="05361-140">NOTES</span></span>

## <span data-ttu-id="05361-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="05361-141">RELATED LINKS</span></span>

[<span data-ttu-id="05361-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="05361-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="05361-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="05361-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="05361-144">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05361-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

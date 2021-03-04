---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: 10338e63ed060c1b93c67a2050d28346641f1911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916650"
---
# <span data-ttu-id="5744f-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="5744f-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="5744f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5744f-102">SYNOPSIS</span></span>
<span data-ttu-id="5744f-103">根據資料組識別碼分組的節點狀態，獲得批次節點計數。</span><span class="sxs-lookup"><span data-stu-id="5744f-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="5744f-104">語法</span><span class="sxs-lookup"><span data-stu-id="5744f-104">SYNTAX</span></span>

### <span data-ttu-id="5744f-105">AzureBatchPoolNodeCounts (預設) </span><span class="sxs-lookup"><span data-stu-id="5744f-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5744f-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="5744f-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5744f-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5744f-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5744f-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="5744f-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5744f-109">描述</span><span class="sxs-lookup"><span data-stu-id="5744f-109">DESCRIPTION</span></span>
<span data-ttu-id="5744f-110">Cmdlet Get-AzBatchPoolNodeCount可讓客戶取得每個節點狀態根據群組分組的節點計數。</span><span class="sxs-lookup"><span data-stu-id="5744f-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="5744f-111">可能的節點狀態為建立、閒置、離開Pool、離線、優先、重新開機、重新映射、執行、啟動、startTaskFailed、未知、無法使用和等待ForStartTask。</span><span class="sxs-lookup"><span data-stu-id="5744f-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="5744f-112">Cmdlet 會採用 PoolId 或 Pool 參數，只篩選指定有資料組識別碼的區。</span><span class="sxs-lookup"><span data-stu-id="5744f-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="5744f-113">例子</span><span class="sxs-lookup"><span data-stu-id="5744f-113">EXAMPLES</span></span>

### <span data-ttu-id="5744f-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="5744f-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="5744f-115">在目前批次帳戶上下文下的資料庫每個節點狀態的清單節點計數。</span><span class="sxs-lookup"><span data-stu-id="5744f-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="5744f-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="5744f-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="5744f-117">顯示給定資料組識別碼之每個節點狀態節點計數。</span><span class="sxs-lookup"><span data-stu-id="5744f-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="5744f-118">參數</span><span class="sxs-lookup"><span data-stu-id="5744f-118">PARAMETERS</span></span>

### <span data-ttu-id="5744f-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="5744f-119">-BatchContext</span></span>
<span data-ttu-id="5744f-120">BatchAccountCoNtext 實例，用於與批次處理服務互動。</span><span class="sxs-lookup"><span data-stu-id="5744f-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="5744f-121">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="5744f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="5744f-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="5744f-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="5744f-123">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5744f-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="5744f-124">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="5744f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5744f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5744f-125">-DefaultProfile</span></span>
<span data-ttu-id="5744f-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5744f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5744f-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5744f-127">-MaxCount</span></span>
<span data-ttu-id="5744f-128">指定要返回的資料庫數量上限。</span><span class="sxs-lookup"><span data-stu-id="5744f-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="5744f-129">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="5744f-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5744f-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="5744f-130">-Pool</span></span>
<span data-ttu-id="5744f-131">指定 **PSCloudPool，** 以取得節點計數。</span><span class="sxs-lookup"><span data-stu-id="5744f-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5744f-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5744f-132">-PoolId</span></span>
<span data-ttu-id="5744f-133">取得節點計數之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5744f-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5744f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5744f-134">CommonParameters</span></span>
<span data-ttu-id="5744f-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5744f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5744f-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5744f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5744f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="5744f-137">INPUTS</span></span>

### <span data-ttu-id="5744f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5744f-138">System.String</span></span>

### <span data-ttu-id="5744f-139">Microsoft.Azure.Commands.Batch。Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="5744f-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="5744f-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5744f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5744f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5744f-141">OUTPUTS</span></span>

### <span data-ttu-id="5744f-142">Microsoft.Azure.Commands.Batch。Models.PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="5744f-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="5744f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5744f-143">NOTES</span></span>

## <span data-ttu-id="5744f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5744f-144">RELATED LINKS</span></span>

[<span data-ttu-id="5744f-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5744f-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="5744f-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5744f-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="5744f-147">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5744f-147">Azure Batch Cmdlets</span></span>]()


---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolnodecounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolNodeCounts.md
ms.openlocfilehash: 6cd15b6a8ee59982bf328f751a20807835f54513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624626"
---
# <span data-ttu-id="fed1c-101">Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="fed1c-101">Get-AzureBatchPoolNodeCounts</span></span>

## <span data-ttu-id="fed1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fed1c-102">SYNOPSIS</span></span>
<span data-ttu-id="fed1c-103">取得依 [池 id] 分組的每個節點狀態的批節點計數。</span><span class="sxs-lookup"><span data-stu-id="fed1c-103">Gets Batch node counts per node state grouped by pool id.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fed1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="fed1c-104">SYNTAX</span></span>

### <span data-ttu-id="fed1c-105">AzureBatchPoolNodeCounts (預設) </span><span class="sxs-lookup"><span data-stu-id="fed1c-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzureBatchPoolNodeCounts -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fed1c-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="fed1c-106">PoolId</span></span>
```
Get-AzureBatchPoolNodeCounts [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fed1c-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="fed1c-107">ParentObject</span></span>
```
Get-AzureBatchPoolNodeCounts [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fed1c-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="fed1c-108">ODataFilter</span></span>
```
Get-AzureBatchPoolNodeCounts [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fed1c-109">說明</span><span class="sxs-lookup"><span data-stu-id="fed1c-109">DESCRIPTION</span></span>
<span data-ttu-id="fed1c-110">Get-AzureBatchPoolNodeCounts Cmdlet 可讓客戶取得依池分組的每個節點狀態的節點數。</span><span class="sxs-lookup"><span data-stu-id="fed1c-110">The Get-AzureBatchPoolNodeCounts cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="fed1c-111">可能的節點狀態是 [建立]、[空閒]、[leavingPool]、[離線]、[已搶佔]、[重新開機]、[重新格式化]、[執行]、[無法</span><span class="sxs-lookup"><span data-stu-id="fed1c-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="fed1c-112">這個 Cmdlet 會採用 PoolId 或 Pool 參數，只篩選指定了 pool id 的 pool。</span><span class="sxs-lookup"><span data-stu-id="fed1c-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="fed1c-113">示例</span><span class="sxs-lookup"><span data-stu-id="fed1c-113">EXAMPLES</span></span>

### <span data-ttu-id="fed1c-114">範例1</span><span class="sxs-lookup"><span data-stu-id="fed1c-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="fed1c-115">在目前的批次帳戶內容下，針對每個節點狀態的清單節點計數。</span><span class="sxs-lookup"><span data-stu-id="fed1c-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="fed1c-116">範例2</span><span class="sxs-lookup"><span data-stu-id="fed1c-116">Example 2</span></span>

```powershell
PS C:\> Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzureBatchPoolNodeCounts -BatchContext $batchContext -PoolId "contosopool1"
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

PS C:\> Get-AzureBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzureBatchPoolNodeCounts -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="fed1c-117">針對指定的 pool id 顯示每個節點的節點計數（針對每個節點的狀態）。</span><span class="sxs-lookup"><span data-stu-id="fed1c-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="fed1c-118">參數</span><span class="sxs-lookup"><span data-stu-id="fed1c-118">PARAMETERS</span></span>

### <span data-ttu-id="fed1c-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="fed1c-119">-BatchContext</span></span>
<span data-ttu-id="fed1c-120">與批次服務互動時要使用的 BatchAccountCoNtext 實例。</span><span class="sxs-lookup"><span data-stu-id="fed1c-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="fed1c-121">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="fed1c-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="fed1c-122">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="fed1c-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="fed1c-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="fed1c-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="fed1c-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="fed1c-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fed1c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed1c-125">-DefaultProfile</span></span>
<span data-ttu-id="fed1c-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fed1c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fed1c-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fed1c-127">-MaxCount</span></span>
<span data-ttu-id="fed1c-128">指定要傳回的最大池數。</span><span class="sxs-lookup"><span data-stu-id="fed1c-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="fed1c-129">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="fed1c-129">The default value is 10.</span></span>

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

### <span data-ttu-id="fed1c-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="fed1c-130">-Pool</span></span>
<span data-ttu-id="fed1c-131">指定要取得其節點計數的 **PSCloudPool** 。</span><span class="sxs-lookup"><span data-stu-id="fed1c-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="fed1c-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="fed1c-132">-PoolId</span></span>
<span data-ttu-id="fed1c-133">要取得節點計數的池 id。</span><span class="sxs-lookup"><span data-stu-id="fed1c-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="fed1c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed1c-134">CommonParameters</span></span>
<span data-ttu-id="fed1c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fed1c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed1c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fed1c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed1c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="fed1c-137">INPUTS</span></span>

### <span data-ttu-id="fed1c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="fed1c-138">System.String</span></span>

### <span data-ttu-id="fed1c-139">Microsoft.Azure.Commands.Batch。PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="fed1c-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="fed1c-140">參數： Pool (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fed1c-140">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="fed1c-141">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="fed1c-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="fed1c-142">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fed1c-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="fed1c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="fed1c-143">OUTPUTS</span></span>

### <span data-ttu-id="fed1c-144">Microsoft.Azure.Commands.Batch。PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="fed1c-144">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="fed1c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="fed1c-145">NOTES</span></span>

## <span data-ttu-id="fed1c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="fed1c-146">RELATED LINKS</span></span>

[<span data-ttu-id="fed1c-147">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fed1c-147">Get-AzureRmBatchAccountKeys</span></span>]()

[<span data-ttu-id="fed1c-148">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fed1c-148">Get-AzureBatchJob</span></span>]()

[<span data-ttu-id="fed1c-149">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fed1c-149">Azure Batch Cmdlets</span></span>]()


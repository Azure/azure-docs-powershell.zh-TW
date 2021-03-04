---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: 2adaebc28f27d2ea785df5a93510375020bcd542
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911762"
---
# <span data-ttu-id="d5061-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d5061-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="d5061-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d5061-102">SYNOPSIS</span></span>
<span data-ttu-id="d5061-103">從資料庫獲得批次處理節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="d5061-104">語法</span><span class="sxs-lookup"><span data-stu-id="d5061-104">SYNTAX</span></span>

### <span data-ttu-id="d5061-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="d5061-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5061-106">Id</span><span class="sxs-lookup"><span data-stu-id="d5061-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5061-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="d5061-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5061-108">描述</span><span class="sxs-lookup"><span data-stu-id="d5061-108">DESCRIPTION</span></span>
<span data-ttu-id="d5061-109">**Get-AzBatchComputeNode** Cmdlet 會從資料庫取得 Azure Batch 計算節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="d5061-110">指定 *PoolID 或 Pool* *參數* 。</span><span class="sxs-lookup"><span data-stu-id="d5061-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="d5061-111">指定 *Id* 參數以取得單一計算節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="d5061-112">指定 *Filter* 參數，以取得符合 OData (開啟資料通訊協定) 節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="d5061-113">例子</span><span class="sxs-lookup"><span data-stu-id="d5061-113">EXAMPLES</span></span>

### <span data-ttu-id="d5061-114">範例 1：根據識別碼取得計算節點</span><span class="sxs-lookup"><span data-stu-id="d5061-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="d5061-115">此命令會從具有識別碼 Pool06 的集中，獲得具有 ID tvm-2316545714_1-20150725t21320z 的計算節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d5061-116">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="d5061-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d5061-117">範例 2：從資料庫取得所有閒置計算節點</span><span class="sxs-lookup"><span data-stu-id="d5061-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="d5061-118">此命令會獲得包含識別碼資料庫06 之資料庫中的所有閒置計算節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d5061-119">命令會使用 Filter 參數指定 *閒置狀態。*</span><span class="sxs-lookup"><span data-stu-id="d5061-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="d5061-120">範例 3：取得指定資料集中的所有計算節點</span><span class="sxs-lookup"><span data-stu-id="d5061-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="d5061-121">此命令會使用 Cmdlet 的識別碼Get-AzBatchPool。</span><span class="sxs-lookup"><span data-stu-id="d5061-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="d5061-122">該命令會使用管線運算子，將該區段傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5061-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d5061-123">該 Cmdlet 會從該計算區獲得所有計算節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="d5061-124">參數</span><span class="sxs-lookup"><span data-stu-id="d5061-124">PARAMETERS</span></span>

### <span data-ttu-id="d5061-125">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d5061-125">-BatchContext</span></span>
<span data-ttu-id="d5061-126">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d5061-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d5061-127">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="d5061-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d5061-128">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="d5061-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d5061-129">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d5061-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d5061-130">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="d5061-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d5061-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5061-131">-DefaultProfile</span></span>
<span data-ttu-id="d5061-132">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5061-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5061-133">-篩選</span><span class="sxs-lookup"><span data-stu-id="d5061-133">-Filter</span></span>
<span data-ttu-id="d5061-134">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="d5061-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="d5061-135">此 Cmdlet 會返回符合此參數指定之篩選的計算節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="d5061-136">如果您未指定篩選，此 Cmdlet 會針對該資料庫會返回所有計算節點。</span><span class="sxs-lookup"><span data-stu-id="d5061-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5061-137">-Id</span><span class="sxs-lookup"><span data-stu-id="d5061-137">-Id</span></span>
<span data-ttu-id="d5061-138">指定此 Cmdlet 從資料組獲得之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5061-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="d5061-139">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d5061-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5061-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d5061-140">-MaxCount</span></span>
<span data-ttu-id="d5061-141">指定要返回的計算節點數目上限。</span><span class="sxs-lookup"><span data-stu-id="d5061-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="d5061-142">如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="d5061-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="d5061-143">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="d5061-143">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5061-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="d5061-144">-Pool</span></span>
<span data-ttu-id="d5061-145">指定包含計算節點 **的 PSCloudPool** 物件集區。</span><span class="sxs-lookup"><span data-stu-id="d5061-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="d5061-146">若要取得 **PSCloudPool** 物件，請使用 Get-AzBatchPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5061-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5061-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d5061-147">-PoolId</span></span>
<span data-ttu-id="d5061-148">指定包含計算節點之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5061-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5061-149">-選取</span><span class="sxs-lookup"><span data-stu-id="d5061-149">-Select</span></span>
<span data-ttu-id="d5061-150">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="d5061-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="d5061-151">指定此參數的值以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="d5061-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5061-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5061-152">CommonParameters</span></span>
<span data-ttu-id="d5061-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d5061-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5061-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5061-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5061-155">輸入</span><span class="sxs-lookup"><span data-stu-id="d5061-155">INPUTS</span></span>

### <span data-ttu-id="d5061-156">System.String</span><span class="sxs-lookup"><span data-stu-id="d5061-156">System.String</span></span>

### <span data-ttu-id="d5061-157">Microsoft.Azure.Commands.Batch。Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="d5061-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="d5061-158">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d5061-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d5061-159">輸出</span><span class="sxs-lookup"><span data-stu-id="d5061-159">OUTPUTS</span></span>

### <span data-ttu-id="d5061-160">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d5061-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="d5061-161">筆記</span><span class="sxs-lookup"><span data-stu-id="d5061-161">NOTES</span></span>

## <span data-ttu-id="d5061-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5061-162">RELATED LINKS</span></span>

[<span data-ttu-id="d5061-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d5061-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d5061-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="d5061-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="d5061-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="d5061-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="d5061-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d5061-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="d5061-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d5061-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="d5061-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d5061-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="d5061-169">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d5061-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

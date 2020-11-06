---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: 81f357f2394e266aa70c0d7e4a7720d8252f2edb
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623340"
---
# <span data-ttu-id="54c0b-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="54c0b-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="54c0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="54c0b-103">從池中取得批次計算節點。</span><span class="sxs-lookup"><span data-stu-id="54c0b-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="54c0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="54c0b-104">SYNTAX</span></span>

### <span data-ttu-id="54c0b-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="54c0b-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c0b-106">標識號</span><span class="sxs-lookup"><span data-stu-id="54c0b-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c0b-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="54c0b-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c0b-108">說明</span><span class="sxs-lookup"><span data-stu-id="54c0b-108">DESCRIPTION</span></span>
<span data-ttu-id="54c0b-109">**AzBatchComputeNode** Cmdlet 會從池中取得 Azure 批次計算節點。</span><span class="sxs-lookup"><span data-stu-id="54c0b-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="54c0b-110">請指定 *PoolID* 或 *Pool* 參數。</span><span class="sxs-lookup"><span data-stu-id="54c0b-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="54c0b-111">指定 *識別碼* 參數以取得單一計算節點。</span><span class="sxs-lookup"><span data-stu-id="54c0b-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="54c0b-112">指定 *篩選* 參數，以取得符合開啟資料通訊協定的計算節點 (OData) 篩選。</span><span class="sxs-lookup"><span data-stu-id="54c0b-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="54c0b-113">示例</span><span class="sxs-lookup"><span data-stu-id="54c0b-113">EXAMPLES</span></span>

### <span data-ttu-id="54c0b-114">範例1：依識別碼取得計算節點</span><span class="sxs-lookup"><span data-stu-id="54c0b-114">Example 1: Get a compute node by ID</span></span>
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
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="54c0b-115">這個命令會從擁有 ID Pool06 的池中取得 ID 為 tvm-2316545714_1 20150725t213220z 的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="54c0b-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="54c0b-116">使用 Get-AzBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="54c0b-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="54c0b-117">範例2：從池中取得所有空閒計算節點</span><span class="sxs-lookup"><span data-stu-id="54c0b-117">Example 2: Get all idle compute nodes from a pool</span></span>
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
VirtualMachineSize    : small
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
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="54c0b-118">這個命令會取得擁有識別碼 Pool06 的池中所包含的所有空閒計算節點。</span><span class="sxs-lookup"><span data-stu-id="54c0b-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="54c0b-119">命令會使用 *Filter* 參數指定空閒狀態。</span><span class="sxs-lookup"><span data-stu-id="54c0b-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="54c0b-120">範例3：在指定的池中取得所有計算節點</span><span class="sxs-lookup"><span data-stu-id="54c0b-120">Example 3: Get all compute nodes in a specified pool</span></span>
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
VirtualMachineSize    : small
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
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="54c0b-121">這個命令會透過使用 Get-AzBatchPool Cmdlet 來取得具有識別碼 Pool07 的 pool。</span><span class="sxs-lookup"><span data-stu-id="54c0b-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="54c0b-122">命令會使用管線運算子，將該池子傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54c0b-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="54c0b-123">該 Cmdlet 會從該池中取得所有計算節點。</span><span class="sxs-lookup"><span data-stu-id="54c0b-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="54c0b-124">參數</span><span class="sxs-lookup"><span data-stu-id="54c0b-124">PARAMETERS</span></span>

### <span data-ttu-id="54c0b-125">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="54c0b-125">-BatchContext</span></span>
<span data-ttu-id="54c0b-126">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="54c0b-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="54c0b-127">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="54c0b-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="54c0b-128">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="54c0b-128">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="54c0b-129">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="54c0b-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="54c0b-130">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="54c0b-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="54c0b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c0b-131">-DefaultProfile</span></span>
<span data-ttu-id="54c0b-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54c0b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54c0b-133">-篩選</span><span class="sxs-lookup"><span data-stu-id="54c0b-133">-Filter</span></span>
<span data-ttu-id="54c0b-134">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="54c0b-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="54c0b-135">這個 Cmdlet 會傳回與此參數指定之篩選相符的計算節點。</span><span class="sxs-lookup"><span data-stu-id="54c0b-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="54c0b-136">如果您沒有指定篩選，此 Cmdlet 會傳回該池的所有計算節點。</span><span class="sxs-lookup"><span data-stu-id="54c0b-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="54c0b-137">-識別碼</span><span class="sxs-lookup"><span data-stu-id="54c0b-137">-Id</span></span>
<span data-ttu-id="54c0b-138">指定此 Cmdlet 從池中取得的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="54c0b-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="54c0b-139">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="54c0b-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="54c0b-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="54c0b-140">-MaxCount</span></span>
<span data-ttu-id="54c0b-141">指定要傳回的計算節點數目上限。</span><span class="sxs-lookup"><span data-stu-id="54c0b-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="54c0b-142">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="54c0b-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="54c0b-143">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="54c0b-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="54c0b-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="54c0b-144">-Pool</span></span>
<span data-ttu-id="54c0b-145">指定包含計算節點的 **PSCloudPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="54c0b-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="54c0b-146">若要取得 **PSCloudPool** 物件，請使用 Get-AzBatchPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54c0b-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="54c0b-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="54c0b-147">-PoolId</span></span>
<span data-ttu-id="54c0b-148">指定包含計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="54c0b-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="54c0b-149">-選取</span><span class="sxs-lookup"><span data-stu-id="54c0b-149">-Select</span></span>
<span data-ttu-id="54c0b-150">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="54c0b-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="54c0b-151">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="54c0b-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="54c0b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c0b-152">CommonParameters</span></span>
<span data-ttu-id="54c0b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54c0b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c0b-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54c0b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c0b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="54c0b-155">INPUTS</span></span>

### <span data-ttu-id="54c0b-156">System.object</span><span class="sxs-lookup"><span data-stu-id="54c0b-156">System.String</span></span>

### <span data-ttu-id="54c0b-157">Microsoft.Azure.Commands.Batch。PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="54c0b-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="54c0b-158">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="54c0b-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="54c0b-159">輸出</span><span class="sxs-lookup"><span data-stu-id="54c0b-159">OUTPUTS</span></span>

### <span data-ttu-id="54c0b-160">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="54c0b-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="54c0b-161">筆記</span><span class="sxs-lookup"><span data-stu-id="54c0b-161">NOTES</span></span>

## <span data-ttu-id="54c0b-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="54c0b-162">RELATED LINKS</span></span>

[<span data-ttu-id="54c0b-163">AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="54c0b-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="54c0b-164">AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="54c0b-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="54c0b-165">AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="54c0b-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="54c0b-166">AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="54c0b-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="54c0b-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="54c0b-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="54c0b-168">重新開機-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="54c0b-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="54c0b-169">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54c0b-169">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)



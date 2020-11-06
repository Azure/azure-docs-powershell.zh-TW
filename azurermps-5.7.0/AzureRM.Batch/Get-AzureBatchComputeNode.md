---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: d5cbd8c37f6d527a741f5bb92211d6b4f90b8113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454276"
---
# <span data-ttu-id="6ec2b-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ec2b-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="6ec2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ec2b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec2b-103">從池中取得批次計算節點。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ec2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ec2b-104">SYNTAX</span></span>

### <span data-ttu-id="6ec2b-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="6ec2b-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ec2b-106">標識號</span><span class="sxs-lookup"><span data-stu-id="6ec2b-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ec2b-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="6ec2b-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ec2b-108">說明</span><span class="sxs-lookup"><span data-stu-id="6ec2b-108">DESCRIPTION</span></span>
<span data-ttu-id="6ec2b-109">**AzureBatchComputeNode** Cmdlet 會從池中取得 Azure 批次計算節點。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="6ec2b-110">請指定 *PoolID* 或 *Pool* 參數。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="6ec2b-111">指定 *識別碼* 參數以取得單一計算節點。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="6ec2b-112">指定 *篩選* 參數，以取得符合開啟資料通訊協定的計算節點 (OData) 篩選。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="6ec2b-113">示例</span><span class="sxs-lookup"><span data-stu-id="6ec2b-113">EXAMPLES</span></span>

### <span data-ttu-id="6ec2b-114">範例1：依識別碼取得計算節點</span><span class="sxs-lookup"><span data-stu-id="6ec2b-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
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

<span data-ttu-id="6ec2b-115">這個命令會從擁有 ID Pool06 的池中取得 ID 為 tvm-2316545714_1 20150725t213220z 的 compute 節點。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="6ec2b-116">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6ec2b-117">範例2：從池中取得所有空閒計算節點</span><span class="sxs-lookup"><span data-stu-id="6ec2b-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
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

<span data-ttu-id="6ec2b-118">這個命令會取得擁有識別碼 Pool06 的池中所包含的所有空閒計算節點。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="6ec2b-119">命令會使用 *Filter* 參數指定空閒狀態。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="6ec2b-120">範例3：在指定的池中取得所有計算節點</span><span class="sxs-lookup"><span data-stu-id="6ec2b-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzureBatchPool -Id "Pool07" -BatchContext $Context | Get-AzureBatchComputeNode -BatchContext $Context
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

<span data-ttu-id="6ec2b-121">這個命令會透過使用 Get-AzureBatchPool Cmdlet 來取得具有識別碼 Pool07 的 pool。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="6ec2b-122">命令會使用管線運算子，將該池子傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ec2b-123">該 Cmdlet 會從該池中取得所有計算節點。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="6ec2b-124">參數</span><span class="sxs-lookup"><span data-stu-id="6ec2b-124">PARAMETERS</span></span>

### <span data-ttu-id="6ec2b-125">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ec2b-125">-BatchContext</span></span>
<span data-ttu-id="6ec2b-126">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6ec2b-127">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6ec2b-128">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6ec2b-129">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6ec2b-130">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec2b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec2b-131">-DefaultProfile</span></span>
<span data-ttu-id="6ec2b-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec2b-133">-篩選</span><span class="sxs-lookup"><span data-stu-id="6ec2b-133">-Filter</span></span>
<span data-ttu-id="6ec2b-134">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="6ec2b-135">這個 Cmdlet 會傳回與此參數指定之篩選相符的計算節點。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="6ec2b-136">如果您沒有指定篩選，此 Cmdlet 會傳回該池的所有計算節點。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec2b-137">-識別碼</span><span class="sxs-lookup"><span data-stu-id="6ec2b-137">-Id</span></span>
<span data-ttu-id="6ec2b-138">指定此 Cmdlet 從池中取得的計算節點 ID。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="6ec2b-139">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec2b-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6ec2b-140">-MaxCount</span></span>
<span data-ttu-id="6ec2b-141">指定要傳回的計算節點數目上限。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="6ec2b-142">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6ec2b-143">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-143">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec2b-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="6ec2b-144">-Pool</span></span>
<span data-ttu-id="6ec2b-145">指定包含計算節點的 **PSCloudPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="6ec2b-146">若要取得 **PSCloudPool** 物件，請使用 Get-AzureBatchPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-146">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec2b-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="6ec2b-147">-PoolId</span></span>
<span data-ttu-id="6ec2b-148">指定包含計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec2b-149">-選取</span><span class="sxs-lookup"><span data-stu-id="6ec2b-149">-Select</span></span>
<span data-ttu-id="6ec2b-150">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="6ec2b-151">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec2b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec2b-152">CommonParameters</span></span>
<span data-ttu-id="6ec2b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec2b-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ec2b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec2b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="6ec2b-155">INPUTS</span></span>

### <span data-ttu-id="6ec2b-156">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ec2b-156">BatchAccountContext</span></span>
<span data-ttu-id="6ec2b-157">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6ec2b-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6ec2b-158">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="6ec2b-158">PSCloudPool</span></span>
<span data-ttu-id="6ec2b-159">形參 "Pool" 接受管線中 "PSCloudPool" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6ec2b-159">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="6ec2b-160">輸出</span><span class="sxs-lookup"><span data-stu-id="6ec2b-160">OUTPUTS</span></span>

### <span data-ttu-id="6ec2b-161">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ec2b-161">PSComputeNode</span></span>

## <span data-ttu-id="6ec2b-162">筆記</span><span class="sxs-lookup"><span data-stu-id="6ec2b-162">NOTES</span></span>

## <span data-ttu-id="6ec2b-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ec2b-163">RELATED LINKS</span></span>

[<span data-ttu-id="6ec2b-164">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ec2b-164">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="6ec2b-165">AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="6ec2b-165">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="6ec2b-166">AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="6ec2b-166">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="6ec2b-167">AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6ec2b-167">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="6ec2b-168">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ec2b-168">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="6ec2b-169">重新開機-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ec2b-169">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="6ec2b-170">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ec2b-170">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



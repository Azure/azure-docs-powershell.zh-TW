---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: f861397569671d5269e12edee564acdb55519977
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287943"
---
# <span data-ttu-id="16c0e-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="16c0e-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="16c0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="16c0e-103">在指定的批次帳戶下取得批次池。</span><span class="sxs-lookup"><span data-stu-id="16c0e-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="16c0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="16c0e-104">SYNTAX</span></span>

### <span data-ttu-id="16c0e-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="16c0e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c0e-106">標識號</span><span class="sxs-lookup"><span data-stu-id="16c0e-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16c0e-107">說明</span><span class="sxs-lookup"><span data-stu-id="16c0e-107">DESCRIPTION</span></span>
<span data-ttu-id="16c0e-108">**AzBatchPool** Cmdlet 會在使用 *BatchCoNtext* 參數指定的批次帳戶下取得 Azure Batch pool。</span><span class="sxs-lookup"><span data-stu-id="16c0e-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="16c0e-109">您可以使用 *識別碼* 參數來取得單一池，或者您可以使用 *Filter* 參數，以取得符合開啟資料通訊協定 (OData) 篩選的池。</span><span class="sxs-lookup"><span data-stu-id="16c0e-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="16c0e-110">示例</span><span class="sxs-lookup"><span data-stu-id="16c0e-110">EXAMPLES</span></span>

### <span data-ttu-id="16c0e-111">範例1：依識別碼取得池</span><span class="sxs-lookup"><span data-stu-id="16c0e-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     :
AutoScaleRun                         :
CertificateReferences                :
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          :
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             :
OSFamily                             : 4
ResizeError                          :
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            :
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           :
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="16c0e-112">這個命令會取得 ID 為 MyPool 的池。</span><span class="sxs-lookup"><span data-stu-id="16c0e-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="16c0e-113">範例2：使用 OData 篩選取得所有的 pool</span><span class="sxs-lookup"><span data-stu-id="16c0e-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     :
AutoScaleRun                         :
CertificateReferences                :
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          :
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             :
OSFamily                             : 4
ResizeError                          :
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            :
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           :
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="16c0e-114">這個命令會取得 Id 以 [ *篩選* ] 參數開頭的池。</span><span class="sxs-lookup"><span data-stu-id="16c0e-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="16c0e-115">參數</span><span class="sxs-lookup"><span data-stu-id="16c0e-115">PARAMETERS</span></span>

### <span data-ttu-id="16c0e-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="16c0e-116">-BatchContext</span></span>
<span data-ttu-id="16c0e-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="16c0e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16c0e-118">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="16c0e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="16c0e-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="16c0e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="16c0e-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="16c0e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="16c0e-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="16c0e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="16c0e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c0e-122">-DefaultProfile</span></span>
<span data-ttu-id="16c0e-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16c0e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16c0e-124">-展開</span><span class="sxs-lookup"><span data-stu-id="16c0e-124">-Expand</span></span>
<span data-ttu-id="16c0e-125">指定 (OData) expand 子句中的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="16c0e-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="16c0e-126">指定此參數的值，以取得您所取得之主要實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="16c0e-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="16c0e-127">-篩選</span><span class="sxs-lookup"><span data-stu-id="16c0e-127">-Filter</span></span>
<span data-ttu-id="16c0e-128">指定查詢 [pool] 時要使用的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="16c0e-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="16c0e-129">如果您沒有指定篩選，則會傳回以 *BatchCoNtext* 參數指定的批次帳戶下的所有池。</span><span class="sxs-lookup"><span data-stu-id="16c0e-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c0e-130">-識別碼</span><span class="sxs-lookup"><span data-stu-id="16c0e-130">-Id</span></span>
<span data-ttu-id="16c0e-131">指定要取得的池 ID。</span><span class="sxs-lookup"><span data-stu-id="16c0e-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="16c0e-132">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="16c0e-132">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16c0e-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="16c0e-133">-MaxCount</span></span>
<span data-ttu-id="16c0e-134">指定要傳回的最大池數。</span><span class="sxs-lookup"><span data-stu-id="16c0e-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="16c0e-135">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="16c0e-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="16c0e-136">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="16c0e-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="16c0e-137">-選取</span><span class="sxs-lookup"><span data-stu-id="16c0e-137">-Select</span></span>
<span data-ttu-id="16c0e-138">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="16c0e-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="16c0e-139">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="16c0e-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="16c0e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c0e-140">CommonParameters</span></span>
<span data-ttu-id="16c0e-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16c0e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c0e-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="16c0e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c0e-143">輸入</span><span class="sxs-lookup"><span data-stu-id="16c0e-143">INPUTS</span></span>

### <span data-ttu-id="16c0e-144">System.object</span><span class="sxs-lookup"><span data-stu-id="16c0e-144">System.String</span></span>

### <span data-ttu-id="16c0e-145">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="16c0e-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="16c0e-146">輸出</span><span class="sxs-lookup"><span data-stu-id="16c0e-146">OUTPUTS</span></span>

### <span data-ttu-id="16c0e-147">Microsoft.Azure.Commands.Batch。PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="16c0e-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="16c0e-148">筆記</span><span class="sxs-lookup"><span data-stu-id="16c0e-148">NOTES</span></span>

## <span data-ttu-id="16c0e-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="16c0e-149">RELATED LINKS</span></span>

[<span data-ttu-id="16c0e-150">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="16c0e-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="16c0e-151">新-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="16c0e-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="16c0e-152">移除-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="16c0e-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="16c0e-153">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="16c0e-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

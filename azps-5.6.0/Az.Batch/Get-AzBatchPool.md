---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: 7c3aff3f69ae76765a80c7db1e66ee0a79990c9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903041"
---
# <span data-ttu-id="e557f-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e557f-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="e557f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e557f-102">SYNOPSIS</span></span>
<span data-ttu-id="e557f-103">在指定的批次帳戶下，獲得批次資料庫。</span><span class="sxs-lookup"><span data-stu-id="e557f-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="e557f-104">語法</span><span class="sxs-lookup"><span data-stu-id="e557f-104">SYNTAX</span></span>

### <span data-ttu-id="e557f-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="e557f-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e557f-106">Id</span><span class="sxs-lookup"><span data-stu-id="e557f-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e557f-107">描述</span><span class="sxs-lookup"><span data-stu-id="e557f-107">DESCRIPTION</span></span>
<span data-ttu-id="e557f-108">**Get-AzBatchPool** Cmdlet 會取得使用 *BatchCoNtext* 參數指定的 Batch 帳戶下的 Azure Batch 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e557f-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="e557f-109">您可以使用 *Id* 參數來取得單一資料庫，或者您可以使用 *Filter* 參數來取得符合 OData (OData) 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e557f-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="e557f-110">例子</span><span class="sxs-lookup"><span data-stu-id="e557f-110">EXAMPLES</span></span>

### <span data-ttu-id="e557f-111">範例 1：根據識別碼取得一個區</span><span class="sxs-lookup"><span data-stu-id="e557f-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="e557f-112">此命令會使用 ID MyPool 來得到該區。</span><span class="sxs-lookup"><span data-stu-id="e557f-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="e557f-113">範例 2：使用 OData 篩選取得所有資料庫</span><span class="sxs-lookup"><span data-stu-id="e557f-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="e557f-114">此命令會獲得使用 Filter 參數以 My 做為開始的 *資料庫* 。</span><span class="sxs-lookup"><span data-stu-id="e557f-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="e557f-115">參數</span><span class="sxs-lookup"><span data-stu-id="e557f-115">PARAMETERS</span></span>

### <span data-ttu-id="e557f-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="e557f-116">-BatchContext</span></span>
<span data-ttu-id="e557f-117">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="e557f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e557f-118">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="e557f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e557f-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="e557f-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e557f-120">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e557f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e557f-121">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="e557f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e557f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e557f-122">-DefaultProfile</span></span>
<span data-ttu-id="e557f-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e557f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e557f-124">-展開</span><span class="sxs-lookup"><span data-stu-id="e557f-124">-Expand</span></span>
<span data-ttu-id="e557f-125">指定 Open Data Protocol (OData) expand 子句。</span><span class="sxs-lookup"><span data-stu-id="e557f-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="e557f-126">指定此參數的值，以取得您取得之主實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="e557f-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="e557f-127">-篩選</span><span class="sxs-lookup"><span data-stu-id="e557f-127">-Filter</span></span>
<span data-ttu-id="e557f-128">指定查詢資料庫時要使用 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="e557f-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="e557f-129">如果您未指定篩選，會傳回使用 *BatchCoNtext* 參數指定的 Batch 帳戶下的所有集區。</span><span class="sxs-lookup"><span data-stu-id="e557f-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="e557f-130">-Id</span><span class="sxs-lookup"><span data-stu-id="e557f-130">-Id</span></span>
<span data-ttu-id="e557f-131">指定要取得之該區之識別碼。</span><span class="sxs-lookup"><span data-stu-id="e557f-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="e557f-132">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="e557f-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="e557f-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e557f-133">-MaxCount</span></span>
<span data-ttu-id="e557f-134">指定要返回的資料庫數量上限。</span><span class="sxs-lookup"><span data-stu-id="e557f-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="e557f-135">如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="e557f-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="e557f-136">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="e557f-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="e557f-137">-選取</span><span class="sxs-lookup"><span data-stu-id="e557f-137">-Select</span></span>
<span data-ttu-id="e557f-138">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="e557f-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="e557f-139">指定此參數的值以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="e557f-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="e557f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e557f-140">CommonParameters</span></span>
<span data-ttu-id="e557f-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e557f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e557f-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e557f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e557f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e557f-143">INPUTS</span></span>

### <span data-ttu-id="e557f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e557f-144">System.String</span></span>

### <span data-ttu-id="e557f-145">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="e557f-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e557f-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e557f-146">OUTPUTS</span></span>

### <span data-ttu-id="e557f-147">Microsoft.Azure.Commands.Batch。Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="e557f-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="e557f-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e557f-148">NOTES</span></span>

## <span data-ttu-id="e557f-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e557f-149">RELATED LINKS</span></span>

[<span data-ttu-id="e557f-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e557f-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e557f-151">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e557f-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="e557f-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e557f-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="e557f-153">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e557f-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

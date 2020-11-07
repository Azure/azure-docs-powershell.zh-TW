---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626514"
---
# <span data-ttu-id="eab75-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="eab75-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="eab75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eab75-102">SYNOPSIS</span></span>
<span data-ttu-id="eab75-103">在指定的批次帳戶下取得批次池。</span><span class="sxs-lookup"><span data-stu-id="eab75-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eab75-104">句法</span><span class="sxs-lookup"><span data-stu-id="eab75-104">SYNTAX</span></span>

### <span data-ttu-id="eab75-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="eab75-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eab75-106">標識號</span><span class="sxs-lookup"><span data-stu-id="eab75-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eab75-107">說明</span><span class="sxs-lookup"><span data-stu-id="eab75-107">DESCRIPTION</span></span>
<span data-ttu-id="eab75-108">**AzureBatchPool** Cmdlet 會在使用 *BatchCoNtext* 參數指定的批次帳戶下取得 Azure Batch pool。</span><span class="sxs-lookup"><span data-stu-id="eab75-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="eab75-109">您可以使用 *識別碼* 參數來取得單一池，或者您可以使用 *Filter* 參數，以取得符合開啟資料通訊協定 (OData) 篩選的池。</span><span class="sxs-lookup"><span data-stu-id="eab75-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="eab75-110">示例</span><span class="sxs-lookup"><span data-stu-id="eab75-110">EXAMPLES</span></span>

### <span data-ttu-id="eab75-111">範例1：依識別碼取得池</span><span class="sxs-lookup"><span data-stu-id="eab75-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
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
VirtualMachineSize                   : small
```

<span data-ttu-id="eab75-112">這個命令會取得 ID 為 MyPool 的池。</span><span class="sxs-lookup"><span data-stu-id="eab75-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="eab75-113">範例2：使用 OData 篩選取得所有的 pool</span><span class="sxs-lookup"><span data-stu-id="eab75-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
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
VirtualMachineSize                   : small
```

<span data-ttu-id="eab75-114">這個命令會取得 Id 以 [ *篩選* ] 參數開頭的池。</span><span class="sxs-lookup"><span data-stu-id="eab75-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="eab75-115">參數</span><span class="sxs-lookup"><span data-stu-id="eab75-115">PARAMETERS</span></span>

### <span data-ttu-id="eab75-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="eab75-116">-BatchContext</span></span>
<span data-ttu-id="eab75-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="eab75-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eab75-118">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eab75-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="eab75-119">-展開</span><span class="sxs-lookup"><span data-stu-id="eab75-119">-Expand</span></span>
<span data-ttu-id="eab75-120">指定 (OData) expand 子句中的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="eab75-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="eab75-121">指定此參數的值，以取得您所取得之主要實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="eab75-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="eab75-122">-篩選</span><span class="sxs-lookup"><span data-stu-id="eab75-122">-Filter</span></span>
<span data-ttu-id="eab75-123">指定查詢 [pool] 時要使用的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="eab75-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="eab75-124">如果您沒有指定篩選，則會傳回以 *BatchCoNtext* 參數指定的批次帳戶下的所有池。</span><span class="sxs-lookup"><span data-stu-id="eab75-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="eab75-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="eab75-125">-Id</span></span>
<span data-ttu-id="eab75-126">指定要取得的池 ID。</span><span class="sxs-lookup"><span data-stu-id="eab75-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="eab75-127">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="eab75-127">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="eab75-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="eab75-128">-MaxCount</span></span>
<span data-ttu-id="eab75-129">指定要傳回的最大池數。</span><span class="sxs-lookup"><span data-stu-id="eab75-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="eab75-130">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="eab75-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="eab75-131">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="eab75-131">The default value is 1000.</span></span>

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

### <span data-ttu-id="eab75-132">-選取</span><span class="sxs-lookup"><span data-stu-id="eab75-132">-Select</span></span>
<span data-ttu-id="eab75-133">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="eab75-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="eab75-134">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="eab75-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="eab75-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab75-135">-DefaultProfile</span></span>
<span data-ttu-id="eab75-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eab75-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eab75-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab75-137">CommonParameters</span></span>
<span data-ttu-id="eab75-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eab75-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab75-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eab75-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab75-140">輸入</span><span class="sxs-lookup"><span data-stu-id="eab75-140">INPUTS</span></span>

### <span data-ttu-id="eab75-141">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="eab75-141">BatchAccountContext</span></span>
<span data-ttu-id="eab75-142">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="eab75-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="eab75-143">字串</span><span class="sxs-lookup"><span data-stu-id="eab75-143">String</span></span>
<span data-ttu-id="eab75-144">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="eab75-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="eab75-145">輸出</span><span class="sxs-lookup"><span data-stu-id="eab75-145">OUTPUTS</span></span>

### <span data-ttu-id="eab75-146">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="eab75-146">PSCloudPool</span></span>

## <span data-ttu-id="eab75-147">筆記</span><span class="sxs-lookup"><span data-stu-id="eab75-147">NOTES</span></span>

## <span data-ttu-id="eab75-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="eab75-148">RELATED LINKS</span></span>

[<span data-ttu-id="eab75-149">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="eab75-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="eab75-150">新-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="eab75-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="eab75-151">移除-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="eab75-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="eab75-152">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eab75-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



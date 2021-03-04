---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 0d33ce7e41fb8058acb36a4668eeb337d54f187e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907166"
---
# <span data-ttu-id="b0dcb-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dcb-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="b0dcb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b0dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="b0dcb-103">獲得批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="b0dcb-104">語法</span><span class="sxs-lookup"><span data-stu-id="b0dcb-104">SYNTAX</span></span>

### <span data-ttu-id="b0dcb-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="b0dcb-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0dcb-106">Id</span><span class="sxs-lookup"><span data-stu-id="b0dcb-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0dcb-107">描述</span><span class="sxs-lookup"><span data-stu-id="b0dcb-107">DESCRIPTION</span></span>
<span data-ttu-id="b0dcb-108">**Get-AzBatchJobSchedule** Cmdlet 會取得 Batch 帳戶由 *BatchCoNtext* 參數指定的 Azure 批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="b0dcb-109">指定識別碼以取得單一工作排程。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="b0dcb-110">指定 *Filter* 參數，以取得符合 OData (篩選) 排程。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b0dcb-111">例子</span><span class="sxs-lookup"><span data-stu-id="b0dcb-111">EXAMPLES</span></span>

### <span data-ttu-id="b0dcb-112">範例 1：指定識別碼以取得工作排程</span><span class="sxs-lookup"><span data-stu-id="b0dcb-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="b0dcb-113">此命令會獲得具有 ID JobSchedule23 的工作排程。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="b0dcb-114">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b0dcb-115">範例 2：使用篩選取得工作排程</span><span class="sxs-lookup"><span data-stu-id="b0dcb-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 :
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="b0dcb-116">此命令會指定 Filter 參數，以使用 Job 做為開始的所有工作排 *程。*</span><span class="sxs-lookup"><span data-stu-id="b0dcb-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="b0dcb-117">參數</span><span class="sxs-lookup"><span data-stu-id="b0dcb-117">PARAMETERS</span></span>

### <span data-ttu-id="b0dcb-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="b0dcb-118">-BatchContext</span></span>
<span data-ttu-id="b0dcb-119">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b0dcb-120">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b0dcb-121">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b0dcb-122">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b0dcb-123">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b0dcb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0dcb-124">-DefaultProfile</span></span>
<span data-ttu-id="b0dcb-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0dcb-126">-展開</span><span class="sxs-lookup"><span data-stu-id="b0dcb-126">-Expand</span></span>
<span data-ttu-id="b0dcb-127">指定 Open Data Protocol (OData) expand 子句。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b0dcb-128">指定此參數的值，以取得您取得之主實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="b0dcb-129">-篩選</span><span class="sxs-lookup"><span data-stu-id="b0dcb-129">-Filter</span></span>
<span data-ttu-id="b0dcb-130">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="b0dcb-131">此 Cmdlet 會返回符合此參數指定之篩選的工作排程。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="b0dcb-132">如果您未指定篩選，此 Cmdlet 會針對批次上下文，會返回所有工作排程。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="b0dcb-133">-Id</span><span class="sxs-lookup"><span data-stu-id="b0dcb-133">-Id</span></span>
<span data-ttu-id="b0dcb-134">指定此 Cmdlet 獲得的工作排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="b0dcb-135">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b0dcb-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b0dcb-136">-MaxCount</span></span>
<span data-ttu-id="b0dcb-137">指定要退回的工作排程數上限。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="b0dcb-138">如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b0dcb-139">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="b0dcb-140">-選取</span><span class="sxs-lookup"><span data-stu-id="b0dcb-140">-Select</span></span>
<span data-ttu-id="b0dcb-141">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="b0dcb-142">指定此參數的值以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b0dcb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0dcb-143">CommonParameters</span></span>
<span data-ttu-id="b0dcb-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b0dcb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0dcb-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0dcb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0dcb-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b0dcb-146">INPUTS</span></span>

### <span data-ttu-id="b0dcb-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b0dcb-147">System.String</span></span>

### <span data-ttu-id="b0dcb-148">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="b0dcb-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b0dcb-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b0dcb-149">OUTPUTS</span></span>

### <span data-ttu-id="b0dcb-150">Microsoft.Azure.Commands.Batch。Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dcb-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="b0dcb-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b0dcb-151">NOTES</span></span>

## <span data-ttu-id="b0dcb-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0dcb-152">RELATED LINKS</span></span>

[<span data-ttu-id="b0dcb-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dcb-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="b0dcb-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dcb-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="b0dcb-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b0dcb-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b0dcb-156">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dcb-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="b0dcb-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dcb-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="b0dcb-158">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dcb-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="b0dcb-159">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0dcb-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

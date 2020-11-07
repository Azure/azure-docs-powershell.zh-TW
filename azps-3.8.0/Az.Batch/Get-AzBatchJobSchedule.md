---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: a90f437bc593e1abcb6dc2d92292e04dd9c9f74b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968750"
---
# <span data-ttu-id="f5cf2-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5cf2-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f5cf2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cf2-103">取得批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="f5cf2-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5cf2-104">SYNTAX</span></span>

### <span data-ttu-id="f5cf2-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="f5cf2-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5cf2-106">標識號</span><span class="sxs-lookup"><span data-stu-id="f5cf2-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5cf2-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5cf2-107">DESCRIPTION</span></span>
<span data-ttu-id="f5cf2-108">**AzBatchJobSchedule** Cmdlet 會針對 *BatchCoNtext* 參數指定的批次帳戶取得 Azure Batch 作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="f5cf2-109">指定識別碼以取得單一作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="f5cf2-110">指定 *篩選* 參數，以取得符合開啟資料通訊協定的作業排程 (OData) 篩選。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="f5cf2-111">示例</span><span class="sxs-lookup"><span data-stu-id="f5cf2-111">EXAMPLES</span></span>

### <span data-ttu-id="f5cf2-112">範例1：指定 ID 以取得作業排程</span><span class="sxs-lookup"><span data-stu-id="f5cf2-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="f5cf2-113">這個命令會取得 ID 為 JobSchedule23 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="f5cf2-114">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f5cf2-115">範例2：使用篩選取得作業排程</span><span class="sxs-lookup"><span data-stu-id="f5cf2-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="f5cf2-116">這個命令會透過指定 *Filter* 參數，來取得所有 id 都以 job 開始的作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="f5cf2-117">參數</span><span class="sxs-lookup"><span data-stu-id="f5cf2-117">PARAMETERS</span></span>

### <span data-ttu-id="f5cf2-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="f5cf2-118">-BatchContext</span></span>
<span data-ttu-id="f5cf2-119">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f5cf2-120">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f5cf2-121">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f5cf2-122">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f5cf2-123">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f5cf2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cf2-124">-DefaultProfile</span></span>
<span data-ttu-id="f5cf2-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5cf2-126">-展開</span><span class="sxs-lookup"><span data-stu-id="f5cf2-126">-Expand</span></span>
<span data-ttu-id="f5cf2-127">指定 (OData) expand 子句中的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="f5cf2-128">指定此參數的值，以取得您所取得之主要實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="f5cf2-129">-篩選</span><span class="sxs-lookup"><span data-stu-id="f5cf2-129">-Filter</span></span>
<span data-ttu-id="f5cf2-130">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="f5cf2-131">這個 Cmdlet 會傳回符合此參數指定之篩選準則的作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="f5cf2-132">如果您沒有指定篩選，這個 Cmdlet 會傳回批內容的所有作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="f5cf2-133">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f5cf2-133">-Id</span></span>
<span data-ttu-id="f5cf2-134">指定此 Cmdlet 取得之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="f5cf2-135">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="f5cf2-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f5cf2-136">-MaxCount</span></span>
<span data-ttu-id="f5cf2-137">指定要傳回的作業排程數目上限。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="f5cf2-138">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="f5cf2-139">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="f5cf2-140">-選取</span><span class="sxs-lookup"><span data-stu-id="f5cf2-140">-Select</span></span>
<span data-ttu-id="f5cf2-141">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="f5cf2-142">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="f5cf2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cf2-143">CommonParameters</span></span>
<span data-ttu-id="f5cf2-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cf2-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f5cf2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cf2-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f5cf2-146">INPUTS</span></span>

### <span data-ttu-id="f5cf2-147">System.object</span><span class="sxs-lookup"><span data-stu-id="f5cf2-147">System.String</span></span>

### <span data-ttu-id="f5cf2-148">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="f5cf2-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f5cf2-149">輸出</span><span class="sxs-lookup"><span data-stu-id="f5cf2-149">OUTPUTS</span></span>

### <span data-ttu-id="f5cf2-150">Microsoft.Azure.Commands.Batch。PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5cf2-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="f5cf2-151">筆記</span><span class="sxs-lookup"><span data-stu-id="f5cf2-151">NOTES</span></span>

## <span data-ttu-id="f5cf2-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5cf2-152">RELATED LINKS</span></span>

[<span data-ttu-id="f5cf2-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5cf2-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="f5cf2-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5cf2-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="f5cf2-155">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f5cf2-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f5cf2-156">新-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5cf2-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="f5cf2-157">移除-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5cf2-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="f5cf2-158">停止 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5cf2-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="f5cf2-159">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5cf2-159">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)



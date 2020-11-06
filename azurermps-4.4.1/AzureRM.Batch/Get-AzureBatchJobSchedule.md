---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 139282332fb1c5d0ace02ddd7b998c1875af931a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449647"
---
# <span data-ttu-id="98700-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98700-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="98700-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98700-102">SYNOPSIS</span></span>
<span data-ttu-id="98700-103">取得批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="98700-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98700-104">句法</span><span class="sxs-lookup"><span data-stu-id="98700-104">SYNTAX</span></span>

### <span data-ttu-id="98700-105">ODataFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="98700-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98700-106">標識號</span><span class="sxs-lookup"><span data-stu-id="98700-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98700-107">說明</span><span class="sxs-lookup"><span data-stu-id="98700-107">DESCRIPTION</span></span>
<span data-ttu-id="98700-108">**AzureBatchJobSchedule** Cmdlet 會針對 *BatchCoNtext* 參數指定的批次帳戶取得 Azure Batch 作業排程。</span><span class="sxs-lookup"><span data-stu-id="98700-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="98700-109">指定識別碼以取得單一作業排程。</span><span class="sxs-lookup"><span data-stu-id="98700-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="98700-110">指定 *篩選* 參數，以取得符合開啟資料通訊協定的作業排程 (OData) 篩選。</span><span class="sxs-lookup"><span data-stu-id="98700-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="98700-111">示例</span><span class="sxs-lookup"><span data-stu-id="98700-111">EXAMPLES</span></span>

### <span data-ttu-id="98700-112">範例1：指定 ID 以取得作業排程</span><span class="sxs-lookup"><span data-stu-id="98700-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="98700-113">這個命令會取得 ID 為 JobSchedule23 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="98700-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="98700-114">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="98700-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="98700-115">範例2：使用篩選取得作業排程</span><span class="sxs-lookup"><span data-stu-id="98700-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="98700-116">這個命令會透過指定 *Filter* 參數，來取得所有 id 都以 job 開始的作業排程。</span><span class="sxs-lookup"><span data-stu-id="98700-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="98700-117">參數</span><span class="sxs-lookup"><span data-stu-id="98700-117">PARAMETERS</span></span>

### <span data-ttu-id="98700-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="98700-118">-BatchContext</span></span>
<span data-ttu-id="98700-119">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="98700-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98700-120">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98700-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="98700-121">-展開</span><span class="sxs-lookup"><span data-stu-id="98700-121">-Expand</span></span>
<span data-ttu-id="98700-122">指定 (OData) expand 子句中的開放式資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="98700-122">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="98700-123">指定此參數的值，以取得您所取得之主要實體的關聯實體。</span><span class="sxs-lookup"><span data-stu-id="98700-123">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="98700-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="98700-124">-Filter</span></span>
<span data-ttu-id="98700-125">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="98700-125">Specifies an OData filter clause.</span></span>
<span data-ttu-id="98700-126">這個 Cmdlet 會傳回符合此參數指定之篩選準則的作業排程。</span><span class="sxs-lookup"><span data-stu-id="98700-126">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="98700-127">如果您沒有指定篩選，這個 Cmdlet 會傳回批內容的所有作業排程。</span><span class="sxs-lookup"><span data-stu-id="98700-127">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="98700-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="98700-128">-Id</span></span>
<span data-ttu-id="98700-129">指定此 Cmdlet 取得之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="98700-129">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="98700-130">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="98700-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="98700-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="98700-131">-MaxCount</span></span>
<span data-ttu-id="98700-132">指定要傳回的作業排程數目上限。</span><span class="sxs-lookup"><span data-stu-id="98700-132">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="98700-133">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="98700-133">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="98700-134">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="98700-134">The default value is 1000.</span></span>

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

### <span data-ttu-id="98700-135">-選取</span><span class="sxs-lookup"><span data-stu-id="98700-135">-Select</span></span>
<span data-ttu-id="98700-136">指定 OData select 子句。</span><span class="sxs-lookup"><span data-stu-id="98700-136">Specifies an OData select clause.</span></span>
<span data-ttu-id="98700-137">指定此參數的值，以取得特定屬性，而不是所有物件屬性。</span><span class="sxs-lookup"><span data-stu-id="98700-137">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="98700-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98700-138">-DefaultProfile</span></span>
<span data-ttu-id="98700-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98700-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98700-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98700-140">CommonParameters</span></span>
<span data-ttu-id="98700-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98700-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98700-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98700-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98700-143">輸入</span><span class="sxs-lookup"><span data-stu-id="98700-143">INPUTS</span></span>

### <span data-ttu-id="98700-144">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="98700-144">BatchAccountContext</span></span>
<span data-ttu-id="98700-145">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="98700-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="98700-146">字串</span><span class="sxs-lookup"><span data-stu-id="98700-146">String</span></span>
<span data-ttu-id="98700-147">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="98700-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="98700-148">輸出</span><span class="sxs-lookup"><span data-stu-id="98700-148">OUTPUTS</span></span>

### <span data-ttu-id="98700-149">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98700-149">PSCloudJobSchedule</span></span>

## <span data-ttu-id="98700-150">筆記</span><span class="sxs-lookup"><span data-stu-id="98700-150">NOTES</span></span>

## <span data-ttu-id="98700-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="98700-151">RELATED LINKS</span></span>

[<span data-ttu-id="98700-152">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98700-152">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="98700-153">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98700-153">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="98700-154">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="98700-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="98700-155">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98700-155">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="98700-156">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98700-156">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="98700-157">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98700-157">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="98700-158">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="98700-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



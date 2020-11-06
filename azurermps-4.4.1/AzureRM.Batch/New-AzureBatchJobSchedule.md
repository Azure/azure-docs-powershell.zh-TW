---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450030"
---
# <span data-ttu-id="22163-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22163-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="22163-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22163-102">SYNOPSIS</span></span>
<span data-ttu-id="22163-103">在批次服務中建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="22163-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22163-104">句法</span><span class="sxs-lookup"><span data-stu-id="22163-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22163-105">說明</span><span class="sxs-lookup"><span data-stu-id="22163-105">DESCRIPTION</span></span>
<span data-ttu-id="22163-106">**新的-AzureBatchJobSchedule** Cmdlet 會在 Azure Batch service 中建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="22163-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="22163-107">*BatchAccountCoNtext* 參數會指定此 Cmdlet 建立排程的帳戶。</span><span class="sxs-lookup"><span data-stu-id="22163-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="22163-108">示例</span><span class="sxs-lookup"><span data-stu-id="22163-108">EXAMPLES</span></span>

### <span data-ttu-id="22163-109">範例1：建立作業排程</span><span class="sxs-lookup"><span data-stu-id="22163-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="22163-110">這個範例會建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="22163-110">This example creates a job schedule.</span></span>

<span data-ttu-id="22163-111">前五個命令會建立及修改 **PSSchedule** 、 **PSJobSpecification** 和 **PSPoolInformation** 物件。</span><span class="sxs-lookup"><span data-stu-id="22163-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="22163-112">這些命令會使用 New-Object Cmdlet 和標準的 Azure PowerShell 語法。</span><span class="sxs-lookup"><span data-stu-id="22163-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="22163-113">這些命令會將這些物件儲存在 $Schedule 並 $JobSpecification 變數中。</span><span class="sxs-lookup"><span data-stu-id="22163-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="22163-114">最後一個命令會建立具有識別碼 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="22163-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="22163-115">此排程會建立含一天的定期間隔的工作。</span><span class="sxs-lookup"><span data-stu-id="22163-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="22163-116">作業會在擁有識別碼 ContosoPool06 的池中執行，如5個命令所指定。</span><span class="sxs-lookup"><span data-stu-id="22163-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="22163-117">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="22163-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="22163-118">參數</span><span class="sxs-lookup"><span data-stu-id="22163-118">PARAMETERS</span></span>

### <span data-ttu-id="22163-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="22163-119">-BatchContext</span></span>
<span data-ttu-id="22163-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="22163-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="22163-121">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22163-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="22163-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="22163-122">-DisplayName</span></span>
<span data-ttu-id="22163-123">指定作業排程的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="22163-123">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="22163-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="22163-124">-Id</span></span>
<span data-ttu-id="22163-125">指定此 Cmdlet 建立之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="22163-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22163-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="22163-126">-JobSpecification</span></span>
<span data-ttu-id="22163-127">指定此 Cmdlet 包含在作業排程中之作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="22163-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22163-128">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="22163-128">-Metadata</span></span>
<span data-ttu-id="22163-129">指定要新增至作業排程的中繼資料（做為索引鍵/值對）。</span><span class="sxs-lookup"><span data-stu-id="22163-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="22163-130">金鑰就是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="22163-130">The key is the metadata name.</span></span>
<span data-ttu-id="22163-131">此值為中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="22163-131">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22163-132">-排程</span><span class="sxs-lookup"><span data-stu-id="22163-132">-Schedule</span></span>
<span data-ttu-id="22163-133">指定決定何時建立作業的排程。</span><span class="sxs-lookup"><span data-stu-id="22163-133">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22163-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22163-134">-DefaultProfile</span></span>
<span data-ttu-id="22163-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22163-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22163-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22163-136">CommonParameters</span></span>
<span data-ttu-id="22163-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22163-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22163-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22163-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22163-139">輸入</span><span class="sxs-lookup"><span data-stu-id="22163-139">INPUTS</span></span>

### <span data-ttu-id="22163-140">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="22163-140">BatchAccountContext</span></span>
<span data-ttu-id="22163-141">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="22163-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="22163-142">輸出</span><span class="sxs-lookup"><span data-stu-id="22163-142">OUTPUTS</span></span>

## <span data-ttu-id="22163-143">筆記</span><span class="sxs-lookup"><span data-stu-id="22163-143">NOTES</span></span>

## <span data-ttu-id="22163-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="22163-144">RELATED LINKS</span></span>

[<span data-ttu-id="22163-145">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22163-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="22163-146">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22163-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="22163-147">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="22163-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="22163-148">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22163-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="22163-149">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22163-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="22163-150">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22163-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="22163-151">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="22163-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



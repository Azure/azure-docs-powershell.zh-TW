---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: a1841fb569cf6ef29bad685679372e0385133568
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457184"
---
# <span data-ttu-id="1d886-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1d886-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="1d886-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d886-102">SYNOPSIS</span></span>
<span data-ttu-id="1d886-103">在批次服務中建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="1d886-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d886-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d886-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d886-105">說明</span><span class="sxs-lookup"><span data-stu-id="1d886-105">DESCRIPTION</span></span>
<span data-ttu-id="1d886-106">**新的-AzureBatchJobSchedule** Cmdlet 會在 Azure Batch service 中建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="1d886-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="1d886-107">*BatchAccountCoNtext* 參數會指定此 Cmdlet 建立排程的帳戶。</span><span class="sxs-lookup"><span data-stu-id="1d886-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="1d886-108">示例</span><span class="sxs-lookup"><span data-stu-id="1d886-108">EXAMPLES</span></span>

### <span data-ttu-id="1d886-109">範例1：建立作業排程</span><span class="sxs-lookup"><span data-stu-id="1d886-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="1d886-110">這個範例會建立作業排程。</span><span class="sxs-lookup"><span data-stu-id="1d886-110">This example creates a job schedule.</span></span>

<span data-ttu-id="1d886-111">前五個命令會建立及修改 **PSSchedule** 、 **PSJobSpecification** 和 **PSPoolInformation** 物件。</span><span class="sxs-lookup"><span data-stu-id="1d886-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="1d886-112">這些命令會使用 New-Object Cmdlet 和標準的 Azure PowerShell 語法。</span><span class="sxs-lookup"><span data-stu-id="1d886-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="1d886-113">這些命令會將這些物件儲存在 $Schedule 並 $JobSpecification 變數中。</span><span class="sxs-lookup"><span data-stu-id="1d886-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="1d886-114">最後一個命令會建立具有識別碼 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="1d886-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="1d886-115">此排程會建立含一天的定期間隔的工作。</span><span class="sxs-lookup"><span data-stu-id="1d886-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="1d886-116">作業會在擁有識別碼 ContosoPool06 的池中執行，如5個命令所指定。</span><span class="sxs-lookup"><span data-stu-id="1d886-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="1d886-117">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="1d886-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="1d886-118">參數</span><span class="sxs-lookup"><span data-stu-id="1d886-118">PARAMETERS</span></span>

### <span data-ttu-id="1d886-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="1d886-119">-BatchContext</span></span>
<span data-ttu-id="1d886-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="1d886-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1d886-121">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="1d886-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1d886-122">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="1d886-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1d886-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="1d886-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1d886-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="1d886-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1d886-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d886-125">-DefaultProfile</span></span>
<span data-ttu-id="1d886-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d886-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d886-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1d886-127">-DisplayName</span></span>
<span data-ttu-id="1d886-128">指定作業排程的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1d886-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="1d886-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="1d886-129">-Id</span></span>
<span data-ttu-id="1d886-130">指定此 Cmdlet 建立之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d886-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d886-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="1d886-131">-JobSpecification</span></span>
<span data-ttu-id="1d886-132">指定此 Cmdlet 包含在作業排程中之作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1d886-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d886-133">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="1d886-133">-Metadata</span></span>
<span data-ttu-id="1d886-134">指定要新增至作業排程的中繼資料（做為索引鍵/值對）。</span><span class="sxs-lookup"><span data-stu-id="1d886-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="1d886-135">金鑰就是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="1d886-135">The key is the metadata name.</span></span>
<span data-ttu-id="1d886-136">此值為中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="1d886-136">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d886-137">-排程</span><span class="sxs-lookup"><span data-stu-id="1d886-137">-Schedule</span></span>
<span data-ttu-id="1d886-138">指定決定何時建立作業的排程。</span><span class="sxs-lookup"><span data-stu-id="1d886-138">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d886-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d886-139">CommonParameters</span></span>
<span data-ttu-id="1d886-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d886-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d886-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d886-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d886-142">輸入</span><span class="sxs-lookup"><span data-stu-id="1d886-142">INPUTS</span></span>

### <span data-ttu-id="1d886-143">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="1d886-143">BatchAccountContext</span></span>
<span data-ttu-id="1d886-144">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1d886-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="1d886-145">輸出</span><span class="sxs-lookup"><span data-stu-id="1d886-145">OUTPUTS</span></span>

## <span data-ttu-id="1d886-146">筆記</span><span class="sxs-lookup"><span data-stu-id="1d886-146">NOTES</span></span>

## <span data-ttu-id="1d886-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d886-147">RELATED LINKS</span></span>

[<span data-ttu-id="1d886-148">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1d886-148">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="1d886-149">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1d886-149">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="1d886-150">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1d886-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1d886-151">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1d886-151">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="1d886-152">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1d886-152">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="1d886-153">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1d886-153">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="1d886-154">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d886-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



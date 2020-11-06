---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 0f33807c112ea770e3d02d972d52ca7a166bb791
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446487"
---
# <span data-ttu-id="5b56d-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5b56d-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="5b56d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b56d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b56d-103">停止批次作業。</span><span class="sxs-lookup"><span data-stu-id="5b56d-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b56d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b56d-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b56d-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b56d-105">DESCRIPTION</span></span>
<span data-ttu-id="5b56d-106">**AzureBatchJob** Cmdlet 會停止 Azure 批次作業。</span><span class="sxs-lookup"><span data-stu-id="5b56d-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="5b56d-107">這個命令會將工作標示為已完成。</span><span class="sxs-lookup"><span data-stu-id="5b56d-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="5b56d-108">示例</span><span class="sxs-lookup"><span data-stu-id="5b56d-108">EXAMPLES</span></span>

### <span data-ttu-id="5b56d-109">範例1：停止批次作業</span><span class="sxs-lookup"><span data-stu-id="5b56d-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="5b56d-110">這個命令會停止具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="5b56d-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5b56d-111">該命令會指定您選擇停止作業的原因。</span><span class="sxs-lookup"><span data-stu-id="5b56d-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="5b56d-112">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="5b56d-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5b56d-113">參數</span><span class="sxs-lookup"><span data-stu-id="5b56d-113">PARAMETERS</span></span>

### <span data-ttu-id="5b56d-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="5b56d-114">-BatchContext</span></span>
<span data-ttu-id="5b56d-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="5b56d-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5b56d-116">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="5b56d-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5b56d-117">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="5b56d-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5b56d-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5b56d-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5b56d-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b56d-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5b56d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b56d-120">-DefaultProfile</span></span>
<span data-ttu-id="5b56d-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b56d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b56d-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5b56d-122">-Id</span></span>
<span data-ttu-id="5b56d-123">指定此 Cmdlet 停止的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b56d-123">Specifies the ID of the job that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b56d-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="5b56d-124">-TerminateReason</span></span>
<span data-ttu-id="5b56d-125">指定您決定停止作業的原因。</span><span class="sxs-lookup"><span data-stu-id="5b56d-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="5b56d-126">這個 Cmdlet 會將此文字儲存為作業的 **TerminateReason** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b56d-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b56d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b56d-127">CommonParameters</span></span>
<span data-ttu-id="5b56d-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b56d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b56d-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b56d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b56d-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5b56d-130">INPUTS</span></span>

### <span data-ttu-id="5b56d-131">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5b56d-131">BatchAccountContext</span></span>
<span data-ttu-id="5b56d-132">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5b56d-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5b56d-133">字串</span><span class="sxs-lookup"><span data-stu-id="5b56d-133">String</span></span>
<span data-ttu-id="5b56d-134">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="5b56d-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5b56d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5b56d-135">OUTPUTS</span></span>

## <span data-ttu-id="5b56d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="5b56d-136">NOTES</span></span>

## <span data-ttu-id="5b56d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b56d-137">RELATED LINKS</span></span>

[<span data-ttu-id="5b56d-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5b56d-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="5b56d-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5b56d-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5b56d-140">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5b56d-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5b56d-141">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5b56d-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="5b56d-142">新-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5b56d-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5b56d-143">移除-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5b56d-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="5b56d-144">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b56d-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



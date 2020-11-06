---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: fb1f9cf884b3443ec9746eca7cef603c7b9f3a38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457448"
---
# <span data-ttu-id="dc88f-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dc88f-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="dc88f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc88f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc88f-103">停用批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="dc88f-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc88f-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc88f-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc88f-105">說明</span><span class="sxs-lookup"><span data-stu-id="dc88f-105">DESCRIPTION</span></span>
<span data-ttu-id="dc88f-106">**Disable AzureBatchJobSchedule** Cmdlet 會停用 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="dc88f-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="dc88f-107">如果您停用排程，就不會根據該排程建立工作。</span><span class="sxs-lookup"><span data-stu-id="dc88f-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="dc88f-108">您可以稍後啟用停用的時程表。</span><span class="sxs-lookup"><span data-stu-id="dc88f-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="dc88f-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc88f-109">EXAMPLES</span></span>

### <span data-ttu-id="dc88f-110">範例1：停用作業排程</span><span class="sxs-lookup"><span data-stu-id="dc88f-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="dc88f-111">這個命令會停用 ID 為 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="dc88f-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="dc88f-112">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="dc88f-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dc88f-113">參數</span><span class="sxs-lookup"><span data-stu-id="dc88f-113">PARAMETERS</span></span>

### <span data-ttu-id="dc88f-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="dc88f-114">-BatchContext</span></span>
<span data-ttu-id="dc88f-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="dc88f-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dc88f-116">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="dc88f-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dc88f-117">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="dc88f-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dc88f-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="dc88f-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dc88f-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc88f-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dc88f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc88f-120">-DefaultProfile</span></span>
<span data-ttu-id="dc88f-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc88f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc88f-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="dc88f-122">-Id</span></span>
<span data-ttu-id="dc88f-123">指定此 Cmdlet 停用之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc88f-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="dc88f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc88f-124">CommonParameters</span></span>
<span data-ttu-id="dc88f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc88f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc88f-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc88f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc88f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="dc88f-127">INPUTS</span></span>

### <span data-ttu-id="dc88f-128">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="dc88f-128">BatchAccountContext</span></span>
<span data-ttu-id="dc88f-129">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="dc88f-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="dc88f-130">字串</span><span class="sxs-lookup"><span data-stu-id="dc88f-130">String</span></span>
<span data-ttu-id="dc88f-131">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="dc88f-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dc88f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="dc88f-132">OUTPUTS</span></span>

## <span data-ttu-id="dc88f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dc88f-133">NOTES</span></span>

## <span data-ttu-id="dc88f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc88f-134">RELATED LINKS</span></span>

[<span data-ttu-id="dc88f-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dc88f-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="dc88f-136">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dc88f-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dc88f-137">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dc88f-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="dc88f-138">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dc88f-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="dc88f-139">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dc88f-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="dc88f-140">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dc88f-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="dc88f-141">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc88f-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



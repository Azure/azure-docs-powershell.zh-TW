---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: 3081721db5cb113d48417ddf28d8a96512d27f99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454279"
---
# <span data-ttu-id="88615-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="88615-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="88615-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88615-102">SYNOPSIS</span></span>
<span data-ttu-id="88615-103">啟用批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="88615-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88615-104">句法</span><span class="sxs-lookup"><span data-stu-id="88615-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88615-105">說明</span><span class="sxs-lookup"><span data-stu-id="88615-105">DESCRIPTION</span></span>
<span data-ttu-id="88615-106">**Enable-AzureBatchJobSchedule** Cmdlet 可啟用 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="88615-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="88615-107">啟用作業排程後，就可以根據該排程來建立工作。</span><span class="sxs-lookup"><span data-stu-id="88615-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="88615-108">示例</span><span class="sxs-lookup"><span data-stu-id="88615-108">EXAMPLES</span></span>

### <span data-ttu-id="88615-109">範例1：啟用作業排程</span><span class="sxs-lookup"><span data-stu-id="88615-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="88615-110">這個命令會啟用 ID 為 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="88615-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="88615-111">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="88615-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="88615-112">參數</span><span class="sxs-lookup"><span data-stu-id="88615-112">PARAMETERS</span></span>

### <span data-ttu-id="88615-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="88615-113">-BatchContext</span></span>
<span data-ttu-id="88615-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="88615-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88615-115">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="88615-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88615-116">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="88615-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88615-117">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="88615-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88615-118">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="88615-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88615-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88615-119">-DefaultProfile</span></span>
<span data-ttu-id="88615-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88615-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88615-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="88615-121">-Id</span></span>
<span data-ttu-id="88615-122">指定此 Cmdlet 啟用之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88615-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="88615-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88615-123">CommonParameters</span></span>
<span data-ttu-id="88615-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88615-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88615-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88615-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88615-126">輸入</span><span class="sxs-lookup"><span data-stu-id="88615-126">INPUTS</span></span>

### <span data-ttu-id="88615-127">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="88615-127">BatchAccountContext</span></span>
<span data-ttu-id="88615-128">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="88615-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="88615-129">字串</span><span class="sxs-lookup"><span data-stu-id="88615-129">String</span></span>
<span data-ttu-id="88615-130">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="88615-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="88615-131">輸出</span><span class="sxs-lookup"><span data-stu-id="88615-131">OUTPUTS</span></span>

## <span data-ttu-id="88615-132">筆記</span><span class="sxs-lookup"><span data-stu-id="88615-132">NOTES</span></span>

## <span data-ttu-id="88615-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="88615-133">RELATED LINKS</span></span>

[<span data-ttu-id="88615-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="88615-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="88615-135">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="88615-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="88615-136">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="88615-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="88615-137">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="88615-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="88615-138">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="88615-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="88615-139">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="88615-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="88615-140">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88615-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: e1eb586ff23f5f56cd9fc117f5039d3ccc841367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450312"
---
# <span data-ttu-id="d9e74-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d9e74-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="d9e74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9e74-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e74-103">停用批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="d9e74-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9e74-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9e74-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9e74-105">說明</span><span class="sxs-lookup"><span data-stu-id="d9e74-105">DESCRIPTION</span></span>
<span data-ttu-id="d9e74-106">**Disable AzureBatchJobSchedule** Cmdlet 會停用 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="d9e74-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="d9e74-107">如果您停用排程，就不會根據該排程建立工作。</span><span class="sxs-lookup"><span data-stu-id="d9e74-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="d9e74-108">您可以稍後啟用停用的時程表。</span><span class="sxs-lookup"><span data-stu-id="d9e74-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="d9e74-109">示例</span><span class="sxs-lookup"><span data-stu-id="d9e74-109">EXAMPLES</span></span>

### <span data-ttu-id="d9e74-110">範例1：停用作業排程</span><span class="sxs-lookup"><span data-stu-id="d9e74-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="d9e74-111">這個命令會停用 ID 為 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="d9e74-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="d9e74-112">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="d9e74-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d9e74-113">參數</span><span class="sxs-lookup"><span data-stu-id="d9e74-113">PARAMETERS</span></span>

### <span data-ttu-id="d9e74-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d9e74-114">-BatchContext</span></span>
<span data-ttu-id="d9e74-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d9e74-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d9e74-116">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="d9e74-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d9e74-117">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="d9e74-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d9e74-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d9e74-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d9e74-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="d9e74-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d9e74-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e74-120">-DefaultProfile</span></span>
<span data-ttu-id="d9e74-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9e74-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9e74-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d9e74-122">-Id</span></span>
<span data-ttu-id="d9e74-123">指定此 Cmdlet 停用之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9e74-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e74-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e74-124">CommonParameters</span></span>
<span data-ttu-id="d9e74-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9e74-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e74-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9e74-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e74-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d9e74-127">INPUTS</span></span>

### <span data-ttu-id="d9e74-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d9e74-128">System.String</span></span>

### <span data-ttu-id="d9e74-129">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d9e74-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="d9e74-130">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d9e74-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="d9e74-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d9e74-131">OUTPUTS</span></span>

### <span data-ttu-id="d9e74-132">System.void</span><span class="sxs-lookup"><span data-stu-id="d9e74-132">System.Void</span></span>

## <span data-ttu-id="d9e74-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d9e74-133">NOTES</span></span>

## <span data-ttu-id="d9e74-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9e74-134">RELATED LINKS</span></span>

[<span data-ttu-id="d9e74-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d9e74-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d9e74-136">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d9e74-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d9e74-137">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d9e74-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="d9e74-138">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d9e74-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="d9e74-139">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d9e74-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="d9e74-140">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d9e74-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="d9e74-141">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d9e74-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



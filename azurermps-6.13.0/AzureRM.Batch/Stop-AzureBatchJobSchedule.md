---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 33ae727ea31d533652943240cd9cd25014635533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451924"
---
# <span data-ttu-id="07802-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="07802-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="07802-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07802-102">SYNOPSIS</span></span>
<span data-ttu-id="07802-103">停止批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="07802-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07802-104">句法</span><span class="sxs-lookup"><span data-stu-id="07802-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07802-105">說明</span><span class="sxs-lookup"><span data-stu-id="07802-105">DESCRIPTION</span></span>
<span data-ttu-id="07802-106">**AzureBatchJobSchedule** Cmdlet 會停止 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="07802-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="07802-107">示例</span><span class="sxs-lookup"><span data-stu-id="07802-107">EXAMPLES</span></span>

### <span data-ttu-id="07802-108">範例1：停止作業排程</span><span class="sxs-lookup"><span data-stu-id="07802-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="07802-109">這個命令會停止具有識別碼 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="07802-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="07802-110">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="07802-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="07802-111">參數</span><span class="sxs-lookup"><span data-stu-id="07802-111">PARAMETERS</span></span>

### <span data-ttu-id="07802-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="07802-112">-BatchContext</span></span>
<span data-ttu-id="07802-113">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="07802-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="07802-114">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="07802-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="07802-115">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="07802-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="07802-116">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="07802-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="07802-117">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="07802-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="07802-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07802-118">-DefaultProfile</span></span>
<span data-ttu-id="07802-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07802-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07802-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="07802-120">-Id</span></span>
<span data-ttu-id="07802-121">指定此 Cmdlet 停止的作業排程 ID。</span><span class="sxs-lookup"><span data-stu-id="07802-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="07802-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07802-122">CommonParameters</span></span>
<span data-ttu-id="07802-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07802-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07802-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07802-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07802-125">輸入</span><span class="sxs-lookup"><span data-stu-id="07802-125">INPUTS</span></span>

### <span data-ttu-id="07802-126">System.object</span><span class="sxs-lookup"><span data-stu-id="07802-126">System.String</span></span>

### <span data-ttu-id="07802-127">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="07802-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="07802-128">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="07802-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="07802-129">輸出</span><span class="sxs-lookup"><span data-stu-id="07802-129">OUTPUTS</span></span>

### <span data-ttu-id="07802-130">System.void</span><span class="sxs-lookup"><span data-stu-id="07802-130">System.Void</span></span>

## <span data-ttu-id="07802-131">筆記</span><span class="sxs-lookup"><span data-stu-id="07802-131">NOTES</span></span>

## <span data-ttu-id="07802-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="07802-132">RELATED LINKS</span></span>

[<span data-ttu-id="07802-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="07802-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="07802-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="07802-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="07802-135">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="07802-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="07802-136">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="07802-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="07802-137">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="07802-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="07802-138">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="07802-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="07802-139">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07802-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454724"
---
# <span data-ttu-id="62d4e-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="62d4e-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="62d4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="62d4e-103">更新批次作業。</span><span class="sxs-lookup"><span data-stu-id="62d4e-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62d4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="62d4e-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62d4e-105">說明</span><span class="sxs-lookup"><span data-stu-id="62d4e-105">DESCRIPTION</span></span>
<span data-ttu-id="62d4e-106">**AzureBatchJob** Cmdlet 會更新 Azure Batch 作業。</span><span class="sxs-lookup"><span data-stu-id="62d4e-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="62d4e-107">使用 Get-AzureBatchJob Cmdlet 來取得 **PSCloudJob** 物件。</span><span class="sxs-lookup"><span data-stu-id="62d4e-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="62d4e-108">修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。</span><span class="sxs-lookup"><span data-stu-id="62d4e-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="62d4e-109">示例</span><span class="sxs-lookup"><span data-stu-id="62d4e-109">EXAMPLES</span></span>

### <span data-ttu-id="62d4e-110">範例1：更新作業</span><span class="sxs-lookup"><span data-stu-id="62d4e-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="62d4e-111">第一個命令會使用 **AzureBatchJob** 來取得池子，然後將它儲存在 $Job 變數中。</span><span class="sxs-lookup"><span data-stu-id="62d4e-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="62d4e-112">第二個命令會修改 $Job 物件的優先順序規格。</span><span class="sxs-lookup"><span data-stu-id="62d4e-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="62d4e-113">最後一個命令會更新批次服務，以符合 $Job 中的本機物件。</span><span class="sxs-lookup"><span data-stu-id="62d4e-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="62d4e-114">參數</span><span class="sxs-lookup"><span data-stu-id="62d4e-114">PARAMETERS</span></span>

### <span data-ttu-id="62d4e-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="62d4e-115">-BatchContext</span></span>
<span data-ttu-id="62d4e-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="62d4e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="62d4e-117">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="62d4e-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="62d4e-118">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="62d4e-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="62d4e-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="62d4e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="62d4e-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="62d4e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="62d4e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d4e-121">-DefaultProfile</span></span>
<span data-ttu-id="62d4e-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62d4e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62d4e-123">-工作</span><span class="sxs-lookup"><span data-stu-id="62d4e-123">-Job</span></span>
<span data-ttu-id="62d4e-124">指定此 Cmdlet 更新批次服務的 **PSCloudJob** 。</span><span class="sxs-lookup"><span data-stu-id="62d4e-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62d4e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d4e-125">CommonParameters</span></span>
<span data-ttu-id="62d4e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62d4e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d4e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62d4e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d4e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="62d4e-128">INPUTS</span></span>

### <span data-ttu-id="62d4e-129">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="62d4e-129">BatchAccountContext</span></span>
<span data-ttu-id="62d4e-130">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="62d4e-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="62d4e-131">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="62d4e-131">PSCloudJob</span></span>
<span data-ttu-id="62d4e-132">參數「作業」接受管道中類型 ' PSCloudJob」的值</span><span class="sxs-lookup"><span data-stu-id="62d4e-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="62d4e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="62d4e-133">OUTPUTS</span></span>

## <span data-ttu-id="62d4e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="62d4e-134">NOTES</span></span>

## <span data-ttu-id="62d4e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="62d4e-135">RELATED LINKS</span></span>

[<span data-ttu-id="62d4e-136">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="62d4e-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="62d4e-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="62d4e-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="62d4e-138">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="62d4e-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="62d4e-139">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="62d4e-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="62d4e-140">新-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="62d4e-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="62d4e-141">移除-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="62d4e-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="62d4e-142">停止 AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="62d4e-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="62d4e-143">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="62d4e-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



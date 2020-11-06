---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: be73b757bf20a2f688d7f7293ac4022e7bc8f4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450303"
---
# <span data-ttu-id="0e3d3-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e3d3-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="0e3d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3d3-103">啟用批次作業。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e3d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e3d3-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e3d3-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e3d3-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3d3-106">**AzureBatchJob** Cmdlet 可啟用 Azure Batch 作業。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="0e3d3-107">啟用作業之後，就可以執行新的工作。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="0e3d3-108">示例</span><span class="sxs-lookup"><span data-stu-id="0e3d3-108">EXAMPLES</span></span>

### <span data-ttu-id="0e3d3-109">範例1：啟用批次作業</span><span class="sxs-lookup"><span data-stu-id="0e3d3-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="0e3d3-110">這個命令會啟用具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="0e3d3-111">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0e3d3-112">參數</span><span class="sxs-lookup"><span data-stu-id="0e3d3-112">PARAMETERS</span></span>

### <span data-ttu-id="0e3d3-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="0e3d3-113">-BatchContext</span></span>
<span data-ttu-id="0e3d3-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0e3d3-115">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0e3d3-116">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0e3d3-117">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0e3d3-118">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0e3d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3d3-119">-DefaultProfile</span></span>
<span data-ttu-id="0e3d3-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e3d3-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0e3d3-121">-Id</span></span>
<span data-ttu-id="0e3d3-122">指定此 Cmdlet 啟用之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="0e3d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3d3-123">CommonParameters</span></span>
<span data-ttu-id="0e3d3-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3d3-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e3d3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3d3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0e3d3-126">INPUTS</span></span>

### <span data-ttu-id="0e3d3-127">System.object</span><span class="sxs-lookup"><span data-stu-id="0e3d3-127">System.String</span></span>

### <span data-ttu-id="0e3d3-128">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="0e3d3-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="0e3d3-129">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="0e3d3-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="0e3d3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0e3d3-130">OUTPUTS</span></span>

### <span data-ttu-id="0e3d3-131">System.void</span><span class="sxs-lookup"><span data-stu-id="0e3d3-131">System.Void</span></span>

## <span data-ttu-id="0e3d3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0e3d3-132">NOTES</span></span>

## <span data-ttu-id="0e3d3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e3d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="0e3d3-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e3d3-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="0e3d3-135">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e3d3-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="0e3d3-136">新-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e3d3-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="0e3d3-137">移除-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e3d3-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="0e3d3-138">停止 AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e3d3-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="0e3d3-139">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e3d3-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



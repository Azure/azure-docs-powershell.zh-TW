---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626351"
---
# <span data-ttu-id="dfeb2-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfeb2-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="dfeb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfeb2-102">SYNOPSIS</span></span>
<span data-ttu-id="dfeb2-103">啟用批次作業。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfeb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfeb2-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfeb2-105">說明</span><span class="sxs-lookup"><span data-stu-id="dfeb2-105">DESCRIPTION</span></span>
<span data-ttu-id="dfeb2-106">**AzureBatchJob** Cmdlet 可啟用 Azure Batch 作業。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="dfeb2-107">啟用作業之後，就可以執行新的工作。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="dfeb2-108">示例</span><span class="sxs-lookup"><span data-stu-id="dfeb2-108">EXAMPLES</span></span>

### <span data-ttu-id="dfeb2-109">範例1：啟用批次作業</span><span class="sxs-lookup"><span data-stu-id="dfeb2-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="dfeb2-110">這個命令會啟用具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="dfeb2-111">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dfeb2-112">參數</span><span class="sxs-lookup"><span data-stu-id="dfeb2-112">PARAMETERS</span></span>

### <span data-ttu-id="dfeb2-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="dfeb2-113">-BatchContext</span></span>
<span data-ttu-id="dfeb2-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dfeb2-115">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="dfeb2-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="dfeb2-116">-Id</span></span>
<span data-ttu-id="dfeb2-117">指定此 Cmdlet 啟用之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="dfeb2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfeb2-118">-DefaultProfile</span></span>
<span data-ttu-id="dfeb2-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfeb2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfeb2-120">CommonParameters</span></span>
<span data-ttu-id="dfeb2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfeb2-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dfeb2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfeb2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="dfeb2-123">INPUTS</span></span>

### <span data-ttu-id="dfeb2-124">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="dfeb2-124">BatchAccountContext</span></span>
<span data-ttu-id="dfeb2-125">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="dfeb2-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="dfeb2-126">字串</span><span class="sxs-lookup"><span data-stu-id="dfeb2-126">String</span></span>
<span data-ttu-id="dfeb2-127">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="dfeb2-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dfeb2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="dfeb2-128">OUTPUTS</span></span>

## <span data-ttu-id="dfeb2-129">筆記</span><span class="sxs-lookup"><span data-stu-id="dfeb2-129">NOTES</span></span>

## <span data-ttu-id="dfeb2-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfeb2-130">RELATED LINKS</span></span>

[<span data-ttu-id="dfeb2-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfeb2-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="dfeb2-132">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfeb2-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="dfeb2-133">新-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfeb2-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="dfeb2-134">移除-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfeb2-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="dfeb2-135">停止 AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dfeb2-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="dfeb2-136">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dfeb2-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



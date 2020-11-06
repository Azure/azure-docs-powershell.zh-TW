---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451755"
---
# <span data-ttu-id="46ce6-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="46ce6-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="46ce6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="46ce6-103">停止批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="46ce6-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46ce6-104">句法</span><span class="sxs-lookup"><span data-stu-id="46ce6-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ce6-105">說明</span><span class="sxs-lookup"><span data-stu-id="46ce6-105">DESCRIPTION</span></span>
<span data-ttu-id="46ce6-106">**AzureBatchJobSchedule** Cmdlet 會停止 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="46ce6-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="46ce6-107">示例</span><span class="sxs-lookup"><span data-stu-id="46ce6-107">EXAMPLES</span></span>

### <span data-ttu-id="46ce6-108">範例1：停止作業排程</span><span class="sxs-lookup"><span data-stu-id="46ce6-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="46ce6-109">這個命令會停止具有識別碼 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="46ce6-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="46ce6-110">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="46ce6-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="46ce6-111">參數</span><span class="sxs-lookup"><span data-stu-id="46ce6-111">PARAMETERS</span></span>

### <span data-ttu-id="46ce6-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="46ce6-112">-BatchContext</span></span>
<span data-ttu-id="46ce6-113">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="46ce6-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="46ce6-114">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46ce6-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="46ce6-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="46ce6-115">-Id</span></span>
<span data-ttu-id="46ce6-116">指定此 Cmdlet 停止的作業排程 ID。</span><span class="sxs-lookup"><span data-stu-id="46ce6-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="46ce6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ce6-117">-DefaultProfile</span></span>
<span data-ttu-id="46ce6-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46ce6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46ce6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ce6-119">CommonParameters</span></span>
<span data-ttu-id="46ce6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46ce6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ce6-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46ce6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ce6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="46ce6-122">INPUTS</span></span>

### <span data-ttu-id="46ce6-123">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="46ce6-123">BatchAccountContext</span></span>
<span data-ttu-id="46ce6-124">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="46ce6-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="46ce6-125">字串</span><span class="sxs-lookup"><span data-stu-id="46ce6-125">String</span></span>
<span data-ttu-id="46ce6-126">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="46ce6-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="46ce6-127">輸出</span><span class="sxs-lookup"><span data-stu-id="46ce6-127">OUTPUTS</span></span>

## <span data-ttu-id="46ce6-128">筆記</span><span class="sxs-lookup"><span data-stu-id="46ce6-128">NOTES</span></span>

## <span data-ttu-id="46ce6-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="46ce6-129">RELATED LINKS</span></span>

[<span data-ttu-id="46ce6-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="46ce6-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="46ce6-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="46ce6-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="46ce6-132">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="46ce6-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="46ce6-133">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="46ce6-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="46ce6-134">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="46ce6-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="46ce6-135">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="46ce6-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="46ce6-136">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46ce6-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



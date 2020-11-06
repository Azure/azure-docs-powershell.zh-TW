---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456911"
---
# <span data-ttu-id="d57e3-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d57e3-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="d57e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d57e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d57e3-103">啟用批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="d57e3-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d57e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="d57e3-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d57e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="d57e3-105">DESCRIPTION</span></span>
<span data-ttu-id="d57e3-106">**Enable-AzureBatchJobSchedule** Cmdlet 可啟用 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="d57e3-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="d57e3-107">啟用作業排程後，就可以根據該排程來建立工作。</span><span class="sxs-lookup"><span data-stu-id="d57e3-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="d57e3-108">示例</span><span class="sxs-lookup"><span data-stu-id="d57e3-108">EXAMPLES</span></span>

### <span data-ttu-id="d57e3-109">範例1：啟用作業排程</span><span class="sxs-lookup"><span data-stu-id="d57e3-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="d57e3-110">這個命令會啟用 ID 為 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="d57e3-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="d57e3-111">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="d57e3-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d57e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="d57e3-112">PARAMETERS</span></span>

### <span data-ttu-id="d57e3-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d57e3-113">-BatchContext</span></span>
<span data-ttu-id="d57e3-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d57e3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d57e3-115">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d57e3-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d57e3-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d57e3-116">-Id</span></span>
<span data-ttu-id="d57e3-117">指定此 Cmdlet 啟用之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d57e3-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="d57e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57e3-118">-DefaultProfile</span></span>
<span data-ttu-id="d57e3-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d57e3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d57e3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57e3-120">CommonParameters</span></span>
<span data-ttu-id="d57e3-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d57e3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57e3-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d57e3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57e3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="d57e3-123">INPUTS</span></span>

### <span data-ttu-id="d57e3-124">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d57e3-124">BatchAccountContext</span></span>
<span data-ttu-id="d57e3-125">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d57e3-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d57e3-126">字串</span><span class="sxs-lookup"><span data-stu-id="d57e3-126">String</span></span>
<span data-ttu-id="d57e3-127">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="d57e3-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d57e3-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d57e3-128">OUTPUTS</span></span>

## <span data-ttu-id="d57e3-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d57e3-129">NOTES</span></span>

## <span data-ttu-id="d57e3-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d57e3-130">RELATED LINKS</span></span>

[<span data-ttu-id="d57e3-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d57e3-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d57e3-132">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d57e3-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d57e3-133">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d57e3-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="d57e3-134">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d57e3-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="d57e3-135">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d57e3-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="d57e3-136">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d57e3-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="d57e3-137">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d57e3-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)



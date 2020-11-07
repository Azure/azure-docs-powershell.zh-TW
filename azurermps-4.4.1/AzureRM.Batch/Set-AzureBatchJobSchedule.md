---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626346"
---
# <span data-ttu-id="0128f-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="0128f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0128f-102">SYNOPSIS</span></span>
<span data-ttu-id="0128f-103">設定作業排程。</span><span class="sxs-lookup"><span data-stu-id="0128f-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0128f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0128f-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0128f-105">說明</span><span class="sxs-lookup"><span data-stu-id="0128f-105">DESCRIPTION</span></span>
<span data-ttu-id="0128f-106">**AzureBatchJobSchedule** Cmdlet 會在 Azure Batch service 中設定作業排程。</span><span class="sxs-lookup"><span data-stu-id="0128f-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="0128f-107">示例</span><span class="sxs-lookup"><span data-stu-id="0128f-107">EXAMPLES</span></span>

## <span data-ttu-id="0128f-108">參數</span><span class="sxs-lookup"><span data-stu-id="0128f-108">PARAMETERS</span></span>

### <span data-ttu-id="0128f-109">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="0128f-109">-BatchContext</span></span>
<span data-ttu-id="0128f-110">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="0128f-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0128f-111">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0128f-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0128f-112">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-112">-JobSchedule</span></span>
<span data-ttu-id="0128f-113">指定代表作業排程的 **PSCloudJobSchedule** 物件。</span><span class="sxs-lookup"><span data-stu-id="0128f-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="0128f-114">若要取得 **PSCloudJobSchedule** 物件，請使用 Get-AzureBatchJobSchedule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0128f-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0128f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0128f-115">-DefaultProfile</span></span>
<span data-ttu-id="0128f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0128f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0128f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0128f-117">CommonParameters</span></span>
<span data-ttu-id="0128f-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0128f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0128f-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0128f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0128f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0128f-120">INPUTS</span></span>

### <span data-ttu-id="0128f-121">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="0128f-121">BatchAccountContext</span></span>
<span data-ttu-id="0128f-122">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0128f-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0128f-123">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="0128f-124">形參 "JobSchedule" 接受管線中 "PSCloudJobSchedule" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0128f-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="0128f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="0128f-125">OUTPUTS</span></span>

## <span data-ttu-id="0128f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0128f-126">NOTES</span></span>

## <span data-ttu-id="0128f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0128f-127">RELATED LINKS</span></span>

[<span data-ttu-id="0128f-128">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0128f-129">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0128f-130">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="0128f-131">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="0128f-132">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="0128f-133">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0128f-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)



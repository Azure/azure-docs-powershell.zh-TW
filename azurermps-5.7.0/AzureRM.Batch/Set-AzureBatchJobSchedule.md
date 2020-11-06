---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 85e47b9f9bea7a19bb11817c414e5d3b9a35d6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453128"
---
# <span data-ttu-id="55257-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="55257-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55257-102">SYNOPSIS</span></span>
<span data-ttu-id="55257-103">設定作業排程。</span><span class="sxs-lookup"><span data-stu-id="55257-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55257-104">句法</span><span class="sxs-lookup"><span data-stu-id="55257-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55257-105">說明</span><span class="sxs-lookup"><span data-stu-id="55257-105">DESCRIPTION</span></span>
<span data-ttu-id="55257-106">**AzureBatchJobSchedule** Cmdlet 會在 Azure Batch service 中設定作業排程。</span><span class="sxs-lookup"><span data-stu-id="55257-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="55257-107">示例</span><span class="sxs-lookup"><span data-stu-id="55257-107">EXAMPLES</span></span>

## <span data-ttu-id="55257-108">參數</span><span class="sxs-lookup"><span data-stu-id="55257-108">PARAMETERS</span></span>

### <span data-ttu-id="55257-109">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="55257-109">-BatchContext</span></span>
<span data-ttu-id="55257-110">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="55257-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="55257-111">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="55257-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="55257-112">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="55257-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="55257-113">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="55257-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="55257-114">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="55257-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="55257-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55257-115">-DefaultProfile</span></span>
<span data-ttu-id="55257-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55257-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55257-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-117">-JobSchedule</span></span>
<span data-ttu-id="55257-118">指定代表作業排程的 **PSCloudJobSchedule** 物件。</span><span class="sxs-lookup"><span data-stu-id="55257-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="55257-119">若要取得 **PSCloudJobSchedule** 物件，請使用 Get-AzureBatchJobSchedule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55257-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: PSCloudJobSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55257-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55257-120">CommonParameters</span></span>
<span data-ttu-id="55257-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55257-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55257-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55257-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55257-123">輸入</span><span class="sxs-lookup"><span data-stu-id="55257-123">INPUTS</span></span>

### <span data-ttu-id="55257-124">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="55257-124">BatchAccountContext</span></span>
<span data-ttu-id="55257-125">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="55257-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="55257-126">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-126">PSCloudJobSchedule</span></span>
<span data-ttu-id="55257-127">形參 "JobSchedule" 接受管線中 "PSCloudJobSchedule" 類型的值</span><span class="sxs-lookup"><span data-stu-id="55257-127">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="55257-128">輸出</span><span class="sxs-lookup"><span data-stu-id="55257-128">OUTPUTS</span></span>

## <span data-ttu-id="55257-129">筆記</span><span class="sxs-lookup"><span data-stu-id="55257-129">NOTES</span></span>

## <span data-ttu-id="55257-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="55257-130">RELATED LINKS</span></span>

[<span data-ttu-id="55257-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="55257-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="55257-133">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="55257-134">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="55257-135">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="55257-136">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55257-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)



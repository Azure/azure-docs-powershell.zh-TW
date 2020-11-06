---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: 0f6bee54c5abf795a49148e7c2d93707b45ba9a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451936"
---
# <span data-ttu-id="73a2c-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="73a2c-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="73a2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="73a2c-103">取得批次帳戶的 [池摘要統計資料]。</span><span class="sxs-lookup"><span data-stu-id="73a2c-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73a2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="73a2c-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73a2c-105">說明</span><span class="sxs-lookup"><span data-stu-id="73a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="73a2c-106">**AzureBatchPoolStatistics** Cmdlet 會取得指定帳戶中所有池的存留期統計資料。</span><span class="sxs-lookup"><span data-stu-id="73a2c-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="73a2c-107">每個已存在於帳戶中的所有池都會匯總統計資料，從帳戶建立到統計的最後一次更新時間。</span><span class="sxs-lookup"><span data-stu-id="73a2c-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="73a2c-108">示例</span><span class="sxs-lookup"><span data-stu-id="73a2c-108">EXAMPLES</span></span>

### <span data-ttu-id="73a2c-109">範例1：取得帳戶中所有池的資源統計資料</span><span class="sxs-lookup"><span data-stu-id="73a2c-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzureBatchPoolStatistics -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics 
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="73a2c-110">第一個命令會使用 **AzureRmBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="73a2c-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="73a2c-111">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="73a2c-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="73a2c-112">第二個命令會取得指定帳戶中所有池的統計資料，然後將它們儲存在 $PoolStatistics 中。</span><span class="sxs-lookup"><span data-stu-id="73a2c-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="73a2c-113">最後一個命令會顯示 $PoolStatistics 的 **ResourceStatistics** 屬性。</span><span class="sxs-lookup"><span data-stu-id="73a2c-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="73a2c-114">參數</span><span class="sxs-lookup"><span data-stu-id="73a2c-114">PARAMETERS</span></span>

### <span data-ttu-id="73a2c-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="73a2c-115">-BatchContext</span></span>
<span data-ttu-id="73a2c-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="73a2c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="73a2c-117">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="73a2c-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="73a2c-118">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="73a2c-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="73a2c-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="73a2c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="73a2c-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="73a2c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="73a2c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a2c-121">-DefaultProfile</span></span>
<span data-ttu-id="73a2c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73a2c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73a2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a2c-123">CommonParameters</span></span>
<span data-ttu-id="73a2c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73a2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a2c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73a2c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a2c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="73a2c-126">INPUTS</span></span>

### <span data-ttu-id="73a2c-127">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="73a2c-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="73a2c-128">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="73a2c-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="73a2c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="73a2c-129">OUTPUTS</span></span>

### <span data-ttu-id="73a2c-130">Microsoft.Azure.Commands.Batch。PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="73a2c-130">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="73a2c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="73a2c-131">NOTES</span></span>

## <span data-ttu-id="73a2c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="73a2c-132">RELATED LINKS</span></span>

[<span data-ttu-id="73a2c-133">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="73a2c-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="73a2c-134">AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="73a2c-134">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="73a2c-135">AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="73a2c-135">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


